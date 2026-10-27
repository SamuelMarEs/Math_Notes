#Algoritmos 
El arreglo $A$ guarda referencias a nodos. Cada nodo contiene una clave en su atributo `dato` y puede guardar información adicional.

#### Definición:
Una ***tabla de direccionamiento directo*** es un arreglo con una casilla por cada clave del universo $U=\{ 0,1,\dots,m-1 \}$. La casilla $T[k]$ referencia al elemento con clave $k$, o contiene `None` si no está almacenado.
Es decir, cada elemento de la tabla es accesible mediante una clave específica.
El problema es que es una lista con todos sus elementos, y algunos son `None`, por lo que ocupa mucho espacio en la memoria.
##### Operaciones
```python
def buscar_directo(T, k):
	return T[k]
def insertar_directo(T. nodo):
	T[nodo.dato] = nodo
def 

```

#### Definición:
Una función ***hash*** asigna a cada clave una casilla en la tabla: 
$$
	h:U\to \{ 0,1,\dots,m-1 \}.
$$
La tabla utiliza $h(k)$ para localizar dónde almacenar o buscar la clave $k$.
- **Clave**, identifica el elemento que buscamos.
- **Índice**, indica una casilla del arreglo.
- **Elemento**, contiene la clave y, eventualmente, otros datos.

##### Definición:
Dos claves distintas ***colisionan*** cuando llegan a la misma casilla: 
$$
	k_{1}=k_{2},\quad h(k_{1})=h(k_{2}).
$$
Si $\lvert U \rvert>m$, hay más claves posibles que casillas. Por el principio del palomar (si hay más casas que palomas, al menos dos palomas comparten casa), alguna pareja debe compartir casilla. La colisión no implica igualdad.
Las colisiones se resuelven con *encadenamiento* y *direccionamiento abierto*.

##### Método de división
Para una clave entera $k\geq 0$ y una tabla de tamaño $m>0$, definimos: 
$$
	h(k)=k\quad\mathrm{mod}(m),\quad 0\leq h(k)<m.
$$
Esta función es determinista. Misma clave, mismo índice. 
Si las claves siguen algún patrón, muchas pueden colisionar.
Calcular $h(k)$ tiene costo $\Theta(1)$.

##### Método de multiplicación
Para una clave entera $k\geq 0$, tamaño $m>0$ y una constante fija $0<A<1$: 
$$
	h(k)=\lfloor m(kA\quad\mathrm{mod}(1)) \rfloor ,\quad 0\leq h(k)<m.
$$
$kA\quad\mathrm{mod}(1)=kA-\lfloor kA \rfloor$ es la parte fraccionaria de $kA$.

#### Encadenamiento
Cada casilla referencia la cabeza de una lista con las claves que llegan a ella.
```python
class NodoHash:
	def __init__(self, dato):
		self.dato = dato
		self.anterior = None
		self.siguiente = None
	
Class TablaHash:
	def __init__(self, m)
		self.casillas = [None] * m
```
Las listas son [[TercerSemestre/Datos_Algoritmos/Parcial1/Listas|doblemente enlazadas]]: podremos retirar en tiempo constante un nodo que ya tengamos localizado. La clave de un nodo no cambia mientras esté en la tabla.

Una tabla hash con encadenamiento es como un cajón de ropa. La lista que tenemos es nuestro armario, y la clave numérica de cada índice de la lista es el cajón en el que va cada tipo de ropa. Si ya sabemos en que cajón va la prenda que necesitamos, únicamente abrimos ese cajón, y nos encontramos una pila de ropa (nodos doblemente enlazados).
Entonces vamos revisando la ropa de arriba a abajo hasta encontrar la prenda que queremos. Esta es la función de buscar.
Si queremos añadir una prenda al cajón, lo lógico es ponerla hasta arriba. Esta es la función de insertar.
Si queremos agarrar una prenda en específico, tenemos que levantar la ropa de arriba, para poder sacar la prenda que queremos, y volver a poner la pila de ropa de arriba sobre la pila de ropa de abajo. Esta es la función eliminar.

