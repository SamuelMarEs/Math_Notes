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

Como consecuencia inmediata, tenemos que si $f|_{S}$ tiene un min o un max en $x_{0}$, entonces $\nabla f(x_{0})$ es normal a $S$ en $x_{0}$. 

Para resolver $\nabla f(x_{0})=\lambda \nabla g(x_{0})$, tenemos que resolver 
$$
	g(x_{0})=c,\quad \frac{\partial f}{\partial x_{i}}(x_{0})=\lambda \frac{\partial g}{\partial x_{i}}(x_{0})
$$
para $i=1,\dots,n$.
Si definimos $h(x_{0},\lambda)=f(x_{0})-\lambda (g(x_{0})-c)$, lo que tenemos que resolver es $\frac{\partial h}{\partial x_{i}}(x_{0},\lambda)=0$ para $i=1,\dots,n$.

##### Ejemplo:
1.- Sea $f(x,y)=x^{2}+y^{2}$ y $S$ la recta que pasa por $(-1,0)$ con un ángulo respecto al eje $x$ de $\theta=\frac{\pi}{4}$.
**Sol:**
Primero tenemos que encontrar la función $g$ de forma que tenga como conjunto de nivel la recta que nos dieron. La recta está dada por 
$$
	y-0=\tan(\theta)(x+1)\implies S=\left\{  (x,y):y-x-1=0  \right\}.
$$
Entonces nuestra función es $g(x,y)=y-x-1$. Además tenemos que $\nabla g(x,y)=(-1,1)$.
Entonces nuestro sistema de ecuaciones va a estar dado por 
$$
	y-x-1=0,\quad 2x=-\lambda, \quad 2y=\lambda,
$$
cuya solución es $(x,y)=\left( -\frac{1}{2}, \frac{1}{2} \right)$ y $\lambda=1$.
Esto implica que el punto $\left( -\frac{1}{2}, \frac{1}{2} \right)$ es un punto crítico de $f|_{S}$. Si nos imaginamos la imagen de $S$ bajo $f$, se vería como un corte del paraboloide $z=x^{2}+y^{2}$, que sería una parábola que se abre hacia arriba, es decir que el punto que encontramos es un mínimo local de $f|_{S}$. 

2.- Sea $f(x,y)=x^{2}-y^{2}$ y $S=\{ (x,y):x^{2}+y^{2}=1 \}$.
**Sol:**
Podemos tomar directamente $g(x,y)=x^{2}+y^{2}$, de modo que tenemos que $\nabla g(x,y)=(2x,2y)$ y $\nabla f(x,y)=(2x,-2y)$. Observemos que $\nabla g(x,y)=0\iff x=0\wedge y=0$, y el punto $(0,0)$ no se encuentra en el conjunto de nivel, por lo tanto $\nabla g(x_{0})\neq 0,\forall x_{0}\in S$. Entonces el sistema que tenemos que resolver es 
$$
	x^{2}+y^{2}=1,\quad 2x=\lambda 2x,\quad -2y=\lambda 2y.
$$
No podemos dividir entre $x$ o entre $y$, pues alguno podría ser cero. Dado que $\lambda$ no tiene sentido que sea cero, entonces tenemos 2 casos:
Caso 1: $x=0,y\neq 0$.
Entonces tenemos que $\lambda=-1$ y $y=\pm 1$, entonces tenemos los puntos $(0,1),(0,-1)$, para los cuales tenemos que $\nabla f(0,1)=(0,-2)=-1(0,2)=-1\nabla g(0,1)$.
Caso 2: $x\neq 0, y=0$.
De forma análoga tenemos que $\lambda=1$ y $x=\pm 1$, por lo que los puntos son $(1,0),(-1,0)$, y podemos ver que $\nabla f(1,0)=(2,0)=1\nabla g(1,0)$, y de igual forma para el punto $(-1,0)$.

Entonces los puntos que buscamos son $(0,1),(1,0),(0,-1),(-1,0)$. Sin embargo, si observamos la imagen de $S$ bajo $f$, veríamos que todos los puntos estarían a la misma "altura", por  lo tanto técnicamente no son ni máximos ni mínimos.

3.- Sea $f(x,y,z)=x+z$ y $S=\{ (x,y,z)\in R^{3} : x^{2}+y^{2}+z^{2}=1\}$.
**Sol:** 
Tomando a $g(x,y,z)=x^{2}+y^{2}+z=1$, nuestros gradientes son $\nabla g(x,y,z)=(2x,2y,2z)$ y $\nabla f(x,y,z)=(1,0,1)$. Entonces lo que queremos es resolver el sistema 
$$
	2x\lambda=1,\quad 2y\lambda=0,\quad 2z\lambda=1,\quad x^{2}+y^{2}+z^{2}=1.
$$
De la segunda ecuación podemos intuir que $y=0$, entonces tenemos que $x=z=\frac{1}{2\lambda}$, entonces tenemos la ecuación 
$$
	\frac{1}{2\lambda^{2}}=1\implies \lambda^{2}=\frac{1}{2}\implies \lambda = \pm \frac{1}{\sqrt{ 2 }}.
$$
Entonces los puntos que nos quedan son $\left( \frac{1}{\sqrt{ 2 }}, 0 , \frac{1}{\sqrt{ 2 }} \right)$ y $\left( -\frac{1}{\sqrt{ 2 }}, 0 , -\frac{1}{\sqrt{ 2 }} \right)$.




#### Varias Restricciones
Si definimos $S$ por $g_{i}(x_{0})=c_{i}$, $i=1,\dots,k$, entonces $f|_{S}$ tiene un máximo o un mínimo sobre $S$ en $x_{0}$ si $\exists \lambda_{i}\in\mathbb{R}$, $i=1,\dots,k$ tales que $\nabla f(x_{0})=\lambda_{1}\nabla g_{1}(x_{0})+\dots+\lambda_{k}\nabla g_{k}(x_{0})$.
##### Ejemplo
Sea $f(x,y,z)=x+y+z$ restringida a $x^{2}+y^{2}=2$ y $x+z=1$. Entonces tenemos dos funciones $g_{1}(x,y,z)=x^{2}+y^{2}-2$ y $g_{2}(x,y,z)=x+z-1$, y $c_{1}=0=c_{2}$. Sus gradientes son $\nabla g_{1}(x,y,z)=(2x,2y,0)$ y $\nabla g_{2}(x,y,z)=(1,0,1)$, y $\nabla f(x,y,z)=(1,1,1)$, entonces el sistema que tendríamos que resolver es 
$$
	1=\lambda_{1} 2x+\lambda_{2},\quad 1=\lambda_{1} 2y,\quad 1= \lambda_{2},\quad x^{2}+y^{2}=2,\quad x+z=1.
$$
Inmediatamente tenemos que $\lambda_{2}=1$. Además, de la primera ecuación, tenemos que $x=0$ y se sigue que $z=1$. Además nos queda que $y=\pm \sqrt{ 2 }$. Por lo tanto tenemos dos puntos, $(0,\sqrt{ 2 }, 1)$ y $(0,-\sqrt{ 2 }, 1)$, por lo tanto $\lambda_{1}=\pm \frac{1}{2\sqrt{ 2 }}$.