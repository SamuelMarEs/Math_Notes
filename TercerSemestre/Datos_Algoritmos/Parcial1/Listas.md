Ya usamos `list` como una secuencia con acceso por índice. Ahora, estudiaremos otra forma de representar esa secuencia y cómo cambia el costo de sus operaciones.
- El [[TDA]] lista describe qué podemos hacer con la secuencia.
- La **representación** determina cómo se almacenan y conectan sus elementos.

`list`: arreglo dinámico de referencias. En Python, las referencias ocupan posiciones contiguas. Es decir, que lo elementos están uno al lado del otro.
***Lista enlazada***: nodos y referencias. El orden lo determinan los enlaces, no la cercanía física de los nodos. Se usan "flechas" para indicar cual es el siguiente valor, sin necesidad de que estén uno al lado del otro.
![[Excalidraw/Listas|Listas]]

#### Definición:
Una ***lista*** es una secuencia finita de elementos en la que importa la posición. Permite valores repetidos y no exige que estén ordenados por valor. Sus operaciones se describen sin fijar una representación en memoria.

Algunas operaciones son consultar un elemento, recorrer la secuencia, insertar, y remover.

#### Definición: 
Una ***lista simplemente enlazada*** es una estructura lineal formada por nodos. Cada nodo almacena un dato y una referencia al siguiente nodo de la secuencia.
Tiene una estructura de la forma 
$$
	\text{dato|siguiente}
$$
![[ListaEnlazada]]
#### Nodo en Python
```Python
class Nodo:
	def __init__(self, dato, siguiente=None):
		self.dato = dato
		self.siguiente = siguiente
```
- Dato: el valor almacenado.
- Siguiente: una referencia a otro Nodo, o `None`.
Podemos construir una lista de la siguiente forma:
```Python
n1 = Nodo(10)
n2 = Nodo(20)
n3 = Nodo(30)

n1.siguiente = n2
n2.siguiente = n3
head = n1
```
Para crear una lista vacía, basta poner `head = None`.

Para movernos en la lista, podemos hacerlo de la forma
```Python
actual = head
actual = actual.siguiente
```
que cambia el nodo al que se refiere la variable `actual`.
También podemos cambiar un enlace 
```Python
actual = head
actual.siguiente = n3
```
En este caso estamos cambiando el elemento siguiente a actual.

##### Recorrido
```Python
def recorrer(head):
	actual = head
	while actual is not None:
		print(actual.dato)
		actual = actual.siguiente
```

##### Obtener por posición
```Python
def obtener(head, i):
	if i < 0:
		raise IndexError("indice negativo")
	actual = head
	posicion = 0
	while actual is not None and posicion < i:
		actual = actual.siguiente
		posicion += 1
	if actual is None:
		raise IndexError("indice fuera de rango")
	return actual.dato
```
Para $0\leq i<n$, tenemos que $T(i)\in\Theta(i+1)$, que en el peor caso es $\Theta(n)$.

##### Buscar un valor
```Python
def buscar(head, x):
	actual = head
	while actual is not None and actual.dato != x:
		actual = actual.siguiente
	return actual
```
Devuelve el primer nodo cuyo dato coincide con $x$, o `None` si no existe. La complejidad de este algoritmo es nuevamente lineal: $T_{\text{buscar}}(n)\in \Theta(n)$ en el peor caso.

##### Insertar al inicio
```Python
def insertar_inicio(head, x):
	nuevo = Nodo(x)
	nuevo.siguiente = head
	return nuevo
	
head = insertar_inicio(head, 10)
```
Esta operación tiene un orden de complejidad constante $T(n)\in \Theta(1)$.

##### Eliminar al inicio
```Python
def eliminar_inicio(head):
	if head is None:
		raise ValueError("lista vacia")
	eliminado = head.dato
	head = head.siguiente
	return head, eliminado
	
head, eliminado = eliminar_inicio(head)
```
Esta operación tiene un orden de complejidad constante $T(n)\in \Theta(1)$.

##### Insertar después
Ya tenemos la referencia al nodo 10 y queremos insertar 20 después de él.
```Python
def insertar_despues(nodo, x):
	if nodo is None:
		raise ValueError("nodo no puede ser None")
	nuevo = Nodo(x)
	nuevo.siguiente = nodo.siguiente
	nodo.siguiente = nuevo
```
El nuevo nodo conserva el enlace al resto de la cadena.
El nodo anterior se enlaza al nuevo.
Insertar un nodo requiere un número finito de operaciones que no depende del tamaño de la lista. Es decir que tiene complejidad $T(n)\in \Theta(1)$.

##### Eliminar después
Ahora, en vez de insertar 20 después del nodo de 10, queremos eliminar el nodo que le sigue.
```Python
def eliminar_despues(nodo):
	if nodo is None or nodo.siguiente is None:
		raise ValueError("no hay nodo que eliminar")
	eliminado = nodo.siguiente
	nodo.siguiente = eliminado.siguiente
	return eliminado.dato
```
Desenlazar el nodo que seguía no implica destruirlo: otra referencia podría conservarlo. Nuevamente la complejidad es constante.

#### Tail
Así como tenemos la referencia `head` para indicar donde inicia la lista, podemos crear una referencia nueva que se llame `tail` para llegar de forma inmediata al último elemento de la lista.
De la misma forma podríamos crear nuevas referencias que nos ayuden a disminuir la complejidad de buscar un elemento en específico.

#### Lista como objeto
```Python
class ListaEnlazada:
	def __init__(self):
		self._head = None
		
	def esta_vacia(self):
		return self._head is None
	
	def insertar_inicio(self, x):
		self._head = Nodo(x, self._head)
```

#### Doble enlace
Podemos definir una lista doblemente enlazada. Cada nodo almacena un dato y dos referencias: una al nodo anterior y otra al siguiente.
Ahora tenemos una estructura de forma 
$$
	\text{anterior | dato | siguiente}
$$
- Podemos avanzar y retroceder
- Desde un nodo conocido también accedemos a su predecesor.
- A cambio: una referencia adicional por nodo y más enlaces por actualizar.

#### Lista circular
En una lista circular no vacía, el último nodo vuelve a enlazar al primero.
La circularidad y el doble enlace son independientes. Podemos tener una lista circular doblemente enlazada.

#### Problema de Josefo
Contamos con $k$ participantes por ronda, incluyendo al inicial, y eliminamos al que recibe el número $k$. Aquí hay cinco participantes y $k=2$: se elimina a cada segundo participante hasta que queda uno.
- Comenzamos en el participante 1: cuenta como uno.
- El siguiente cuenta como dos y lo mata el 1.
- Reiniciamos la cuenta en el siguiente al eliminado.
Este problema se resuelve utilizando una lista enlazada circular.