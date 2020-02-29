# Operadores y expresiones
Los operadores son símbolos especiales que permiten realizar operaciones aritméticas o lógicas.

## Operadores aritméticos

Los operadores aritméticos se utilizan para realizar operaciones matemáticas (suma, resta, multiplicación,...). La tabla siguiente contiene todos los operadores aritméticos permitidos por Python:

| Operador | Ejemplo | Significado |
| :--:         |     :--:     |          -- |
| +   | a + b     | Suma    |
|  -  |  a - b    |  Resta|
|  -  |  -a    |  Negación (asignar valor negativo)|
|  *  |  a * b    |  Multiplicación|
|  / |   a / b   |  División|
|  %  |  a % b    | Módulo (resto de la división) |
|  //  | a // b     | División entera |
|  **  | a ** b     |  Exponente |

Ejemplos:

```python
x = 5	
y = 2
print(x + y) # 7
print(x - y) # 3
print(x * y) # 10
print(x / y) # 2.5
```


## Operadores relacionales o de comparación

Los operadores relacionales se utilizan para comparar valores y devuelven como resultado un booleano: `True` o `False`.

| Operador | Ejemplo | Significado |
| :--:         |     :--:     |          -- |
| >   | a > b     | Mayor que: `True` si a es mayor que b    |
| <   | a > b     | Menor que: `True` si a es menor que b|
| ==   | a == b     | Igual: `True` si a y b son iguales|
| !=   | a != b     | Distinto: `True` si a y b son distintos    |
| >=   | a >= b     | Mayor o igual: `True` si a es igual o mayor que b    |
| <=   | a >= b     | Menor o igual: `True` si a es igual o menor que b|


## Operadores lógicos
Los operadores lógicos `and` `or`, y `not` evalúan valores devolviendo también `True`o `False` como resultado:

| Operador | Ejemplo | Significado |
| :--:         |     :--:     |          -- |
| and   | a and b     | True si a y b son True    |
| or   | a or b     | True si a o b son true|
| not   | not b     | True si b es falso|


## Coding time!

### Ejercicio 1

Crea un programa que solicite al usuario un número del 1 al 10 y muestre por pantalla la tabla de multiplicación del 1 al 10.
Ejemplo:
```
Introduce un número del 1 al 10: 3
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
3 x 6 = 18
3 x 7 = 21
3 x 8 = 24
3 x 9 = 27
3 x 10 = 30
```

### Ejercicio 2
Crea un programa que solicite al usuario dos números enteros y muestre por pantalla el resultado de las siguientes operaciones: suma, resta, multiplicación y división.
Ejemplo:

```
Introduce el primer número: 8
Introduce el segundo número: 2
La suma es: 10
La resta es: 6
La multiplicación es: 16
La división es: 4.0
```

### Ejercicio 3
Crea un programa que solicite al usuario el radio de un círculo y calcule el área.
Nota: Utiliza 3.14159 como número PI para el cálculo del área.

Ejemplo:
```
Introduce el radio: 3
El área es: 28.274309999999996
```


