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
TODO

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
