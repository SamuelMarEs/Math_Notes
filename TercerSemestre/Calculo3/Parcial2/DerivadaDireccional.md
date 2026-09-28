#Calculo #Geometria
#### Definición:
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ y $\bar{u}$ un vector unitario. La derivada en la dirección $\bar{u}$ en el punto $\bar{a}$ se define como 
$$
	D_{\bar{u}}f(\bar{a})=\lim_{ h \to 0 } \frac{f(\bar{a}+h \bar{u})-f(\bar{a})}{h}.
$$

#### Teorema:
Sea $f:\mathbb{R}^{n}\to \mathbb{R}$. Si $f$ es diferenciable en $\bar{a}$, entonces para toda dirección $\bar{u}=(u_{1},u_{2},\dots,u_{n})$, existe la derivada en $\bar{a}$ en la dirección $\bar{u}$, y 
$$
	D_{\bar{u}}f(\bar{a})=\nabla f\cdot \bar{u},
$$
para $\nabla f$ el [[Gradiente|gradiente]].
##### Demostración:
Sea $c:\mathbb{R}\to\mathbb{R}^{n}$ la recta dada por $c(t)=\bar{a}+t\bar{u}$. Consideremos $f(c(t)):\mathbb{R}\to\mathbb{R}$. Podemos tomar la derivada de esta función usando la [[ReglaDeLaCadena|regla de la cadena]], de modo que tenemos 
$$
	\frac{d}{dt}f(c(t))=\left( \frac{\partial}{\partial x_{1}}f(c(t)), \frac{\partial}{\partial x_{2}}f(c(t)),\dots, \frac{\partial}{\partial x_{n}}f(c(t)) \right)\cdot c'(t),
$$
o lo que es lo mismo que 
$$
	\frac{d}{dt}f(c(t))=\nabla f(c(t))\cdot c'(t).
$$
Observemos que $c(0)=\bar{a}$ y $c'(t)=\bar{u}$. Entonces tenemos que 
$$
	D_{\bar{u}}f(\bar{a})=\nabla f(\bar{a})\cdot \bar{u}.\quad\square
$$

#### Teorema:
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ diferenciable y $\bar{x}\in\mathbb{R}^{n}$ un punto tal que 
$$
	\nabla f(x)\neq 0.
$$
Entonces la dirección del vector gradiente $\nabla f(\bar{x})$ es la dirección en la cual $f(x)$ crece más rápidamente.
##### Demostración:
Sabemos que 
$$
	D_{\bar{u}}f(\bar{x})=\nabla f(\bar{x})\cdot\bar{u}=\lvert \lvert \nabla f(\bar{x}) \rvert  \rvert \cdot \lvert \lvert \bar{u} \rvert  \rvert \cos \theta,
$$
dónde $\theta$ es el ángulo entre $\bar{u}$ y $\nabla f(\bar{x})$. Además, como $\bar{u}$ es unitario, esto es únicamente 
$$
	\lvert \lvert \nabla f(\bar{x}) \rvert  \rvert \cos \theta.
$$
Esta expresión alcanza su máximo en $\cos \theta=1$, o lo que es lo mismo que $\theta=0$, es decir que alcanza su máximo cuando los vectores $\nabla f(\bar{x})$ y $\bar{u}$ son paralelos. $\quad\square$
Se puede interpretar como el punto en el cual la pendiente es más inclinada.

##### Ejemplo:
Sea $f(x,y)=x^{2}y$. Para el punto $(x,y)=(3,2)$, ¿cuál es la dirección en la cuál la derivada direccional es máxima? Entonctrar la derivada en esa dirección.
**Sol:**
El gradiente de nuestra función es $\nabla f=(2xy,x^{2})$, por lo tanto $\nabla f(3,2)=(12,9)=3(4,3)$. Por el teorema anterior, sabemos que esta es la dirección de mayor crecimiento. Tomemos entonces $\bar{u}=\frac{1}{5}(4,3)$ como nuestra dirección unitaria. Entonces la derivada en esta dirección es 
$$
	\nabla f(\bar{a})\cdot \bar{u}=(12,9)\cdot\left( \frac{4}{5}, \frac{3}{5} \right)=\frac{12(4)+9(3)}{5}=\frac{75}{5}=15.
$$

