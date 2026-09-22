#AlgebraLineal
#### Teorema 5.5
Sea $T$ un operador lineal en un espacio vectorial $V$ y sean $\lambda_{1},\lambda_{2},\dots,\lambda_{k}$ [[Eigenvectores_Eigenvalores|eigenvalores]] distintos de $T$. Si $v_{1},v_{2},\dots,v_{k}$ son eigenvectores de $T$ tal que $\lambda_{i}$ corresponde a $v_{i}$, $1\leq i\leq k$, entonces el conjunto $\{ v_{1},\dots,v_{k} \}$ es linealmente independiente.
##### Demostración:
Por inducción sobre $K$.
Para $k=1$, únicamente tenemos $\lambda_{1},v_{1}$, y el conjunto $\{ v_{1} \}$ es linealmente independiente.
Supongamos que el resultado es cierto para $k-1$ eigenvalores distintos.
Tenemos $\lambda_{1},\lambda_{2},\dots,\lambda_{k}$ eigenvalores distintos y $v_{1},\dots,v_{k}$ eigenvectores asociados a los $\lambda_{i}$. Queremos demostrar que 
$$
	a_{1}v_{1}+\dots+a_{k}v_{k}=0
$$
si y sólo si $a_{i}=0$ para todo $1\leq i\leq k$. Apliquemos la transformación $T-\lambda_{k}I$ y tenemos 
$$
	a_{1}(\lambda_{1}-\lambda_{k})v_{1}+a_{2}(\lambda_{2}-\lambda_{k})v_{k}+\dots+a_{k}(\lambda_{k}-\lambda_{k})v_{k}=0,
$$
y por hipótesis de inducción sabemos que los $k-1$ vectoes son linealmente independientes, es decir que 
$$
	a_{i}(\lambda_{i}-\lambda_{k})=0\quad 1\leq i\leq k-1,
$$
y como los eigenvalores son distintos, esto implica que $a_{i}=0$. Entonces esto implica que la única forma en que la combinación original sea cero es si $a_{k}=0$, pues $v_{k}$ no puede ser cero por ser un eigenvector. Entonces llegamos a que $a_{i}=0$ para cualquier $1\leq i\leq k$, por lo tanto 
$$
	\{ v_{1},\dots,v_{k} \}\text{ es linealmente independiente.}\quad\square
$$

##### Corolario
Sea $T$ un operador lineal en un espacio vectorial $n$-dimensional $V$. Si $T$ tiene $n$ eigenvalores distintos, entonces $T$ es diagonalizable.


