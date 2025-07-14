Este Proyecto consite en un monitor de recursos para computadoras. 
Es una aplicación web desarrollada con Django que permite visualizar en tiempo real el estado del sistema, incluyendo el uso de CPU, memoria RAM, almacenamiento en disco y otros recursos relevantes. Utiliza la librería externa `psutil`.
Para la ejecucion del programa se requier descargar el archivo "monitor proyecto.zip"
Extraer el contenido para descomprimir.

Objetivo General

Crear una aplicación web que permita monitorear recursos del sistema en tiempo real desde un navegador web, utilizando Django como framework y `psutil` para la recolección de datos.
Aplicar librerías externas en Python para monitorear el sistema.
Desarrollar una aplicación web con Django.
Validar el funcionamiento correcto de servicios y mostrar métricas en tiempo real.
Mejorar la experiencia de usuario con una interfaz clara y actualizable.
Componentes del Proyecto

1. `manage.py`
Archivo principal para interactuar con Django. Permite correr el servidor, ejecutar migraciones, entre otros comandos.

2. `monitor/`
Contiene:
- `settings.py`: Configuración del proyecto (apps, idioma, base de datos, etc.).
- `urls.py`: Define las rutas del sitio.
- `wsgi.py`: Configura el servidor web para ejecutar Django.

3. `sistema/`
Aplicación interna que contiene:
- `views.py`: Lógica para recolectar datos del sistema usando `psutil`.
- `templates/sistema/index.html`: Página web donde se muestran los datos en tarjetas.

Funcionalidad

Cuando se accede a la página principal, se obtiene la siguiente informacion:

1. Se ejecuta la vista `sistema_info()` que recolecta datos del sistema:
   - Uso del CPU
   - Uso de memoria RAM (GB y %)
   - Uso del disco (GB y %)
   - Sistema operativo
   - Núcleos del procesador
2. Esta información se envía a la plantilla HTML.
3. La página se muestra con los datos y se actualiza automáticamente cada 10 segundos, o mediante un botón "Actualizar".

Instrucciones para ejecutar el proyecto

1. Clona o descomprime el proyecto

monitor_proyecto.zip

En la ruta de almacenamiento ejecutar un Terminal o PowerShell en modo administrador.
Ejecutar el comando # Monitor del Sistema con Django y Psutil

1. Crea un entorno virtual

Copiar código
python -m venv venv

2. Activa el entorno virtual en Windows

Copiar código
.\venv\Scripts\activate

3. Instala las dependencias

Copiar código
pip install -r requirements.txt

4.Ejecuta migraciones

Copiar código
python manage.py migrate

5.Corre el servidor

Copiar código
python manage.py runserver

6.Abrir el navegador y visitar:
http://127.0.0.1:8000

Autor
Nombre: (Adrian Benitez Gonzales)
Curso: Arquitectura de Computadoras
Universidad: (Universidd Tecnologica de Honduras)
