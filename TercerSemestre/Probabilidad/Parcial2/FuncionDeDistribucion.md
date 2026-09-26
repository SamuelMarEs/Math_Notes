#Probabilidad 
#### Definición:
Sea $X$ una [[VariablesAleatorias|variable aleatoria]] discreta que toma valores $x_{1},x_{2},\dots$. La función $F:\mathbb{R}\to[0,1]$ dada por 
$$
	F(x)=P(X\leq x)
$$
se conoce como ***función de distribución*** o ***función de probabilidad acumulada***, y se suele denotar como cdf, por sus siglas en inglés (Cumulative Density Function).

###### Ejemplo:
Suponga que $X$ es una variable aleatoria con pdf

| x      | 1   | 2   | 3   | 4   |
| ------ | --- | --- | --- | --- |
| $f(x)$ | 0,1 | 0.2 | 0.3 | 0.4 |
Podemos calcular $F(0.5)=P(X\leq 0.5)=0$, $F(X\leq 2)=0.3$ y $F(X\leq 10)=1$.

#### Proposición:
Toda función de distribución $F$ cumple:
a) $\lim_{ n \to \infty }F(n)=1$
b) $\lim_{ n \to -\infty }F(n)=0$
c) Si $x_{1}\leq x_{2}$, entonces $F(x_{1})\leq F(x_{2})$, es decir, la función es no decreciente.
d) $F(x)=F(x+)$, donde $F(x+)=\lim_{ h \searrow 0 }F(x+h)$. En otras palabras, $F$ es continua por la derecha.
##### Demostración:
a) Sea $x_{1},x_{2},\dots$ una sucesión de número reales tales que $x_{1}\leq x_{2}\leq\dots$ y que la sucesión diverge a infinito.
Definimos los eventos 
$$
	A_{n}=(X\leq x_{n})=\{ w\in \Omega|X(w)\leq x_{n} \}.
$$
Notar que $A_{1}\subset A_{2}\subset\dots$ y $\bigcup_{n=1}^{\infty}A_{n}=\Omega$.
Entonces tenemos que 
$$
	\begin{align}
	1=P(\Omega)=P(\bigcup_{n=1}^{\infty}A_{n})&=P(\lim_{ n \to \infty } A_{n}) \\
	&=\lim_{ n \to \infty } P(A_{n})=\lim_{ n \to \infty } F(x_{n}).
	\end{align}
$$
(El hecho de que la unión converja a $\Omega$ no era necesario, basta con ver que la sucesión converge por si sola a $\Omega$).

b) La demostración es análoga, pero tomando una sucesión decreciente de eventos que converge a $\emptyset$.

c) Si $x_{1}\leq x_{2}$, entonces $(X\leq x_{1})\subset(X\leq x_{2})$, y por lo tanto $P(X\leq x_{1})\leq P(X\leq x_{2})$, es decir que $F(x_{1})\leq F(x_{2})$.

d) Sea $0\leq\dots\leq x_{2}\leq x_{1}$ una sucesión no creciente de reales no negativos que converge a cero. Definamos los eventos 
$$
	A_{n}=(x<X\leq x+x_{n})=\{ w\in \Omega|x<X(w)\leq x+x_{n} \},
$$
y observemos que $P(A_{n})=F(x+x_{n})-F(x)$. Entonces $A_{1}\supset A_{2}\supset\dots \supset A_{n}$, y $\lim_{ n \to \infty }A_{n}=\emptyset$ (pues eventualmente no habrá ningún número $x<X\leq x$). Entonces tenemos que 
$$
	0=P(\emptyset)=P(\lim_{ n \to \infty } A_{n})=\lim_{ n \to \infty } P(A_{n})=\lim_{ n \to \infty } F(x+x_{n})-F(x),
$$
es decir que 
$$
	F(x)=\lim_{ n \to \infty } F(x+x_{n})=\lim_{ h \to 0 } F(x+h).\quad\square
$$

#### Definición:
Cualquier función que cumple las cuatro propiedades anteriores se llama función de distribución, aún si no especificamos ninguna variable aleatoria.

De forma general, sea $f(x)$ la pdf y $F(x)$ la cdf, entonces 
$$
	f(x)=F(x)-F(x-).
$$
($F(x-)$ es el límite por la izquierda).

A continuación se enlistan algunas probabilidades en términos de $F(x)$:
- $P(X<a)=F(a-)$.
- $P(a<X\leq b)=F(b)-F(a)$.
- $P(a\leq X\leq b)=F(b)-F(a-)$.
- $P(a<X<b)=F(b-)-F(a)$.
- $P(a\leq X<b)=F(b-)-F(a-)$.

#### Teorema de Cambio de Variable
Sea $X$ una [[VariablesAleatorias|variable aleatoria]] discreta, y sea $Y=\psi(x)$. Entonces 
$$
	P_{y}(Y= y)=P_{x}[X\in \psi ^{-1}(y)],
$$
donde $\psi ^{-1}(y)$ es la imagen inversa de $y$ bajo la transformación $\psi$, 
$$
	\psi ^{-1}(y)=\{ x|\psi(x)=y \}.
$$
La notación $P_{y}, P_{x}$ indica si la probabilidad se calcula con respecto a $Y$ o $X$.
##### Demostración:
Por definición de $Y$, tenemos que 
$$
	\begin{align}
	P_{y}(Y=y)=P_{y}(\psi(X)=y)=P_{x}(\{ x|\psi(x)=y \})=P_{x}(X\in \psi ^{-1}(y))
	\end{align}.\quad\square
$$
Es decir que $Y$ toma el valor $y$ si y sólo si $X$ toma algún valor en $\psi ^{-1}(y)$.
###### Ejemplo:
Si $X$ es una variable aleatoria con pdf 

| x      | -1  | 0   | 1   |
| ------ | --- | --- | --- |
| $f(x)$ | 1/3 | 1/3 | 1/3 |
Sea $Y=X^{2}$, entonces tenemos que $Y\in \{ 0,1 \}$. Entonces 
$$
	P(Y=0)=P(X=0)=\frac{1}{3}
$$
y 
$$
	P(Y=1)=P(X=1\text{ o }X=-1)=P(X=1)+P(X=-1)=\frac{2}{3}.
$$
