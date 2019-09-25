# Listas
Las listas permiten **guardar más de un elemento** dentro de una variable en un orden concreto. Pueden contener un número **ilimitado** de variables de **cualquier tipo**:

    alumnos = ["Ane", "Unai", "Itziar", "Mikel"]
    print(alumnos [0]) # muestra "Ane"
    print(alumnos [1]) # muestra "Unai"
    print(alumnos [2]) # muestra "Itziar"
    print(alumnos [-1]) # muestra "Mikel"

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

## Recorrer una lista
TODO
