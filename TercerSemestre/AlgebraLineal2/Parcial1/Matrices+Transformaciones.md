##### Definición:
Sea $V$ un [[EspaciosVectoriales|espacio vectorial]] sobre $F$ y sea $\beta=\{ v_{1},\dots,v_{n} \}$ una [[BasesOrdenadas|base ordenada]] de $V$.
El ***vector coordenada*** de $x\in V$ con respecto a la base $\beta$ esta dado por $$[x]_{\beta}=\begin{pmatrix}
a_{1} \\
a_{2} \\
\vdots \\
a_{n}
\end{pmatrix}$$ donde $x=\sum_{i=1}^{n}a_{i}v_{i}$.

##### Definición:
Sean $V$ y $W$ espacios vectoriales sobre $F$ con sus respectivas bases ordenadas $\beta=\{ v_{1},\dots,v_{n} \}$ $\gamma=\{ w_{1},\dots,w_{m} \}$. Sea $T:V\to W$ una transformación lineal.
Para cada $j=1,2,\dots,n$ existen escalares únicos $a_{ij}\in F, i=1,2,\dots,m$ tales que 
$$
	T(v_{j})=\sum_{i=1}^{m}a_{ij}w_{i},\quad\text{para }j=1,2,\dots,n.
$$
Llamamos matriz $A$ de dimensiones $m\times n$ definida por $A=A_{ij}=[a_{ij}]$ la ***representación matricial de $T$ dada las bases ordenadas $\beta$ y $\gamma$***, que se denota de la forma.
$$
	A=[T]_{\beta}^{\gamma}=(a_{ij}),\quad 1\leq i\leq m,1\leq j\leq n,
$$
dónde $$T(v_{j})=\sum_{i=1}^{m}a_{ij}w_{i}\quad\text{para}\quad1\leq j\leq n.$$
Si tenemos que $V=W$ y $\beta=\gamma$, entonces escribimos $A=[T]_{\beta}$.


Notese que la $j$-ésima columna de $A$ es simplemente $[T(v_j)]_{\gamma}$. Tambien tenemos que si $U:V\to W$ es una transformación lineal tal que $[U]_{\beta}^{\gamma}=[T]_{\beta}^{\gamma}$, entonces $U=T$ por el corolario del [[BasesOrdenadas|teorema 2.6.]] 


#AlgebraLineal