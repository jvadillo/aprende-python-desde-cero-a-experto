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
    		print("¡Conectado!)
    
    # la clase base se indica entre paréntesis
    class Teclado(Dispositivo):
    	def __init__(self,identificador,marca,tipo):
	    	# llamada al constructor del padre
    		Dispositivo.__init__(self,identificador,marca)
    		self.marca = marca
    	# metodo de la subclase
    	def pulsar_tecla(self,tecla):
    		print(tecla)

    t1 = Teclado("0001", "Logitech", "AZERTY")
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
