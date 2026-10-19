#Calculo 
#### Definición: 
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ definida en un abierto $U\subset\mathbb{R}^{n}$, decimos que $x_{0}\in U$ es un punto crítico si 
$$
	Df(x_{0})=\bar{0},
$$
o si $f$ no es diferenciable en $x_{0}$.

#### Definición:
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ definida en un abierto $U\subset\mathbb{R}^{n}$, decimos que $x_{0}\in U$ es un punto de mínimo local si existe una vecindad $V\subset U$ de $x_{0}$ tal que $f(x_{0})\leq f(x)$ para todo $x\in V$.
De forma análoga, es un punto de máximo local si existe una vecindad tal que $f(x_{0})\geq f(x)$ para todo $x\in V$.

#### Teorema
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ definida en un abierto $U\subset\mathbb{R}^{n}$ y $x_{0}\in U$ un punto de máximo local o un punto de mínimo local, entonce $Df(x_{0})=\bar{0}$, es decir que $x_{0}$ es un punto crítico. Esto es lo mismo que $\nabla f(x_{0})=\bar{0}$.
##### Demostración:
Sean $x_{0}$ y $h$ dos vectores fijos, y definimos 
$$
	g(t)=f(x_{0}+th),
$$
i.e. restringimos nuestra función a una recta con dirección $h$ que pasa por $x_{0}$. Supongamos que $f(x_{0})$ es un máximo local ($x_{0}$ es un punto de máximo local), entonces se tiene que $g(0)=f(x_{0})$ también es un máximo local para la imagen de $g$, por lo tanto $g'(0)=0$.
Además, por la regla de la cadena, tenemos que 
$$
	g'(t)=Df(x_{0}+th)\cdot h\implies 0=g´(0)=Df(x_{0})\cdot h.
$$
Esto se satisface para cualquier dirección $h$, es decir que 
$$
	\nabla f(x_{0})\cdot h=0,\quad\forall h\in\mathbb{R}^{n},
$$
por lo tanto $\nabla f(x_{0})=\bar{0}.\quad\square$

##### Ejemplos
1.- Sea $f(x,y)=x^{2}+y^{2}$, tenemos que la derivada es $\nabla f(x,y)=(2x,2y)$, de modo que $\nabla f(0,0)=0$, es decir que el único punto crítico es $(0,0)$. Además, notemos que $f(x,y)\geq 0$ para todo $(x,y)$, y además $f(0,0)=0$, por lo tanto el punto es un mínimo local.

#### Definición
