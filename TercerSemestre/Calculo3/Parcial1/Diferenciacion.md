##### Definición:
Sea $f:R^{n}\to R$ una [[Funciones|función]] de varias variables con valores reales, definida en un abierto $U\subset R^{n}$. Definimos la ***derivada parcial*** de $f$ respecto a la variable $x_{j}$, con $j=1,\dots,n$, como 
$$
	\frac{\partial f(x_{1},\dots,x_{n})}{\partial x_{j}}=\lim_{ h \to 0 } \frac{f(x_{1},\dots,x_{j}+h, \dots,x_{n})-f(x_{1},\dots,x_{n})}{h},
$$
para algún $j=1,\dots,n$, siempre que el límite exista.
A 
$$
	\frac{\partial f}{\partial x_{1}},\dots, \frac{\partial f}{\partial x_{n}}
$$
les llamamos derivadas pariales respecto a la primera variable, segunda varialbe, ..., $n$-ésima variable.
Notemos que nos estamos basando en la idea de [[Limite|limite]] para funciones de una sola variable, no multivarialbe, pues las variables distintas a $x_{j}$ las estamos tomando como constantes.

##### Ejemplo:
Sea $f:R^{2}\to R$ definida como $f(x,y)=x^{2}y^{3}$. Entonces 
$$
	\begin{align}
	\frac{\partial}{\partial x}f(x,y)&=\lim_{ h \to 0 } \frac{f(x+h,y)-f(x,y)}{h}=\lim_{ h \to 0 } \frac{(x+h)^{2}y^{3}-x^{2}y^{3}}{h} \\
	&=\lim_{ h \to 0 } \frac{(x^{2}+2xh+h^{2})y^{3}-x^{2}y^{3}}{h}=\lim_{ h \to 0 } 2xy^{3}+hy^{3} \\
	&=2xy^{3}.
	\end{align}
$$
Ahora, si tomamos la derivada parcial respecto a $y$, tenemos 
$$
	\begin{align}
	\frac{\partial}{\partial y}f(x,y)&=\lim_{ h \to 0 } \frac{x^{2}(y+h)^{3}-x^{2}y^{3}}{h} \\
	&=\lim_{ h \to 0 } \frac{x^{2}h^{3}+3x^{2}y^{2}h+3x^{2}yh^{2}}{h} \\
	&=\lim_{ h \to 0 } x^{2}h^{2}+3x^{2}y^{2}+3x^{2}yh &= 3x^{2}y^{2}.
	\end{align}
$$
Como estamos manteniendo todas las variables como constantes, menos la que estamos derivando, entonces aplican todas las reglas de diferenciación que conocemos de cálculo 1.


#Calculo