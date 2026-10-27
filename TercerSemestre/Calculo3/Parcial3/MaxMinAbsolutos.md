#Calculo 
#### Definición:
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ definida para $A\subset\mathbb{R}^{n}$. Si $x_{0}\in A$ y $f(x_{0})\geq f(x)\forall x\in A$, entonces decimos que en $x_{0}$ se alcanza un máximo absoluto.
Análogamente, si $f(x_{0})\leq f(x)\forall x\in A$, decimos que en $x_{0}$ se alcanza un mínimo absoluto. 
Otro nombre son mínimos y máximos globales.

#### Definiciones:
Sea $D\subset\mathbb{R}^{n}$, decimos que $D$ es ***cerrado*** si $D^{c}$ es abierto.
Sea $D\subset\mathbb{R}^{n}$, decimos que es ***acotado*** si existe $M>0$ tal que $\lvert \lvert x \rvert \rvert\leq M,\quad\forall x\in D$.
Sea $D\subset\mathbb{R}^{n}$ decimos que $x\in D$ es un ***punto límite*** o ***punto frontera*** si para cada $\varepsilon>0$, $B_{\varepsilon}(x)\cap D\neq \emptyset$ y $B_{\varepsilon}(x)\cap D^{c}\neq \emptyset$. Es decir que, cualquier bola centrada en $x$ contiene un punto dentro y un punto afuera del conjunto.
Un conjunto cerrado y acotado es un compacto.

#### Teorema
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ una función continua en un conjunto cerrado y acotado $D$, entonces $f$ tiene un valor máximo absoluto y un valor mínimo absoluto.

#### Algoritmo para $f:\mathbb{R}^{n}\to\mathbb{R}$
Sea $f$ diferenciable en un compacto $D\subset\mathbb{R}^{n}$ y $U=\mathrm{int}D$ tal que $\mathrm{bd} U$ (frontera) es suave, entonces el algoritmo que tenemos que seguir es:
1.- Encontrar los puntos críticos de $f$ en $U$.
2.- Usar [[MultiplicadoresDeLagrange|multiplicadores de Lagrange]] para encontrar los puntos críticos de $f|_{\mathrm{bd}U}$.
3.- Comparar los valores de $f$ en los puntos críticos.

##### Ejemplo
Sea $f(x,y)=\frac{1}{2}(x^{2}+y^{2})$ y $D=\left\{  (x,y)\in\mathbb{R}^{2}: \frac{x^{2}}{2}+y^{2}  \leq 1\right\}$.
**Sol:**
Primero, para encontrar los puntos críticos de $f$ en $U=\left\{  (x,y)\in\mathbb{R}^{2}: \frac{x^{2}}{2}+y^{2}<1  \right\}$. Los puntos críticos de $f$ son $(x,y)$ tales que 
$$
	0=\nabla f(x,y)=(x, y),
$$
entonces el único punto crítico de $f$ en $U$ (y en general) es $(x,y)=(0,0)$.
Ahora para encontrar los puntos críticos de la frontera, tomemos $g(x,y)=\frac{x^{2}}{2}+y^{2}$, y su curva de nivel $g(x,y)=1$. El gradiente es $\nabla g(x,y)=(x,2y)$, y vamos a comparar las parciales. Entonces tenemos que resolver el siguiente sistema: 
$$
	\frac{x^{2}}{2}+y^{2} =1,\quad x= \lambda x,\quad y=2\lambda y.
$$
Tenemos que considerar dos casos, el primero, $x\neq 0, y=0$, que nos da que $\lambda=1$, y $x=\pm \sqrt{ 2 }, y=0$, por lo que tenemos dos puntos, $(\sqrt{ 2 },0),(-\sqrt{ 2 },0)$.
En el segundo caso, para $x=0, y\neq 0$, tenemos que $\lambda =1 / 2$ y que $y=\pm 1$, por lo que tenemos los puntos $(0,1),(0,-1)$.
Entonces los puntos críticos de $f$ en $D$ son $(0,0),(0,1),(0,-1),(\sqrt{ 2 },0),(-\sqrt{ 2 },0)$. Al evaluar los puntos tenemos 
$$
	f(0,0)=0,f(0,1)=\frac{1}{2} , f(0,-1)=\frac{1}{2}, f(\sqrt{ 2 },0)=1, f(-\sqrt{ 2 },0)=1.
$$
Entonces el punto de mínimo global en $D$ es $(0,0)$, y los puntos de máximo son $(\pm \sqrt{ 2 },0)$.

