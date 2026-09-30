#Algoritmos 
Mientras que una [[Pilas|pila]] sigue el principio **LIFO**, una cola, sigue el principio **FIFO**, First In, First Out.
Toda cola esta compuesta por un frente y un final.
Una cola es también un [[TDA]], al igual que las pilas. Recordemos que el tipo de dato sólo indica las operaciones que se pueden realizar, no la forma en que se almacenan los elementos.

#### Definición
Una cola es una secuencia finita de elementos en la que se insertan elementos por el extremo llamado **final**, y se remueven o consultan por el extremo contrario llamado **frente**. Sigue el principio **FIFO**, el primer elemento agregado es el primero que se retira.

| Operación    | Efecto                                         | Devuelve           |
| ------------ | ---------------------------------------------- | ------------------ |
| encolar(x)   | Agrega x al final                              | None               |
| desencolar() | Retira el elemento del frente                  | Dato retirado      |
| frente()     | Consulta el elemento del frente, sin retirarlo | Dato consultado    |
| esta_vacia() | Consulta si no hay elementos                   | Booleano           |
| longitud()   | Consulta cuántos elementos hay                 | Entero no negativo |
No se ofrece acceso por índice ni nada que hacer con los elementos del medio.

#### Implementación con list
```python
class ColaLista:
	def __init__(self, lista_datos = []):
		self._datos = lista_datos
	
	def encolar(self, x):
		self._datos.append(x)
		
	def desencolar(self):
		if self.esta_vacia():
			raise IndexError("cola vacía")
		return self._datos.pop(0)
	
	def frente(self):
		if self.esta_vacia():
			raise IndexError("cola vacía")
		return self._datos[0]
		
	def esta_vacia(self):
		return len(self._datos) == 0
```

Al utilizar la función .pop(0) para retirar el primer elemento de una `list`, tiene una complejidad lineal $\Theta(n)$, pues necesita recorrer $n-1$ elementos. Por otro lado .append(x) tiene una complejidad constante $\Theta(1)$.

#### deque
Existe una libreria incorporada en python que permite agregar po la derecha y retirar por la izquierda sin desplazar todos los elementos.
```python
from collections import deque
class ColaDeque:
	def __init__(self):
		self._datos = deque()
	
	def encolar(self, x):
		self._datos.append(x)
	
	def desencolar(self):
		return self._datos.popleft()
		
		
```
La función .popleft() ya produce un `IndexError` en caso de que la cola esté vacía.
Nuevamente, esta_vacia() y longitud() se obtienen mediante la función len().

#### Cola enlazada
Reutilizamos los [[TercerSemestre/Datos_Algoritmos/Parcial1/Listas|nodos]] para guardar regerencias a los dos extremos.
```python
class ColaEnlazada:
	def __init__(self):
		self._head = None
		self._tail = None
		self._n = 0
	
	def esta_vacia(self):
		return self._head is None
		
	def longitud(self):
		return self._n
		
	def encolar(self, x):
		nuevo = Nodo(x, None)
		if self._tail is None:
			self._head = nuevo
		else
			self._tail.siguiente = nuevo
		self._tail = nuevo
		self._n += 1
		
	def desencolar(self):
		if self._head is None
			raise IndexError("cola vacía")
		dato = self._head.dato
		self._head = self._head.siguiente
		if self._head is None:
			self._tail = None
		self._n -= 1
		return dato
		
	def frente(self):
		if self._head is None:
			raise IndexError("cola vacía")
		return self._head.dato
```

###### Ejemplo: media móvil
Dada una sucesión 
$$
	x_{1},x_{2},\dots,x_{n}
$$
queremos calcular, para cada posición, el promedio de los últimos $k$ valores: 
$$
	M_{i}=\frac{x_{i-k+1}+\dots+x_{i}}{k},\quad i\geq k.
$$
```pseudocodigo
Inicializar una cola vacía Q y una suma s <- 0.
Para i=1,2,...,n:
	Encolar x_i en Q
	s <- s + x_i
	Si longitud(Q) > k:
		v <- desencolar(Q)
		s <- s - v
	Si longitud(Q) = k:
		Mostrar s/k
```