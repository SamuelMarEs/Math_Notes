#Algoritmos 
Recordemos que una lista organiza una secuencia. Un árbol organiza una jerarquía. Al trabajar con recursion, ya utilizamos raíces, ramas y hojas. Ahora, vamos a extender los mismos conceptos a vínculos con datos.

#### Definición:
Un árbol es una estructura jerárquica finita de nodos conectados mediante enlaces **padre-hijo**. Tienen un nodo llamado **raíz** que no tiene un padre. Cada nodo tiene exactamente un padre y se alcanza desde la raíz mediante un único camino.
![[Excalidraw/Arboles|Arboles]]

Un árbol tiene muchos elementos:
- Raíz.
- Padre.
- Hijos.
- Hermanos.
- Descendientes.
- Ancestros.
- Hojas.
- Nodo interno (que no son la raíz ni las hojas).
- Grado de un nodo, que es el número de hijos de un nodo.
- Rama, el enlace directo entre un padre y uno de sus hijos.
- Grado del árbol, que es el mayor grado entre sus nodos.
- Camino, secuencia de nodos unidos por enlaces padre-hijo. La longitud de un camino cuenta los enlaces, no los nodos.
- Nivel de un nodo, el número de enlaces desde la raíz, más 1 (la raíz ocupa el nivel 1).
- Altura de un nodo, la máxima longitud del camino desde el nodo hasta una hoja.
- Altura del árbol, es la altura de su raíz, el camino más largo desde la raíz a cualquier hoja.
- Profundidad, número de enlaces desde la raíz hasta el nodo.
- Subárbol, un nodo y todos sus descendientes (la raíz del subárbol es el nodo donde comienza).
- Bosque, una colección de árboles disjuntos. Al eliminar la raíz, quedan tantos árboles como el grado de la raíz.

#### Árbol binario
Un árbol binario es un árbol en el que cada nodo tiene como máximo dos hijos, distinguidos como hijo izquierdo e hijo derecho. Cualquiera de ellos puede estar ausente.
Cada subárbol de un árbol binario, es también un árbol binario.

##### Formas de árboles binarios
- Estricto: cada nodo tiene 0 o 2 hijos.
- Perfecto: todos los niveles están llenos.
- Completo: todos los niveles anteriores al último están llenos; el último se ocupa de izquierda a derecha.
- Degenerado: los nodos forman una cadena.

##### Capacidad de un árbol binario
En el nivel $i\geq 1$ hay como máximo $2^{i-1}$ nodos. Un árbol binario no vacío de altura $h$ tiene como máximo 
$$
n\leq 2^{h+1}-1.
$$
Sea $N_{i}$ el número de nodos en el nivel $i$, comenzando en 1. 
Base: $N_{1}=1=2^{0}$ porque solo hay una raíz.
Paso inductivo: si $N_{i}\leq 2^{i-1}$, cada nodo tiene a lo sumo dos hijos: 
$$
	N_{i+1}\leq 2N_{i}\leq 2 \cdot 2^{i-1}=2^{i}.
$$
Un árbol de altura $h$ tiene niveles desde 1 hasta $h+1$. Sumando tenemos que: 
$$
	n=\sum_{i=1}^{h+1}N_{i}\leq \sum_{i=1}^{h+1} 2^{i-1},
$$
que es lo mismo que 
$$
	 \sum_{i=1}^{h+1} 2^{i-1}=\frac{2^{h+1}-1}{2-1}=2^{h+1}-1.
$$
Es decir que llegamos a que $$n\leq 2^{h+1}-1.\quad\square$$
#### Operaciones

| Operación          | Comportamiento                       | Resultado         |
| ------------------ | ------------------------------------ | ----------------- |
| Consultar          | Obtener raíz, hijos o dato           | Referencia o dato |
| Recorrer           | Procesar todos los nodos en un orden | Lista de datos    |
| contar_nodos(raiz) | Contar                               |                   |

#### Recorridos
Recorrer un árbol consiste en visitar cada nodo una vez, siguiendo un orden definido. Visitar puede significar registrar el dato, consultarlo o realizar un cálculo.
**En profundidad:** se explora un subárbol antes de continuar con otro. 

Procedimiento Preorden: raíz, subárbol izquierdo, subárbol derecho.
```pseudocodigo
Preorden(nodo):
	Si nodo es vacio:
		Retornar
	Visitar(nodo)
	Preorden(nodo.izuierdo)
	Preorden(nodo.derecho)
```

Procedimiento Inorden: subárbol izquierdo, raíz, subárbol derecho.
```pseudocodigo
Inorden(nodo):
	Si nodo es vacio:
		Retornar
	Inorden(nodo.izquierdo)
	Visitar(nodo)
	Inorden(nodo.derecho)
```

Procedimiento Postorden: subárbol izquierdo, subárbol derecho, raíz.
```pseudocodigo
Postorden(nodo):
	Si nodo es vacio:
		Retornar
	Postorden(nodo.izquierdo)
	Postorden(nodo.derecho)
	Visitar(nodo)
```

Como elegir un recorrido: 

| Recorrido | Momento                                   | Ejemplos de uso                                                                            |
| --------- | ----------------------------------------- | ------------------------------------------------------------------------------------------ |
| Preorden  | Antes de sus descendientes.               | Mostrar una jerarquía desde sus superiores; generar notación prefija.                      |
| Inorden   | Entre los subárboles izquierdo y derecho. | Obtener valores ordenados en un árbol binario de búsqueda; notación infija con paréntesis. |
| Postorden | Después de sus descendientes.             | Calcular altura, combinar conteos de subárboles y evaluar expresiones                      |
Con una visita de costo constante, los tres recorridos completos cuestan $\Theta(n)$. Cambia el orden de procesamiento, no la cantidad de nodos visitados.