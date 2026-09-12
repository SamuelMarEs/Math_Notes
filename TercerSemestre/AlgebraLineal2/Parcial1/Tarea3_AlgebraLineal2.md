### Sección 2.4 Friedberg
2.- Para cada una de las siguientes transformaciones, determina si son invertibles y justifica tu respuesta.
- $T:R^{2}\to R^{3}$ definida como $T(a_{1},a_{2})=(a_{1}-2a_{2},a_{2},3a_{1}+4a_{2})$.
  **Sol:**
  No es invertible. Sabemos que existe un isomorfismo entre $V$ y $W$ si y solo si $\text{dim}(V)=\text{dim}(W)$. Sin embargo $\text{dim}(R^{2})=2$ y $\text{dim}(R^{3})=3$, por lo tanto $T$ no puede ser un isomorfismo, y como es lineal, esto implica que no es invertible.
- $T:R^{2}\to R^{3}$ definida como $T(a_{1},a_{2})=(3a_{1}-a_{2},a_{2},4a_{1})$.
  **Sol:**
  No es invertible, pues las dimensiones del dominio y codominio son distintas.
- $T:R^{3}\to R^{3}$ definida como $T(a_{1},a_{2},a_{3})=(3a_{1}-2a_{3},a_{2},3a_{1}+4a_{2})$.
  **Sol:**
  No es invertible. Misma razón que el inciso anterior.
- $T:P_{3}(R)\to P_{2}(R)$ definida como $T(p(x))=p'(x)$.
  **Sol:**
  No es invertible. Misma razón que el inciso anterior.
- $T:M_{2\times 2}(R)\to P_{2}(R)$ definida como $T\begin{pmatrix}a & b \\  c & d\end{pmatrix}=a+2bx+(c+d)x^{2}$.
  **Sol:**
  No es invertible. Misma razón que el inciso anterior.
- $T:M_{2\times 2}(R)\to M_{2\times 2}(R)$ definida como $T\begin{pmatrix}a & b \\  c & d\end{pmatrix}=\begin{pmatrix}a+b & a \\  c & c+d\end{pmatrix}$.
  **Sol:**
  Sea $\beta$ la base canónica de $M_{2\times 2}$. Tenemos entonces que 
  $$
	T(\beta)=\left\{ \begin{pmatrix}
	1 & 1 \\
	0 & 0
	\end{pmatrix}, \begin{pmatrix}
	1 & 0 \\
	0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 \\
	1 & 1
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 \\
	0 & 1
	\end{pmatrix} \right\}.
  $$
  Dada la imagen de la base, podemos calcular la matriz asociada: 
  $$
	[T]_{\beta}=\begin{pmatrix}
	1 & 1 & 0 & 0 \\
	1 & 0 & 0 & 0 \\
	0 & 0 & 1 & 0 \\
	0 & 0 & 1 & 1
	\end{pmatrix},
  $$
  cuyo determinante es -1, por lo tanto es invertible, y por el corolario 1 del teorema 2.18 la transformación $T$ también es invertible.

3.- ¿Cuál de los siguientes pares de espacios vectoriales son isomorfos? Justifique su respuesta.
- $F^{3}$ y $P_{3}(F)$.
  **Sol:**
  No son isomorfos, pues $P_{3}(F)$ es de dimensión 4, mientras que $F^{3}$ es de dimensión 3.
- $F^{4}$ y $P_{3}(F)$.
  **Sol:**
  Si son isomorfos, pues $P_{3}(F)$ y $F^{4}$ son ambos de dimensión 4. (Teo 2.19)
- $M_{2\times 2}(R)$ y $P_{3}(R)$.
  **Sol:**
  Si son isomorfos, pues $\text{dim}(M_{2\times 2}(R))=4=\text{dim}(P_{3}(R))$.
- $V=\{ A\in M_{2\times 2}(R):\text{tr}(A)=0 \}$ y $R^{4}$.
  **Sol:**
  Observemos que 
  $$
	\beta=\left\{ \begin{pmatrix}
	1 & 0 \\
	0 & -1
	\end{pmatrix}, \begin{pmatrix}
	0 & 1 \\
	0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 \\
	1 & 0
	\end{pmatrix} \right\}
	
  $$
  es una base de $V$. Por lo tanto no son isomorfos, ya que $V$ es de dimensión 3 y $R^{4}$ de dimensión 4.


