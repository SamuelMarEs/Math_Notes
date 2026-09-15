#AlgebraLineal

¿Existe alguna [[BasesOrdenadas|base ordenada]] $\beta$ de un [[EspaciosVectoriales|espacio vectorial]] $V$ tal que $[T]_{\beta}$ es una matriz diagonal?
Si la base existe, ¿cómo podemos encontrarla?

##### Definición:
Un operador $T$ en un espacio vectorial $V$ de dimensión finita se llama ***diagonalizable*** si existe una base ordenada $\beta$ tal que $[T]_{\beta}$ es una matriz diagonal. Lo mismo si tenemos una matriz $A$.

##### Definición:
Sea $T$ un operador lineal en un espacio vectoril $V$ diferente de cero. Un vector diferente de cero $v\in V$ es llamado ***eigenvector*** de $T$ si existe un escalar $\lambda$ tal que $T(v)=\lambda v$.
El escalar $\lambda$ se llama el ***eigenvalor*** asociado al eigenvector $v$. De la misma forma se define para matrices.

***Nota:*** otros nombres que reciben son vector principal, vector característico, vector propio. Igualmente para valor principal, propio y característico.

#### Teorema 5.1
Un operador lineal $T$ sobre un espacio vectorial de dimensión finita $V$ es diagonalizable si y sólo si existe una base ordenada $\beta$ tal que esta formada por eigenvectores.
##### Demostración:
$\Rightarrow$ Supongamos que tenemos una base $\beta=\{ v_{1},\dots,v_{n} \}$ una base ordenada tal que $[T]_{\beta}$ es diagonal. 
$$
	D=[T]_{\beta}=\begin{pmatrix}
	D_{11} & 0 & \dots & 0 \\
	0 & D_{22} & \dots & 0 \\
	\vdots &  &  & \vdots \\
	0 & 0 & \dots & D_{nn}
	\end{pmatrix}.
$$
Para cualquier vector $v_{i}\in \beta$ tenemos que 
$$
	T(v_{i})=\sum_{i=1}^{n}D_{ij}v_{i}=D_{jj}v_{j}=\lambda_{j}v_{j}
$$
es decir que todo vector de la base es un eigenvector.

$\Leftarrow$ Ahora, supongamos que existe una basse $\beta$ tal que $T(v_{j})=\lambda_{j}v_{j}$ para algunos escalares $\lambda_{1},\lambda_{2},\dots,\lambda_{n}$. Entonces 
$$
	D=[T]_{\beta}=\begin{pmatrix}
	\lambda_{1} & 0 & \dots & 0 \\
	0 & \lambda_{2} & \dots & 0 \\
	\vdots &  &  & \vdots \\
	0 & 0 & \dots & \lambda_{n}
	\end{pmatrix}.\quad\square
$$

##### Ejemplos:
1.- $A=\begin{pmatrix}1 & 3 \\  4 & 2\end{pmatrix}$, $v_{1}=\begin{pmatrix}1 \\  -1 \end{pmatrix}$ y $v_{2}=\begin{pmatrix}3 \\  4\end{pmatrix}$.
$$
	\begin{pmatrix}
	1 & 3 \\
	4 & 2
	\end{pmatrix}\begin{pmatrix}
	1 \\
	-1
	\end{pmatrix}=\begin{pmatrix}
	-2 \\
	2
	\end{pmatrix}=-2\begin{pmatrix}
	1 \\
	-1
	\end{pmatrix}=-2v_{1},
$$
es decir que $v_{1}$ es un eigenvector de $A$ y su eigenvalor es $-2$.
$$
	\begin{pmatrix}
	1 & 3 \\
	4 & 2
	\end{pmatrix}\begin{pmatrix}
	3 \\
	4
	\end{pmatrix}=\begin{pmatrix}
	15 \\
	20
	\end{pmatrix}=5\begin{pmatrix}
	3 \\
	4
	\end{pmatrix}=5v_{2},
$$
es decir que $v_{2}$ también es un eigenvector de $A$ con eigenvalor $5$.
Ahora, para encontrar la matriz diagonal $D$, podemos auxiliarnos de una matriz de cambio de base 
$$
	Q=\begin{pmatrix}
	1 & 3 \\
	-1 & 4
	\end{pmatrix},\quad \text{tal que}\quad Q^{-1}AQ=D=\begin{pmatrix}
	-2 & 0 \\
	0 & 5
	\end{pmatrix}.
$$
2.- Sea $T$ el operador lineal en $R^{2}$ que rota cada vector $\frac{\pi}{2}$.
Esta transformación no tiene eigenvectores, por lo tanto no es diagonalizable.

3.- Sea $C^{\infty}$ el conjunto de todas las funciones $f:R\to R$ con derivadas en todos los órdenes. Sea $T$ la transformación lineal $T(f)=f´$.
Para cualquier constante tenemos $T(c)=0(c)$, es decir que cualquier función constante es un eigenvalor.
Queremos todas las funciones que satisfagan esta ecuación diferencial $T(f)=cf=f´$. $f=e^{ cx }$. 
Entonces $T$ tiene un eigenvalor por cada $c\in R$ (de hecho dos).

#### Teorema 5.2
Sea $A\in M_{n\times n}(F)$. Entonces el escalar $\lambda$ es un eigenvalor de $A$ si y sólo si $\det(A-\lambda I_{n})$=0.
##### Demostración:
Un escalar $\lambda$ es un eigenvalor de $A$ si y sólo si $Av=\lambda v$, $v\neq 0$. Entonces $Av-\lambda v=0$, o lo que es lo mismo $Av-\lambda I_{n}v=0\Rightarrow (A-\lambda I_{n})v=0$. Este sistema tiene una solución $v\neq 0$ si y sólo si 
$$
	\det(A-\lambda I_{n})=0.\quad\square
