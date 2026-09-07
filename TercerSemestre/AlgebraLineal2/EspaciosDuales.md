##### Definición:
Sea $V$ un [[EspaciosVectoriales|espacio vectorial]] sobre $F$. El ***espacio dual*** es 
$$
	V^{*}=\mathcal{L}(V,F).
$$
Si $\text{dim}(V)=n$, entonces $\text{dim}(V^{*})=n$, por lo tanto $V\cong V^{*}$.

##### Definición:
Sea $V$ un espacio vectorial de dimensión finita, y sea $\beta=\{ s_{1},\dots,x_{n} \}$ una [[BasesOrdenadas|base ordenada]] de $V$. Para cada $i=1,2,\dots,n$ definimos $f_{i}(x)=a_{i}$, donde 
$$
	[x]_{\beta}=\begin{pmatrix}
	a_{1} \\
	a_{2} \\
	\vdots \\
	a_{n}
	\end{pmatrix}
$$
es el [[RepresentacionEstandar|vector coordenada]] de $x$ relativo a $\beta$. Entonces $f_{i}$ es un operador lineal sobre $V$ llamado la $i$-ésima función coordenada con respecto a la base $\beta$. Notese que $f_{i}(x_{j})=\delta_{ij}$ la delta de Kronecker. 

#### Teorema 2.24
Sea $V$ un espacio vectorial sobre $F$. Sea $\beta=\{ x_{1},\dots,x_{n} \}$ una base ordenada. Sean $f_{i}\in\mathcal{L}(V,F)$ para $1\leq i\leq n$, las [[TransformacionesLineales|transformaciones lineales]] que corresponden a la $i$-ésima coordenada. Entonces 
$$
	\beta^{*}=\{ f_{1},f_{2},\dots,f_{n} \}
$$
es una base ordenada de $V^{*}$. Más aún 
$$
	\forall f\in V^{*}=\mathcal{L}(V,F),\quad f=\sum_{i=1}^{n}f(x_{i})f_{i}.
$$
##### Ejemplo: 
Sea $V=R^{2}$ y $\beta_{0}\{ (2,1),(3,1) \}$. Encontrar $\beta^{*}=\{ f_{1},f_{2} \}$.


#AlgebraLineal