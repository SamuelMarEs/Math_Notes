#Probabilidad 
1.- Cuando se rueda un comercial de televisión, la probabilidad de que un actor diga sus lineas bien en una toma es de 0.4.
	a) ¿Cuál es la probabilidad de que el actor diga bien sus líneas por primera vez en la cuarta toma?
	b) ¿Cuál es el número esperado de tomas necesarias para filmar el comercial correctamente?
**Sol:**
Sea $X$ la v.a. que indica el número de tomas hasta tener una toma bien. Entonces tenemos que $X\sim \mathrm{Geom}(p=0.4)$, y entonces para el inciso a), la probabilidad es de 
$$
	P(X=4)=(1-0.4)^{4}(0.4).
$$
Para calcular el valor esperado, dado que $X$ es una v.a. geométrica, entonces 
$$
	E(X)=\frac{1-p}{p}=\frac{0.6}{0.4}=\frac{3}{2}.
$$
Es decir, se espera que tome 1.5 tomas filmar correctamente el comercial (i.e. al menos dos tomas).


2.- En la inspección de piezas de hojalata producidas por un proceso electrolítico se identifican 0.5 imperfecciones en promedio por minuto. Determine la probabilidad de identificar, por lo menos, 2 imperfecciones en 5 minutos.
**Sol:**
Sea $X$ la v.a. que mide el número de imperfecciones en un intervalo de 5 minutos. Suponiendo que el promedio de imperfecciones de cada minuto es independiente, y que se mantiene constante, entonces el número de imperfecciones en un intervalo de 5 minutos es de 
$\lambda=5\left( \frac{1}{2} \right)=\frac{5}{2}$. Tenemos entonces que $X\sim \mathrm{Poisson}\left( \lambda=\frac{5}{2} \right)$. Dado que queremos calcular la probabilidad de que haya al menos 2 imperfecciones, tenemos entonces que lo que queremos calcular es 
$$
	P(X\geq 2)=1-P(X\leq 2)=1-P(X=0)-P(X=1)=1-e^{-5 / 3}-\frac{5}{3}e^{-5/3}.
$$


3.- Un paquete contiene 10 tarjetas de memoria RAM y dos son defectuosas. Si en el área de calidad se revisan 4 tarjetas del paquete:
	a) ¿Cuál es la probabilidad de que haya, a lo más, 1 tarjeta defectuosa en la muestra?
	b) ¿Cuál es la probabilidad de que haya 3 tarjetas defectuosas?
**Sol:**
Sea $X=$ número de tarjetas defectuosas en una muestra de tamaño 4. La probabilidad de que, al tomar una sola tarjeta del paquete, esta sea defectuosa, es $4 / 10=2 /5$. 
Entonces tenemos que $X\sim\text{Binom}(4, 2 / 5)$.
Para el inciso a), queremos calcular 
$$
	P(X\leq 1)=P(X=0)+P(X=1)={4\choose 0}\left( \frac{2}{5} \right)^{0}\left( \frac{3}{5} \right)^{4}+{4\choose 1}\left( \frac{2}{5} \right)^{1}\left( \frac{3}{5} \right)^{3}=\left( \frac{3}{5} \right)^{3}\left( \frac{11}{5} \right).
$$
Para el inciso b), lo que queremos calcular es 
$$
	P(X=3)={4\choose 3}\left( \frac{2}{5} \right)^{3}\left( \frac{3}{5} \right)^{1}.
$$


4.- Sea $Z$ una v.a. con $E(Z)=0$ y $\mathrm{Var}(Z)=1$. Sea $X=Z+1$ y $Y=Z-1$. Demuestra que 
$E(XY)=0$.
**Sol:**
Sabemos que 
$$
	E(XY)=E((Z+1)(Z-1))=E(Z^{2}-1)=E(Z^{2})+E(-1)=E(Z^{2})-1.
$$
Si recordamos que $\mathrm{Var}(Z)=E(Z^{2})-[E(Z)]^{2}$, y notamos que $\mathrm{Var}(Z)=1$ y $E(Z)=0$, tenemos entonces que 
$$
	1=E(Z^{2})-0^{2}\implies E(Z^{2})=1,
$$
y por lo tanto tenemos que 
$$
	E(XY)=E(Z^{2})-1=1-1=0.\quad\square
$$


5.- Sea $X$ una v.a. con pdf 

