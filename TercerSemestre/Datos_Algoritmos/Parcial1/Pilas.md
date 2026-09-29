#Algoritmos 
Una pila restringe las operaciones de una lista a un solo extremo: la **cima**. Este comportamiento se llama **LIFO** (Last In, First Out).
- El [[TDA]] pila establece el comportamiento LIFO.
- la representación puede usar un arreglo dinámico o nodos enlazados.
- Una `list` de Python no es una pila por sí misma: podemos usarla como pila mediante una interfaz restringida.

#### Definición
Una pila es una secuencia finita de elemenos en la que la inserción y la remoción se realizan en un extremo llamado cima, y solo puede consultarse el elemento situado en ese extremo. El último elemento ingresado es el primero que se retira.

| Operación    | Efecto                                 | Devuelve           |
| ------------ | -------------------------------------- | ------------------ |
| apilar(x)    | AAgrega x en la cima                   | None               |
| desapilar()  | Retira el elemento de la cima          | Dato retirado      |
| cima()       | Consulta la cima sin modificar la pila | Dato consultado    |
| esta_vacia() | Consulta si no hay elementos           | True o False       |
| longitud()   | Consulta cuántos elementos hay         | Entero no negativo |
#### Pila usando list
```python
class Pila:
	def __init__(self, lista_datos=[]):
		self._datos = lista_datos
	
	def esta_vacia(self):
		return len(self._datos) == 0
	
	def longitud(self):
		return len(self._datos)
		
	def apilar(self, x):
		self._datos.append(x)
		
	def cima(self):
		if self.esta_vacia():
			raise IndexError("pila vacia")
		return self._datos[-1]
		
	def desapilar(self):
		if self.esta_vacia():
			raise IndexError("pila vacia")
		return self._datos.pop()
		
```

#### Pila enlazada
```python
class PilaEnlazada:
	def __init__(self):
		self._head = None
		self._n = 0
	
	def esta_vacia(self):
		return self._head is None
	
	def longitud(self):
		return self._n
	
	def apilar(self, x):
		
	
	def cima(self):
		
	
	def desapilar(self):
		if self.esta_vacia():
			raise IndexError("pila vacia")
		
```

#### Notación posfija
Cada operador aparece desués de sus operandos. El orden de los símbolos determina la agrupación sis utilizar paréntesis.
**Infija:** (3 + 4) * 2
**Posjifa:** 3 4 + 2 *

Usaremos una lista de **tokens**: cada elemento es un entero o un símbolo de operador.
tokens = $[3, 4, \text{"+"}, 2, \text{"*"}]$.

**Precondición:** expresión bien formada, con enteros y operadores binarios $+, -, *$.
```pseudocodigo
Evaluar(tokens)
	P = pila vacía
	Para cada t en tokens:
		Si t es un entero:
			P.apilar(t)
		Si no
			derecho = P.desapilar
			izquierdo = P.desapilar
			valor = apilar(t, izquierdo, derecho)
	Devolver P.desapilar
```

Una pila es conveniente cuando necesitamos:
- Recuperar lo más reciente: el último elemento agregado sale primero.
- Manejar anidamiento: la apertura más reciente se cierra antes.
- Conservar trabajo pendiente: una llamada espera el resultado de otra.
