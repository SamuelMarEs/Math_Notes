#Probabilidad 
1.- Compruebe que las siguientes funciones son de densidad.
![[GraficasEjerciciosProba3]]
**Sol:**
a) Por la gráfica, podemos ver que $f(x)\geq 0,\forall x$. Además tenemos que 
$$
	\int_{-\infty}^{\infty}f(x)dx=\int_{0}^{2}f(x)dx=\mathrm{Area}(\Delta ABC),
$$
para $A=(0,0),B=(1,1),C=(2,0)$, entonces tenemos que $\mathrm{Area}(\Delta ABC)=\frac{2\cdot 1}{2}=1$. Por lo tanto si es función de densidad.

b) Por la gráfica, podemos ver que $f(x)\geq 0$ para todo $x$. Además, tenemos que 
$$
	\int_{-\infty}^{\infty}f(x)dx=\int_{0}^{a}f(x)dx=\mathrm{Area}(\Delta ABC),
$$
dónde $A=(0,0),B=(a,2 / a), C=(a,0)$, por lo tanto $\mathrm{Area}(\Delta ABC)=\frac{a \cdot 2 / a}{2}=1$. Por lo tanto si es función de densidad.

c) Nuevamente por la gráfica, tenemos que $f(x)\geq 0$ para todo $x$. Y su integral va a estar dada por 
$$
	\int_{-\infty}^{\infty}f(x)dx=\int_{-\sqrt{ 2 / \pi }}^{-\sqrt{ 2/\pi }}f(x)dx=A,
$$
donde $A$ es el área de medio círculo de radio $\sqrt{ 2/\pi }$, que es 
$$
	A=\frac{\pi r^{2}}{2}=\frac{\pi(\sqrt{ 2 / \pi })^{2}}{2}=1.
$$
Por lo tanto la función si es función de densidad.

d) Por el dibujo vemos que $f(x)\geq 0$ para todo $x$. Además tenemos que 
$$
	\int_{-\infty}^{\infty}f(x)dx=\int_{-a}^{0}f(x)dx+\int_{0}^{a}f(x)dx,
$$
donde ambas integrales representan un triángulo con base $a$ y altura $1 / a$, por lo tanto el área de cada uno es 
$$
	A=\frac{a\cdot(1 / a)}{2}=\frac{1}{2},
$$
y entonces tenemos que 
$$
	\int_{-a}^{0}f(x)dx+\int_{0}^{a}f(x)dx=A+A=2A=1.
$$
Por lo tanto la función si es una función de densidad.

2.- Determina si las siguientes funciones son de distribución y encuentra la función de densidad.
a) $F(x)=\begin{cases}0, & x<0 \\  1-\cos x, & 0\leq x\leq \frac{\pi}{2} \\  1, & x> \frac{\pi}{2} \end{cases}$.
b) $F(x)=\begin{cases}0, & x<0 \\  x^{2}, & 0\leq x< \frac{1}{2} \\  1-3(1-x) / 2, & 1 / 2\leq x <1 \\  1, & \text{en otro caso}\end{cases}$.

**Sol:**
a)
![[CDF1_EjerciciosProba3.png]]
Observemos que la función cumple las siguientes propiedades: 
$$
	\lim_{ x \to \infty } F(x)=\lim_{ x \to \infty } 1=1,\quad \lim_{ x \to -\infty }F(x)=\lim_{ x \to -\infty } 0=0.
$$
La gráfica nos muestra que la función es no decreciente. Por último, para comprobar que en efecto es continua, veamos que en cada cacho las funciones son continuas, por lo tanto tenemos que analizar la función en los límites entre cada cacho.
Primero, para $x=0$, tenemos que $F(0)=1-\cos(0)=0$, y $\lim_{ x^{-} \to 0 }F(x)=\lim_{ x^{-} \to 0 }0=0$, y $\lim_{ x^{+} \to 0 }F(x)=\lim_{ x^{+} \to 0 }1-\cos(x)=0$, por lo tanto la función si es continua en $x=0$.
Ahora, para $x=\frac{\pi}{2}$, tenemos que $F(\pi / 2)=1-\cos(\pi / 2)=1$, y $\lim_{ x^{-} \to \pi / 2 }F(x)=1-\cos(\pi / 2)=1$, y $\lim_{ x^{+} \to \pi / 2 }F(x)=\lim_{ x^{+} \to \pi / 2 }1=1$, por lo tanto la función también es continua en los extremos entre intervalos.
Para encontrar las funciones de densidad, tenemos que derivar: 
$$
	f(x)=\frac{d}{dx}F(x)=\begin{cases}
	0, & x<0 \\
	\sin x, & 0\leq x\leq \pi / 2 \\
	0, & x > \pi/2
	\end{cases}.
$$

b) 
![[CDF2_EjerciciosProba3.png]]
(Notar que aunque las gráficas se parecen, los puntos donde alcanza su máximo por primera vez difieren).
La función cumple que 
$$
	\lim_{ x \to \infty } F(x)=\lim_{ x \to \infty } 1=1,\quad \lim_{ x \to -\infty } F(x)=\lim_{ x \to -\infty } 0=0.
$$
La gráfica de la función muestra que es no decreciente. Además, nuevamente dentro de cada intervalo, las funciones a pedazos son continuas, por lo que únicamente falta analizar los extremos 
$$
	\lim_{ x^{-} \to 0 } F(x)=\lim_{ x^{-} \to 0 } 0=0=\lim_{ x^{+} \to 0 } x^{2}=\lim_{ x^{+} \to 0 } F(x),\quad F(0)=0^{2}=0;