8.- Pruebe los corolarios 1 y 2 del teorema 2.18 ($[T^{-1}]_{\gamma}^{\beta}=([T]_{\beta}^{\gamma})^{-1}$).
###### Corolario 1:
Sea $V$ un espacio vectorial de dimensión finita con base ordenada $\beta$, y sea $T:V\to V$ lineal. Entonces $T$ es invertible si y sólo si $[T]_{\beta}$ es invertible. Más aún, $[T^{-1}]_{\beta}=([T]_{\beta})^{-1}$.
**Sol:**
Sea $T:V\to W$ con $V=W$ y $\beta=\gamma$. Por el teorema 2.18 tenemos que 
$$
	[T^{-1}]_{\beta}=[T^{-1}]_{\gamma}^{\beta}=([T]_{\beta}^{\gamma})^{-1}=([T]_{\beta})^{-1}. \quad\square
$$
###### Corolario 2:
Sea $A$ una matriz de $n\times n$. Entonces $A$ es invertible si y sólo si $L_{A}$ es invertible. Más aún, $(L_{A})^{-1}=L_{A^{-1}}$.
**Sol:**
Sea $L_{A}:R^{n}\to R^{n}$ la transformación asociada a la matriz $A$, es decir $L_{A}=T$ con $[T]_{\beta}^{\gamma}=A$ para alguna $T:R^{n}\to R^{n}$, y $\beta,\gamma$ dos bases de $R^{n}$. Entonces $(L_{A})^{-1}=T^{-1}$ con 
$$
	[T^{-1}]_{\gamma}^{\beta}=([T]_{\beta}^{\gamma})^{-1}=A^{-1},
$$
cuya transformación asociada es también $L_{A^{-1}}$, es decir que $(L_{A})^{-1}=L_{A^{-1}}.\quad\square$


12.- Pruebe el teorema 2.21:
###### Teorema 2.21:
Para cualquier espacio vectorial $V$ con base $\beta$ de dimensión $n$, la transformación $\phi_{\beta}:V\to F^{n}$, definida como $\phi_{\beta}(x)=[x]_{\beta}$, es un isomorfismo.
**Sol:**
Sea $\beta=\{ v_{1},\dots,v_{n} \}$, sabemos que para todo $x\in V$ existen escalares únicos $a_{1},\dots,a_{n}$ tales que $x=a_{1}v_{1}+\dots+a_{n}v_{n}$. Además, $x=0$ si y sólo si $a_{1}=\dots=a_{n}=0$, ya que $\beta$ es una base. Entonces, tenemos que 
$$
	\phi_{\beta}(x)=\begin{pmatrix}
	a_{1} \\
	\vdots \\
	a_{n}
	\end{pmatrix}=\bar{0}\Longleftrightarrow a_{1}=\dots=a_{n}=0\Longleftrightarrow x=0,
$$
es decir que $N(\phi_{\beta})=\{ 0 \}$, por lo tanto es inyectiva, y por el teorema 2.5, también suprayectiva, y por lo tanto es invertible, es decir que $\phi_{\beta}$ es un isomorfismo. $\quad\square$


14.- Sea 
$$
	V=\left\{ \begin{pmatrix}
	a & a+b \\
	0 & c
	\end{pmatrix} :a,b,c\in F\right\}.
$$
Construya un isomorfismo de $V$ en $F^{3}$.
**Sol:**
Dada la base $\beta=\left\{ \begin{pmatrix}1 & 1 \\  0 & 0\end{pmatrix}, \begin{pmatrix}0 & 1 \\  0 & 0\end{pmatrix}, \begin{pmatrix}0 & 0 \\  0 & 1\end{pmatrix} \right\}$ para $V$. Definamos $\psi_{\beta}(x)=[x]_{\beta}$, es decir, para 
$$
	x=a\begin{pmatrix}
	1 & 1 \\
	0 & 0
	\end{pmatrix}+b\begin{pmatrix}
	0 & 1 \\
	0 & 0
	\end{pmatrix}+ c\begin{pmatrix}
	0 & 0 \\
	0 & 1
	\end{pmatrix},
