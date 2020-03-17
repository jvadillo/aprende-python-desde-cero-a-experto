# Herencia

La herencia es una técnica de la Programación Orientada a Objetos en la que una clase (conocida como **clase hija** o **subclase**) hereda todos los métodos y propiedades de otra clase (conocida como **padre** o **clase base**).

La sintaxis para definir una clase que herede de otra es la siguiente:

```python
class ClaseBase:
	# código de la clase base

class Subclase(BaseClass):
	# código de la subclase
```

La subclase puede añadir funcionalidades. Esta técnica permite **reutilizar código**.

```python
class Dispositivo:
	def __init__(self,identificador,marca):
		self.identificador = identificador
		self.marca = marca

	def conectar(self):
		print("¡Conectado!")

# la clase base se indica entre paréntesis
class Teclado(Dispositivo):
	def __init__(self,identificador,marca,tipo):
		# llamada al constructor del padre
		Dispositivo.__init__(self,identificador,marca)
		self.tipo = tipo
	# metodo de la subclase
	def pulsar_tecla(self,tecla):
		print(tecla)

t1 = Teclado("0001", "Logitech", "AZERTY")
print(f"Id: {t1.identificador}, Marca: {t1.marca}, tipo: {t1.tipo}")
t1.conectar()
t1.pulsar_tecla("a")
```	

## Herencia múltiple

Python soporta la herencia múltiple, es decir, heredad métodos y atributos de más de un padre. En caso de heredar atributos o métodos con el mismo nombre, Python dará prioridad al posicionado más a la izquierda en la declaración.

```python
# en caso de conflicto Dispositivo tendrá prioridad sobre Periférico
class Teclado(Dispositivo, Periférico):
	# cuerpo de la clase
```

## Coding time!

### Ejercicio 1
Continuando con el Ejercicio 1 del tema anterior, crea una clase `Vehículo` y otra llamada `Bicicleta`. La clase Vehículo será el padré de `Coche` y `Bicicleta` y contendrá las propiedades y/o métodos comunes de ambos. La bicicleta no tendrá gasolina ni repostará, pero cada 50 kilometros necesitará invocar al método `hinchar_ruedas()` o no podrá continuar.

Puedes utilizar este código para comprobar que todo funciona correctamente:

```python
# Coche:
coche = Coche("1122PKL","Audi")
coche.repostar(20)
coche.avanzar(120)
print(f"Total de kms coche: {coche.kilometros}. Gasolina: {coche.gasolina}")
coche.avanzar(40)
print(f"Total de kms coche: {coche.kilometros}. Gasolina: {coche.gasolina}")

# Bicicleta
bicicleta = Bicicleta("BH")
bicicleta.avanzar(30)
print(f"Total de kms bici: {bicicleta.kilometros}")
bicicleta.avanzar(25)
print(f"Total de kms bici: {bicicleta.kilometros}")
bicicleta.hinchar_ruedas()
bicicleta.avanzar(25)
print(f"Total de kms bici: {bicicleta.kilometros}")
```

Resultado:

```
Total de kms coche: 120. Gasolina: 8.0
Total de kms coche: 160. Gasolina: 4.0

Total de kms bici: 30
Es necesario hinchar para recorrer la cantidad indicada de kms.
Total de kms bici: 30
Total de kms bici: 55
```

### Ejercicio 2
Continuando con el Ejercicio 4 del tema anterior, crea una clase `Poligono` y otra llamada `Cuadrado`. La clase `Poligono` será el padre de `Triangulo` y `Cuadrado`, y contendrá las propiedades y métodos comunes de ambos. Ambos tendrán también otra propiedad llamada `color`.

```python
t1 = Triangulo("rojo",[2, 5, 2])
print(f" Es un {t1.forma()} {t1.color} con {t1.perimetro()}m de perímetro.")

c1 = Cuadrado("azul",[4, 4, 4, 4])
print(f" Cuadrado {c1.color} con {c1.perimetro()}m de perímetro.")
```

Resultado:

```
Es un Triángulo isósceles rojo con 9m de perímetro.
Cuadrado azul con 16m de perímetro.
```

