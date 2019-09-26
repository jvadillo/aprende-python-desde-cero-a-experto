# Clases y objetos
Python soporta la programación orientada a objetos. Esto quiere decir que podemos definir entidades agrupando (encapsulando) sus atributos y comportamiento (métodos) en clases.

La definición de una clase en Python se hace de la siguiente manera:

```python
    class Persona: 
	    # atributos
	    nombre = "Josune"
	    edad = 24 
	    
	    # metodos
	    def camina(self):
		    print(self.nombre + " está caminando")
```	    

A partir de una clase se pueden crear tantas **objetos** como se desee. Los objetos de una clase se conocen como **instancias**. Cada objeto **contiene los atributos y métodos de la clase** y podrá asignar a esos atributos unos valores concretos. Esto se conoce como el **estado de un objeto**.

```python
    p1 = Persona() # la variable p1 contiene un objeto de la clase Persona
    p1.camina()
    print(p1.nombre)  
    print(p1.edad)
```

Una función dentro de una clase se conoce como **método**. Las clases contienen el método especial `__init__` conocido como **constructor** y que sirve para inicializar un objeto. Al crear un objeto siempre se llama al constructor. Una diferencia importante con otros lenguajes como Java es que solo se puede definir un único constructor.

```python
    class Persona:  
	    def __init__(self, nombre, apellidos, edad):  
		    self.nombre= nombre
		    self.apellidos = apellidos 
		    self.edad = edad 
        
	    def camina(self):
		    print(self.nombre + " está caminando")
```

En la creación del objeto es necesario indicar los argumentos del constructor:

```python
    p1 = Persona("Mike", "Mendiola", 25)
    p1.camina()
    print(p1.nombre)  
    print(p1.edad)
```

El parámetro `self` de los métodos es una referencia a la propia instancia y se utiliza para acceder a las variables que pertenecen a la clase. Si no se define un constructor, la clase hereda uno que únicamente recibe el argumento `self`.

## Atributos de clase vs Atributos de instancia
Los atributos definidos dentro del constructor se conocen como **atributos de instancia**, por lo tanto, los atributos definidos dentro de la clase pero fuera del constructor se conocen como **atributes de clase**.

La principal diferencia es que un atributto de clase puede ser accedido aunque no existan instancias de la clase. Además, si se modifica su valor, se modificará el valor en todas las instancias existentes de dicha clase.

```python
class Demo:
	atrib_estatico = 123 # compartido por todos los objetos
	def __init__(self,numero):
		self.atrib_instancia = numero # específico de cada objeto

c1 = Demo(456)
c2 = Demo(789)

# Valor inicial
print("C1: Estatico {0} - Instancia: {1}".format(c1.atrib_estatico, c1.atrib_instancia))
# output: C1: Estatico 123 - Instancia: 456
print("C2: Estatico {0} - Instancia: {1}".format(c2.atrib_estatico, c2.atrib_instancia))
# output: C2: Estatico 123 - Instancia: 789

Demo.atrib_estatico = -1
 
print("C2: Estatico {0} - Instancia: {1}".format(c2.atrib_estatico, c2.atrib_instancia))
# output: C2: Estatico -1 - Instancia: 456
print("C2: Estatico {0} - Instancia: {1}".format(c2.atrib_estatico, c2.atrib_instancia))
# output: C2: Estatico -1 - Instancia: 789

c1.atrib_instancia = 999
  
print("C1: Estatico {0} - Instancia: {1}".format(c1.atrib_estatico, c1.atrib_instancia))
# output: C1: Estatico -1 - Instancia: 999

print("C2: Estatico {0} - Instancia: {1}".format(c2.atrib_estatico, c2.atrib_instancia))
# output: C2: Estatico -1 - Instancia: 789
```

## Private y protected
A diferencia de otros lenguajes de Programación Orientada a Objetos, todos los métodos y atributos en Python son públicos. Es decir, **no es posible definir una variable como** `private` o `protected`. 

Existe una convención de añadir como prefijo un **guión bajo** (`_`) a los atributos que consideramos como **protected** y dos guiones bajos (__) a las variables que consideramos private.

```python
class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre  # atributo protected 
        self.__edad = edad # atributo private
```
