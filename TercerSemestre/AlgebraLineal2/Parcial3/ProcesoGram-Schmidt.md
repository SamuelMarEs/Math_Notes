#AlgebraLineal
Este proceso nos dice como construir un conjunto ortogonal a partir de un conjunto linealmente independiente de vectores, de forma que ambos conjuntos generen el mismo subespacio. 
Supongamos que tenemos un conjunto $\{ w_{1},w_{2} \}$ linealmente independiente en un espacio de [[ProductoInterno|producto interno]], de modo que es una base de algún subespacio de dimensión 2. Si queremos construir una base ortogonal a partir de $\{ w_{1},w_{2} \}$, podemos hacerlo con $\{ v_{1},v_{2} \}$ donde $v_{1}=w_{1}$ y $v_{2}=w_{2}-cw_{1}$, donde elegimos $c$ de forma que $v_{2}$ sea ortogonal a $v_{1}$, como se muestra en la siguiente figura:
DIBUJO EXCALIDRAW

Para encontrar $c$, basta resolver la ecuación: 
$$
	0=\langle v_{2},w_{1}\rangle=\langle w_{2}-cw_{1},w_{1}\rangle=\langle w_{2},w_{1}\rangle-c\langle w_{1}, w_{1}\rangle,
$$
de modo que llegamos a que 
$$
	c=\frac{\langle w_{2},w_{1}\rangle}{\lvert \lvert w_{1} \rvert  \rvert ^{2}}.
$$
Por lo tanto 
$$
	v_{2}=w_{2}- \frac{\langle w_{2},w_{1}\rangle}{\lvert \lvert w_{1} \rvert  \rvert ^{2}}w_{1}.
$$
El siguiente teorema generaliza el resultado para cualquier conjunto linealmente independiente.

#### Teorema 6.4
Sea $V$ un espacio de producto interno y $S=\{ w_{1},w_{2},\dots,w_{n} \}$ un conjunto linealmente independiente de $V$. Definamos $S'=\{ v_{1},\dots,v_{n} \}$, donde $v_{1}=w_{1}$ y 
$$
	v_{k}=w_{k}-\sum_{j=1}^{k-1} \frac{\langle w_{k}, v_{j}\rangle}{\lvert \lvert v_{j} \rvert  \rvert ^{2}}v_{j}\quad \text{para }2\leq k\leq n.
$$
Entonces $S'$ es un conjunto ortogonal de vectores no cero tal que $\mathrm{span}(S)=\mathrm{span}(S')$.
##### Demostración:
La demostración es por inducción sobre $n$, el número de vectores de $S$. Si $n=1$, entonces el teorema es trivial tomando $S'=S$.
Supongamos que el conjunto $S´_{k-1}=\{ v_{1},\dots,v_{k-1} \}$ cumple las condiciones del teorema. Vamos a demostrar que el conjunto $S_{k}'=\{ v_{1},\dots,v_{k} \}$ también cumple las propiedades deseadas, donde $v_{k}$ se obtiene a partir de $S_{k-1}'$ de la forma que indica el teorema.
Si $v_{k}=0$, entonces tenemos que $w_{k}\in \mathrm{Span}(S_{k-1}´)=\mathrm{Span}(S_{k-1})$ lo que contradice que $S_{k-1}$ fuera linealmente independiente. Para $1\leq i\leq k-1$, y $v_{k}$ definido como en el teorema, se sigue que 
$$
	\langle v_{k},v_{i}\rangle=\langle w_{k},v_{i}\rangle-\sum_{j=1}^{k-1} \frac{\langle w_{k}v_{j}\rangle}{\lvert \lvert v_{j} \rvert  \rvert ^{2}} \langle v_{j}, v_{i}\rangle=\langle w_{k}v_{i}\rangle- \frac{\langle w_{k}, v_{i}\rangle}{\lvert \lvert v_{i} \rvert  \rvert ^{2}}\lvert \lvert v_{i} \rvert  \rvert ^{2}=0,
$$
dado que por la hipótesis de inducción, los vectores de $S_{k-1}'$ son ortogonales. Entonces tenemos que $S_{k}'$ es un conjunto de vectores no cero ortogonales.
Por la forma en la que lo construimos, tenemos que $\mathrm{span}(S_{k}´)\subset\mathrm{span}(S_{k})$, pero por los corolarios del [[BasesOrtonormales|teorema 6.3]] tenemos que $S_{k}'$ es linealmente independiente, y por lo tanto necesariamente $\mathrm{span}(S_{k}´)=\mathrm{span}(S_{k}).\quad\square$

El siguiente teorema nos da una forma de representar un vector como combinación lineal de vectores de una base ortonormal.
#### Teorema 6.5
Sea $V$ un espacio de dimensión finita no cero con producto interno. Entonces $V$ tiene una base ortonormal $\beta$. Más aún, si $\beta=\{ v_{1},\dots,v_{n} \}$ y $x\in V$, entonces 
$$
	x=\sum_{i=1}^{n}\langle x,v_{i}\rangle v_{i}.
$$
##### Demostración:
Si partimos de una base cualquiera $\beta'=\{ w_{1},\dots,w_{n} \}$, sabemos por el teorema 6.4 que podemos llevarla a una base ortogonal $\beta_{1}=\{ z_{1},\dots,z_{n} \}$, y si normalizamos los vectores llegamos a nuestra base $\beta=\{ v_{1},\dots,v_{n} \}=\{ z_{1} / \lvert \lvert z_{1} \rvert \rvert,\dots, z_{n} / \lvert \lvert z_{n} \rvert \rvert \}$. Entonces, por el teorema 6.3 tenemos que 
$$
	x=\sum_{i=1}^{n} \frac{\langle x, v_{i}\rangle}{\lvert \lvert v_{i} \rvert  \rvert^{2} }v_{i}=\sum_{i=1}^{n} \langle x, v_{i}\rangle v_{i}.\quad\square
$$

##### Corolario:
Si $\beta=\{ v_{1},\dots,v_{n} \}$ es una base ortonormal de $V$, y $T$ un operador lineal sobre $V$ con $A=[T]_{\beta}$. Entonces para cualesquiera $i$ y $j$, $A_{ij}=\langle T(v_{j}), v_{i}\rangle$.
###### Demostración:
Por el teorema 6.5, tenemos que 
$$
	T(v_{j})=\sum_{i=1}^{n}\langle T(v_{j}), v_{i}\rangle v_{i},
$$
y por definición de la matriz asociada a la transformación esto implica que $A_{ij}=\langle T(v_{j}), v_{i}\rangle.\quad\square$
