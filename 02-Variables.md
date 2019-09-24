# Variables y Tipos de datos
Las variables permiten almacenar datos del programa. Las variables será de un tipo u otro en función de la información que se guarde en ellas. El nombre de una variable se conoce como **identificador**, y deberá cumplir las siguientes reglas:

 - Comenzar con una letra o un guión bajo
 - El resto de nombre estará formado por letras, números o guiones bajos.
 - Los nombres de las variables son case sensitive, es decir, no es lo mismo que una variable se llame `resultado` que `RESULTADO`.
 - Existe una serie de palabras reservadas que no se pueden utilizar (def, global, return, if, for, ...).

Existen algunas recomendaciones respecto a los nombres de las variables, recogidas en la [guía de estilo PEP8 de Python](https://www.python.org/dev/peps/pep-0008/):

 - Utilizar nombres descriptivos, en minúsculas y separados por guiones bajos si fuese necesario: `resultado`, `mi_variable`, `valor_anterior`,...
 - Escribir las constantes en mayúsculas: `MI_CONSTANTE`, `NUMERO_PI`, ...
 - Antes y después del signo `=`, debe haber uno (y solo un) espacio en blanco.

## Resumen de tipos de variables

    edad = 24 # número entero (integer)
    precio = 112.9 # número de punto flotante (float)
    titulo = ‘Aprende Python desde cero’ # cadena de texto (string)
    test = True # booleano

## Lectura de datos en Python

La función input() permite introducir datos al usuario:

    >>> nombre = input()
    Leire
    >>> print(nombre)
    Leire

Como se puede ver en el siguiente ejemplo, es posible pasarle como argumento el mensaje a mostrar al usuario.

    >>> nombre = input("Escribe tu nombre: ")
    Escribe tu nombre: Leire
    >>> print(nombre)
    Leire
