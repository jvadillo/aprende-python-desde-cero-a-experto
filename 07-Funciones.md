# Funciones
Una función es un grupo de sentencias que realizan una tarea concreta. Esta forma de agrupar código es una forma de **ordenar** nuestra aplicación en pequeños bloques, **facilitando así su lectura** y permitiendo **reutilizar** el código que contienen sin esfuerzo.

## Definir y llamar a una función

La sintaxis de una función en Python es la siguiente:

```python
    def saludo(nombre):
	# codigo de la función
    	print("Hola, " + nombre+ ". ¡Bienvenido!")
```
	
Se escribe la palabra reservada `def` seguida del nombre de la función y sus parámetros entre paréntesis.

Para **llamar a una función** solo hay que escribir el nombre de la función seguida de los parámetros (si los hubiera) entre paréntesis.

```python
    >>> saludo('Maitane')
    Hola, Maitane. ¡Bienvenida!
```

Es posible asignar al parámetro un **valor por defecto**.

```python
    def saludo(nombre = "Anónimo"):  
    	print("Hola, " + nombre+ ". ¡Bienvenido!")
    
    saludo("Leire") # Hola, Maitane. ¡Bienvenida!
    saludo() # Hola, Anónimo. ¡Bienvenida!
```
Existen dos tipos de parámetros o argumentos:

 - **Parámetros posicionales**: la posición en la que se pasan importa
 - **Parámetros con palabra clave (keyword arguments)**: la posición no
   importa, se indica una clave para cada parámetro.

```python
def suma(a, b):
	resultado = a + b
	print(resultado)
suma(45, 20) # parámentros posicionales
suma(a = 45, b =20) # parametros mediante clave
```

Las funciones pueden **devolver un valor** utilizando la palabra `return`. Una vez devuelto un valor, la función finaliza su ejecución.

```python
    def suma(a, b):
	resultado = a + b
	return resultado

    print(suma(4,5)) # 9
```

## Funciones con argumentos múltiples

Es posible recibir un **número desconocido** de parámetros añadiendo un `*` en la definición de la función.

```python
    def suma_todo(*args):
    	resultado = 0
    	for i in args:
    		resultado += i
    		return resultado
    v, w, x, y, z = 5, 2, 12, 6, 9
    total = suma_todo(v, w, x, y, z)
    print("La suma total es:" + str(total))  # La suma total es: 34
```

## Ámbito de las variables (scope)
El ámbito de una variable (*scope*) se refiere a la zona del programa dónde una variable "existe". Fuera del ámbito de una variable no podremos acceder a su valor ni manejarla.

Los parámetros y variables definidos en una función no estarán accesibles fuera de la función. A este ámbito se le conoce como **ámbito local**. Es importante mencionar que una vez ejecutada una función, el valor de las variables locales no se almacena, por lo que la próxima vez que se llame a la función, ésta no recordará ningún valor de llamadas anteriores.

```python
    def calcula():
    	a = 1
    	print("Dentro de la función:", a)
    
    a = 5
    calcula()
    print("Fuera de la función:", a)
    
    ### Output ###
    # Dentro de la función:1
    # Fuera de la función:5
```

Por el contrario, las variables definidas fuera de una función sí que están accesibles desde dentro de la función. Se considera que están en el **ámbito global**. No obstante, no se podrán modifican dentro de la función a no ser que estén definidas con la palabra clave `global`.

