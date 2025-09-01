# 🔬 Proyecto de Ciencias de Datos

Este proyecto utiliza un entorno virtual de Python para gestionar las dependencias.

## 📋 Requisitos previos
- Python 3.x instalado

## ⚙️ Crear y activar el entorno virtual

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

## � Conjunto de Datos

### US Cars Dataset

**Descripción:** El conjunto de datos incluye información de autos usados y "limpios" (sin daños) a la venta en Estados Unidos. Según las referencias, abarca datos de 28 marcas diferentes y contiene 12 atributos por vehículo. Entre las características se incluyen la marca, modelo, año, color, precio de venta, número de identificación vehicular (VIN), kilometraje, ubicación (estado y ciudad), estado del título, número de lote y condición del vehículo. En total el dataset registra 2.499 vehículos en venta.

**Etiquetas (tags):** Automóviles y vehículos. 

**Licencia:** No se especifica una licencia estándar.

**Fecha de publicación y última actualización:** El dataset fue publicado en 2020. 

**Autor/equipo:** Doaa Alsenani.


**Archivos incluidos:**
- `USA_cars_datasets.csv` — Formato CSV (tamaño aproximado: 284 KB según la página de Kaggle).

**Fuentes:** Información obtenida de referencias relacionadas con el dataset de Kaggle, que describen su contenido, atributos y metadatos.

## �🚀 Ejecutar Jupyter Notebook

Para iniciar Jupyter Notebook y trabajar con tus notebooks, asegúrate de tener el entorno virtual activado y ejecuta:

```powershell
jupyter notebook
```

Esto abrirá una ventana en tu navegador donde podrás crear y editar notebooks
