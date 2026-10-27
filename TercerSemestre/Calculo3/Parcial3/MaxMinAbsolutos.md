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

### Máximos y mínimos absolutos para $f:\mathbb{R}^{n}\to\mathbb{R}$
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
Entonces los puntos criticos de $f$ en $D$ son $(0,0),(0,1),(0,-1),(\sqrt{ 2 },0),(-\sqrt{ 2 },0)$. Al evaluar los puntos tenemos 
$$
	f(0,0)=0,f(0,1)=\frac{1}{2} , f(0,-1)=\frac{1}{2}, f(\sqrt{ 2 },0)=1, f(-\sqrt{ 2 },0)=1.
$$
Entonces el punto de mínimo global en $D$ es $(0,0)$, y los puntos de máximo son $(\pm \sqrt{ 2 },0)$.