$$
$$
	\lim_{ x^{-} \to 1 / 2 } F(x)=\lim_{ x^{-} \to 1 / 2 } x^{2}=1 / 4=\lim_{ x^{+} \to 1 / 2 } 1-\frac{3(1-x)}{2}=\lim_{ x^{+} \to 1 / 2 } F(x),\quad F(1 / 2)=1-\frac{3(1- 1 / 2)}{2}=1 / 4;
$$
$$
	\lim_{ x^{-} \to 1 } F(x)=\lim_{ x^{-} \to 1 }1-\frac{3(1-x)}{2} =1=\lim_{ x^{+} \to 1 } 1=\lim_{ x^{+} \to 1 } F(x),\quad F(1)=1.
$$
Por lo tanto la función es continua en todos los puntos.
Por último, si derivamos para obtener la pdf, tenemos que 
$$
	f(x)=\frac{d}{dx}F(x)=\begin{cases}
	0, & x<0 \\
	2x,  & 0\leq x< 1 / 2 \\
	3 / 2, & 1 / 2\leq x < 1 \\
	0, & x \geq 1
	\end{cases}.
$$


3.- Sea $X$ una v.a. continua con pdf $f(x)=\begin{cases}1 / 4, & \lvert x \rvert\leq 1 \\  1/(4x^{2}), & \lvert x \rvert>1\end{cases}$.
a) Graficar $f(x)$.
b) Calcular 
- $P(\lvert X \rvert< 3 / 2)$
- $P(X>0)$
- $P(1 / 2<X< 3 / 2)$
- $P(\lvert X \rvert \leq 1)$
**Sol:**
a) Gráfica hecha en python.
![[PDF1_EjerciciosProba3.png]]
b) 
Para el primer inciso, tenemos 
$$
	\begin{align}
	P(\lvert X \rvert < 3 / 2)&=P(-3 / 2<X< 3 / 2)=\int_{-3 / 2}^{3 / 2}f(x)dx \\
	&=\int_{-3 / 2}^{-1} \frac{1}{4}x^{-2}dx + \int_{-1}^{1} \frac{1}{ 4}dx+\int_{1}^{3 / 2} \frac{1}{4}x^{-2}dx \\
	&= \frac{1}{4}\left( 1-\frac{2}{3} \right)+ \frac{1}{2}+ \frac{1}{4}\left(  -\frac{2}{3 } + 1\right) \\
	&= 1- \frac{1}{3} = \frac{2}{3}.
	\end{align}
$$
Para el segundo inciso, lo que buscamos es 
$$
	P(X>0)=\int_{0}^{\infty}f(x)dx=\int_{0}^{1} \frac{1}{ 4}dx+\lim_{ n \to \infty } \int_{1}^{n} \frac{1}{4}x^{-2}dx=\frac{1}{4}+\frac{1}{4} \lim_{ n \to \infty }-1 / n+1=1 / 2. 
$$
Para el tercer inciso, tenemos 
$$
	\begin{align}
	P\left( \frac{1}{2}< X < \frac{3}{2} \right)&= \int_{1 / 2}^{3 / 2}f(x)dx \\
	&= \int_{1 / 2}^{1} \frac{1}{4} dx+\int_{1}^{3 / 2} \frac{1}{4} x^{-2}dx \\
	&= \frac{1}{4}-\frac{1}{8}+\frac{1}{4}\left( -\frac{2}{3}+1 \right) \\
	&= \frac{1}{2} - \frac{1}{8} - \frac{1}{6}=\frac{12-3-4}{24}=\frac{5}{24}.
	\end{align}
$$
Por último, el cuarto inciso tenemos 
$$
	P(\lvert X \rvert \leq 1)=P(-1\leq X\leq 1)= \int_{-1}^{1}f(x)dx=\int_{-1}^{1} \frac{1}{4} dx=\frac{1}{2}.
$$


4.- Sea $X$ v.a. continua con pdf $f_{x}(x)=\begin{cases}x^{2}+x+c, & 0<x<1 \\  0, & \text{en otro caso}\end{cases}$.
a) Encuentre el valor de $c$ que hace que $f$ sea función de densidad.
b) Encuentre la pdf de $Y=\psi(X)$, donde 
- $\psi(x)=2x-1$;
- $\psi(x)=\sqrt{ x }$;
- $\psi(x)=ax+b,\quad a>0,b$ constantes.
**Sol:**
a) Queremos encontrar $c$ tal que 
$$
	1=\int_{-\infty}^{\infty}x^{2}+x+cdx=\int_{0}^{1}x^{2}+x+cdx,
$$
es decir que 
$$
	1=\frac{1}{3}+\frac{1}{2}+c\implies c= 1 / 6.
$$
b) Para resolver cada inciso, usamos el teorema de cambio de variable.
Para $Y=\psi(x)=2x-1$, la función es estrictamente creciente, y su inversa es $\psi ^{-1}(y)=\frac{y+1}{2}$, y su derivada es $\frac{d}{dy}\psi ^{-1}(y)=\frac{1}{2}$, por lo tanto 
$$
	f_{y}(y)=\begin{cases}
	\frac{1}{2} ((2y-1)^{2}+\left( 2y-1)+\frac{1}{6} \right), & 0<x<1 \\
	0, & \text{en otro caso}.
	\end{cases}
$$


5.- Sea $X$ una v.a. continua con pdf $f(x)=\begin{cases}cx, & 0<x\leq 1 / 2 \\  c(1-x), & 1 / 2<x<1 \\  0, & \text{en otro caso}\end{cases}$.
a) Encuentre $c$ tal que $f$ es función de densidad.
b) Encuentre los valores de $a$ y $b$ tales que $P(a<X<b)=7 / 16$ y $b-a$ es mínimo.