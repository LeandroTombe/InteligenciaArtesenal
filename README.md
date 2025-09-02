El objetivo es aplicar técnicas de **carga, exploración, limpieza y análisis** de datasets utilizando **Python**, **pandas** y **Jupyter Notebooks**.  

---

## 📋 Requisitos previos

- **Python 3.9+** (se recomienda Python 3.11 para compatibilidad total)
- `pip` actualizado
- Git (opcional, para clonar el repositorio)

---

## 📋 Requisitos previos
- Python 3.x instalado

## ⚙️ Configuración del entorno virtual

Se emplea un entorno virtual para aislar las dependencias del proyecto y garantizar la reproducibilidad.


### 🪟 Windows (PowerShell)
```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

### 🪟 Windows (CMD)
```cmd
python -m venv venv
.\venv\Scripts\activate.bat
```

### 🐧 Linux/MacO
```bash
python3 -m venv venv
source venv/bin/activate
```

## 📦 Instalar dependencias

Una vez activado el entorno virtual, instala las dependencias necesarias (si tienes un archivo `requirements.txt`):

```powershell
pip install -r requirements.txt
```

## 🔁 Exportar dependencias a requirements.txt

Si agregas o actualizas paquetes en tu entorno virtual, puedes exportar todas las dependencias instaladas a un archivo `requirements.txt` con el siguiente comando:

```powershell
pip freeze > requirements.txt
```

Esto actualizará el archivo `requirements.txt` con todas las dependencias actuales del entorno virtual.

## ⬆️ Actualizar dependencias

Para instalar o actualizar todas las dependencias listadas en `requirements.txt` ejecuta:

```powershell
pip install --upgrade -r requirements.txt
```

## ⛔ Desactivar el entorno virtual

```powershell
deactivate
```



## 🚀 Ejecutar Jupyter Notebook

Para iniciar Jupyter Notebook y trabajar con tus notebooks, asegúrate de tener el entorno virtual activado y ejecuta:

```powershell
jupyter notebook
```

Esto abrirá una ventana en tu navegador donde podrás crear y editar notebooks



## 📊 Conjuntos de Datos

### 1. US Cars Dataset
- **Descripción:** Dataset con información de autos usados y “limpios” en venta en EE.UU.  
- **Atributos:** marca, modelo, año, color, precio, VIN, kilometraje, ubicación, estado del título, lote, condición.  
- **Tamaño:** 2.499 vehículos (28 marcas, 12 atributos).  
- **Etiquetas:** Automóviles, vehículos usados.  
- **Archivo:** `datasets/USA_cars_datasets.csv` (~284 KB).  
- **Fuente:** Kaggle (Doaa Alsenani, 2020).  

---

### 2. DummyJSON — API de Productos
- **Descripción:** API pública que provee datos ficticios en formato JSON para pruebas.  
- **Ejemplo de endpoint:** [`https://dummyjson.com/products`](https://dummyjson.com/products)  
- **Atributos:** id, título, descripción, precio, descuento, rating, stock, marca, categoría, imágenes.  
- **Etiquetas:** API REST, comercio electrónico, datos ficticios.  
- **Fuente:** [DummyJSON](https://dummyjson.com).  

---

## 📂 Estructura del Repositorio

```

├── datasets/                    # Conjuntos de datos en formato CSV/JSON usados en notebooks  
├── export/                      # Resultados exportados (datasets limpios, ejemplos procesados)  
├── .gitignore                   # Archivos/carpetas ignorados por Git  
├── Notebook_de_ejercicios.ipynb # Notebook con un ejercicio práctico y un desafio 
├── Notebook_demo.ipynb          # Notebook principal con ejemplos guiados paso a paso  
├── README.md                    # Documentación principal del proyecto  
└── requirements.txt             # Dependencias de Python necesarias para ejecutar el proyecto  
```

---