##### Insertar
```python
def insertar_encadenado(self, nodo):
	m = len(self.casillas)
	j = nodo.dato % m
	nodo.anterior = None
	nodo.siguiente = self.casillas[j]
	if self.casillas[j] is not None:
		self.casillas[j].anterior = nodo
	self.casillas[j] = nodo
```
##### Buscar
```python
def buscar_encadenado(self, k):
	m = len(self.casillas)
	j = k % m
	nodo = self.casillas[j]
	while (nodo is not None and nodo.dato != k):
		nodo = nodo.siguiente
	return nodo
```
El costo de buscar es $\Theta(\ell)$, donde $\ell$ es el número de nodos de la casilla de la lista. El pero caso es donde los $n$ nodos estén en la misma casilla, en cuyo caso tendríamos un costo $\Theta(n)$.
##### Eliminar
```python
def eliminar_encadenado(self, nodo):
	j = nodo.dato % len(self.casillas)
	a = nodo.anterior
	s = nodo.siguiente
	if a is None:
		self.casillas[j] = s
	else:
		a.siguiente = s
	if s is not None:
		s.anterior = a
```
Bajo el supuesto que ya conocemos el nodo que queremos eliminar, el costo es $\Theta(1)$.

#### Direccionamiento abierto
En lugar de utilizar listas doblemente enlazadas como en el encadenamiento, lo que hacemos es buscar un espacio vacío en nuestras casillas.
Para una clave fija $k$, $i$ indica el intento de examinar una casilla: $i=0$ es el primero, $i=1$ es el segundo, etc. 
$$
	h:U\times \{ 0,\dots,m-1 \}\to \{ 0,\dots,m-1 \}.
$$
Al variar $i$, la secuencia $h(k,0),\dots,h(k,m-1)$ debe visitar las $m$ casillas sin repetirlas.
- **Insertar**, avanzar por la secuencia hasta encontrar una casilla disponible.
- **Buscar**, seguir es misma secuencia para localizar la clave.
- Si almacenamos $n$ claves, $0\leq n\leq m$. Cuando $n=m$, la tabla está llena, y ya no vamos a poder añadir nuevos datos a la tabla.

##### Sondeo lineal
```python
def sondeo(self, k, i):
	m = len(self.casillas)
	return ((k % m) + i) % m
```

Que tal que borramos un elemento que iba a ocupar otro elemento que ya pusimos en otro lado. Entonces tendríamos que, al buscar el elemento que aún sigue en la lista, iríamos primero al que acabamos de borrar, que estará vacío, haciéndonos pensar que el elemento no está en la lista. Para esto creamos un nuevo estado:
```python 
BORRADO = object()
```
##### Insertar
```python
def insertar_abierto(self, k):
	m = len(self.casillas)
	for i in range(m):
		q = self.sondeo(k, i)
		if (self.casillas[q] is None or self.casillas[q] is BORRADO):
			self.casillas[q] = k
			return q
	raise OverflowError("Tabla llena")
```
La complejidad es contante en el menor caso, y en el peor de los casos es de orden lineal.
##### Buscar
```python
def buscar_abierto(self, k):
	m = len(self.casillas)
	for i in range(m):
		q = self.sondeo(k, i)
		if self.casillas is None:
			return None
		if (self.casillas[q] is not BORRADO and self.casillas[q] == k):
			return q
	return None
```
La complejidad es contante en el menor caso, y en el peor de los casos es de orden lineal.
##### Eliminar
```python
def eliminar_abierto(self, posicion):
	self.casillas[posicion] = BORRADO
```
Suponiendo que ya conocemos la posición del valor que queremos eliminar, el costo es constante.
##### Sondeo doble
```python
def sondeo(self, k, i):
	m = len(self.casillas)
	h1 = k % m
	h2 = 1 + (k % (m - 2))
	return (h1 + i*h2) % m
```
Esto para $m$ primo y $m\geq 3$.
##### Cambiar el tamaño
Si aumentamos el tamaño de la tabla, debemos volver a calcular dónde va cada clave.
1. Crear una tabla vacía con el nuevo tamaño.
2. Recorrer los elementos que siguen almacenados.
3. Reinsertarlos usando la nueva función de indexación y su política de colisiones.