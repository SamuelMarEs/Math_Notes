160.- Suponga que un experimento aleatorio consiste en escoger un número al azar dentro del intervalo $(0,1)$. Cada resultado $w$ del experimento se expresa en su expansión decimal 
$$
	w=0.a_{1}a_{2}\dots
$$
en donde $a_{i}\in \{ 0,1,\dots,9 \}, i=1,2,\dots$ Para cada una de las siguientes variables aleatorias determine si ésta es discreta o continua, y establezca el conjunto de valores que puede tomar.

a) $X(w)=1-w$.
**Sol:**
Sea $w\in(0,1)$, tenemos que $0<w<1$, y por lo tanto tenemos que $0<1-w<1$, es decir $X(w)\in(0,1)$. Sabemos que este intervalo no es numerable, por lo tanto $X$ es una v.a. continua.

b) $X(w)=a_{1}$.
**Sol:**
Sabemos que $a_{1}\in \{ 0,1,\dots,9 \}$, por lo tanto $X(w)\in \{ 0,1,\dots,9 \}$, y tenemos que $X$ es una v.a. continua.

c) $X(w)=0.0a_{1}a_{2}a_{3}\dots$
**Sol:**
Básicamente estamos mandando $X(w)=w\cdot 10^{-1}$, entonces $X(w)\in\left( 0, 1 / 10 \right)$, y por la misma razón que el inciso a), $X$ es una v.a. continua.

d) $X(w)=\lfloor 100w \rfloor.$
**Sol:**
Sea $w=0.a_{1}a_{2}a_{3},\dots$, entonces $X(w)=a_{1}a_{2}\in[0,99]$, pero más importante $X$ solo va a tomar valores enteros, i.e. $X(w)\in \{ 0,1,\dots,99 \}$, por lo tanto es una v.a. discreta.

e) $X(w) = a_{1}+a_{2}$.
**Sol:**
Dado que $a_{1},a_{2}\in \{ 0,1,\dots,9 \}$, tenemos que el valor mínimo que puede tomar $X$ es $X(0.00a_{3}a_{4}\dots)=0+0=0$, mientras que el máximo que puede tomar es $X(0.99a_{3}a_{4}\dots)=9+9=18$. Por lo tanto tenemos que $X(w)\in \{ 0,1,\dots,18 \}$, es decir que es una v.a. discreta.

f) $X(w)=a_{1}\cdot a_{2}.$
**Sol:**
Dado que $a_{1},a_{2}\in \{ 0,1,\dots,9 \}$, tenemos que el valor mínimo que puede tomar $X$ es si $a_{1}=0$ o $a_{2}=0$ en cuyo caso $X(w)=0$. Por otro lado, el valor máximo vuelve a ocurrir en el caso $a_{1}=9=a_{2}$, para el cual $X(w)=9^{2}=81$, es decir que $X(w)\in \{ 0,1,\dots,81 \}$, y por lo tanto $X$ es una v.a. discreta.


164.- **Función indicadora.** Sea $(\Omega,\mathcal{F},P)$ un espacio de probabilidad y sea $A$ un evento. Defina la variable aleatoria $X$ como aquella que toma el valor 1 si $A$ ocurre y toma el valor $0$ si $A$ no ocurre. Es decir 
$$
	X(w)=\begin{cases}
	1 & \text{si }w\in A, \\
	0 & \text{si }w\notin A.
	\end{cases}
$$
Demuestre que $X$ es, efectivamente, una variable aleatoria. A esta variable se le llama función indicadora del evento $A$ y se denota también por $1_{A}(w)$.
**Sol:**
De inicio es evidente que $X:\Omega\to \{ 0,1 \}$, es decir que cumple ser una función del espacio muestral en los reales.
Sea $x\in\mathbb{R}$, queremos demostrar que $\{ w\in \Omega|X(w)\leq x \}\in\mathcal{F}$. Hagamos esto por casos:
- Caso $x\geq 1$. Tenemos que 
  $$
  	\{ w\in \Omega|X(w)\leq x \}=\{ w\in \Omega|X(w)\leq 1 \}=\Omega.
  $$
  Dado que $\mathcal{F}$ es una sigma álgebra sobre $\Omega$, entonces $\Omega\in\mathcal{F}$.
- Caso $0\leq x<1$. Para este caso basta tomar el conjunto de la forma $$\{ w\in \Omega|X(w)\leq x \}=\{ w\in \Omega|X(w)\leq 0 \}=\{ w\in \Omega|w\not\in A \}=A^{c}. $$
  Como $A$ es un evento, tenemos que $A\in\mathcal{F}$, y al ser una sigma álgebra, es cerrada bajo complementos, por lo tanto $A^{c}\in\mathcal{F}$.
- Caso $x<0$. Para este caso, tenemos que 
  $$
  	\{ w\in \Omega|X(w)\leq x<0 \}=\emptyset\in\mathcal{F},
  $$
  ya que $X$ no toma valores negativos. Como $\mathcal{F}$ es una sigma álgebra, se cumple que $\emptyset\in\mathcal{F}$.


