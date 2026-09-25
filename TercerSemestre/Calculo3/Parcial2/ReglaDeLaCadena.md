#Calculo
#### Caso general
Sean $U\subset R^{n}$ y $V\subset R^{m}$ abiertos. Sean $f:U\to R^{m}$ y $g:V\to R^{p}$ funciones dadas tales que $f$ manda $U$ en $V$ y tales que $g\circ f$ está definida.
Supongamos que $f$ es diferenciable en $x_{0}$ y que $g$ es diferenciable en $y_{0}=f(x_{0})$. Entonces $g\circ f$ es diferenciable en $x_{0}$, y 
$$
	D(g\circ f)(x_{0})=Dg(f(x_{0}))Df(x_{0}).
$$
$Dg$ es una matriz de $p\times m$ y $Df$ es una matriz de $m\times n$, por lo tanto la composición es una matriz de $p\times n$.
(Demostración pendiente)

##### Corolario:
Sea $k(x,y,z)\to(u(x,y,z),v(x,y,z),w(x,y,z))$ una transformación diferenciable en un conjunto abierto $U\subset R^{3}$ y $f$ una función de $R^{2}\to R$.
Sea $h(x,y,z)=f(u(x,y,z),v(x,y,z),w(x,y,z))$, tenemos que 
$$
	\frac{\partial h}{\partial x}=\frac{\partial f}{\partial u} \frac{\partial u}{\partial x}+\frac{\partial f}{\partial v} \frac{\partial v}{\partial x}+\frac{\partial f}{\partial w} \frac{\partial w}{\partial x}.
$$
Las fórmulas son análogas para las parciales respecto a $y$ y $z$.
###### Demostración:
Supongamos que la regla de cadena para el caso general se cumple. Tenemos entonces que 
$$
	Dh(x,y,z)=Df(u,v,w)Dk(x,y,z),
$$
o lo que es lo mismo 
$$
	\left[ \frac{\partial h}{\partial x}, \frac{\partial h}{\partial y}, \frac{\partial h}{\partial z} \right]=\left[ \frac{\partial f}{\partial u}, \frac{\partial f}{\partial v}, \frac{\partial f}{\partial w} \right] \begin{bmatrix}
	\frac{\partial u}{\partial x} & \frac{\partial u}{\partial y} & \frac{\partial u}{\partial z} \\
	\frac{\partial v}{\partial x} & \frac{\partial v}{\partial y} & \frac{\partial v}{\partial z} \\
	\frac{\partial w}{\partial x} & \frac{\partial w}{\partial y} & \frac{\partial w}{\partial z}
	\end{bmatrix}.
$$
Si realizamos el producto matricial, y consideramos la igualdad de las matrices, el resultado es evidente hasta para un niño de primaria. $\quad\square$

##### Corolario:
Sean $c:R\to R^{3}$ y $f:R^{3}\to R$ diferenciables. Si $h(t)=f(c(t))$, o lo que es lo mismo 
$$
	f(c(t))=f(x(t),y(t),z(t)),\quad c(t)=(x(t),y(t),z(t)).
$$
Entonces tenemos que 
$$
	\frac{dh}{dt}= \frac{\partial f}{\partial x} \frac{dx}{dt}+ \frac{\partial f}{\partial y} \frac{dy}{dt} + \frac{\partial f}{\partial z } \frac{dz}{dt}.
$$
Notemos que $h:R\to R$, y por lo tanto estamos trabajando con una derivada clásica, no parcial.
Es decir que
$$
	\frac{dh}{dt}= <\nabla f,c'(t)>.
$$
***Note:*** la notación $<u,v>$ denota el producto interno de los vectores $u,v$, que en este caso es $\sum u_{i}v_{i}$.
Como $f:R^{3}\to R$, entonces $Df=\nabla f=\left(  \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z} \right)$, y aparte $c:R\to R^{3}$ implica que $c'(t)=\left(  \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right)$.
###### Demostración:
Por la regla de la cadena, tenemos que 
$$
	Dh=Df(c(t))Dc(t),
$$
que es lo mismo que 
$$
	\frac{dh}{dt}=\left[\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z}\right]\begin{bmatrix}
	\frac{dx}{dt} \\
    \frac{dy}{dt} \\
	\frac{dz}{dt}
	\end{bmatrix},
$$
por lo que es trivialote que el corolario se cumple. $\quad\square$

###### Ejemplo
$f(x,y)=(x^{2}+1,y^{2}), g(u,v)=(u+v,u,v^{2})$. 
$g\circ f:R^{2}\to R^{3}$
$Dg\circ f(1,1)= Dg(f(1,1))Df(1,1)$
$Dg=\begin{pmatrix}1 & 1 \\  1 & 0 \\  0 & 2v\end{pmatrix}$
$Df=\begin{pmatrix}2x & 0 \\  0 & 2y\end{pmatrix}$
$f(1,1)=(2,1)$
$Dg(f)(1,1)=Dg(2,1)Df(1,1)=\begin{pmatrix}1 & 1 \\  1 & 0 \\  0 & 2\end{pmatrix}\begin{pmatrix}2 & 0 \\  0 & 2\end{pmatrix}=\begin{pmatrix}2 & 2 \\  2 & 0 \\  0 & 4\end{pmatrix}.$
