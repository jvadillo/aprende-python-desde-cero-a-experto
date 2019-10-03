# Excepciones
Las excepciones son **errores en la ejecución de un programa** que hacen que el programa termine de forma inesperada. Normalmente ocurren debido a un uso indebido de los datos (p.ej. una división entre cero). La manera de controlar las excepciones es agrupando el código en 2 bloques (más 1 opcional):

 - `try`: agrupa el bloque de código en el que se pueda dar una excepción.
 - `catch`: contiene el código a ejecutar en caso de que la excepción haya
   sido lanzada.
 - `finally` (opcional): permite ejecutar un bloque de    código siempre,
   se haya capturado o no una excepción.
```python
try:
	numero = int(input(‘Introduce un número: ‘))
	dividendo = 150
	resultado = dividendo / numero
	print(resultado)
except ValueError:
	print(‘Número inválido’)
except ZeroDivisionError:
	print(‘No se puede dividir entre 0’)
finally:
	print("Ejecutando finally antes de salir")
```

También es posible lanzar excepciones de forma controlada mediante la sentencia raise.

```python
    raise NameError('¡Soy una excepción!')
```

## Excepciones comunes
Hay algunas excepciones que son bastante comunes a la hora de programar en Python y que deberíamos contemplar en nuestros programas:

**TypeError**  es lanzado cuando se intenta realizar una operación o una función sobre un objeto de un tipo inapropiado.
```
>>> '1'+1  
Traceback (most recent call last):  
File "<pyshell#23>", line 1, in <module>  
'2'+2  
TypeError: must be str, not int
```

**ValueError**  es lanzado cuando el argumento de una función es de un tipo inapropiado.
```
>>> int('hola')  
Traceback (most recent call last):  
File "<pyshell#14>", line 1, in <module>  
int('xyz')  
ValueError: invalid literal for int() with base 10: 'hola'
```

**NameError**  es lanzado cuando no utiliza un objeto que no existe.
```
>>> persona  
Traceback (most recent call last):  
File "<pyshell#6>", line 1, in <module>  
age  
NameError: name 'persona' is not defined
```

**IndexError** es lanzado al intentar acceder a un índice que no existe en un array.
```
>>> lista = [1,2,3]  
>>> lista[5]  
Traceback (most recent call last):  
File "<pyshell#18>", line 1, in <module>  
lista[5]  
IndexError: list index out of range
```

**KeyError**  es lanzado cuando no se encuentra la clave (key),
```
>>> diccionario={'1':"esto", '2':"es", '3':"python"}  
>>> diccionario['4']  
Traceback (most recent call last):  
File "<pyshell#15>", line 1, in <module>  
diccionario['4']  
KeyError: '4'
````

**ModuleNotFoundError**  es lanzado cuando no se encuentra el módulo indicado.
```
>>> import mimodulo  
Traceback (most recent call last):  
File "<pyshell#10>", line 1, in <module>  
import mimodulo  
ModuleNotFoundError: No module named 'mimodulo'
```

## 👩‍💻Coding time! 👨‍💻

### Ejercicio 1
Crea un programa que acceda a la posición que el usuario indique de la siguiente lista: `[6,14,11,3,2,1,15,19]`. No olvides capturar las excepciones que puedan surgir en caso de que el usuario introduzca un índice incorrecto o que no exista en la lista.

### Ejercicio 2
Crea una aplicación reciba la clave de un diccionario y acceda a uno de sus valores. Asegúrate de que capturas las excepciones que puedan saltar al intentar acceder a una clave del diccionario inexistente.

