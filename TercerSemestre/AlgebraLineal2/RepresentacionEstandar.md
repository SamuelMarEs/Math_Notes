##### Teorema 2.20
Sean $V$ y $W$ espacios vectoriales sobre un campo $F$ de dimensión $n$ y $m$ respectivamente, con bases $\beta=\{ v_{1},\dots,v_{n} \}$ y $\gamma=\{ w_{1},\dots,w_{m} \}$. La función $\Phi:\mathcal{L}(V,W)\to M_{m\times n}$ definida como 
$$
	\Phi(T)=[T]_{\beta}^{\gamma}.
$$
es un isomorfismo.
##### Demostración:
La demostración de que $\Phi$ es una transformación lineal es el Teorema 2.8 de la segunda tarea. Por lo tanto, para mostrar que $\Phi$ es invertible, vamos a probar que $\Phi$ es biyectiva. Es decir que 
$$
	\forall A\quad\exists!U\in\mathcal{L}(V,W)\quad\text{tal que}\quad\Phi(U)=A.
$$
Definamos $U:V\to W$ como $$U(v_{i})=\sum_{i=1}^{m}A_{ij}w_{i}\quad\forall 1\leq j\leq n.$$
Entonces, por definición, podemos observar que $[T]_{\beta}^{\gamma}=A$, y por el [[BasesOrdenadas|teorema 2.6]], $U$ es única. $\quad\square$ 

Este resultado se generaliza a que $\mathcal{L}(V,W)\cong F^{nm}$.

##### Definición:
Sea $V$ un espacio vectorial sobre un campo $F$ y base $\beta=\{ v_{1},\dots,v_{n} \}$. La ***representación estándar*** de $V$ con respecto a $\beta$ es $\Phi_{\beta}:V\to F^{n}$ definida como 
$$
	\Phi_{\beta}(x)=[x]^{\beta}=\begin{pmatrix}
	a_{1} \\
	\vdots \\
	a_{n}
	\end{pmatrix}\quad\text{donde}\quad x=\sum_{i=1}^{n}a_{i}v_{i}.
$$
Es decir, todo espacio de dimensión finita puede verse como una eneada de escalares. El siguiente teorema muestra que esto es un isomorfismo.

##### Teorema 2.21
