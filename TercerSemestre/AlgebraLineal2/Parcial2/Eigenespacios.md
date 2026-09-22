#AlgebraLineal
#### Definición
Sea $\lambda$ un [[Eigenvectores_Eigenvalores|eigenvalor]] de un operador lineal o una matriz con polinomio característico $f(t)$. La ***multiplicidad*** de $\lambda$ es el mayor entero positivo $k$ para el cual $(t-\lambda)^{k}$ es un factor de $f(t)$.

En otras palabras, la multiplicidad es la cantidad de veces que se va a repetir una raíz del polinomio. Esto en general se aplica a cualquier polinomio factorizable sobre un campo $F$. (Gero una vez lo usó en un problema de la OMUM).

#### Definición
Sea $T$ un operador lineal sobre un espacio vectorial $V$, y sea $\lambda$ un eigenvalor de $T$. Definamos 
$$
	E_{\lambda}=\{ x\in V:T(x)=\lambda x \}=N(T-\lambda I_{V}).
$$
El conjunto $E_{\lambda}$ es el ***eigenespacio*** de $T$ correspondiente al eigenvalor $\lambda$. Se define de forma análoga el eigenespacio de una matriz cuadrada $A$ como el eigenespacio de $L_{A}$ correspondiente a $\lambda$.

**Evidentemente** este es un subespacio vectorial de $V$, cuya dimensión es el máximo número de eigenvalores asociados a $\lambda$ que son linealmente independientes.

#### Teorema 5.7
Sea $T$ un operador lineal sobre un espacio vectorial $V$ de dimensión finita, y sea $\lambda$ un eigenvalor de $T$ con multiplicidad $m$. Entonces $1\leq\text{dim}(E_{\lambda})\leq m$.
##### Demostración:
Tomemos una base ordenada $\{ v_{1},\dots,v_{p} \}$ para $E_{\lambda}$, y extendámosla a una base para $V$ de la forma $\beta=\{ v_{1},\dots,v_{p},v_{p+1},\dots v_{n} \}$. Sea además $A=[T]_{\beta}$. Observemos que $v_{i}$ $(1\leq i\leq p)$ es un eigenvalor de $T$ correspondiente a $\lambda$, y por lo tanto 
$$
	A=\begin{pmatrix}
	\lambda I_{p} & B \\
	O & C
	\end{pmatrix}.
$$
El polinomio característico de $T$ esta dado por 
$$
	\begin{align}
	f(t)&=\det(A-tI_{n})=\det \begin{pmatrix}
	(\lambda-t)I_{p} & B \\
	O & C-t\lambda I_{n-p}
	\end{pmatrix} \\
	&=\det((\lambda-t)I_{p})\cdot \det(C-tI_{n-p}) \\
	&=(\lambda-t)^{p}g(t)
	\end{align}
$$
donde $g(t)$ es otro polinomio. Entonces $(\lambda-t)^{p}$ es un factor de $f(t)$, y por lo tanto la multiplicidad de $\lambda$ es *por lo menos* $p$, pero $\text{dim}(E_{\lambda})=p$, y por lo tanto $\text{dim}(E_{\lambda})\leq m.\quad\square$
