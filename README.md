````markdown
# 🔬 Proyecto de Ciencias de Datos

Este repositorio contiene el trabajo práctico de **Ciencias de Datos**, con el objetivo de aplicar técnicas de carga, limpieza, análisis y visualización de datos utilizando **Python** y **Jupyter Notebooks**.

---

## 📋 Requisitos previos

- **Python 3.9+** instalado (se recomienda usar 3.11 para mejor compatibilidad).
- `pip` actualizado.
- Git instalado para clonar y gestionar el repositorio.

---

## ⚙️ Entorno Virtual

Para mantener las dependencias ordenadas, se recomienda crear y activar un entorno virtual.

### 🪟 Windows (PowerShell)

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```
````

### 🪟 Windows (CMD)

```cmd
python -m venv venv
.\venv\Scripts\activate.bat
```

### 🐧 Linux / 🍏 macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 📦 Dependencias

### 🔽 Instalar dependencias

Con el entorno virtual activado:

```bash
pip install -r requirements.txt
```

### 📤 Exportar dependencias

Si instalás o actualizás paquetes:

```bash
pip freeze > requirements.txt
```

### 🔄 Actualizar dependencias

Para reinstalar todo desde `requirements.txt`:

```bash
pip install --upgrade -r requirements.txt
```

### ⛔ Desactivar el entorno virtual

```bash
deactivate
```

---

## 📊 Conjunto de Datos

### **US Cars Dataset**

- **Descripción:** Incluye información de autos usados y "limpios" (sin daños) en venta en EE.UU.
- **Registros:** 2.499 vehículos.
- **Columnas:** 12 atributos (marca, modelo, año, color, precio, VIN, kilometraje, ubicación, estado del título, lote, condición, etc.).
- **Etiquetas:** Automóviles y vehículos.
- **Fuente:** Kaggle.
- **Tamaño:** \~284 KB (CSV).
- **Fecha publicación:** 2020.
- **Autor:** Doaa Alsenani.
- **Licencia:** No especificada.

**Archivos incluidos:**

- `USA_cars_datasets.csv` — archivo en formato CSV.

---

## 🚀 Ejecutar Jupyter Notebook

1. Activar el entorno virtual.
2. Instalar dependencias (`pip install -r requirements.txt`).
3. Iniciar Jupyter:

   ```bash
   jupyter notebook
   ```

4. Se abrirá el navegador y podrás trabajar con los notebooks.

---

## 📚 Estructura del Repositorio

```
.
├── datasets/
│   └── USA_cars_datasets.csv    # Dataset principal
├── notebooks/
│   └── analisis_inicial.ipynb   # Ejemplo de notebook
├── requirements.txt             # Dependencias del proyecto
└── README.md                    # Documentación
```

---
