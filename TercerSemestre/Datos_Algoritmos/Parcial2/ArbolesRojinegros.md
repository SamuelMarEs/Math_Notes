#Algoritmos
#### Definición:
Un árbol rojinegro es un [[ArbolBinarioDeBusqueda]] con un atributo adicional por nodo: su color, rojo o negro. Los colores satisfacen las siguientes propiedades:
- Cada nodo es rojo o negro.
- La raíz es negra.
- Cada posición vacía None se considera negra.
- Si un nodo es rojo, sus dos hijos son negros.
- Desde cada nodo, todos los caminos descendentes hasta una posición vacía contienen la misma cantidad de negros.

###### Altura negra
$\mathrm{bh}(x)$ cuenta los negros de un camino desde $x$ hasta una posición vacía. Escluye a $x$ e incluye el extremo None, considerado negro. Por convención se define $\mathrm{bh}(None)=0$.
##### Representación:
```python
ROJO = "rojo"
NEGRO = "negro"

class NodoNN:
	def __init__(self, dato):
		self.dato = dato
		self.izquierdo = None
		self.derecho = None
		self.padre = None
		self.color = ROJO
		
class ArbolRN:
	def __init__(self):
		self.raiz = None

def color(nodo):
	if nodo is None:
		return Negro
	return nodo.color
```

##### Resultado
El subárbol de raíz $x$ contiene al menos $2^{\mathrm{bh}(x)}-1$ nodos con datos (no vacíos).
###### Demostración
Utilizaremos la altura habitual: $H(None)=-1$ y una hoja tiene altura 0.
La demostración será por inducción sobre $H(x)$.
Caso base: Si $x=None$, su altura es $-1$, y no hay nodos con datos: $0=2^{0}-1$.
Paso inductivo: Sea $b=\mathrm{bh}(x)$. Cada hijo tiene altura menor y altura negra $b-1$ si es negro, o $b$ si es rojo. Por hipótesis inductiva, cada subárbol hijo tiene al menos $2^{b-1}-1$ nodos con datos. Entonces 
$$
	N(x)=1+N(x.izquierdo)+N(x.derecho)\geq 1+(2^{b-1}-1)+(2^{b-1}-1)=2^{b}-1.
$$

