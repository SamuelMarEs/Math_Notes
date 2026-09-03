##### Definición:
Dado un [[EspaciosVectoriales|espacio vectorial]] $V$ sobre $F$ de dimensión finita, un operador lineal es una transformación lineal 
$$
	T:V\to V.
$$

##### Definición:
Dado un espacio vectorial $V$ y dos [[BasesOrdenadas|bases ordenadas]] $\beta$ y $\beta'$. La matriz de cambio de base de $\beta'$ a $\beta$ está dada por 
$$
	Q=[a_{ij}],
$$
dónde $a_{ij}$ son los escalares que generan al vector $T(v_{j})=\sum_{i=1}^{n}a_{ij}w_{j}$ para $v_{j}\in \beta'$ y $w_{j}\in \beta$.
El libro lo denota como 
$$
	Q=[I_{V}]_{\beta'}^{\beta}.
$$
dónde $I_{V}:V\to V$ es lineal y está definida como $I_{V}(v_{j})=w_{j}$ para $v_{j}\in \beta'$ y $w_{j}\in \beta$.

#### Teorema 2.22
Sean $\beta$ y $\beta'$ dos bases ordenadas del espacio vectorial $V$ de dimensión $n$. Sea $Q$ la matriz de cambio de base definida anteriormente, entonces 
$$
	Q[v]_{\beta'}=[v]_{\beta}\text{ y }Q\text{ es invertible}.
$$
Dónde $[v]_{\beta'}$ y $[v]_{\beta}$ son los [[RepresentacionEstandar|vectores coordenada]] de $v$ en cada una de las bases. 
##### Demostración:
$$
	[v]_{\beta}=[I_{V}(v)]_{\beta}=[I_{V}]_{\beta'}^{\beta}[v]_{\beta'}=Q[v]_{\beta'}.
$$


#AlgebraLineal