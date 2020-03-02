# Listas y tuplas

Las listas permiten **guardar más de un elemento** dentro de una variable, y además hacerlo en un orden concreto. Pueden contener un número **ilimitado** de elementos de **cualquier tipo**:

```python
    # Lista vacía
    lista_vacia = []

    # Lista con valores
    alumnos = ["Ane", "Unai", "Itziar", "Mikel"]
    
    # Acceder a elementos
    print(alumnos[0]) # muestra "Ane"
    print(alumnos[1]) # muestra "Unai"
    print(alumnos[2]) # muestra "Itziar"
    print(alumnos[-1]) # muestra "Mikel"
    
    # Cambiar un elemento
    alumnos[0] = "Nora" 
```

Los **métodos más utilizados** con las listas son los siguientes:
| Método | Acción |
|--|--|
| `alumnos.append("Amaia")` | Inserta "Jon" al final de la lista |
| `alumnos.insert(0,"Amaia")` | Inserta "Amaia" en la posición 0 |
| `alumnos.remove("Amaia")` | Elimina la primera aparición de "Amaia" de la lista |
| `alumnos.pop()` | Elimina el último elemento de la lista |
| `alumnos.pop(3)` | Elimina el cuarto elemento de la lista |
| `alumnos.clear()` | Elimina todos los elementos de la lista |
| `alumnos.index("Amaia")` | Devuelve el índice de la primera aparición de "Amaia" |
| `alumnos.sort()` | Ordena la lista (los elementos deben ser comparables) |
| `sorted(alumnos)` | Devuelve una copia de la lista 'alumnos' ordenada (no ordena la pasada como parámetro)  |
| `alumnos.reverse()` | Ordena la lista en orden inverso |
| `alumnos.copy()` | Devuelve una copia de la lista |
| `alumnos.extend(otra_lista)` | Fusiona las dos listas |

### Acceder a varios elementos de una lista

Si queremos acceder a un subconjunto de elementos de la lista, es posible hacerlo de la siguiente manera:

```python
lista = ['a','b','c','d','e','f']
# Elementos de la segunda a la cuarta posición
print(lista[1:3]) # Salida: ['b', 'c']

# Elementos desde la primera hasta la cuarta posición
print(lista[:3]) # Salida: ['a', 'b', 'c']

# Elementos desde la tercera posición hasta el final
print(lista[2:]) # Salida: ['c', 'd', 'e', 'f']
```

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
    valores = (1,2,3,4,5)
    print(valores)  # Salida: (1, 2, 3, 4, 5) 
    
    # tuple with mixed datatypes
    valores_mixtos = (1, "Hola", 2.5, False)
    print(valores_mixtos)  # Salida: (1, 'Hola', 2.5, False)
```
El acceso a sus elementos se hace de igual que con listas:

```python
    valores = ("a", "b", "c","d","e","f")  
    print(valores[1]) # Salida: 'b'
    print(valores[2:4]) # Salida: ('c', 'd')
```

Una acción típica de las tuplas es "desempaquetar" (unpack) sus valores, es decir, asignarlos a variables directamente:

```python
    tupla = (1, "Hola", 2.5) # Creamos la tupla
    
    var1, var2, var3 = tupla # Hacemos el unpack
    
    print(var1)      # 1
    print(var2)      # 'Hola' 
    print(var3)      # 2.5
```

## Coding time!

### Ejercicio 1
Dada la siguiente lista `[12, 23, 5, 29, 92, 64]` realiza las siguientes operaciones y vete mostrando la lista resultante por pantalla:
1. Elimina el último número y añádelo al principio.
2. Mueve el segundo elemento a la última posición.
3. Añade el número `14` al comienzo de la lista.
4. Suma todos los números de la lista y añade el resultado al final de la lista.
5. Fusiona la lista actual con la siguiente: `[4, 11, 32]`
6. Elimina todos los números impares de la lista.
7. Ordena los números de la lista de forma ascendente.
8. Vacía la lista.

Resultado:

```
[64, 12, 23, 5, 29, 92]
[64, 23, 5, 29, 92, 12]
[14, 64, 23, 5, 29, 92, 12]
[14, 64, 23, 5, 29, 92, 12, 239]
[14, 64, 23, 5, 29, 92, 12, 239, 4, 11, 32]
[14, 64, 92, 12, 4, 32]
[4, 12, 14, 32, 64, 92]
[]
```

### Ejercicio 2
Crea un programa que solicite al usuario 5 números y los guarde en una lista. A continuación el programa pedirá otros 5 números al usuario almacenándolos en una segunda lista. El programa mostrará al usuario una lista que contenga los números que tienen en común las dos listas anteriores.
- Ejemplo: Lista 1 = `[6,14,11,78,5]` y Lista 2 = `[3,14,22,78,9]`
- Resultado: `[14, 78]`