$$
tenemos que 
$$
	\psi_{\beta}(x)=\begin{pmatrix}
	a \\
	b \\
	c
	\end{pmatrix}.
$$
Entonces, por el teorema 2.21, $\psi_{\beta}$ es un isomorfismo.


15.- Sean $V,W$ espacios vectoriales de dimensión $n$, y sea $T:V\to W$ lineal. Suponga que $\beta$ es una base para $V$. Muestre que $T$ es un isomorfismo si y sólo si $T(\beta)$ es una base de $W$.
**Sol:**
$\Rightarrow$ Supongamos que $T$ es invertible, y $\beta=\{ v_{1},\dots,v_{n} \}$. Dado que $V$ y $W$ tienen la misma dimensión, basta demostrar que $T(\beta)=\{ T(v_{1}),\dots,T(v_{n}) \}$ es linealmente independiente.
Sea $x\in V$ con $x=a_{1}v_{1}+\dots+a_{n}v_{n}$, entonces tenemos que 
$$
	\begin{align}
	T(x)&=T(a_{1}v_{1}+\dots+a_{n}v_{n}) \\
	&=a_{1}T(v_{1})+\dots+a_{n}T(v_{n}).
	\end{align}
$$
Como $T$ es invertible, es inyectiva, es decir que $N(T)=\{ 0_{V} \}$. Por lo tanto 
$$
	T(x)=0_{W}\Longleftrightarrow x = 0_{V}\Longleftrightarrow a_{1}=\dots=a_{n}=0.
$$
Entonces $a_{1}T(v_{1})+\dots+a_{n}T(v_{n})=0\Longleftrightarrow a_{1}=\dots=a_{n}=0$. Por lo tanto $T(\beta)$ es linealmente independiente. 

$\Leftarrow$ Supongamos ahora que $T(\beta)$ es linealmente independiente. Para mostrar que es invertible, basta probar que es biyectiva, y por el teorema 2.5, basta probar que $N(T)=\{ 0_{V} \}$.
Sea $x=a_{1}v_{1}+\dots+a_{n}v_{n}\in V$ tal que $T(x)=0_{W}$ (i.e $x\in N(T)$). Entonces 
$$
	T(x)=a_{1}T(v_{1})+\dots+a_{n}T(v_{n})=0_{W}.
$$
Sin embargo, $T(\beta)$ es base, por lo tanto $a_{1}T(v_{1})+\dots+a_{n}T(v_{n})\Longleftrightarrow a_{1}=\dots=a_{n}=0$. Por lo tanto tenemo que $x=0_{V}\Rightarrow N(T)=\{ 0_{V} \}.\quad\square$ 


### Sección 2.5 Friedberg
2.- Para cada uno de los siguientes pares de bases ordenadas $\beta$ y $\beta'$ para $R^{2}$, encuentre la matriz de cambio de base que cambia las coordenadas $\beta'$ en coordenadas $\beta$.
- $\beta=\{ e_{1},e_{2} \},\beta'=\{ (a_{1},a_{2}),(b_{1},b_{2}) \}$.
- $\beta=\{ (-1,3),(2,-1) \},\beta'=\{ (0,10),(5,0) \}$.
- $\beta=\{ (2,5),(-1,-3) \},\beta'=\{ (e_{1},e_{2}) \}$.
- $\beta=\{ (-4,3),(2,-1) \},\beta'=\{ (2,1),(-4,1) \}$.

