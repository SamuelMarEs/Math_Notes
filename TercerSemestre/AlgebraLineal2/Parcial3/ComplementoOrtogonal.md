#AlgebraLineal 
#### Definición:
Sea $S$ un subconjunto de $V$ un espacio vectorial con [[ProductoInterno|producto interno]]. Definimos 
$$
	S^{\perp}:=\{ x\in V :\langle x,y\rangle=0\quad\forall y\in S\}
$$
el complemento ortogonal de $S$. Es el conjunto de todos los vectores en $V$ que son ortogonales a todos los vectores en $S$.


#### Teorema 6.6
Sea $W$ un subespacio de $V$ un espacio vectorial con producto interno.
$$
	\forall y\in V,\exists!u\in W\wedge \exists!z\in W^{\perp}:y=u+z.
$$
Más aún, si $\langle v_{1},\dots,v_{k}\rangle$ es una base ortonormal de $W$, entonces 
$$
	u=\sum_{i=1}^{k}\langle y,v_{i}\rangle v_{i}.
$$
##### Demostración:
Sea $\{ v_{1},\dots,v_{k} \}$ una base ortonormal de $W$ y sea $u$ definida como en el teorema, y $z=y-u$. Claramente $u\in W$ y $y=u+z$. Para ver que $z\in W^{\perp}$, basta mostrar que $z$ es ortogonal a cualquier vector de la base, es decir que 
$$
	\begin{align}
	\langle z,v_{j}\rangle&=\left\langle \left( y-\sum_{i=1}^{k}\langle y,v_{i}\rangle v_{i} \right), v_{j}\right\rangle = \langle y, v_{j}\rangle -\sum_{i=1}^{k}\langle y,v_{j}\rangle \langle v_{i},v_{j}\rangle \\
	&=\langle y,v_{j}\rangle -\langle y,v_{j}\rangle =0.
	\end{align}
$$
Para mostrar la unicidad, supongamos que $y=u+z=u´+z´$, donde $u'\in W$ y $z'\in W^{\perp}$. Entonces $u-u´=z'-z\in W\cap W^{\perp}=\{ 0 \}$, por lo tanto $u=u'$ y $z=z'.\quad\square$

El vector $u$ del teorema recibe el nombre de la ***proyección ortogonal*** de $y$ sobre $W$.

#### Teorema 6.7
Suponga que $S=\{ v_{1},\dots,v_{k} \}$ es un conjunto ortonormal en un espacio de producto interno $V$ de dimensión $n$. Entonces 
a) $S$ se puede extender a una base ortonormal $\{ v_{1},\dots,v_{k},v_{k+1},\dots,v_{n} \}$ para $V$.
b) Si $W=\mathrm{span}(S)$, entonces $S_{1}=\{ v_{k+1},\dots,v_{n} \}$ es una base ortonormal de $W^{\perp}$.
c) SI $W$ es cualquier subespacio de $V$, entonces $\mathrm{dim}(V)=\mathrm{dim}(W)+\mathrm{dim}(W^{\perp})$.
##### Demostración:
a) Sabemos que cualquier conjunto linealmente independiente se puede extender a una base $S'=\{ v_{1},\dots,v_{k},w_{k+1},\dots,w_{n} \}$ de $V$, y usando el proceso Gram-Schmidt sobre $S'$, los primeros $k$ vectores se mantienen igual, (pues al ser ortonormales, sus productos puntos dan cero), y el nuevo conjunto genera $V$, por lo que solo falta normalizar los vectores nuevos para obtener la base ortonormal de $V$.
b) Es evidente que $\{ v_{k+1},\dots,v_{n} \}$ es linealmente independiente, y solo falta ver que genera $W^{\perp}$. Para cualquier $x\in V$, tenemos 
$$
	x=\sum_{i=1}^{n}\langle x,v_{i}\rangle v_{i},
$$
y si $x\in W^{\perp}$, entonces su producto interno con los primeros $k$ vectores es cero, por lo tanto 
$$
	x=\sum_{i=k+1}^{n}\langle x,v_{i}\rangle v_{i}\in \mathrm{span}(S_{1}).
$$
c) Se sigue de forma directa que $\mathrm{dim}(V)=n=k+(n-k)=\mathrm{dim}(W)+\mathrm{dim}(W^{\perp}).\quad\square$
