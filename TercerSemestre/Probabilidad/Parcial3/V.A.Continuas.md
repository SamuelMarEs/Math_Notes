#Probabilidad 
En general, una [[VariablesAleatorias|v.a.]] continua es aquella que toma valores en un intervalo $(a,b)\subset\mathbb{R}$. 
#### Definición:
Decimos que una v.a. $X$ es continua si su [[FuncionDeDistribucion|función de distribución acumulada]] $F(x)$ es continua.
#### Definición:
Decimos que una v.a. $X$ es ***absolutamente*** continua si existe una función $f:\mathbb{R}\to\mathbb{R}$ tal que: 
1. $f(x)\geq 0$ para todo $x\in\mathbb{R}$;
2. $\int_{-\infty}^{\infty}f(x)=1$;
3. $\int_{a}^{b}f(x)=P(X\in(a,b))$.
A esta función $f$ se le conoce como ***función de densidad de probabilidad*** (pdf). 
La función de densidad indica donde se concentra más la probabilidad.
Notemos que si queremos calcular una cierta probabilidad, tenemos que 
$$
	P(X=a)=\int_{a}^{a}f(x)dx=0\quad \forall a\in\mathbb{R}.
$$
Al trabajar con variables continuas, nos interesa 
$$
    P(X\leq a)=\int_{-\infty}^{a}f(x)dx,\quad P(X>a)=\int_{a}^{\infty}f(x)dx,\quad P(a\leq X\leq b)=\int_{a}^{b}f(x)dx.
$$

##### Ejemplos
1.- Sea $X$ una v.a. continua con función de densidad $f(x)=\begin{cases}c\lvert x \rvert, & -2\leq x\leq 2 \\  0, & \text{en otro caso}\end{cases}$. ¿Existe algún valor de $c$ que haga que sea realmente una función de densidad?
**Sol:**
Para la primera condición, $f(x)\geq 0$, basta tomar $c\geq 0$.
Para la segunda condición, queremos que $\int_{-\infty}^{\infty}f(x)dx=1$, es decir que 
$$
	c\int_{-\infty}^{\infty}\lvert x \rvert dx=1\implies c\left(\int_{-\infty}^{-2}0dx+\int_{-2}^{0}-xdx+\int_{0}^{2}xdx+\int_{2}^{\infty}0dx\right)=1.
$$
Esto es lo mismo que 
$$
	c\left( \left(0+\frac{4}{2}\right)+\left( \frac{4}{2}-0 \right) \right)=1\implies 4c=1,
$$
es decir que el valor que necesitamos es $c=\frac{1}{4}$.

2.- Sea $X$ una v.a. continua con función de densidad 
$$
	f(x)=\begin{cases}
	\lambda e^{-\lambda x}, & x>0; \\
	0 & \text{en otro caso}.
	\end{cases}
$$
**Sol:**
Si $\lambda$ es positivo, es evidente que la función siempre es no negativa, por lo tanto basta con confirmar que la integral es 1. 
$$
	\int_{-\infty}^{\infty}f(x)dx=\int_{0}^{\infty}\lambda e^{-\lambda x}dx=\lim_{ a \to \infty } \int_{0}^{a}\lambda e^{-\lambda x}dx.
$$
Sea $u=-\lambda x$, tenemos $du=-\lambda dx$, y además $x\to 0 \implies u\to 0$ y $x\to a\implies u\to \lambda a$. Entonces tenemos 
$$
	\lim_{ a \to \infty } \int_{0}^{\lambda a}-e^{u}du=\lim_{ a \to \infty } -e^{\lambda a}+e^{0}=1.
$$

##### Note
Si conocemos la función de distribución acumulada $F(x)$, podemos calcular cualquier probabilidad relacionada con $X$. 
$$
	P(X\leq a)=F(a),\quad P(X>a)=1-F(a),\quad P(a\leq X\leq b)=F(b)-F(a).
$$

##### Ejercicios
1.- Sea $X$ una v.a. continua con pdf $f(x)=\begin{cases}\lvert x \rvert / 4, & -2\leq x\leq 2 \\  0, & \text{en otro caso}\end{cases}$. ¿Podemos encontrar una fórmula explicita para $F(x)$?
**Sol:**
Básicamente sólo tenemos que resolver una integral: 
$$
	F(x)=\int_{-\infty}^{x}f(t)dt=\int_{-2}^{x}f(t)dt=\begin{cases}
	\int_{-2}^{x}-t / 4 dt, & x\in(-2,0); \\
	\int_{-2}^{0}-t /4 dt+\int_{0}^{x}t / 4dt, & x\in[0,2) \\
	1,  & x\geq 2.
	\end{cases}
$$
Para el primer caso, tenemos que 
$$
	\int_{-2}^{x}-\frac{t}{4}dt=-\frac{1}{4}\left( \frac{x^{2}}{2}-2 \right)=\frac{4-x^{2}}{8}.
$$
Para el segundo, la primera integral ya sabemos que es $2$. La segunda integral es 
$$
	\int_{0}^{x} \frac{t}{4}dt=\frac{1}{4}\left( \frac{x^{2}}{2}-0 \right)=\frac{x^{2}}{8}.
$$
Entonces tenemos que la función está dada por 
$$
	F(x)=\begin{cases}
	0, & x<-2 \\
	(4-x^{2})/8, & -2\leq x<0 \\
	(x^{2}+4) / 8, & 0\leq x<2 \\
	1, & x\geq 2.
	\end{cases}
$$


