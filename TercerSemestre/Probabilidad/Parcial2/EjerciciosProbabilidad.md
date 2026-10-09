#Probabilidad 

1.- Sea $X$ una v.a. con distribución uniforme en $\{ -1,0,1 \}$. Demostrar que $X^{3}$ y $-X$ tienen la misma distribución de $X$.
**Sol:**
Sea $p=P(X=x)$ para $x=-1,0,1$. 
Además, dado $X\in \{ -1,0,1 \}$, tenemos que $X^{3}=\{ -1,0,1 \}$. Entonces tenemos que 
$$
	P(X^{3}=1)=P(X=1)=p,
$$
y de la misma forma para $X^{3}=0$ y $X^{3}=-1$, de modo que $P(X^{3}=x)=p$ para $x=-1,0,1$.
De la misma forma tenemos que si $X\in \{ -1,0,1 \}$, entonces $-X\in \{ 1,0,-1 \}$. Por lo tanto 
$$
	P(-X=1)=P(X=1)=p.
$$
De forma análoga vemos que $P(-X=0)=P(X=0)$ y $P(-X=-1)=P(X=1)$.

2.- Sea $X$ una v.a. con distribución uniforme en $\{ 1,\dots,n \}$. Demuestra que 
	a) $E(X)=\frac{n+1}{2}$
	b) $E(X^{2})=\frac{(n+1)(2n+1)}{6}$
	c) $\mathrm{Var}(X)=\frac{n^{2}-1}{12}$
**Sol:**
Sea $P(X=x)=1 /n$ para $x=1,\dots,n$, tenemos que 
$$
	E(X)=\sum_{x=1}^{n}xP(X=x)=\frac{1}{n}\sum_{x=1}^{n}x=\frac{1}{n} \frac{n(n+1)}{2}=\frac{n+1}{2}.
$$
Además tenemos que 
$$
	E(X^{2})=\sum_{x=1}^{n}x^{2}P(X=x)=\frac{1}{n}\sum_{x=1}^{n}x^{2}=\frac{1}{n} \frac{n(n+1)(2n+1)}{6}=\frac{(n+1)(2n+1)}{6}.
$$
Por último, dado que $\mathrm{Var}(X)=E(X^{2})-[E(X)]^{2}$, entonces 
$$
	\begin{align}
	\mathrm{Var}(X)&=\frac{(n+1)(2n+1)}{6}-\left( \frac{n+1}{2} \right)^{2} \\
	&= (n+1)\left[ \frac{2n+1}{6} -\frac{n+1}{4}\right] \\
	&=(n+1)\left[ \frac{4n+2-3n-3}{12} \right] \\
	&=\frac{(n+1)(n-1)}{12} \\
	&= \frac{n^{2}-1}{12}.
	\end{align}
$$


3.- Sea $X$ una v.a. con distribución uniforme en $\{ 1,\dots,n \}$ y sea $m\leq n$. Encuentra la distribución de $V=\min\{ X,m \}$.
**Sol:**
Sea $$f(x)=\begin{cases}
\frac{1}{n}, & x=1,\dots,n \\
0, & \text{en otro caso}.
\end{cases}$$
Sea además $m\leq n$, entonces tenemos que $V=\min\{ X,m \}$ va a estar en $\{ 1,2,\dots,m \}$. Queremos encontrar lo siguiente:
$$
	P(V=v)=\begin{cases}
	P(X\geq m), & v=m \\
	P(X=v), & 1\leq v<m.
	\end{cases}
$$
Entonces podemos ver que 
$$
	P(X\leq m)=1-\sum_{x=1}^{m}P(X=x)=1-\sum_{x=1}^{m} \frac{1}{n}=1-\frac{m}{n}=\frac{n-m}{n}.
$$
Es decir que 
$$
	P(V=v)=\begin{cases}
	\frac{n-m}{n}, & v=m; \\
	\frac{1}{n}, & 1\leq v<m.
	\end{cases}
$$



4.- Si $X_{1},X_{2},X_{3}$ son v.a. $\mathrm{Bernoulli}(p)$ independientes, encuentre las distribuciones de $Y=X_{1}+X_{2}+X_{3}$. ¿Se puede generalizar el resultado a $Y=\sum_{i=1}^{n}X_{i}$?
**Sol:**
Sabemos que $X_i$ puede tomar los valores $\{ 0,1 \}$, entonces $Y=X_{1}+X_{2}+X_{3}$ puede tomar los valores $\{ 0,1,2,3 \}$, de forma que, por ejemplo, tenemos que 
$$
	P(Y=0)={3\choose 0}p^{0}(1-p)^{3},
$$
lo que se generaliza a que
$$
	P(Y=y)=\begin{cases}
	{3 \choose y}p^{y}(1-p)^{3-y}, & y=0,1,2,3; \\
	0, & \text{en otoro caso}.
	\end{cases}
$$
Es decir, tenemos que $Y\sim \mathrm{Binom}(3,p)$. 
De la misma forma esto se puede generalizar a que $Y=\sum_{i=1}^{n}X_{i}\sim \mathrm{Binom}(n,p)$.


5.- Si $X\sim \mathrm{Binom}(n,p)$, demuestre que $Y=n-X\sim \mathrm{Binom}(n,1-p)$.
**Sol:**
Sea $X\sim \mathrm{Binom}(n,p)$, podemos interpretar a $X$ como el número de éxitos de un experimento aleatorio con probabilidad $p$ en $n$ intentos, es decir que $X$ se encuentra en $\{ 0,1,\dots,n \}$. Entonces, podemos interpretar $Y=n-X$ como el número de fallas del mismo experimento en $n$ intentos, es decir que se encuentra en $\{ n-0,n-1,\dots n-n \}=\{ n,n-1,\dots,0 \}$, o sea los mismos valores.
Sea $y=n-x$, tenemos que $Y=y\iff X=n-y$, por lo tanto
$$
	P(Y=y)=P(X=n-y)={n\choose n-y}p^{n-y}(1-p)^{y}={n\choose y}(1-p)^{y}p^{n-y},
