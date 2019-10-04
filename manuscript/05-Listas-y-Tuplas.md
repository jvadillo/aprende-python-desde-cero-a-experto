# Listas y tuplas

Las listas permiten **guardar más de un elemento** dentro de una variable en un orden concreto. Pueden contener un número **ilimitado** de variables de **cualquier tipo**:

```python
    alumnos = ["Ane", "Unai", "Itziar", "Mikel"]
    print(alumnos [0]) # muestra "Ane"
    print(alumnos [1]) # muestra "Unai"
    print(alumnos [2]) # muestra "Itziar"
    print(alumnos [-1]) # muestra "Mikel"
```

Los **métodos más utilizados** con las listas son los siguientes:
| Método | Acción |
|--|--|
| `alumnos.append("Amaia")` | Inserta "Jon" al final de la lista |
| `alumnos.insert(0,"Amaia")` | Inserta "Amaia" en la posición 0 |
| `alumnos.remove("Amaia")` | Elimina la primera aparición de "Amaia" de la lista |
| `alumnos.pop()` | Elimina el último elemento de la lista |
| `alumnos.clear()` | Elimina todos los elementos de la lista |
| `alumnos.index("Amaia")` | Devuelve el índice de la primera aparición de "Amaia" |
| `alumnos.sort()` | Ordena la lista (los elementos deben ser comparables) |
| `sorted(alumnos)` | Devuelve una copia de la lista 'alumnos' ordenada (no ordena la pasada como parámetro)  |
| `alumnos.reverse()` | Ordena la lista en orden inverso |
| `alumnos.copy()` | Devuelve una copia de la lista |
| `alumnos.extend(otra_lista)` | Fusiona las dos listas |

### Recorrer una lista
La forma habitual de recorrer una lista es mediante la sentencia `for`, tal y como muestra el ejemplo a continuación:

```python
    for elemento in ['Python','JavaScript','JAVA']:
        print("Programo en ", elemento)
```
De igual manera se podría hacer mediante la sentencia `while`:

```python
    lista =  ['Python','JavaScript','JAVA']
    i = 0
    sizeofList = len(lista) 
    while i < sizeofList :
        print(lista[i]) 
        i += 1
```


## Tuplas
Las tuplas son **listas inmutables**. Es decir, una vez declaradas, no se pueden realizar modificaciones sobre ellas (añadir/eliminar elementos o hacer modificaciones sobre ellos). Para definir una tupla se escriben los elementos entre paréntesis:

```python
    valores = (1,2,3)
```
El acceso a sus elementos se hace de igual que con listas:

```python
    valores = ("a", "b", "c","d","e","f")  
    print(valores[1])
    print(valores[2:4])
```

Una acción típica de las tuplas es "desempaquetar" (unpack) sus valores:

```python
    a, b, c = valores 
```

## Coding time!

### Ejercicio 1
Dada la siguiente lista `[12, 23, 5, 29, 92, 64]` realiza las siguientes operaciones y vete mostrando la lista resultante por pantalla:
1. Elimina el último número y añádelo al principio.
2. Mueve el segundo elemento a la última posición.
3. Añade el número `14` al comienzo de la lista.
4. Suma todos los números de la lista y añade el resultado al final de la lista.
5. Comina la lista actual con la siguiente: `[4, 11, 32]`
6. Elimina todos los números impares de la lista.
7. Ordena los números de la lista de forma ascendente.
8. Vacía la lista.

### Ejercicio 2
Crea un programa que solicite al usuario 5 números y los guarde en una lista. A continuación el programa pedirá otros 5 números al usuario almacenándolos en una segunda lista. El programa mostrará al usuario una lista que contenga los números que tienen en común las dos listas anteriores.
- Ejemplo: Lista 1 = `[6,14,11,78,5]` y Lista 2 = `[3,14,22,78,9]`
- Resultado: `[14, 78]`
