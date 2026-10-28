#Algoritmos 
#### Definición
Una cola de prioridad mantiene elementos con una clave asociada. En una cola de prioridad de máximos se consulta o retira un elemento cuya clave es máxima.
Un [[Heap|max-heap]] implementa este comportamiento. Una cola de mínimos retira el elemento cuya clave es mínima. Este segundo tipo de cola lo implementa un *min-heap*.

#### Operaciones

#### Implementación:
```python
def maximo(self):
	if self.tamano == 0:
		raise IndexError("heap vacio")
	return self.datos[0]
	
def extraer_maximo(self):
	retirado = self.maximo()
	u = self.tamano - 1
	if u > 0:
		self.datos[0] = self.datos[u]
		self.datos[0].indice = 0
	self.datos[u] = None
	self.tamano = u
	retirado.indice = None
	if u > 0:
		self.hundir(0)
	return retirado
	
def aumentar_clave(self, nodo, k):
	if k < nodo.dato:
		raise ValueError("clave menor")
	nodo.dato = k
	self.flotar(nodo.indice)
	
def insertar(self, elemento):
	if self.tamaño == len(self.datos):
		raise OverflowError("heap lleno")
	i = self.tamano
	self.datos[i]=elemento
	elemento.indice = i
	self.tamano += 1
	self.flotar(i)
```
Costos en orden: $\Theta(1), O(\log_{2}(n+1)), O(\log_{2}(n+1)), O(\log_{2}(n+1))$.