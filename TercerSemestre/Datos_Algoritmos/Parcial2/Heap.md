#Algoritmos 
#### Definición:
Une ***heap binario*** es una estructura representada mediante un arreglo que podemos interpretar como un árbol binario completo (todos los niveles menos el último están completos) y cuyos valores satisfacen la propiedad de *max-heap* o de *min-heap*. 
Estos árboles no tienen porque satisfacer la propiedad de búsqueda de los [[ArbolBinarioDeBusqueda|árboles binarios de búsqueda]].
###### max-heap
Para cada hijo $i$: $A[\mathrm{Padre}(i)]\geq A[i]$
Los hijos no pueden ser más grandes que los padres.
###### min-heap
Para cada hijo $i$: $A[\mathrm{Padre}(i)]\leq A[i]$
Los padres no pueden ser más grandes que los hijos.

La raíz ocupa el índice $0$. 
El recorrido por niveles determina la posición de cada elemento en el arreglo. 
Las relaciones padre-hijo se calculan mediante índices; no almacenamos referencias a los hijos ni al padre.

##### Índices
```python
def padre(i):
	return (i-1) // 2
def izquierdo(i):
	return 2 * i + 1
def derecho(i):
	return 2 * i +2
```
Usando estas funciones, calcular un índice tiene un costo $\Theta(1)$.

##### Tamaño y capacidad
$n=$ tamaño, es el número de elementos que pertenecen al heap, $m=len(\mathrm{datos})$ es la capacidad del arreglo. $0\leq n\leq m$.
##### Altura y tamaño
Un heap de altura $h$ llena los niveles $1,\dots,h$ y tiene al menos un nodo en el nivel $h+1$. Si sumamos por niveles 
$$
	n\geq \sum_{i=1}^{h}2^{i-1}+1= \frac{2^{h}-1}{2-1}+1=2^{h}.
$$
Tomando logaritmos, tenemos que $h\leq \log_{2}n<\log_{2}(n+1)$, y como $h$ tiene que ser entero, tenemos que $h\leq \lceil \log_{2}(n+1) \rceil -1$.

#### Representación en Python
```python
class NodoHeap:
	def __init__(self, dato):
		self.dato = dato
		self.indice = None

class HeapMaximo:
	def __init__(self, datos, tamano):
		self.datos = datos
		self.tamano = tamano
		for i in range(tamano):
			datos[i].indice = i
```
##### Intercambiar
```python
def intercambiar(self, i, j):
	A = self.datos
	A[i], A[j] = A[j], A[i]
	A[i].indice = i
	A[j].indice = j
```
Costo $\Theta(1)$.

#### Hundir y Flotar
Supongamos que los subárboles de los hijos de $i$ ya son max-heaps, y solo la clave de $i$ es menor que la de alguno de sus hijos. Entonces, seguimos el siguiente procedimiento:
1. Elegimos el mayor entre el elemento y sus hijos existentes.
2. Si gana un hijo, intercambiamos y continuamos en ese subárbol.
3. Una llamada en la raíz no construye por si sola un heap a partir de cualquier arreglo.
```python
def hundir(self, i):
	A, n = self.datos, self.tamaño
	l, r = izquierdo(i), derecho(i)
	mayor = i
	if (l < n and A[l.dato] > datos[i].dato):
		mayor = l
	if (r < n and A[r].dato > A[mayor].dato):
		mayor = r
	if mayor != i:
		self.intercambiar(i, mayor)
		self.hundir(mayor)
```
La función es análoga para un min-heap, solo que ahora realizamos el cambio solo si algún hijo es menor al nodo que tenemos.
```python
def flotar(self, i):
	A = self.datos
	while (i > 0 and A[padre(i)].dato < A[i].dato):
		p = padre(i)
		self.intercambiar(i, p)
		i = p
```
En el peor de los casos, esta función tiene un costo $O(\log_{2}(n+1))$. Nuevamente, si trabajáramos con un min-heap, las desigualdades irían al revés.

#### Construir un heap
Las hojas ya son max-heaps de un elemento. Aplicamos hundir a los nodos internos desde el último hasta la raíz.
```python
def construir(self):
	n = self.tamano
	for i in range(n // 2 - 1, -1, -1):
		self.hundir(i)
```
Construir tiene un costo de orden lineal.