168.- En cada caso encuentre el valor de la constante $c$ que hace a la función $f(x)$ una función de probabilidad. Suponga que $n$ es un entero positivo fijo.
b) $f(x)=\begin{cases}cx^{2} & \text{si }x=1,2,\dots,n \\  0 & \text{en otro caso.}\end{cases}$
**Sol:**
Para que $f(x)$ sea una función de probabilidad, necesitamos que 
$$
	\sum_{x=1}^{n}cx^{2}=1\implies c\left( \frac{n(n+1)(2n+1)}{6} \right)=1,
$$
es decir que la constante que satisface que $f$ sea función de probabilidad es 
$$
	c=\frac{6}{n(n+1)(2n+1)}.
$$

d) $f(x)=\begin{cases}c / 2^{x} & \text{si }x=1,2,\dots \\  0 & \text{en otro caso.}\end{cases}$
**Sol:**
Para que $f$ sea función de probabilidad, se necesita 
$$
	\sum_{x=1}^{\infty}c\left( \frac{1}{2} \right)^{x}=1.
$$
La suma que tenemos es una suma geométrica que converge a 
$$
	\sum_{x=1}^{\infty}c\left( \frac{1}{2} \right)^{x}=\frac{c}{1-1 /2}-c=c(2-1)=c,
$$
es decir que la constante que satisface la ecuación es $c=1.$


e) $f(x)=\begin{cases}c /3^{x} & \text{si }x=1,3,5,\dots \\  c / 4^{x} & \text{si }x=2,4,6,\dots \\  0 & \text{en otro caso.}\end{cases}$
**Sol:**
Para que $f$ sea función de probabilidad, necesitamos que se cumpla lo siguiente:
$$
	\sum_{x=1}^{\infty}f(x)=\sum_{x=0}^{\infty}c \left( \frac{1}{3} \right)^{2x+1}+\sum_{x=1}^{\infty}c\left( \frac{1}{4} \right)^{2x}.
$$
Fijémonos primero en la suma de exponentes impares: 
$$
	\sum_{x=0}^{\infty}c\left( \left( \frac{1}{3} \right)^{2} \right)^{x}\left( \frac{1}{3} \right)=\frac{c}{3}\sum_{x=0}^{\infty}\left( \frac{1}{9} \right)^{x}=\frac{c / 3}{1- 1/9}=c \frac{3}{8}.
$$
Ahora, de forma análoga encontramos la seria de la derecha para exponentes pares: 
$$
	\sum_{x=1}^{\infty}c\left( \frac{1}{4} \right)2x=c\sum_{x=1}^{\infty}\left( \frac{1}{16} \right)^{x}= \frac{c}{1-1 / 16}-c=c\left( \frac{16}{15} -1\right)=\frac{c}{15}.
$$
Entonces tenemos que 
$$
	\sum_{x=1}^{\infty}f(x)=1\Longleftrightarrow c\left( \frac{3}{8}+ \frac{1}{15} \right)=1,
$$
entonces tenemos que 
$$
	c=\frac{53}{120}.
$$


170.- Sea $X$ una variable aleatoria discreta con función de probabilidad como se indica en la siguiente tabla: 

| x    | -2  | -1  | 0   | 1   | 2   |
| ---- | --- | --- | --- | --- | --- |
| f(x) | 1/8 | 1/8 | 1/2 | 1/8 | 1/8 |
Grafique la función $f(x)$ y calcule las siguientes probabilidades.
a) $P(X\leq 1)=1-P(X>1)=1-P(X=2)=7 / 8$.
b) $P(|X|\leq 1)=P(-1\leq X\leq 1)=P(X=-1)+P(X=0)+P(X=1)=1 / 8+1 / 2 + 1 / 8=3 / 4.$
c) $P(-1<X\leq 2)=P(X=0)+P(X=1)+P(X=2)=1 / 2+ 1/8+ 1 / 8=3 / 4.$
d) $P(X^{2}\geq 1)=1-P(X^{2} = 0)=1-P(X=0)=1-1 / 2=1 / 2.$
e) $P(|X-1|<2)=P(-2<X-1<2)=P(-1<X<3)=P(-1<X\leq 2)=3 / 4$.
f) $P(X-X^{2}<0)=P(X<X^{2})=P(X=-2)+P(X=2)=1 / 8+ 1 / 8= 1 / 4.$


174.- Sean $f(x)$ y $g(x)$ dos funciones de probabilidad. Demuestre o proporcione un contra ejemplo, en cada caso, para la afirmación que establece que la siguiente función es de probabilidad.
a) $f(x)+g(x)$.
**Sol:**
Sea $X\in \{ 0,1 \}$ con $f(0)=f(1)=1 / 2$, y $g=f$ una función de probabilidad, entonces tenemos que $f(x)+g(x)=2f(x)$. Entonces 
$$
	2f(0)+2f(1)=1+1=2,
$$
por lo tanto no es función de probabilidad.

