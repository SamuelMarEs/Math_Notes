#Calculo 
#### Qué tan curva es una curva?
Para conocer la curvatura de una curva, debemos fijarnos en cómo va cambiando la dirección conforme recorremos la curva.

Sea $c(t)$ una curva suave, definimos al vector 
$$
	T(t)=\frac{c'(t)}{\lvert \lvert c'(t) \rvert  \rvert }
$$
el ***vector tangente unitario***, y en base a esto se define la curvatura como 
$$
	k=\left\lvert  \left\lvert  \frac{dT}{ds}  \right\rvert   \right\rvert ,
$$
que por regla de la cadena es lo mismo que 
$$
	\frac{dT}{dt}=\frac{dT}{ds}\cdot \frac{ds}{dt},
$$
es decir que 
$$
	k(t)=\left\lvert  \left\lvert  \frac{dT}{ds}  \right\rvert   \right\rvert =\frac{\lvert \lvert T'(t) \rvert  \rvert }{\lvert \lvert c'(t) \rvert  \rvert }.
$$
Si $\gamma(s)$ es una parametrización por [[LongitudDeArco|longitud de arco]], entonces $k(s)=\lvert \lvert T'(s) \rvert \rvert$ pues $\lvert \lvert \gamma'(s) \rvert \rvert=1$, entonces $T(s)=\gamma'(s)$ y esto implica que $T'(s)=\gamma''(s)$, por lo tanto 
$$
	k(s)=\lvert \lvert \gamma''(s) \rvert  \rvert ,
$$
es decir que, si nuestra curva está parametrizada por longitud de arco, entonces su curvatura es la segunda derviada.

##### Para $R^{3}$:
Dada una curva $c:\mathbb{R}\to\mathbb{R}^{2}$, definimos para $c(t_{0})$ el ***círculo osculador*** como el círculo que comparte tangente con $c(t)$ en $c(t_{0})$.
Para $c:\mathbb{R}\to\mathbb{R}^{3}$, si $k\neq 0$ definimos el ***vector normal unitario*** 
$$
	N(t)=\frac{T'(t)}{\lvert \lvert T'(t) \rvert  \rvert }
$$
y al ***vector binomial*** 
$$
	B(t)=T(t)\times N(t).
$$
Si tenemos una curva parametrizada por longitud de arco, entonces 
$$
	N(s)=\frac{T'(s)}{\lvert \lvert T'(s) \rvert  \rvert }.
$$
En base a esto, la curvatura se puede calcular como 
$$
	k(t)=\frac{\lvert \lvert c'(t)\times c''(t) \rvert  \rvert }{\lvert \lvert c'(t) \rvert  \rvert ^{3}}.
$$
Estos tres vectores se conocen como el triedro de Frenet $(T(t), N(t), B(t))$, comunmente encontrados como $(\tau(t), n(t), b(t))$.

#### ¿Qué tan plana es una curva?
Dada una curva $\gamma(s)$ parametrizada por longitud de arco, sabemos que podemos definir los vectores tangente, normal, y binomial como 
$$
	T(s)=\frac{\gamma'(s)}{\lvert \lvert \gamma'(s) \rvert  \rvert },\quad N(s)=\frac{T'(s)}{\lvert \lvert T'(s) \rvert  \rvert },\quad B=T\times N.
$$
Sabemos que $B$ es un vector unitario, por lo tanto $B\cdot B=1$, por lo que podemos tomar la derivada y ver que 
$$
	\frac{d}{ds}(B\cdot B)=\frac{d}{ds}1,
$$
que aplicando la regla de la cadena es lo mismo que 
$$
	\frac{dB}{ds}\cdot B=0,
$$
es decir que $\frac{dB}{ds}\perp B$ (son perpendiculares).
Además, sabemos que $T$ y $B$ son perpendiculares (por definición), entonces 
$$
	B\cdot T=0,
$$
y por regla de la cadena esto es 
$$
	\frac{dB}{ds}\cdot T+B\cdot \frac{dT}{ds}=0.
$$
Recordando la definición del vector normal unitario, esto nos dice que 
$$
	\frac{dB}{ds}\cdot T+\left\lvert  \left\lvert  \frac{dT}{ds}  \right\rvert   \right\rvert B\cdot N=0,
$$
pero por la definición de curvatura $k$, tenemos que 
$$
	\frac{dB}{ds}\cdot T+kB\cdot N=0,
$$
pero $B$ y $N$ son perpendiculares, por lo tanto llegamos a que 
$$
	\frac{dB}{ds}\cdot T=0\implies \frac{dB}{ds}\perp T.
$$
Recordemos que estamos en $\mathbb{R}^{3}$, notemos que $\frac{dB}{ds}$ es perpendicular tanto a $B$ como a $T$, entonces $\frac{dB}{ds}$ es paralelo a $N$. Es decir que 
$$
	\frac{dB}{ds}=-\tau N,\quad\tau\in\mathbb{R}
$$

#### Plano normal
Sea $c:\mathbb{R}\to\mathbb{R}^{n}$ una curva diferenciable, y $P_{0}=c(t_{0})$ un punto sobre la curva donde $c'(t_{0})\neq 0$. El plano normal a la curva en $P_{0}$ es el plano perpendicular a la recta tangente en ese punto, y que pasa por $P_{0}$.
Es decir, el plano normal a la curva es el plano cuyo vector normal es $T(t)$, el vector normal tangente a la curva.
Por lo tanto, la ecuación de nuestro plano normal es 
$$
	c'(t_{0})\cdot((x,y,z)-c(t_{0}))=0.
$$
En términos del triedro de Frenet, (para $\mathbb{R}^{3}$) el plano normal es $\mathrm{span}\{ N,B \}$.

#### Plano osculador
Sea $c:\mathbb{R}\to\mathbb{R}^{n}$ una curva diferenciable, y $P_{0}=c(t_{0})$ un punto sobre la curva donde $c'(t_{0})\neq 0$. El plano osculador de $c$ en el punto $P_{0}$ es el plano que contiene a la recta tangete y a la recta normal principal. Es decir, el plano osculador es el plano que mejor aproxima a la curva en el punto $P_{0}$.
Tiene como vector normal al binomial $B=T\times N$, o en otras palabras es el $\mathrm{span}\{ T,N \}$. Las dos formas de encontrar su ecuación son las siguientes: 
$$
	B(t_{0})\cdot((x,y,z)-c(t_{0}))=0,\quad (c'(t_{0})\times c''(t_{0}))\cdot((x,y,z)-c(t_{0}))=0.
$$

#### Circulo osculador
El circulo osculador, también llamado círculo de curvatura, es la circunferencia que mejor aproxima a la curva en un punto $P_{0}$. Está contenida en el plano osculador.
El radio de la circunferencia es 
$$
	R=\frac{1}{k(P_{0})}=\frac{\lvert \lvert c'(t_{0}) \rvert  \rvert ^{3}}{\lvert \lvert c'(t_{0})\times c''(t_{0}) \rvert  \rvert }.
$$
Por otro lado, el centro de la circunferencia está en la dirección del vector normal $N$: 
$$
	C=c(t_{0})+ \frac{1}{k(t_{0})}N(t_{0}).
$$



