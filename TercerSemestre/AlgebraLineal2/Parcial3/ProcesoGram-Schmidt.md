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
