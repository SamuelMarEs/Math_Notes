#Probabilidad 
#### Definición:
Sea $X$ una [[VariablesAleatorias|variable aleatoria]] discreta. Sea $f$ una funión que va de los reales al intervalo $[0,1]$ tal que 
$$
	f(x)=P(X=x).
$$
A $f$ se le conoce como ***función de probabilidad/función de masa/función de densidad de probabilidad***. (En general, el término función de densidad se usa para variables aleatorias continuas, por lo tanto es recomendable usar los términos función de probabilidad o función de masa).
Esta función debe cumplir las siguientes dos propiedades: 
- $\sum_{x}f(x)=\sum_{x}P(X=x)=1$.
- $f(x)\geq 0\quad\forall x$.

Notese que la función de probabilidad existe sin necesidad de definir un espacio de probabilidad específico.

###### Ejemplo:
Sea $X$ una variable aleatoria discreta que tome valores en $\{ 0,1,2,3 \}$ y con función de probabilidad 

| x      | 0   | 1   | 2   | 3   |
| ------ | --- | --- | --- | --- |
| $f(x)$ | 0.1 | 0.3 | 0.4 | 0.2 |

Hay varias formas de representar una función de probabilidad: una tabla, una gráfica, o una ecuación.

###### Ejemplo:
Sea $X$ una variable aleatoria con función de probabilidad dada por 
$$
	f(x)=\begin{cases}
	\frac{10e^{-10x}}{x!}, & x=0,1,2,\dots \\
	0, & \text{otro caso}.
	\end{cases}
$$
Se puede demostrar que 
$$
	\sum_{x=0}^{\infty} \frac{10^{x}e^{-10}}{x!}=1
$$
(Este es un tipo de variable aleatoria que se conoce como variable aleatoria Poisson con parámetro $\lambda=10$).

###### Ejemplo:
Sea $X$ una variable aleatoria que toma valores en el conjunto $\{ 0,1,2,\dots,10 \}$, y sea su función de probabilidad 
$$
	f(x)=\begin{cases}
	cx, & x=0,1,\dots,10 \\
	0, & \text{en otro caso.}
	\end{cases}
$$
¿Cuál es el valor de $c$ tal que $f(x)$ es función de probabilidad?
**Sol:**
Queremos confirmar las dos condiciones 
$$
	\sum_{x}f(x)=1\quad\text{y}\quad f(x)\geq 0.
$$
Para que se cumpla la segunda condición, necesitamos necesariamente que $c>0$. Para la primera, tenemos que 
$$
	\sum_{x=0}^{10}cx=c \frac{10(11)}{2}=c55=1\implies c=\frac{1}{55}.
$$
En general, todas las funciones de probabilidad pueden escribirse de la siguiente forma: 
$$
	f(x)=ck(x),
$$
donde $c$ es una *constante de normalización* y $k(x)$ se conoce como el *kernel* de la función.

###### Ejemplo
Ya que conocemos la función de probabilidad (pdf por sus siglas en inglés Probability Density Function), podemos usarla para calcular diferentes probabilidades.
Dada la siguiente pdf: 

| x      | 0    | 1    | 2    | 3   | 4   | 5   |
| ------ | ---- | ---- | ---- | --- | --- | --- |
| $f(x)$ | 0.01 | 0.07 | 0.12 | 0.4 | 0.2 | 0.2 |
Podemos calcular de forma directa $P(X=3)=0.4$, o $P(X=10)=0$. También podríamos querer calcular algo de la forma
$P(X\leq 4)=P(X=0)+P(X=1)+\dots+P(X=4)=0.8$, o alternativamente 
$P(X>3)=P(X=4)+P(X=5)=0.4$, y también $P(-1\leq X\leq 2)=P(X=0)+P(X=1)+P(X=2)=0.2$.

###### Ejemplo
Supongamos que tenemos un examen de opción múltiple contestado al azar, con 10 preguntas, cada una de 4 opciones.
¿Cuál es la probabilidad de aprobar?
Podemos definir nuestra variable aleatoria como $X=$ # de aciertos de 10, que es lo mismo que $X=\{ 0,1,\dots,10 \}$, y entonces tenemos que la probabilidad de aprobar es
$$
	P(X\geq 6)=\sum_{x=6}^{10}\begin{pmatrix}
	10 \\
	x
	\end{pmatrix}\left( \frac{1}{4} \right)^{x}\left( \frac{3}{4} \right)^{10-x}.
$$
En este caso tenemos que $X\sim\text{Binomial}(n=10,p=0.25)$, aunque eso se verá más a fondo después. (Distribución binomial).

##### Ejercicios
Determina si las siguientes son funciones de probabilidad.
1.- Sea $f(x)=\begin{cases} \frac{x-1}{2^{x}}, & x=1,2,\dots \\  0,&\text{en otro caso}\end{cases}$. 
**Sol:**
Para $x\geq 1$, tenemos que $x-1\geq 0$. Además $2^{x}>0$ para toda $x$, por lo tanto $f(x)\geq 0$ para toda $x$. Tomemos 
$$
	\sum_{x=1}^{\infty} \frac{x-1}{2^{x}}.
$$
Realicemos un cambio de variable $n=x-1$, de modo que tenemos 
$$
	\sum_{n=0}^{\infty} \frac{n}{2^{n+1}}=\frac{1}{2}\sum_{n=0}^{\infty} \frac{n}{2^{n}}.
$$
Esta es una serie geométrica ligeramente modificada, que converge a 
$$
	\sum_{n=0}^{\infty} \frac{n}{2^{n}}=\frac{1 / 2}{(1- 1 / 2)^{2}}=2,
$$
por lo tanto 
$$
	\sum_{x=1}^{\infty} \frac{x-1}{2^{x}}=\frac{1}{2}2=1.
$$


2.- Sea $f(x)=\begin{cases} \frac{p^{x-1}(1-p)}{1-p^{n}}, & x=1,\dots,n,\quad p\in(0,1) \\  0, & \text{en otro caso}\end{cases}$.
**Sol:**
Como $0<p<1$, entonces tenemos que $p^{x-1}>0,1-p>0$ y $1-p^{n}>0$ para $n\neq 0$. Por lo tanto $f(x)\geq 0$ para toda $x$.
Ahora, tomemos 
$$
	\sum_{x=1}^{n} \frac{p^{x-1}(1-p)}{1-p^{n}}.
$$
Observemos que los términos $(1-p) / (1-p^{n})$ no dependen de $x$, entonces realmente queremos calcular 
$$
	\sum_{x=1}^{n}p^{x-1}=\sum_{x=0}^{n-1}p^{x}=\frac{1-p^{n}}{1-p},
$$
por lo tanto 
$$
	\sum_{x=1}^{n} \frac{p^{x-1}(1-p)}{1-p^{n}}=\frac{1-p}{1-p^{n}} \frac{1-p^{n}}{1-p}=1.
$$