| x    | -3   | -2   | -1   | 0    | 1    | 2    | 3    |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| f(x) | 1/16 | 2/16 | 3/16 | 4/16 | 3/16 | 2/16 | 1/16 |
a) Graficar $f(x)$.
b) Encontrar $F(x)$.
c) Calcular $E(X)$.
d) Encontrar la distribución de $Y=\lvert X \rvert \text{mod}2$.
e) Calcular los cuartiles de $X$.
f) Calcular $P(X>-2)$, $P(0.3<X\leq 1)$, y $P(X>10)$.
**Sol:**
a) 
b) La cdf se puede representar de la siguiente forma: 
$$
	F(X)=\begin{cases}
	0, & x<-3\\
	\frac{1}{16}, & -3\leq x<-2 \\
	\frac{3}{16}, & -2\leq x<-1 \\
	\frac{6}{16}, & -1\leq x<0 \\
	\frac{10}{16}, & 0\leq x<1 \\
	\frac{13}{16}, & 1\leq x<2 \\
	\frac{15}{16}, & 2\leq x<3 \\
	\frac{15}{16}, & x\geq 3.
	\end{cases}
$$
c)  El valor esperado va a estar dado por 
$$
	\begin{align}
	E(X)=\sum_{x=-3}^{3}xf(x)=\sum_{x=-3}^{-1}xf(x)+\sum_{x=1}^{3}xf(x).
	\end{align}
$$
Podemos ver en la tabla que la pdf es simétrica, y por lo tanto podemos reescribir la primera suma como 
$$
	\sum_{x=-3}^{-1}xf(x)=\sum_{x=1}^{3}-xf(x),
$$
de modo que tenemos que 
$$
	E(X)=\sum_{x=1}^{3}xf(x)-\sum_{x=1}^{3}xf(x)=0.
$$
d) Dado que $X\in \{ -3,-2,-1,0,1,2,3 \}$, tenemos que $\lvert X \rvert\in \{ 0,1,2,3 \}$, y además tenemos que 
$Y=\lvert X \rvert\text{mod}2\in \{ 0,1 \}$. Para encontrar la función de probabilidad de $Y$, basta encontrar $P(Y=0)$ y $P(Y=1)$. Para la primera, observemos que 
$$
	Y=0\iff \lvert X \rvert =0,2\iff X=-2,0,2,
$$
por lo tanto tenemos que 
$$
	P(Y=0)=P(X=0)+P(X=-2)+P(X=-2)=\frac{8}{16}=\frac{1}{2}.
$$
Una vez que tenemos esta probabilidad, es sencillo ver que 
$$
	P(Y=1)=1-P(Y=0)=1-\frac{1}{2}=\frac{1}{2}.
$$
Por lo tanto 
$$
	f(y)=\frac{1}{2},\quad y=0,1.
$$
e) 



6.- La función generadora de probabilidad (fgp) se define como $G(t)=E(t^{x})$. Encuentra la fgp de las distribuciones Bernoulli y Geométrica.
**Sol:**
Sea $X\sim \mathrm{Bernoulli}(p)$, tenemos entonces que 
$$
	P(X=x)=p^{x}(1-p)^{1-x},\quad x= 0,1.
$$
Por lo tanto, tenemos que 
$$
	G(t)=E(t^{x})=\sum_{x}t^{x}p^{x}(1-p)^{1-x}=t^{0}p^{0}(1-p)^{1}+t^{1}p^{1}(1-p)^{0}=(1-p)+tp.
$$
Ahora, sea $Y\sim \mathrm{Geom}(p)$, tenemos que 
$$
	P(Y=y)=(1-p)^{y}p,\quad y=0,1,\dots
$$
Por lo tanto, podemos calcular la fgp como 
$$
	G(t)=E(t^{y})=\sum_{y=0}^{\infty}t^{y}(1-p)^{y}p=p\sum_{y=0}^{\infty}(t-tp)^{y}.
$$
Esta es una serie geométrica que converge si y sólo si $|t-tp|<1$ (notar que $t-tp\geq 0$ para toda $t$). Dado que el producto de dos número es menor a 1 (absolutamente) si y solo si ambos son menores a 1, entonces tenemos que la serie converge si $|t|\leq1$. Suponiendo que converge, tenemos que 
$$
	G(t)=p\sum_{y=0}^{\infty}(t-tp)^{y}=\frac{p}{1-t+tp}.
$$


7.- La función generadora de momentos (fgm) se define como $M(t)=E(e^{tx})$. Encuentra la fgm de la distribución Poisson.
**Sol:**
Sea $X\sim \mathrm{Poisson}(\lambda)$, entonces tenemos que 
$$
	P(X=x)=\frac{\lambda^{x}e^{-\lambda}}{x!},\quad x=0,1,\dots
