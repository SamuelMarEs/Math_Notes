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

#### Definición:
Una forma cuadrática es una función $g:\mathbb{R}^{n}\to\mathbb{R}$ tal que
$$
g(h_{1},\dots,h_{n})=\sum_{i,j=1}^{n}a_{ij}h_{i}h_{j},
$$
donde $A=[a_{ij}]$ es una matriz simétrica. $g=h^{T}Ah$.

#### Definición:
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ definida en un abierto $U$. Si $f$ es diferenciable en $x_{0}\in U$ y $\frac{\partial f}{\partial x_{i}}f(x_{0})$ son continuas para $i=1,\dots,n$. Definimos la ***Hessiana*** de $f$ en $x_{0}$ como 
$$
	\begin{align}
	Hf(x_{0})(h)&=\frac{1}{2}\sum_{i,j=1}^{n} \frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}(x_{0})h_{i}h_{j} \\
	&= \frac{1}{2}\begin{bmatrix}
	h_{1} & h_{2} & \dots & h_{n}
	\end{bmatrix}\begin{bmatrix}
	\frac{\partial^{2}f(x_{0})}{\partial x_{1}^{2}} & \dots  & \frac{\partial^{2}f(x_{0})}{\partial x_{1}\partial x_{n}} \\
	\vdots & \dots & \vdots \\
	\frac{\partial^{2}f(x_{0})}{\partial x_{n}\partial x_{1}} & \dots & \frac{\partial^{2}f(x_{0})}{\partial x_{n}^{2}}
	\end{bmatrix} \begin{bmatrix}
	h_{1} \\
	h_{2} \\
	\vdots \\
	h_{n}
	\end{bmatrix}
	\end{align}
$$


Usando el [[TeoremaDeTaylor|teorema de Taylor]], observemos que se puede rescribir el teorema de segundo orden en términos de la Hessiana, es decir 
$$
	f(x_{0}+h)=f(x_{0})+Df(x_{0})\cdot h+R_{1}(x_{0},h)\quad \text{primer orden}
$$
$$
	f(x_{0}+h)=f(x_{0})+Df(x_{0})\cdot h+Hf(x_{0})(h)+R_{2}(x_{0},h)\quad\text{segundo orden.}
$$
Si $x_{0}$ es un punto crítico de $f$, entonces 
$$
	f(x_{0}+h)=f(x_{0})+Hf(x_{0})(h)+R_{2}(x_{0},h).
$$

#### Definición:
Una forma cuadrática $g:\mathbb{R}^{n}\to\mathbb{R}$ se llama definida positiva si $g(h)\geq 0$ para todo $h\in\mathbb{R}^{n}$ y $g(h)=0$ si y sólo si $h=0$. Análogamente se define que la forma cuadrática sea definida negativa.

#### Teorema (Criterio de la segunda derivada)
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ definida en un abierto $U\subset\mathbb{R}^{n}$ y $C^{3}$. Si $x_{0}$ es un punto crítico y $Hf(x_{0})$ es definida positiva, entonces $x_{0}$ es un punto de mínimo local.
Si $Hf(x_{0})$ es definida negativa, entonces $x_{0}$ es un punto de máximo local.

##### Lema:
Si $A=[a_{ij}]$ es una matriz de $n\times n$ y su forma cuadrática asociada $H$ es definida positiva entonces existe una constante $M>0$ tal que 
$$
	H(h)\geq M\lvert \lvert h \rvert  \rvert^{2}.
$$