c) $\lambda f(x)+(1-\lambda)g(x)$ con $0\leq \lambda\leq 1$ constante.
**Sol:**
Vamos a mostrar que en efecto $\lambda f(x)+(1-\lambda)g(x)$ es una función de probabilidad.
$$
	\sum_{x}\lambda f(x)+(1-\lambda)g(x)=\lambda \sum_{x}f(x)+(1-\lambda)\sum_{x}g(x)=\lambda+1-\lambda=1.\quad\square
$$

e) $f(c-x)$ con $c$ constante.
**Sol:**


f) $\max\{ f(x),g(x) \}$.
**Sol:**
Definamos $f,g$ como 

| x    | 0     | 1     | 2   |
| ---- | ----- | ----- | --- |
| f(x) | 1 / 2 | 1 / 2 | 0   |
| g(x) | 0     | 0     | 1   |
Entonces tenemos que 
$$
	\sum_{x=0}^{2}\max\{ f(x),g(x) \}=\frac{1}{2}+\frac{1}{2}+1=2,
$$
por lo tanto no es función de probabilidad.


180.- Se lanza un dado equilibrado hasta que aparece un "6". Encuentre la función de probabilidad del número de lanzamientos necesarios hasta obtener tal resultado.
**Sol:**
Como el dado es equilibrado, tenemos que la probabilidad de sacar un "6" al lanzarlo una vez es $1 / 6$. Sea $X(w)=1,2,\dots$ el número de lanzamientos necesarios hasta obtener el resultado. Entonces tenemos que 
$$
	f(n)=P(X=n)=\left( \frac{5}{6} \right)^{n-1}\left( \frac{1}{6} \right).
$$
Esta es la probabilidad de que no salga el 6 $n-1$ veces seguidas, por la probabilidad de que salga un 6 en el $n$-esimo intento.
Observemos que 
$$
	\sum_{n=1}^{\infty}\left( \frac{5}{6} \right)^{n-1}\left( \frac{1}{6} \right)=\left( \frac{1}{6} \right)\sum_{n=0}^{\infty}\left( \frac{5}{6} \right)^{n}=\left( \frac{1}{6} \right) \frac{1}{1-5 / 6}=1,
$$
por lo tanto $f$ si es una función de probabilidad.


191.- Suponga que la variable aleatoria discreta $X$ tiene la siguiente función de distribución. 
$$
	F(x)=\begin{cases}
	0 & \text{si }x<-1, \\
	1 / 4 & \text{si }-1\leq x < 1, \\
	1 / 2 & \text{si }1\leq x <3, \\
	3 / 4 & \text{si }3\leq x<5, \\
	1 & \text{si }x\geq 5.
	\end{cases}
$$
Grafique $F(x)$, obtenga y grafique la correspondiente función de probabilidad $f(x)$ y calcule las siguientes probabilidades.
a) $P(X\leq 3)$
b) $P(X=3)$
c) $P(X<3)$
d) $P(X\geq 1)$
e) $P(-1 / 2<X<4)$
f) $P(X=5)$


192.- Muestre que la siguiente función es de probabilidad y encuentra la correspondiente función de distribución. Grafique ambas funciones. 
$$
	f(x)=\begin{cases}
	(1/2)^{x} & \text{si }x=1,2,\dots \\
	0 & \text{en otro caso.}
	\end{cases}
$$
**Sol:**
Veamos primero que $f$ es una función de probabilidad: 
$$
	\sum_{x=1}^{\infty}\left( \frac{1}{2} \right)^{x}=\frac{1}{1-1 / 2}-1=1.
$$
La función de distribución $F$ va a estar dada de la siguiente forma: 
$$
	F(x)=P(X\leq x)=\sum_{n\leq x}f(x).
$$
Supongamos $x\in \{ 1,2,\dots \}$, entonces tenemos que 
$$
	F(x)=\sum_{n=1}^{x}\left( \frac{1}{2} \right)^{n}=\frac{1-(1 / 2)^{x+1}}{1-(1 / 2)}-1=1-\left( \frac{1}{2} \right)^{x}.
$$
Por lo tanto, la función de distribución es
$$
	F(x)=\begin{cases}
	1-\left( \frac{1}{2} \right)^{x}, & \text{si }x\geq 1 \\
	0, & \text{en otro caso}
	\end{cases}.
$$


194.- Grafique la siguiente función y compruebe que es una función de distribución. Determine si se trata de la función de distribución de una variable aleatoria discreta o continua. Encuentre además la correspondiente función de probabilidad o de densidad. 
$$
	F(x)=\begin{cases}
	0 & \text{si }x<0, \\
	1 / 5 & \text{si }0\leq x<1, \\
	3 / 5 & \text{si }1\leq x<2, \\
	1 & \text{si }x\geq 2.
	\end{cases}
$$


207.- Una moneda equilibrada y marcada con "Cara" y "Cruz" se lanza repetidas veces hasta obtener el resultado "Cruz". Defina la variable aleatoria $X$ como el número de lanzamientos necesarios hasta obtener el resultado de interés. Encuentre la función de distribución de $X$.