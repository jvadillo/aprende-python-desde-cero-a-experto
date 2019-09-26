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
