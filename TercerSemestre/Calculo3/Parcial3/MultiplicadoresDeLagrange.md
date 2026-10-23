#Calculo 
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ nuestra función. Supongamos que queremos encontrar los [[MaxMinAbsolutos|máximos o mínimos]] absolutos.
Para esto, restringimos nuestra función a una curva $c:\mathbb{R}\to\mathbb{R}^{n}$ que tomaremos como nuestro conjunto cerrado. Para los puntos en el interior de la curva, basta encontrar los [[MaximosMinimos|máximos y mínimos locales]] usando el criterio de la derivada. Sin embargo, para encontrar si un máximo mínimo se alcanza en la frontera de nuestro conjunto, tendríamos que encontrar directamente el valor máximo y el valor mínimo de $f(c(t))$. 
Esto no es un problema sencillo de resolver, ni siquiera computacionalmente. 

Para encontrar los máximos y los mínimos de una función $f:\mathbb{R}^{n}\to\mathbb{R}$ restringidos a $g(x)=c$ para alguna constante $c$ y alguna función $g:\mathbb{R}^{n}\to\mathbb{R}$, vamos a considerar funciones $f,g\in C^{1}$ en un abierto $U\subset\mathbb{R}^{n}$ y $S=\{ (x_{1},\dots,x_{n}):g(x_{1},\dots,x_{n})=c \}$ el conjunto de nivel de $c$.
Si $\nabla g(x_{0})\neq 0$ para algún $x_{0}\in U$ y $f|_{S}$ ($f$ restringida a $S$) alcanza un máximo o mínimo local en $S$, entonces existe $\lambda\in\mathbb{R}$ tal que $\nabla f(x_{0})=\lambda \nabla g(x_{0})$.

Sea $c(t)$ una curva contenida en $S$ tal que $c(0)=x_{0}$. Como la curva está contenida en $S$, tenemos que $g(c(t))=c$, y por lo tanto $\frac{d}{dt}g(c(t))=0$. Y por la regla de la cadena, la derivada es de la forma 
$$
	\frac{d}{dt}g(c(t))=\nabla g(c(t))\cdot c´(t)=0.
$$
En particular, para $t=0$, tenemos $\nabla g(x_{0})\cdot c´(0)=0$.
Si $f$ tiene un máximo local en $x_{0}$ restringido a $S$ (es decir, $x_{0}$ no necesariamente es un punto crítico de $f$, pero si un punto crítico de $f|_{S}$), entonces también $f|_{S}$, y entonces 
$$
	\frac{d}{dt}f(c(t))=\nabla f(c(t))\cdot c'(t),
$$
y para $t=0$, tenemos que 
$$
	\nabla f(x_{0})\cdot c´(0)=0
$$

#### Teorema (Multiplicadores de Lagrange)
Sean $f,g:\mathbb{R}^{n}\to\mathbb{R}$ funciones $C^{1}$ en un abierto $U\subset\mathbb{R}^{n}$. Sea $S=\{ x\in\mathbb{R}|g(x)=c \}$ para alguna constante $c$. Supongamos que $\nabla g(x_{0})\neq 0$, $x_{0}\in U$.
Si $f|_{S}$ alcanza un máximo o un mínimo en un punto de $x_{0}\in S$, entonces existe $\lambda\in\mathbb{R}$ tal que $\nabla f(x_{0})=\lambda \nabla g(x_{0})$.
##### Idea de la demostración:
Sea $c:\mathbb{R}\to\mathbb{R}^{n}$ una curva suave contenida en $S$ tal que $c(0)=x_{0}$. Si consideramos $h:\mathbb{R}\to\mathbb{R}$ dada por $h(t)=f(c(t))$ (para $f|_{S}$), tenemos que $h(t)=f(c(0))=f(x_{0})$, por lo tanto $h$ alcanza un máximo o un mínimo en $t=0$.
Entonces $\frac{d}{dt}h(t)=0$ para $t=0$, es decir que 
$$
	0=\frac{d}{dt}h(0)=\frac{d}{dt}f(c(0))=\nabla f(x_{0})\cdot c´(0),
$$
esto implica que el gradiente de $f$, $\nabla f(x_{0})$ es perpendicular a cualquier curva suave contenida en $S$ que pasa por $x_{0}$, por lo tanto $\nabla f$ es perpendicular al vector tangente $c'(0)$, por lo que podemos concluir que $\nabla f(x_{0})\parallel \nabla g(x_{0})$, es decir que $\nabla f(x_{0})=\lambda \nabla g(x_{0})$.
Esto último es pues el gradiente de $g$ es también es perpendicular a su conjunto de nivel $S$.