#### Teorema
Sea $f:\mathbb{R}^{2}\to\mathbb{R}$ y $g:\mathbb{R}^{2}\to\mathbb{R}$ funciones $C^{2}$ en un abierto $U\subset\mathbb{R}^{2}$. Sea $x_{0}\in U$ tal que $g(x_{0})=c$ para alguna constante $c\in\mathbb{R}$, y sea $S=\{ (x,y):g(x,y)=c \}$. Supongamos que $\nabla g(x_{0})\neq 0$ y existe $\lambda\in\mathbb{R}$ tal que $\nabla f(x_{0})=\lambda \nabla g(x_{0})$.
Sea $h=f-\lambda g$, entonces definimos la Hessiana de frontera 
$$
	\bar{H}=\begin{bmatrix}
	0  & -\frac{\partial g(x_{0})}{\partial x} & -\frac{\partial g(x_{0})}{\partial y}\\
	-\frac{\partial g(x_{0})}{\partial x}  & \frac{\partial^{2}h(x_{0})}{\partial x^{2}} & \frac{\partial^{2}h(x_{0})}{\partial xy}\\
	-\frac{\partial g(x_{0})}{\partial y} & \frac{\partial^{2}h(x_{0})}{\partial xy} & \frac{\partial^{2}h(x_{0})}{\partial y^{2}}
	\end{bmatrix}.
$$
Entonces:
1.- Si $\det \bar{H}>0$ entonces $x_{0}$ es punto de máximo local para $f|_{S}$.
2.- Si $\det \bar{H}<0$ entonces $x_{0}$ es punto de mínimo local para $f|_{S}$.
3.- Si $\det \bar{H}=0$, entonces el criterio no es concluyente.

##### Ejemplo
Sea $f(x,y)=(x-y)^{2}$, encontrar los máximos y mínimos locales para $x^{2}+y^{2}=1$.
**Sol:**
Primero buscamos los multiplicadores de Lagrange y nuestros gradientes. Sea $g(x,y)=x^{2}+y^{2}$, entonces tenemos que 
$$
	\nabla f(x,y)=(2(x-y), 2(y-x)),\quad \nabla g(x,y)=(2x,2y).
$$
Para puntos críticos en general, tenemos todos de la forma $x=y$.
Entonces para encontrar los coeficientes de Lagrange tenemos el sistema 
$$
	x^{2}+y^{2}=1,\quad 2(x-y)=\lambda 2x,\quad 2(y-x)=\lambda 2y.
$$
De esto obtenemos que $y=x(1-\lambda)$ y $x=y(1-\lambda)$. entonces $x^{2}(1-\lambda)^{2}+y^{2}(1-\lambda)^{2}=1,$ y como $x^{2}+y^{2}=1$, tenemos que $(1-\lambda)^{2}=1$, es decir que $1-\lambda=\pm 1$, por lo tanto $\lambda=0$ o $\lambda = 2$. Como $\lambda$ no puede ser cero, tomamos únicamente $\lambda=2$, que nos da $x=-y$. Entonces tenemos que $x^{2}+y^{2}=2x^{2}=1\implies x=\pm \frac{\sqrt{ 2 }}{2}$, y por lo tanto los puntos son $\left( \frac{\sqrt{ 2 }}{2}, -\frac{\sqrt{ 2 }}{2} \right)$ y $\left( -\frac{\sqrt{ 2 }}{2}, \frac{\sqrt{ 2 }}{2} \right)$.
El caso $\lambda=0$ nos daría $x=y$, entonces lo puntos son $\left( \frac{\sqrt{ 2 }}{2}, \frac{\sqrt{ 2 }}{2} \right)$ y $\left( \frac{\sqrt{ 2 }}{2}, \frac{\sqrt{ 2 }}{2} \right)$.
Como nos dan hueva las cuentas, el Isaac ya calculo el determinante de la Hessiana fronteriza en cada punto.
En los puntos para $\lambda=2$ llegamos a que $\bar{H}=0$, por lo que tenemos que evaluar la función, de modo que $f\left( \frac{\sqrt{ 2 }}{2}, -\frac{\sqrt{ 2 }}{2} \right)=f\left( -\frac{\sqrt{ 2 }}{2}, \frac{\sqrt{ 2 }}{2} \right)=2$.
Para los puntos de $\lambda=0$, se llega a que $\bar{H}=-16$, por lo tanto se trata de puntos de mínimo local.

#### Teorema
Sean $\lambda_{1}$ y $\lambda_{2}$ los eigenvalores de la Hessiana en $(x_{0},y_{0})$ un punto crítico.
1.- Si $\lambda_{1}>0$ y $\lambda_{2}>0$, entonces $(x_{0},y_{0})$ es de mínimo.
2.- Si $\lambda_{1} <0$ y $\lambda_{2}<0$, entonces $x_{0},y_{0}$ es de máximo.
3.- Si $\lambda_{1}<0$ y $\lambda_{2}>0$, o al revés, entonces es un punto silla.
4.- Si $\lambda_{1}=\lambda_{2}=0$, el criterio no es concluyente.