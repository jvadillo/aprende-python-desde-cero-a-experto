# Variables y Tipos de datos
Las variables permiten **almacenar datos del programa**. Las variables será de un tipo u otro en función de la información que se guarde en ellas. El nombre de una variable se conoce como **identificador**, y deberá cumplir las siguientes reglas:

 - Comenzar con una letra o un guión bajo.
 - El resto del nombre estará formado por letras, números o guiones bajos.
 - Los nombres de las variables son *case sensitive*, es decir, no es lo mismo que una variable se llame `resultado` que `RESULTADO`.
 - Existen una serie de palabras reservadas que no se pueden utilizar (def, global, return, if, for, ...).

Algunas de las recomendaciones respecto a los nombres de las variables están recogidas en la [Guía oficial de Estilos PEP8 de Python](https://www.python.org/dev/peps/pep-0008/). Entre las más habituales encontramos las siguientes:

 - Utilizar nombres descriptivos, en minúsculas y separados por guiones bajos si fuese necesario: `resultado`, `mi_variable`, `valor_anterior`,...
 - Escribir las constantes en mayúsculas: `MI_CONSTANTE`, `NUMERO_PI`, ...
 - Antes y después del signo `=`, debe haber uno (y solo un) espacio en blanco.

__Nota__: No olvides que lo que la guía plantea son recomendaciones y no obligaciones. Por ejemplo, mientras PEP8 recomienda tabular el código con 4 espacioes en blanco, la guía particular de los desarrolladores de Google habla de 2 espacios en lugar de 4.

## Resumen de tipos de variables

```python
    edad = 24 # número entero (integer)
    precio = 112.9 # número de punto flotante (float)
    titulo = ‘Aprende Python desde cero’ # cadena de texto (string)
    test = True # booleano
```

## Lectura de datos en Python

La función `input()` permite introducir datos al usuario:

```python
    >>> nombre = input()
    Leire
    >>> print(nombre)
    Leire
```

Como se puede ver en el siguiente ejemplo, es posible pasar como argumento el mensaje a mostrar al usuario.

```python
    >>> nombre = input("Escribe tu nombre: ")
    Escribe tu nombre: Leire
    >>> print(nombre)
    Lei
 ``
## inn! 
 ricio 1
Crrograma que contenga las siguientes variables:

 - nombre: tipo string y valor "Kobe Bryant"
 - edad: tipo integer y valor 45
 - media_puntos: tipo float y valor 28.5
 - activo: False

El programa deberá mostrar en pantalla todos los valores.

 rciio  programa que solicite el nombre, DNI y edad, lo almacene en 3 variables distintas y muestre por pantalla los valores introducidos.


## Números
Python soporta dos tipos de números: enteros (integer) y de punto flotante (float)
 
 ```python
    # integer
    x = 5
    print(x)
    
    # float
    y = 5.0
    print(y)
    
    # Otra forma de declarar un float
    z = float(5)
    print(z)
```

Si tenemos dudas del valor de una variable, podemos utilizar la función `type()`:

```python
    >>> x = 5.5
    >>> type(x)
    <class 'float'>
```

## Cadenas de texto (string)
 Las cadenas de texto o strings se definen mediante comilla simple (`' '`) o doble comilla (`" "`):

```python
    mi_nombre = 'Ane'
    print(mi_nombre)
    mi_nombre= "Ane"
    print(mi_nombre)
```

La diferencia principal es la mayor facilidad de las comillas dobles para introducir apóstrofes:

```python
    mi_nombre = 'I\'m John'
    print(mi_nombre)
    mi_nombre= "I'm John"
    print(mi_nombre)
```

Más información sobre strings y carácteres especiales en: [https://docs.python.org/3/tutorial/introduction.html#strings](https://docs.python.org/3/tutorial/introduction.html#strings)

Para definir strings multi-línea se utiliza la triples comillas (`"""`):

```python
frase = """ esto es una
        frase muy larga de más de
        una línea ..."""
```

### Concatenación de strings
Es posible unir dos strings con el operador `+`:

```python
    >>> primera_palabra = 'Hola'
    >>> frase_completa = primera_palabra + ', mundo'
    >>> print(frase_completa)
    'Hola, mundo'
    
    >>> segunda_palabra = 'mundo'
    >>> frase_completa = primera_palabra + ', ' + segunda_palabra
    >>> print(frase_completa)
    'Hola, mundo'
```

**Método alternativo 1**: str.join():
El método `join()` recibe como argumento el listado (de tipo List, Tuple, String, Dictionary y Set) de strings que se desean concatenar. Se invoca sobre el separador (el cual a su vez es un string también):

```python
    >>> strings = ['do', 're', 'mi']
    >>> separador = ' - '
    >>> separador.join(strings)
    'do - re - mi'
```

  Para iterar un elemento detrás del otro se introducirá como separador un string vacío:

```python
    >>> strings = ['do', 're', 'mi']
    >>> ''.join(strings)
    'doremi'
```
   
**Método alternativo 2**: `str.format()`:
Python 3 introdujo una nueva forma para formatear strings, la cual sustituye a la anterior en la que se hace uso del operador `%`. Para ello se invoca el método `format()` de un string:

```python
    # Ordenado por defecto:
    frase = "Meses: {}, {} y {}".format('Enero','Febrero','Marzo')
    print(frase)
    
    # Especificar el orden indicando la posición:
    frase = "Meses: {1}, {0} y {2}".format('Enero','Febrero','Marzo')
    print(frase)
    
    # Especificar el orden mediante parejas clave-valor:
    orden_palabra = "Meses: {ene}, {feb} y {mar}".format(ene='Enero', feb='Febrero',m='Marzo')
    print(frase)
```

### Conversión de tipos
A la hora de concatenar un string con otras variables como integer o float puede haber problemas:

```python
    >>> edad = 25
    >>> nota_media = 7.3
    >>> print("Tengo " + edad + " años y mi nota media es " + nota_media + ".")
    
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: can only concatenate str (not "int") to str
```

Mediante la función str() podemos convertir un valor a string:

```python
    >>> edad = 25
    >>> nota_media = 7.3
    >>> print("Tengo " + str(edad) + " años y mi nota media es " + str(nota_media) + ".")
    Tengo 25 años y mi nota media es 7.3.
```

De igual manera es posible convertir a otros tipos con las funciones `int()`, `float()` and `bool()`.

### Métodos en cadenas de texto (string)

Es posible **obtener un carácter concreto** de un string utilizando los corchetes `[]`:

```python
    frase = 'Aprendiendo a programar en Python'
    course[0] # devuelve el primer caracter
    course[1] # devuelve el segundo caracter
    course[-1] # devuelve el primer caracter empezando por el final
    course[-2] # # devuelve el segundo caracter empezando por el final
```

Si queremos **obtener un substring**, utilizaremos la siguiente notación:

```python
    frase = 'Aprendiendo a programar en Python'
    mi_substring = frase[1:5] # devuelve los caracteres desde la posición 1 hasta la 5 (no incluye el 5)
```

En caso de dejar la primera variable vacía, se considera la primera posición del string. Dejando la segunda variable vacía se considera la última posición del string:

```python
    >>> frase = 'Aprendiendo a programar en Python'
    >>> mi_substring = frase[:5]
    >>> mi_substring
    'Apren'
    >>> mi_substring = frase[4:]
    >>> mi_substring
    'ndiendo a programar en Python'
```

Otros métodos útiles de string:

```python
    str.upper() # convierte a mayúsculas
    str.lower() # convierte a minúsculas
    str.title() # convierte a mayúsculas la primera letra de cada palabra
    str.count(substring [, inicio, fin]) # devuelve el número de veces que aparece el substring en el string. Opcionalmente se puede indicar el inicio y fin. 
    str.find(‘d’) # devuelve el índice de la primera aparición de 'd' (o -1 si no lo encuentra)
    substr in str # devuelve True si el string contiene el substring
    str.replace(old, new [, count])   # reemplaza 'old' por 'new'un máximo de 'count' veces (opcional).
    str.isnumeric()   # devuelve True si str contiene solamente números
```

## 👩‍💻 Coding time! 👨‍💻
### Ejercicio 1
Escribe un programa que genere un string compuesto por los primeros 3 caracteres y los último 3 caracteres de un string introducido por el usuario.  
Ejemplo 1 : 'aprendiendo'  
Resultado : 'aprndo'  
Ejemplo 2 : 'escribiendo código'  
Resultado : 'escigo' 

### Ejercicio 2
Escribe un programa que solicite al usuario dos números y una frase. El primer número introducido se corresponderá a la posición de inicio del substring que deberá mostrar el programa por pantalla. El segundo número indicará la longitud de dicho substring.
 
- Ejemplo 1 : 4, 8, 'Desarrollar es mi nueva afición'  
- Resultado : ''rollar es"  
- Ejemplo 2 : '11, 8, Bienvenido a la clase de programación'  
- Resultado : 'a la cla' 

### Ejercicio 3
Escribe un programa que solicite al usuario una frase. A continuación le solicitará la letra que quiere reemplazar y por qué letra deberá reemplazarse. Por último el programa mostrará el número de veces que la letra está presente en la frase y el resultado final tras reemplazarla.
 
- Ejemplo 1 : 'Desarrollar es mi nuevo pasatiempos', 'a','e'
- Resultado : 4 apariciones. 'Deserroller es mi nueve pesetiempos'  
