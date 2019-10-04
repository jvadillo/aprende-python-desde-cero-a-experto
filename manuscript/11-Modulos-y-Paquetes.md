
# Módulos y Paquetes

## Módulos
Un módulo es un archivo de Python que contiene variables, funciones y clases. Es una forma de ordenar y reutilizar código ya que todo el contenido de un módulo es accesible por los archivos que lo importen.

```python
# mundo.py

def hola_mundo():
    print("¡Hola Mundo!")

def adios_mundo():
    print("¡Adios Mundo!")

```

Para acceder a las funciones desde otro archivo Python se utiliza la palabra reservada `import`:

```python
# app.py

import mundo

# Llamada a la función
mundo.hola_mundo()
```

También existe la posibilidad de importar únicamente objetos concretos de un módulo mediante la sintaxis `from ... import`:

```python
# app.py

from mundo import adios_mundo

# Llamada a la función
adios_mundo()
```

De esta forma no es necesario escribir el nombre del modulo antes de utilizar la función. De igual manera, se pueden importar varios objetos de un módulo separándolos por una coma:

```python
# app.py

from mundo import adios_mundo, hola_mundo
```

Para importar todos los los objetos de un módulo basta con utilizar el asterisco:

```python
# app.py

from mundo import *
```

### Localización de los módulos
Al importar un módulo Python lo buscara en los siguientes directorios:

 1. En el directorio actual.
 2. En los directorios declarados en el `PYTHONPATH` (variable de entorno que contiene un listado de directorios)
 3. En el directorio de instalación de Python por defecto (en UNIX normalmente '`/usr/local/lib/python`/')

## Paquetes
Es posible agrupar los módulos que tienen relación en un mismo directorio. Estos directorios son conocidos en Python como paquetes y deben contener siempre un archivo llamado `__init__.py` para que Python lo reconozca como un paquete.

A medida que desarrollamos una aplicación es habitual agrupar los archivos en directorios (paquetes) para tener el código organizado.

Para cargar un módulo ubicado en un paquete lo haremos de la siguiente forma:

```python
import mipaquete.mundo
```
o bien de la siguiente manera:
```python
from mipaquete import mundo
```
También es posible importar elementos concretos de un módulo:
```python
from mipaquete.mundo import adios_mundo, hola_mundo
```


