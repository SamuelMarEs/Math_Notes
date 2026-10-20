#Algoritmos 
Para un [[ArbolBinarioDeBusqueda|árbol binario]] con $n\geq 1$ nodos y altura $h$: 
$$
	\lceil \log_{2}(n+1) \rceil -1\leq h\leq n-1.
$$
Buscar, insertar y eliminar siguen caminos cuya longitud depende de la altura: 
$$
	T(n)\in O(h+1).
$$
Insertar valores en orden puede producir una cadena: $h=n-1$.
La propiedad de búsqueda ayuda a ordenar los datos, pero por sí sola no limita la altura. Los árboles balanceados conservan una condición adicional al insertar y eliminar.

#### Definición: Árbol AVL
Un árbol AVL es un árbol binario de búsqueda en el que, para cada nodo, las alturas de sus subárboles izquierdo y derecho difieren a lo más en 1.

En base a esta definición definimos el **factor de equilibrio** de un nodo x como 
$$
	\mathrm{FE}(x)=H(x.\mathrm{izquierdo})-H(x.\mathrm{derecho}),\quad \mathrm{FE}(x)\in \{ -1,0,1 \}.
$$
Una hoja tiene altura 0, y la altura de un árbol vacío es $H(\emptyset)=-1$.

##### Representación:
```python
class NodoAVL:
	def __init__(self, dato):
		self.dato = dato
		self.izquierdo = None
		self.derecho = None
		self.padre = None
		self.altura = 0
		
class ArbolAVL:
	def __init__(self):
		self.raiz = None
```
###### Altura y equilibrio
```python
def actualizar_altura(slef):
	izq = (-1 if self.izquierdo is None else self.izquierdo.altura)
	der = (-1 if self.derecho is None else self.derecho.altura)
	self.altura = 1 + max(izq, der)
	
def factor_equilibrio(self):
	izq = (-1 if self.izquierdo is None else self.izquierdo.altura)
	der = (-1 if self.derecho is None else self.derecho.altura)
	return izq - der
```
Ambas operaciones tienen complejidad $\Theta(1)$.

Decimos que el árbol esta desequilibrado si el factor de equilibrio es absolutamente mayor a 1 (es decir, no es -1, 0 o 1).
En caso de que haya un árbol desequilibrado, lo que queremos hacer es equilibrarlo, generalmente mediante una rotación.
```python
def rotar_derecha(self, T):
	nueva = self.izquierdo
	nieto = nueva.derecho
	self.izquierdo = nieto
	if nieto is not None:
		nieto.padre = self
	transplantar(T, self, nueva)
	nueva.derecho = self
	self.padre = nueva
	self.actualizar_altura()
	nueva.actualizar_altura()
	return nueva
```
De forma análoga podemos definir la rotación a la izquierda.
Cuando hacemos ambas, estamos utilizando una rotación doble.

##### Inserción y eliminación
Para insertar un nuevo nodo en un árbol de búsqueda balanceado, tenemos que realizar los siguientes tres pasos: Descender, Conectar, Re equilibrar.
Por otro lado, para eliminar un nodo en específico, también son tres pasos: Eliminar, Revisar alturas, Re equilibrar.
Buscar, insertar y eliminar, tienen todas un costo de $O(\log_{2}(n+1))$.

