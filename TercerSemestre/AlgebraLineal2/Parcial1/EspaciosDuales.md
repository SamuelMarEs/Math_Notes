##### Definición:
Sea $V$ un [[EspaciosVectoriales|espacio vectorial]] sobre $F$. El ***espacio dual*** es 
$$
	V^{*}=\mathcal{L}(V,F).
$$
Si $\text{dim}(V)=n$, entonces $\text{dim}(V^{*})=n$, por lo tanto $V\cong V^{*}$.

##### Definición:
Sea $V$ un espacio vectorial de dimensión finita, y sea $\beta=\{ s_{1},\dots,x_{n} \}$ una [[BasesOrdenadas|base ordenada]] de $V$. Para cada $i=1,2,\dots,n$ definimos $f_{i}(x)=a_{i}$, donde 
$$
	[x]_{\beta}=\begin{pmatrix}
	a_{1} \\
	a_{2} \\
	\vdots \\
	a_{n}
	\end{pmatrix}
$$
es el [[RepresentacionEstandar|vector coordenada]] de $x$ relativo a $\beta$. Entonces $f_{i}$ es un operador lineal sobre $V$ llamado la $i$-ésima función coordenada con respecto a la base $\beta$. Notese que $f_{i}(x_{j})=\delta_{ij}$ la delta de Kronecker. 

#### Teorema 2.24
Sea $V$ un espacio vectorial sobre $F$. Sea $\beta=\{ x_{1},\dots,x_{n} \}$ una base ordenada. Sean $f_{i}\in\mathcal{L}(V,F)$ para $1\leq i\leq n$, las [[TransformacionesLineales|transformaciones lineales]] que corresponden a la $i$-ésima coordenada. Entonces 
$$
	\beta^{*}=\{ f_{1},f_{2},\dots,f_{n} \}
$$
es una base ordenada de $V^{*}$. Más aún 
$$
	\forall f\in V^{*}=\mathcal{L}(V,F),\quad f=\sum_{i=1}^{n}f(x_{i})f_{i}.
$$
##### Demostración:
Recordemos que una base es un subconjunto linealmente independiente que genera al espacio vectorial. Basta demostrar que $\beta*$ genera a $V*$.
Sea $f\in V*$, definimos 
$$
	g=\sum_{i=1}^{n}f(x_{i})f_{i},
$$
y vamos a demostrar que $f=g$. Para esto, basta demostrar que la imagen de la base es la misma, es decir que $f(x_{j})=g(x_{j})$ para todo $1\leq j\leq n$. Por la forma en que la dejinimos, 
$$
	\begin{align}
	g(x_{j})&=\left(\sum_{i=1}^{n}f(x_{i})f_{i}\right)(x_{j}) \\
	&=\sum_{i=1}^{n}f(x_{i})f_{i}(x_{j}) \\
	&=\sum_{i=1}^{n}f(x_{i})\delta_{ij} \\
	&=f(x_{1})\delta_{1j}+f(x_{2})\delta_{2j}+\dots+f(x_{n})\delta_{nj} \\
	&=f(x_{j}),\quad\text{pues }\delta_{ij}=\begin{cases}
	1,\text{ para }i=j \\
	0,\text{ para }i\neq j.
	\end{cases}
	\end{align}
$$



##### Ejemplo: 
Sea $V=R^{2}$ y $\beta_{0}\{ (2,1),(3,1) \}$. Encontrar $\beta^{*}=\{ f_{1},f_{2} \}$.
Sabemos que $f_{1}:R^{2}\to R$ es de la forma $f_{1}(x_{1})=f_{1}(2,1)=1$ por la definición de delta de Kronecker. Y $f_{1}(x_{2})=f_{1}(3,1)=0$. Entonces tenemos que la función va a estar dada de por las soluciones del sistema de ecuaciones 
$$
	\begin{pmatrix}
	2 & 1 \\
	3 & 1
	\end{pmatrix}\begin{pmatrix}
	\alpha \\
	\beta
	\end{pmatrix}=\begin{pmatrix}
	1 \\
	0
	\end{pmatrix},
$$
dónde $\alpha=f_{1}(e_{1})$ y $\beta=f_{2}(e_{2})$, cuya solución es $(\alpha,\beta)=(-1,3)$. Entonces tenemos que $f_{1}(x,y)=-x+3y$.
De la misma forma, el sistema que nos da $f_{2}$ es 
$$
	\begin{pmatrix}
	2 & 1 \\
	3 & 1
	\end{pmatrix}\begin{pmatrix}
	\gamma \\
	\mu
	\end{pmatrix}=\begin{pmatrix}
	0 \\
	1
	\end{pmatrix},
$$
cuya solución es $(\gamma,\mu)=(1,-2)$, de modo que $f_{2}(x,y)=x-2y$.
Ahora tomemos cualquier función en el espacio dual $V*$, por ejemplo $g(x,y)=x+y$. El teorema 2.24 nos dice que 
$$
	\begin{align}
	g&=\sum_{i=1}^{2}g(x_{i})f_{i} \\
	&=g(2,1)(-x+3y)+g(3,1)(x-2y) \\
	&=3(-x+3y)+4(x-2y) \\
	&=-3x+9y+4x-8y&=x+y.
	\end{align}
$$

#### Teroema 2.25
Sean $V$ y $W$ espacios vectoriales de dimensión finita sobre $F$, con bases ordenadas $\beta=\{ x_{1},\dots,x_{n} \}$ y $\gamma=\{ y_{1},\dots,y_{m} \}$.
Sea $T:V\to W$ lineal.  Sea $A=[T]_{\beta}^{\gamma}$ la matriz de $m\times n$ asociada a la transformación $T$. Sea $T^{t}:W*\to V*$ definida por $T^{t}(g)=gT$. Entonces 
1. $T^{t}$ es lineal.
2. $([T]_{\beta}^{\gamma})^{t}=[T^{t}]_{\gamma*}^{\beta*}$.
##### Demostración:
1.- (Tarea)

2.- 


#AlgebraLineal