$$

##### Definición:
Sea $A\in M_{n\times n}(F)$. El polinomio característico de $A$ es 
$$
	f(t)=\det(A-tI_{n}).
$$
Notemos que si $t=\lambda$ un eigenvalor, entonces $f(\lambda)=0$.

##### Ejemplos:
1.- Encuentra los eigenvalores de $A=\begin{pmatrix}1 & 1 \\ 4 & 1\end{pmatrix}\in M_{2\times 2}(R)$.
**Sol:**
$$f(t)=\det(A-tI_{n})=\begin{vmatrix}1-t & 1 \\  4 & 1-t\end{vmatrix}=(1-t)^{2}-4=(3-t)(-1-t)$$
Tenemos que $f(t)=0$ para $t=3$ y $t=-1$. Es decir que los eigenvalores de $A$ son $3$ y $-1$.

2.- Sea $T$ el operador lineal en $P_{2}(R)$ definido como $T(f(x))=f(x)+(x+1)f´(x)$. Sea $\beta$ la base canónica ordenada de $P_{2}(R)$, y sea $A=[T]_{\beta}$. ¿Cuáles son los eigenvalores?.
**Sol:**
$T(1)=1, T(x)=1+2x,T(x^{2})=2x+3x^{2}$. Entonces 
$$
	A=\begin{pmatrix}
	1 & 1 & 0 \\
	0 & 2 & 2 \\
	0 & 0 & 3
	\end{pmatrix}.
$$
El polinomio característico es:
$$
	f(t)=\det A=(1-t)(2-t)(3-t),
$$
cuyas raíces son $1,2,3$, que son los eigenvalores de $T$.

#### Teorema 5.3
Sea $A\in M_{n\times n}(F)$.
- El polinomio característico de $A$ es un polinomio de grado $n$ con coeficiente principal $(-1)^{n}$.
- $A$ tiene a lo más $n$ eigenvalores distintos.
##### Demostración:
$$
	f(t)=\begin{vmatrix}
	A_{11}-t & A_{12} & \dots & A_{1n} \\
	A_{21} & A_{22}-t & \dots & A_{2n} \\
	\vdots &  &  & \vdots \\
	A_{n1} & \dots & \dots & A_{nn}-t
	\end{vmatrix}.
$$
En el determinante sale el término $(A_{11}-t)(A_{22}-t)\dots(A_{nn}-t)$, por lo que el mayor coeficiente de mayor grado es $(-t)^{n}=(-1)^{n}t^{n}$. 
Entonces $f(t)$ tiene grado a lo más $n$. Por lo tanto (dependiendo del campo) tiene a lo más $n$ raíces, cada una un eigenvalor.

#### Teorema 5.4
Sea $T$ un operador lineal en un espacio vectorial $V$, y sea $\lambda$ un eigenvalor de $T$. Un vector $v\in V$ es un eigenvector de $v$ de $T$ correspondiente a $\lambda$ si y sólo si $v\neq 0$ y $v\in N(T-\lambda I)$.
##### Demostración:
$v\in N(T-\lambda I)$ si y solo si es solución del sistema $(T-\lambda I)v=0$, en cuyo caso $Tv=\lambda Iv=\lambda v$, es decir que $v$ es el eigenvector asociado a $\lambda$.

##### Ejemplo:
Encuentra los eigenvectores para $A=\begin{pmatrix}1 & 1 & 0 \\ 0 & 2 & 2 \\ 0 & 0 & 3\end{pmatrix}$, si sabemos que los eigenvalores son 1,2,3.
**Sol:**
Usando el teorema 5.4, sea 
$$
	\begin{pmatrix}
	0 & 1 & 0 \\
	0 & 1 & 2 \\
	0 & 0 & 2
	\end{pmatrix}\begin{pmatrix}
	x_{1} \\
	x_{2} \\
	x_{3}
	\end{pmatrix}=0,
$$
tenemos el sistema 
$$
	\begin{cases}
	x_{2}=0 \\
	x_{2}+2x_{3}=0 \\
	x_{3}=0
	\end{cases},
$$
cuya solución es $v_{1}=t\begin{pmatrix}1 \\  0 \\  0\end{pmatrix}$ (tomando $x_{1}=t$ para $t$ cualquier escalar). Es decir que el vector $(1,0,0)$ es un eigenvector asociado al valor propio 1.
De la misma forma, para $\lambda=2$, tenemos 
$$
	\begin{pmatrix}
	-1 & 1 & 0 \\
	0 & 0 & 2 \\
	0 & 0 & 1
	\end{pmatrix}\begin{pmatrix}
	x_{1} \\
	x_{2} \\
	x_{3}
	\end{pmatrix}=0,
$$
cuya solución es $x_{3}=0$, $x_{1}=x_{2}=t$, por lo que el eigenvector asociado a 2 es $v_{2}=t\begin{pmatrix}1 \\  1 \\  0\end{pmatrix}$.
Por último, para $\lambda=3$, tenemos 
$$
	\begin{pmatrix}
	-2 & 1 & 0 \\
	0 & -1 & 2 \\
	0 & 0 & 0
	\end{pmatrix}\begin{pmatrix}
	x_{1} \\
	x_{2} \\
	x_{3}
	\end{pmatrix}=0,
$$
que nos da el sistema 
$$
	\begin{cases}
	-2x_{1}+x_{2}=0 \\
	-x_{2}+2x_{3}=0,
	\end{cases}
$$
con solución de la forma $x_{3}=t=x_{1}$, y $x_{2}=2t$, de modo que nuestro eigenvector asociado a $\lambda=3$ es $v_{3}=t\begin{pmatrix}1 \\  2 \\  1\end{pmatrix}$.