$$
y por lo tanto tenemos que 
$$
	M(t)=E(e^{tx})=\sum_{x=0}^{\infty}e^{tx} \frac{\lambda^{x}e^{-\lambda}}{x!}=e^{-\lambda}\sum_{x=0}^{\infty} \frac{(e^{t}\lambda)^{x}}{x!}.
$$
Resulta que esta serie es la serie de Taylor para la función $e^{k}$ con $k=e^{t}\lambda$, es decir que la función generadora de momentos queda como 
$$
	M(t)=e^{-\lambda}e^{e^{t}\lambda}=e^{\lambda(e^{t}-1)}.
$$


8.- De acuerdo a la revista Chemical Engineering Progress, aproximadamente el 30% de las fallas de operación en las tuberías de plantas químicas son ocasionadas por errores del operador. De las siguientes 10 fallas:
	a) ¿cuál es la probabilidad de que no más de 2 se deban a un error del operador?
	b) ¿cuál es la probabilidad de que al menos 3 se deban a un error del operador?
	c) ¿cuál es el número esperado de fallas ocasionadas por el operador?
**Sol:**
Sea $X=$ el número de fallas ocasionadas por un error del operador. Sabemos que la probabilidad de que únicamente una falla sea por error del operador es de $p=1 / 3$. Dado que tenemos una muestra de 10 fallas, se tiene que $X\sim \mathrm{Binom}(10, 1 / 3)$.
a) Queremos calcular $P(X\leq 2)$, es decir 
$$
	P(X\leq 2)=\sum_{x=0}^{2}{10\choose x}\left( \frac{1}{3} \right)^{x}\left( \frac{2}{3} \right)^{10-x}.
$$
b) Ahora, lo que queremos es $P(X\geq 3)$, que es lo mismo que $1-P(X\leq 2)$, es decir que 
$$
	P(X\geq 3)= 1-\sum_{x=0}^{2}{10\choose x}\left( \frac{1}{3} \right)^{x}\left( \frac{2}{3} \right)^{10-x}.
$$
c) Por último, sabemos que el valor esperado de una v.a. Binomial es $E(X)=np$, es decir que en este caso, el número esperado de fallas ocasionadas por el operador es 
$$
	E(X)=10(1 / 3)=\frac{10}{3}=3.333\bar{3},
$$
es decir que se espera que alrededor de 3 fallas sean ocasionadas por el operador.


9.- Si dos portadores del gen del albinismo se casan, existe una probabilidad de 0.1 de que los hijos hereden el gen. Si la pareja tiene 5 hijos, calcular:
	a) la probabilidad de que al menos 1 tenga el gen;
	b) la probabilidad de que exactamente 2 tengan el gen;
	c) el número esperado de hijos con el gen del albinismo.
**Sol:**
Sea $X=$ número de hijos con albinismo de los 5 hijos. Dado que sabemos que la probabilidad de que un hijo tenga albinismo es $p=0.1$, tenemos que $X\sim \mathrm{Binom}(5, 0.1)$.
a) Queremos la probabilidad de que al menos 1 tenga el gen, es decir $P(X\geq 1)$, lo cual es 
$$
	P(X\geq 1)=1-P(X=0)=1-{5\choose 0}(0.1)^{0}(0.9)^{5}=1-(0.9)^{5}.
$$
b) La probabilidad de que exactamente 2 tengan el gen está dada por 
$$
	P(X=2)={5\choose 2}(0.1)^{2}(0.9)^{3}.
$$
c) El valor esperado de una v.a. Binomial es $E(X)=np$, por lo tanto, el número esperado de hijos con el gen de albinismo es 
$$
	E(X)=(5)(0.1)=\frac{5}{10}=\frac{1}{2},
$$
es decir que en promedio se espera que ninguno de los hijos tenga albinismo.


10.- En una población grande, se sabe que el 12% de la población tiene una enfermedad congénita. Para detectar a las personas enfermas en un grupo de 100, se hace una prueba de sangre. Para reducir costos, se crean 10 grupos de 10 muestras de sangre y se combinan para hacer la prueba sobre la muestra combinada. Si la muestra es positiva, se aplican pruebas individuales a cada persona de la muestra. 
¿Cuál es el número esperado de pruebas que se realizaran en total con este esquema?
**Sol:**
La probabilidad de que una persona de la población tenga la enfermedad es $p=0.12$.
