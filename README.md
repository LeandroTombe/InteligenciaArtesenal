
Este proyecto utiliza un entorno virtual de Python para gestionar las dependencias.

- Python 3.x instalado


```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

```cmd
python -m venv venv
.\venv\Scripts\activate.bat
```

```bash
python3 -m venv venv
source venv/bin/activate
```


Una vez activado el entorno virtual, instala las dependencias necesarias (si tienes un archivo `requirements.txt`):

```powershell
pip install -r requirements.txt
```


Si agregas o actualizas paquetes en tu entorno virtual, puedes exportar todas las dependencias instaladas a un archivo `requirements.txt` con el siguiente comando:

```powershell
pip freeze > requirements.txt
```

Esto actualizará el archivo `requirements.txt` con todas las dependencias actuales del entorno virtual.


Para instalar o actualizar todas las dependencias listadas en `requirements.txt` ejecuta:

```powershell
pip install --upgrade -r requirements.txt
```


```powershell
deactivate
```


Para iniciar Jupyter Notebook y trabajar con tus notebooks, asegúrate de tener el entorno virtual activado y ejecuta:

```powershell
jupyter notebook
```

Esto abrirá una ventana en tu navegador donde podrás crear y editar notebooks de Python.
