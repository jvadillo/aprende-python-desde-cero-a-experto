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

Una clase es como una plantilla o modelo para crear a partir de ella objetos. Esta plantilla contiene la información para definir cómo serán los objetos, es decir, qué atributos y métodos tendrán.

A partir de una clase se pueden crear tantos **objetos** como se desee. Los objetos de una clase se conocen como **instancias**. Cada objeto **contiene los atributos y métodos de la clase** y podrá asignar a esos atributos unos valores concretos. Esto se conoce como el **estado de un objeto**.

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
Los atributos definidos dentro del constructor se conocen como **atributos de instancia**, por lo tanto, los atributos definidos dentro de la clase pero fuera del constructor se conocen como **atributos de clase**.

La principal diferencia es que un atributto de clase puede ser accedido aunque no existan instancias de la clase. Además, si se modifica su valor, se modificará el valor en todas las instancias existentes de dicha clase.

```python
class Demo:
	atrib_estatico = 123 # compartido por todos los objetos
	def __init__(self,numero):
		self.atrib_instancia = numero # específico de cada objeto

c1 = Demo(456)
c2 = Demo(789)

# Valor inicial
print(f"C1: Estatico {1.atrib_estatico} - Instancia: {c1.atrib_instancia}")
# output: C1: Estatico 123 - Instancia: 456
print(f"C2: Estatico {c2.atrib_estatico} - Instancia: {c2.atrib_instancia}")
# output: C2: Estatico 123 - Instancia: 789

Demo.atrib_estatico = -1
 
print(f"C2: Estatico {c2.atrib_estatico} - Instancia: {c2.atrib_instancia}")
# output: C2: Estatico -1 - Instancia: 456
print(f"C2: Estatico {c2.atrib_estatico} - Instancia: {c2.atrib_instancia}")
# output: C2: Estatico -1 - Instancia: 789

c1.atrib_instancia = 999
  
print(f"C1: Estatico {c1.atrib_estatico} - Instancia: {c1.atrib_instancia}")
# output: C1: Estatico -1 - Instancia: 999

print(f"C2: Estatico {c2.atrib_estatico} - Instancia: {c2.atrib_instancia}")
# output: C2: Estatico -1 - Instancia: 789
```

Es importante remarcar que para acceder a los atributos de instancia se debe utilizar la palabra reservada `self`, la cual hace referencia al objeto actual. En Python no podemos utilizar `self` en cualquier momento, para utilizarlo hay que indicarlo en los métodos cómo el primer parámetro recibido.

```python
class Persona:  
	def __init__(self, nombre, apellidos, edad):  
		self.nombre= nombre
		self.apellidos = apellidos 
		self.edad = edad 
	
	def camina(self): # es necesario indicar 'self' como primer argumento
		print(self.nombre + " está caminando")

p1 = Persona("Mike", "Mendiola", 25) # no hay que pasarle 'self'
p1.camina() # no hay que pasarle 'self'
print(p1.nombre)  
print(p1.edad)
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

## Coding time!

### Ejercicio 1
Crea la clase Coche que contenga las siguientes propiedades:

- `matrícula` (string)
- `marca` (string)
- `kilometros_recorridos` (float)
- `gasolina` (float)

La clase tendrá un método llamado `avanzar()` que recibirá como argumento el número de kilómetros a conducir y sumará los kilómetros recorridos al valor de la propiedad `kilometros_recorridos`. El método también restará al valor de `gasolina` el resultado de los kilómetros multiplicado por 0'1.
La clase también contendrá otro método llamado `repostar()` que recibirá como argumento los litros introducidos que deberán sumarse a la variable `gasolina`.
Por último, será necesario controlar que el método avanzar nunca obtendrá un número negativo en la gasolina. En dicho caso, deberá mostrar el siguiente mensaje: "Es necesario repostar para recorrer la cantidad indicada de kilómetros".

Ejemplo:

 - `avanzar(50)` # gasolina = 50
 - `avanzar(100)` # kilometros_recorridos = 100, gasolina = 40
 - `avanzar(40)` # kilometros_recorridos = 140, gasolina = 36
 - `avanzar(180)` # kilometros_recorridos = 320, gasolina = 18

### Ejercicio 2
Crea una clase Robot que simule los movimientos de un robot y calcule la posición en la que se encuentra cada momento. El robot se moverá por un tablero infinito de coordenadas X e Y, podrá realizar los siguientes movimientos:
- Avanzar hacia adelante (A)
- Retroceder (R)
- Avanzar hacia la izquierda (I) o hacia la derecha (D)

El robot tendrá un método llamado `mueve()` que recibirá la orden como parámetro y otro método, `posicion_actual()`,  que indicará su posición en las coordenadas X e Y. Al crear el robot este se inicializará a las coordenadas (0,0).

Puedes utilizar el siguiente código para probar la clase creada:

```python
miRobot = Robot()
orden = "A"
while orden != 'fin':
    orden = input("Introduce la orden: ")
    miRobot.mueve(orden)
    print(miRobot.posicion_actual())
```

Ejemplo:

```
>> Introduce la orden: A
Posición actual: 1,0
>> Introduce la orden: A
Posición actual: 2,0
>> Introduce la orden: I
Posición actual: 2,-1
>> Introduce la orden: A
Posición actual: 3,-1
>> Introduce la orden: I
Posición actual: 3,-2
>> Introduce la orden: D
Posición actual: 3,-1
>> Introduce la orden: R
Posición actual: 2,-1
>> Introduce la orden: fin
```

### Ejercicio 3
Mejora el ejercicio anterior de forma que el robot pueda recibir una secuencia de movimientos.
Por ejemplo:
- mueve("AADDADIR")

También deberá tener otros dos métodos: uno que devuelva todas las órdenes recibidas y otro capaz de listar los movimientos necesarios para volver a la posición inicial (0,0).

Aquí tienes un ejemplo de una posible ejecución del programa:

```
Introduce la orden: AADAD
Posición actual: 3,2
Introduce la orden: IAADR
Posición actual: 4,2
Introduce la orden: fin
Posición actual: 4,2

Órdenes recibidas: AADADIAADRfin
Secuencia para posición inicial: RRRRII
```

### Ejercicio 4
Crea la clase Triangulo que almacene la longitud de cada uno de sus lados. Deberá contener los siguientes métodos:
- `area()`: devuelve el área del triángulo
- `forma()`: indica si se trata de un triángulo equilátero, isósceles o irregular.
- `perímetro()`: devuelve el perímetro del triángulo.
