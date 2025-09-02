# 🔬 Proyecto de Ciencias de Datos

Este repositorio contiene el trabajo práctico de **Ciencias de Datos**, cuyo objetivo es aplicar técnicas de **carga, limpieza, análisis y visualización de datos** utilizando **Python** y **Jupyter Notebooks**.

---

## 📋 Requisitos previos

- Python 3.9+ (se recomienda 3.11 para mayor compatibilidad)
- `pip` actualizado
- Git instalado para clonar y gestionar el repositorio

---

## ⚙️ Configuración del entorno virtual

Para mantener las dependencias ordenadas, se recomienda crear y activar un entorno virtual.

### 🪟 Windows (PowerShell)

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

### 🐧 Linux / 🍏 macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 📦 Dependencias

### 🔽 Instalar dependencias

```bash
pip install -r requirements.txt
```

### 📤 Exportar dependencias

```bash
pip freeze > requirements.txt
```

### 🔄 Actualizar dependencias

```bash
pip install --upgrade -r requirements.txt
```

### ⛔ Desactivar entorno virtual

```bash
deactivate
```

---

## 📊 Conjunto de Datos

### US Cars Dataset

```text
Descripción: Información de autos usados y "limpios" (sin daños) en venta en EE.UU.
Registros: 2.499 vehículos
Columnas: 12 atributos (marca, modelo, año, color, precio, VIN, kilometraje, ubicación, estado del título, lote, condición, etc.)
Fuente: Kaggle
Tamaño: ~284 KB (CSV)
Fecha publicación: 2020
Autor: Doaa Alsenani
Licencia: No especificada
```

📂 Archivo incluido:

```text
datasets/USA_cars_datasets.csv
```

---

## 🚀 Ejecutar Jupyter Notebook

```bash
jupyter notebook
```

Al ejecutar este comando se abrirá el navegador y podrás trabajar con los notebooks.

---

## 📚 Estructura del Repositorio

```bash
.
├── datasets/
│   └── USA_cars_datasets.csv    # Dataset principal
├── notebooks/
│   └── analisis_inicial.ipynb   # Ejemplo de notebook
├── requirements.txt             # Dependencias del proyecto
└── README.md                    # Documentación
```

---
