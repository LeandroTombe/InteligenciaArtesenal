
## <div style="background-color:#57ffcfff;padding:8px;border-radius:8px">3. Lectura desde la web (APIs) y JSON → pandas</div>

> Objetivo: **traer datos JSON desde una API web**, convertirlos a **estructuras de Python** y analizarlos con **pandas**. Luego, **persistir** de forma eficiente (Parquet / Pickle).

---

### 🧠 Idea general (flujo)
**API (HTTP)** → **JSON (texto)** → `response.json()` → **dict/list de Python** → `pandas.DataFrame` → (opcional) **guardar** `to_parquet()` / `to_pickle()`

---

### 1) Pedir datos a una API (GET) y convertir a JSON
```python
import requests

url = "https://dummyjson.com/products"   # ejemplo público
resp = requests.get(url)                 # 1) HTTP GET
data = resp.json()                       # 2) JSON → dict/list (Python)
type(data), list(data.keys())[:5]        # inspección rápida
```

**Tips:**  
- `resp.status_code == 200` ⇒ OK.  
- `resp.json()` es igual a `json.loads(resp.text)` pero más directo.  
- Muchos endpoints devuelven un objeto con una **lista** por dentro, p. ej. `data["products"]`.

---

### 2) Pasar JSON a DataFrame
```python
import pandas as pd

items = data["products"]                 # lista de objetos JSON
df = pd.DataFrame(items)                 # columnas = claves del JSON
df.head()
```

Si hay **campos anidados** (p. ej., `rating.details.stars`), usá:
```python
from pandas import json_normalize

df_flat = json_normalize(items)          # "aplana" estructuras anidadas
df_flat.filter(like="rating").head()     # ejemplo: ver columnas relacionadas
```

---

### 3) Seleccionar solo lo útil (columnas)
```python
cols = ["id", "title", "brand", "price", "rating"]
df_view = df_flat[cols]
df_view.head()
```

> Consejo: mantené un subconjunto **mínimo** de columnas para acelerar análisis y visualizaciones.

---

### 4) Limpieza rápida (valores faltantes y tipos)
```python
# Reemplazar null → None en Python ya viene mapeado; luego:
df_view = df_view.copy()
df_view["price"] = pd.to_numeric(df_view["price"], errors="coerce")
df_view["rating"] = pd.to_numeric(df_view["rating"], errors="coerce")
df_view.isna().mean().round(3)           # % faltantes por columna
```

---

### 5) Guardar eficientemente (Parquet / Pickle)
- **Parquet** (columnar, comprimido, portable): ideal para tablas y lectura por columna.  
- **Pickle** (Python-only): útil para objetos de Python; menos portable.

```python
# Parquet (recomendado para data tabular)
df_view.to_parquet("products.parquet", engine="pyarrow", compression="snappy")

# Leer Parquet (y opcional: solo algunas columnas)
df_pq = pd.read_parquet("products.parquet", columns=["id", "title", "price"])
df_pq.head()

# Pickle (si necesitás guardar el objeto tal cual, solo para Python)
df_view.to_pickle("products.pkl")
df_pk = pd.read_pickle("products.pkl")
```

---

### 6) (Opcional) Persistir en SQLite / MongoDB
Como en tu notebook aparecen `sqlite3` y `pymongo`, acá queda el “bridge” mínimo:

**SQLite (local, archivo `.db`):**
```python
import sqlite3
con = sqlite3.connect("products.db")
df_view.to_sql("products", con, if_exists="replace", index=False)
pd.read_sql("SELECT id, title, price FROM products LIMIT 5", con)
con.close()
```

**MongoDB (colección de documentos JSON):**
```python
from pymongo import MongoClient

client = MongoClient("mongodb://localhost:27017/")   # ajustá la URI
db = client["ejemplo_db"]                            # visto en tu notebook
docs = df_view.to_dict(orient="records")
db.libros.insert_many(docs)                          # o la colección que uses
db.libros.find_one()
```

> Elegí **SQLite** si querés SQL rápido en un archivo local. Elegí **MongoDB** si tu JSON es muy **anidado** y preferís un esquema flexible.

---