$$
pues por propiedades del coeficiente binomial ${n\choose k}={n\choose n-k}$.
Es decir que $Y\sim \mathrm{Binom}(n,1-p)$.

6.- Un productor de semillas sabe por experiencia que un 10% de un gran lote de semillas no germina. El productor vende sus semillas en paquetes de 20 piezas, garantizando que, por lo menos 18 germinarán. ¿Cuál es el % de paquetes que no cumplirán la garantía?
**Sol:**
Sea $X\sim \mathrm{Bernoulli}(p=9 /10)$ la v.a. que nos dice si una semilla de cualquier lote germina. 
Al tomar un paquete de 20 piezas, estamos tomando una muestra de tamaño $n=20$. Entonces podemos definir $Y=$ el número de semillas buenas en un paquete de 20. Si suponemos que la probabilidad de que las semillas no germinen es independiente, entonces podemos suponer que $Y\sim \mathrm{Binom}(20, 9 / 10)$. Queremos saber cual es la probabilidad de que germinen menos de 18 semillas, es decir 
$$
	P(Y<18)=1-P(Y\geq 18),
$$
dónde tenemos que 
$$
	P(Y\geq 18)=\sum_{y=18}^{20}{20\choose y}\left( \frac{9}{10} \right)^{y} \left( \frac{1}{10} \right)^{20-y}.
$$
(Calculo para después).

7.- Propiedad de pérdida de memoria. Si $X\sim \mathrm{Geom}(p)$, demuestre que 
$$
	P(X\geq n+m|X\geq n)=P(X\geq m).
$$
**Sol:**
Por el Teorema de Bayes, sabemos que 
$$
	P(X\geq n+m|X\geq n)=\frac{P(X\geq n+m)P(X\geq n|X\geq n+m)}{P(X\geq n)}.
$$
Observemos que $P(X\geq n|X\geq n+m)=1$ para $m\geq 0$, pues si $X$ ya es mayor que $n+m$, entonces por consiguiente es mayor a $n$. Entonces esto nos deja con 
$$
	P(X\geq n+m|X\geq n)=\frac{P(X\geq n+m)}{P(X\geq n)}.
$$
Dado que $X\sim \mathrm{Geom}(p)$, tenemos que 
$$
	\begin{align}
	P(X\geq n)&=1-P(X<n) \\
	&=1-\sum_{i=1}^{n-1}p(1-p)^{i} \\
	&=1-p\left[ \frac{(1-p)^{n}-1}{1-p-1} \right]= \\
	&1+(1-p)^{n}-1=(1-p)^{n}.
	\end{align}
$$
y de la misma forma 
$$
	\begin{align}
	P(X\geq n+m)&=1-P(X<n+m) \\
	&=1-\sum_{i=1}^{n+m-1}p(1-p)^{i} \\
	&=1-p\left[ \frac{(1-p)^{n+m}-1}{1-p-1} \right] \\
	&=(1-p)^{n+m}=(1-p)^{n}(1-p)^{m}.
	\end{align}
$$
Entonces tenemos que 


8.- Si $X$ y $Y$ son v.a. $\mathrm{Poisson}(\lambda)$ independientes, demuestre que $Z=X+Y\sim \mathrm{Poisson}(2\lambda)$.
**Sol:**
Para interpretar esto, podemos ver a $X$ y $Y$ como el número de ocurrencias de dos eventos (posiblemente el mismo) dentro de un intervalo. Sabemos que en promedio, ambos eventos ocurren $\lambda$ veces en este intervalo. Como las ocurrencias de los eventos son independientes, podemos ver a $Z$ como el número de veces que ocurren ambos eventos, y es intuitivo pensar que el número promedio de veces que ocurren ambos a la vez es $2\lambda$.
Sea $P(Z=z)$ para $z=x+y$, entonces tenemos que $P(Z=z)=P(X=x,Y=y)$. Como las v.a. son independientes, tenemos que $P(X=x,Y=y)=P(X=x)P(Y=y)$, es decir que 
$$
	P(Z=z)=\left( \frac{\lambda^{x}e^{-\lambda}}{x!} \right)()
$$

9- En un libro muy voluminoso, el número de errores por página se puede modelar con una v.a. $\mathrm{Poisson}(\lambda=1)$. Calcule la probabilidad de que en una página cualquiera:
	a) no tenga errores;
	b) tenga al menos un error;
	c) tenga a lo más dos errores.
**Sol:**
Para el primer inciso, únicamente hay que usar la fórmula: 
$$
	P(X=0)=\frac{\lambda^{0}e^{-\lambda}}{0!}=e^{-\lambda}=e^{-1}.
$$
Para el segundo inciso, queremos la probabilidad de al menos un error, es decir $P(X\geq 1)$, o lo que es lo mismo que $1-P(X=0)$, o sea 
$$
	P(X\geq 1)=1-P(X=0)=1-\frac{1}{e}=\frac{e-1}{e}.
$$
Por último, la probabilidad de no tener más de dos errores es $P(X\leq 2)$, que es lo mismo que 
$$
	P(X\leq 2)=\sum_{x=0}^{2}P(X=x)=\sum_{x=0}^{2} \frac{e^{-1}}{x!}.
$$
