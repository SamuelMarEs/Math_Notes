##### Definicón para $R^{2}\to R$
Sea $f:R^{2}\to R$. Decimos que la [[Funciones|función]] $f$ es ***diferenciable*** en $(x_{0},y_{0})$ si existen las [[DerivadasParciales|derivadas parciales]] $\frac{\partial f}{\partial x}(x_{0},y_{0})$ y $\frac{\partial f}{\partial y}(x_{0},y_{0})$, y además el siguiente límite cumple 
$$
	\lim_{ (x,y) \to (x_{0},y_{0})} \frac{f(x,y)-f_{x}(x_{0},y_{0})(x-x_{0})-f_{y}(x_{0},y_{0})(y-y_{0})}{\lvert \lvert (x,y)-(x_{0},y_{0}) \rvert  \rvert }=0.
$$
Vamos a decir que la derivada de $f$ en $(x_{0},y_{0})$ es el vector fila (o matriz fila)
$$
	Df(x,y)=\begin{bmatrix}
	\frac{\partial f}{\partial x}(x_{0},y_{0}) & \frac{\partial f}{\partial y}(x_{0},y_{0})
	\end{bmatrix}.
$$

Entonces podemos reescribir el [[PlanoTangente|plano tangente]].
$$
	f(x_{0},y_{0})+\frac{\partial f}{\partial x}(x_{0},y_{0})(x-x_{0})+\frac{\partial f}{\partial y}(x_{0},y_{0})(y-y_{0}) =
	f(x_{0},y_{0})+DF(x_{0},y_{0})
	\begin{bmatrix}
	x-x_{0} \\
	y-y_{0}
	\end{bmatrix}
$$

##### Definición para $R^{n}\to R$
De forma más general, para una función $f:R^{n}\to R$ podemos definir la derivada 
$$
	Df(a_{1},\dots,a_{n})=\left[ \frac{\partial f}{\partial x_{1}}(a_{1},\dots,a_{n}),\dots, \frac{\partial f}{\partial x_{n}}(a_{1},\dots,a_{n}) \right].
$$
También, si lo vemos como un vector, tenemos el [[Gradiente|gradiente]].
De esta forma, podemos generalizar la derivada a funciones de $R^{n}$ en $R$.

Sea $f:R^{n}\to R$, decimos que es diferenciable en $(a_{1},\dots,a_{n})$ si existen 
$$
	\frac{\partial f}{\partial x_{1}}, \frac{\partial f}{\partial x_{2}},\dots, \frac{\partial f}{x_{n}} \quad\text{en }(a_{1},\dots,a_{n}),
$$
y el límite 
$$
	\lim_{ (x_{1},\dots,x_{n}) \to (a_{1},\dots,a_{n}) } \frac{f(x_{1},\dots,x_{n})-f(a_{1},\dots,a_{n})-Df(a_{1},\dots,a_{n})\begin{pmatrix}
	x_{1}-a_{1} \\
	x_{2}-a_{2} \\
	\vdots \\
	x_{n}-a_{n}
	\end{pmatrix}}{\lvert \lvert (x_{1},\dots,x_{n})-(a_{1},\dots,a_{n}) \rvert  \rvert }=0.
$$

##### Definición para $R^{n}\to R^{m}$
Dada $f:R^{n}\to R^{m}$, tenemos que podemos expresar la función como 
$$
	f(x_{1},\dots,x_{n})=(f_{1}(x_{1},\dots,x_{n}),\dots,f_{m}(x_{1},\dots,x_{n}))
$$
donde $f_{i}:R^{n}\to R$, para $i=1,\dots,m$ se llaman funciones coordenadas de $f$.
Las [[DerivadasParciales|derivadas parciales]] son las funciones 
$$
	\frac{\partial f_{i}}{\partial x_{j}},\quad\text{para }i=1,\dots,m\text{ y }j=1,\dots,n.
$$
Si $f$ es diferenciable, entonces la derivada de $f$ la podemos representar con la matriz de $m\times n$ 
$$
	Df(a_{1},\dots,a_{n})=\begin{bmatrix}
	\frac{\partial f_{1}}{\partial x_{1}}(a_{1},\dots,a_{n}) & \frac{\partial f_{1}}{\partial x_{2}}(a_{1},\dots,a_{n}) & \dots & \frac{\partial f_{1}}{\partial x_{n}}(a_{1},\dots,a_{n}) \\
	\frac{\partial f_{2}}{\partial x_{1}}(a_{1},\dots,a_{n}) & \dots & \dots & \frac{\partial f_{2}}{\partial x_{n}}(a_{1},\dots,a_{n}) \\
	\dots &  &  & \dots \\
	\frac{\partial f_{m}}{\partial x_{1}}(a_{1},\dots,a_{n}) & \frac{\partial f_{m}}{\partial x_{2}}(a_{1},\dots,a_{n}) & \dots & \frac{\partial f_{m}}{\partial x_{n}}(a_{1},\dots,a_{n})
	\end{bmatrix}.
$$
Una vez que definimos las derivadas parciales para una función de $R^{n}\to R^{m}$, podemos definir la noción de diferenciación de forma similar de funciones de $R^{n}\to R$. Notese que en este caso la matriz $Df(a_{1},\dots,a_{n})$ es una [[TransformacionesLineales|transformación lineal]], o la [[Matrices+Transformaciones|matriz asociada a una transformación]] de $R^{n}\to R^{m}$. 

Sea $f:R^{n}\to R^{m}$ y $U\subset R^{n}$ abierto, decimos que $f$ es diferenciable en $(a_{1},\dots,a_{n})\in U$ si existen las derivadas parciales 
$$
	\frac{\partial f_{i}}{\partial x_{j}}\text{ en }(a_{1},\dots,a_{n}),\quad i=1,\dots,m,\quad j=1,\dots,n,
$$
y el límite $$
	\lim_{ (x_{1},\dots,x_{n}) \to (a_{1},\dots,a_{n}) } \frac{\lvert \lvert f(x_{1},\dots,x_{n})-f(a_{1},\dots,a_{n})-Df(a_{1},\dots,a_{n})\begin{pmatrix}
	x_{1}-a_{1} \\
	x_{2}-a_{2} \\
	\vdots \\
	x_{n}-a_{n}
	\end{pmatrix} \rvert  \rvert }{\lvert \lvert (x_{1},\dots,x_{n})-(a_{1},\dots,a_{n}) \rvert  \rvert }=0.
$$

#Calculo