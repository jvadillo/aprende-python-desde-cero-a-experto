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
# Acceder al valor de una clave
edad = estudiante["edad"] # devuelve el valor de 'edad'
nota_media = estudiante.get("nota_media") # devuelve el valor de 'nota_media'

# Insertar o actualizar un valor:
estudiante["edad"] = 25 # actualiza el valor de 'edad'
estudiante["suspensos"] = 3 # inserta una nueva pareja clave - valor

# insertar una pareja clave - valor o actualizar si ya existe:
estudiante.update({'aprobados':'8'})
```

Algunos de los métodos más utilizados son los siguientes:

| Método | Acción |
|--|--|
| `diccionario.keys()` | Devuelve todas las claves del diccionario |
| `diccionario.values()` | Devuelve todos los valores del diccionario |
| `diccionario.pop(clave[,<default>])` | Elimina la clave del diccionario y devuelve su valor asociado. Si no la encuentra y se indica un valor por defecto, devuelve el valor por defecto indicado. |
| `diccionario.clear()` | Vacía el diccionario |
| `clave in diccionario` | Devuelve True si el diccionario contiene la clave o False en caso contrario. |
| `valor in diccionario.values()` | Devuelve True si el diccionario contiene el valor o False en caso contrario. |

## Recorrer un diccionario
La forma más habitual de recorrer un diccionario es mediante la sentencia `for`. Al recorrer un diccionario, por defecto se iterará sobre sus claves:

```python
diccionario =  {'a':1,  'b':2,  'c':3}
for key in diccionario:
	print(key)

# Resultado: a b c
```
Es decir, el código anteiror será equivalente al siguiente:
```python
diccionario =  {'a':1,  'b':2,  'c':3}
for key in diccionario.keys():
	print key

# Resultado: a b c
```
Por lo tanto, para iterar accediendo a los valores, realizaremos lo siguiente:

```python
diccionario =  {'a':1,  'b':2,  'c':3}
for key in diccionario:
	print(diccionario[key])

# Resultado: 1 2 3
```
Otro manera alternativa sería empleando la función `items()`, la cual devuelve el diccionario como tuplas de tipo (key,value):
```python
diccionario =  {'a':1,  'b':2,  'c':3}
for key, value in diccionario.items():
	print("El valor de %s is %d" % (key, value))

# Resultado:
# El valor de a is 1
# El valor de b is 2
# El valor de c is 3
```

## Borrar un elemento

Para borrar un elemento de un diccionario se utiliza la instrucción `del`.
```python
edades = {
   "Ane" : 22,
   "Jokin" : 27,
   "Aitor" : 15
}
del edades["Aitor"]
```
Otra alternativa también utilizada y mencionada anteriormente es la función `pop()`, el cual devuelve el valor del elemento eliminado:

```python
edades = {
   "Ane" : 22,
   "Jokin" : 27,
   "Aitor" : 15
}
edades.pop("Aitor")
```
Un diccionario nunca debería contener dos claves iguales. No obstante, en caso de contener una clave repetida, tanto `del` como `pop()` eliminarán todas las claves coincidentes.

## Coding time!

### Ejercicio 1
Crea un programa que recorra una lista y cree un diccionario que contenga el número de veces que aparece cada número en la lista.
- Ejemplo: `[12, 23, 5, 12, 92, 5,12, 5, 29, 92, 64,23]`
- Resultado: `{12: 3, 23: 2, 5: 3, 92: 2, 29: 1, 64: 1}`

### Ejercicio 2
Recorre un diccionario y crea una lista solo con los valores que contiene, sin añadir valores duplicados.
- Ejemplo: `{'Mikel': 3, 'Ane': 8, 'Amaia': 12, 'Unai': 5, 'Jon': 8, 'Ainhoa': 7, 'Maite': 5}`
- Resultado: `[3, 8, 12, 5, 7]`

### Ejercicio 3
Crea una programa de Login que compruebe el usuario y contraseña en el diccionario a continuación:

```python
usuarios = {  
      "iperurena": {  
          "nombre": "Iñaki",  
		  "apellido": "Perurena",  
		  "password": "123123"  
	  },  
	  "fmuguruza": {  
	       "nombre": "Fermín",  
		  "apellido": "Muguruza",  
		  "password": "654321"  
	  },  
	  "aolaizola": {  
	       "nombre": "Aimar",  
		  "apellido": "Olaizola",  
		  "password": "123456"  
	  }  
    }
```

El usuario tendrá un máximo de 3 intentos, y al acceder correctamente se mostrará el nombre y apellido del usuario.

### Ejercicio 4
Crea un programa que permita introducir a un profesor las notas de sus estudiantes (máximo 10 estudiantes). Los datos se deberán almacenar en un diccionario como el siguiente:

```python
estudiantes = {  
   "1": {  
	  "nombre": "Lorea",  
	  "nota": 8  
  },  
  "2": {  
      "nombre": "Markel",  
	  "nota": "4.2"  
  },  
  "3": {  
      "nombre": "Julen",  
	  "nota": 6.5  
  }  
}
```
Una vez introducidos todos los datos, el programa mostrará una lista con los nombres de los estudiantes que han suspendido y otra con los que han aprobado. También calculará y mostrará la nota media de la clase.
