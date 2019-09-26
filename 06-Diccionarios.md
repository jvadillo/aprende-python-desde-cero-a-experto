# Diccionarios
Un diccionario es un conjunto de parejas **clave- valor** (key-value). Es decir, se accede a cada elemento a partir de su clave. Se definen de la siguiente manera:

```python
    estudiante = {
    	"nombre": "Iñaki Perurena",
    	"edad": 30,
    	"nota_media": 7.25,
    	"repetidor" : False
    }
```

Las **claves tienen que ser únicas** y estar formadas por un **string o un número**. Para acceder al valor de una clave exiten dos maneras distintas:

```python
    edad = estudiante["edad"] # devuelve el valor de 'edad'
    nota_media = estudiante.get("nota_media") # devuelve el valor de 'nota_media'
    
    estudiante["edad"] = 25 # actualiza el valor de 'edad'
    estudiante["suspensos"] = 3 # inserta una nueva pareja clave - valor
    estudiante.update({'aprobados':'8'}): inserta una nueva pareja clave - valor o actualiza su valor si ya existiera
```

Algunos de los métodos más utilizados son los siguientes:

| Método | Acción |
|--|--|
| `diccionario.keys()` | Devuelve todas las claves del diccionario |
| `diccionario.values()` | Devuelve todos los valores del diccionario |
| `diccionario.pop(clave[,<default>])` | Elimina la clave del diccionario y devuelve su valor asociado. Si no la encuentra y se indica un valor por defecto, devuelve el valor por defecto indicado. |
| `diccionario.clear()` | Vacía el diccionario |
| `diccionario.clear()` | Vacía el diccionario |
| `clave in diccionario` | Devuelve True si el diccionario contiene la clave o False en caso contrario. |
| `valor in diccionario.values()` | Devuelve True si el diccionario contiene el valor o False en caso contrario. |

## Recorrer un diccionario
//TODO




