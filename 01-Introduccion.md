
# Introducción
Python es uno de los lenguajes de programación más populares. En comparación a otros lenguajes de programación, Python tiene una **curva de aprendizaje pequeña y un gran potencial** realizar tareas de todo tipo, como por ejemplo:
 - Desarrollo de aplicaciones web
 - Inteligencia artificial
 - Automatización de tareas
 - Análisis avanzado de datos

## Características principales
Se trata de un lenguaje **open source** en el que destaca su legibilidad. El código es limpio y ordenado, lo cual lo convierte en un lenguaje fácil de leer y escribir, en definitiva:  **fácil de entender y aprender**. 
Al contrario que otros lenguajes de programación, **Python es un lenguaje interpretado**, lo que significa que no es necesario compilar el código de Python antes de ejecutarlo. El intérprete irá ejecutando el código línea por línea. 

Otra de las principales características de Python es que es que es un lenguaje de programación **dinámicamente tipado**, es decir, el programador no tiene que declarar el tipo de las variables si no que se decide automáticamente en el tiempo de ejecución.

Por último, comentar que una de las mayores ventajas de este lenguaje de programación **orientado a objetos** es la extensa variedad de **liberías y frameworks** disponibles para cualquier propósito, lo cual hace que Python sea la opción perfecta para aplicaciones de todo tipo.

## Instalación de Python
Python es un lenguaje multiplataforma, lo cual significa que podemos trabajar con Python tanto en Windows, Mac o Linux. A pesar de que todavía encontrarás código escrito en Python 2, en la actualidad la versión recomenda es Python 3.

### Instalar Python en Windows
Estos son los pasos para instalar Python en Windows:

 1. Descarga la última versión de Python para Windows desde la página web oficial:https://www.python.org/downloads/windows/
 2. En función de la versión de tu sistema operativo (32 btis o 64 bits), tendrás que escoger entre una de las dos versiones: **Windows x86 executable installer** o **Windows x86-64 executable installer**.
 3. Una vez descargado, ejecuta el instalador marcando las casillas "Add Python 3.6 to PATH" y "Add Python to your environment variables".

### Instalar Python en Ubuntu
En primer lugar comprueba que Python no esté instalado en el sistema mediante el siguiente comando:
```
$ python3 --version
Python 3.6.1
```
En caso de no estar instalado, basta con ejecutar el siguiente comando en la consola:
```
$ sudo apt install python3
```

### Instalar Python en Mac
La instalación para Mac es sencilla y directa. Simplemente descarga la última versión de Python desde la página web oficial y ejecuta el archivo .pkg descargado.

## Entorno de desarrollo
### Editores de código
Para programar en Python es suficiente con tener un editor de texto cualquiera, aunque hoy en día es recomendable utilizar un editor avanzado o un IDE que permita programar de forma ágil. Algunas de las opciones más recomendadas son:

 - Editores de texto 
	 - Atom: [https://atom.io/](https://atom.io/) 
	 - Sublime Text: [https://www.sublimetext.com/3](https://www.sublimetext.com/3)
	 - Visual Studio Code: [https://code.visualstudio.com/](https://code.visualstudio.com/) 
 - IDEs 
	 - PyCharm: [https://www.jetbrains.com/pycharm/](https://www.jetbrains.com/pycharm/) 
	 - Eclipse: [https://www.eclipse.org/](https://www.eclipse.org/)

### Virtual environments / Pipenv / virtualenv
TODO

## Hola Mundo
Ya tenemos Python instalado en nuestro sistema, por lo que estamos preparados para comenzar a escribir y ejecutar código Python. Veremos como ejecutar código Python **desde la consola directamente o desde un archivo** de extensión `.py` 

### Consola de Python
La consola de Python nos **permite ejecutar código directamente**, sin tener que escribir el código previamente ningún fichero. Para entrar en la consola de Python, abre una consola o shell del sistema operativo en el que te encuentres y escribe `py` o `python`:

    python
    Python 3.7.3 (v3.7.3:ef4ec6ed12, Mar 25 2019, 21:26:53) [MSC v.1916 32 bit (Intel)] on win32
    Type "help", "copyright", "credits" or "license" for more information.
    >>>

Verás cómo el cursor cambia y ahora aparece el símbolo `>>>`. A partir de ahora ya podemos ir ejecutando las instrucciones que queramos. En este caso escribiremos nuestro primer programa, el ya conocido ¡Hola Mundo!
```python
    >>> print("¡Hola Mundo!")
    ¡Hola Mundo!
```
También puedes ejecutar otras instrucciones. Prueba a ejecutar la siguiente operación:
```python
    >>> 3*3
    9
```

Para salir de la consola de Python, escribe `exit()` o pulsa `CTRL + Z` y `ENTER`.


### Ejecutar fichero

También podemos escribir nuestro código en un fichero con extensión `.py` y ejecutarlo. Abre un editor de texto y crea un fichero llamado holamundo.py con el siguiente contenido:

```python
    print("¡Hola Mundo!")
```

Para ejecutar el archivo, abre una consola de comandos y escribe lo siguiente:

    python holamundo.py

¡Enhorabuena! Ya has escrito tu primer programa en Python.

## Sintaxis

### Indentación

Un aspecto muy importante a mencionar antes de comenzar a programar en Python es el hecho de que **Python utiliza la indentación** (también conocida como sangría, tabulación o espaciado) para **delimitar los bloques de código**. La indentación estándar de Python requiere una tabulación de 4 espacios:

```python
    x = 5
    if x == 5:
        # tabulación de 4 espacios
        print("El valor de x es 5.")
```

En caso contrario, al ejecutar nuestro código recibiremos un error como el siguiente

    IndentationError: unindent does not match any outer indentation level

### Comentarios

A la hora de programar es posible que queramos introducir en el código comentarios que añadan información extra sin afectar a la ejecución del programa. En Python los comentarios se insertan mediante el carácter hash (#):

## Funcionamiento de Python

TODO