3.- Para cada uno de los siguientes pares de bases ordenadas $\beta$ y $\beta'$ para $P_{2}(R)$, encuentre la matriz de cambio de base que cambia las coordenadas $\beta'$ en coordenadas $\beta$.
- $\beta=\{ x^{2},x,1 \},\beta'=\{ a_{2}x^{2}+a_{1}x+a_{0},b_{2}x^{2}+b_{1}x+b_{0},c_{2}x^{2}+c_{1}x+c_{0} \}$.
- $\beta=\{ 1,x,x^{2} \},\beta'=\{  a_{2}x^{2}+a_{1}x+a_{0},b_{2}x^{2}+b_{1}x+b_{0},c_{2}x^{2}+c_{1}x+c_{0}  \}$.
- $\beta = \{ 2x^{2}-x,3x^{2}+1,x^{2} \},\beta'=\{ 1,x,x^{2} \}$.
- $\beta=\{ x^{2}-x+1,x+1,x^{2}+1 \},\beta'=\{ x^{2}+x+4,4x^{2}-3x+2,2x^{2}+3 \}$.
- $\beta=\{ x_{2}-x,x_{2}+1,x-1 \},\beta'=\{ 5x^{2}-2x-3,-2x^{2}+5x+5,2x^{2}-x-3 \}$.
- $\beta=\{ 2x^{2}-x+1,x^{2}+3x-2,-x^{2}+2x+1 \}, \beta'=\{ 9x-9,x^{2}+21x-2,3x^{2}+5x+2 \}$

4.- Sea $T$ un operador lineal sobre $R^{2}$ definido como 
$$
	T\begin{pmatrix}
	a \\
	b
	\end{pmatrix}=\begin{pmatrix}
	2a+b \\
	a-3b
	\end{pmatrix},
$$
sea $\beta$ la base ordenada estándar para $R^{2}$, y sea $\beta'=\left\{ \begin{pmatrix}1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  2\end{pmatrix} \right\}$. Use el Teorema 2.23 y el hecho de que 
$$
	\begin{pmatrix}
	1 & 1 \\
	1 & 2
	\end{pmatrix}^{-1}=\begin{pmatrix}
	2 & -1 \\
	-1 & 1
	\end{pmatrix}
$$
para encontrar $[T]_{\beta'}$

5.- Sea $T$ el operador lineal sobre $P_{1}(R)$ definido como $T(p(x))=p'(x)$, la derivada de $p(x)$. Sea $\beta=\{ 1,x \}$ y $\beta'=\{ 1+x,1-x \}$. Use el Teorema 2.23 y el hecho de que 
$$
	\begin{pmatrix}
	1 & 1 \\
	1 & -1
	\end{pmatrix}^{-1}=\begin{pmatrix}
	2 & -1 \\
	-1 & 1
	\end{pmatrix}
$$
para encontrar $[T]_{\beta'}$.

6.- Para cada matriz $A$ y base ordenada $\beta$, encuentra $[L_{A}]_{\beta}$. También, encuentra una matriz invertible $Q$ tal que $[L_{A}]_{\beta}=Q^{-1}AQ$.
- $A=\begin{pmatrix}1 & 3 \\  1 & 1\end{pmatrix}$ y $\beta=\left\{ \begin{pmatrix}1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  2\end{pmatrix} \right\}$.
- $A=\begin{pmatrix}1 & 2 \\  2 & 1\end{pmatrix}$ y $\beta=\left\{ \begin{pmatrix}1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  -1\end{pmatrix} \right\}$.
- $A=\begin{pmatrix}1 & 1 & -1 \\  2 & 0 & 1 \\  1 & 1 & 0\end{pmatrix}$ y $\beta=\left\{ \begin{pmatrix}1 \\  1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  0 \\  1\end{pmatrix},\begin{pmatrix}1 \\  1 \\  2\end{pmatrix} \right\}$.
- $A=\begin{pmatrix}13 & 1 & 4 \\ 1 & 13 & 4 \\  4 & 4 & 10\end{pmatrix}$ y $\beta=\left\{ \begin{pmatrix}1 \\  1 \\  -2\end{pmatrix},\begin{pmatrix}1 \\  -1 \\  0\end{pmatrix},\begin{pmatrix}1 \\  1 \\  1\end{pmatrix} \right\}$.

11.- Sea $V$ un espacio vectorial de dimensión finita con bases ordenadas $\alpha, \beta, \gamma$. 
- Pruebe que si $Q$ y $R$ son las matrices de cambio de base de $\alpha$ en $\beta$, y $\beta$ en $\gamma$, respectivamente, entonces $RQ$ es la matriz de cambio de base de $\alpha$ en $\gamma$.
- Pruebe que si $Q$ cambia las coordenadas $\alpha$ en coordenadas $\beta$, entonces $Q^{-1}$ cambia las coordenadas $\beta$ en coordenadas $\alpha$.
