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
c) Si $x_{1}\leq x_{2}$, entonces $F(x_{1})\leq F(x_{2})$, es decir, la función es decreciente.
d) $F(x)=F(x+)$, donde $F(x+)=\lim_{ h \searrow 0 }F(x+h)$. En otras palabras, $F$ es continua por la derecha.
##### Demostración:
a) Sea $x_{1},x_{2},\dots$ una sucesión de número reales tales que $x_{1}\leq x_{2}\leq\dots$ y que la sucesión tiende a infinito..
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

b) La demostración es análoga, pero tomando una sucesión decreciente.

c)

d)

#### Definición:
Cualquier función que cumple las cuatro propiedades anteriores se llama función de distribución, aún si no especificamos ninguna variable aleatoria.

De forma general, sea $f(x)$ la pdf y $F(x)$ la cdf, entonces 
$$
	f(x)=F(x)-F(x-).
$$
($F(x-)$ es el límite por la izquierda.)

#### Teorema de Cambio de Variable
Sea $X$ una [[VariablesAleatorias|variable aleatoria]] discreta, y sea $Y=\psi(x)$. Entonces 
$$
	P_{y}(Y\leq y)=P_{x}[X\in \psi ^{-1}(y)],
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
