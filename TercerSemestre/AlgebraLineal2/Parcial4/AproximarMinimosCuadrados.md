#AlgebraLineal 
Supongamos que se colectan datos ${}y_{1},\dots,y_{m}{}$ en los tiempos ${}t_{1},\dots,t_{m}{}$ respectivamente. Si tenemos las parejas ${}(t_{i},y_{i}){}$, ${}1\leq i\leq m{}$, y suponemos una relación lineal entre ${}y{}$ y ${}t{}$, es decir ${}y=ct+d{}$, lo que queremos hacer es encontrar las constantes ${}c{}$ y ${}d{}$ de modo que la recta aproxime de la mejor forma posible a los datos recabados.
Una forma de estimar que tan buena es una aproximación dados ${}c{}$ y ${}t{}$, es tomar el error como la suma de los cuadrados de las distancias verticales entre los puntos de los datos recabados y la recta aproximada, es decir 
$$
E=\sum_{i=1}^{m}(y_{i}-ct_{i}-d)^{2}.
$$
De este modo, lo que queremos encontrar son ${}c{}$ y ${}d{}$ que minimicen ${}E{}$.
Si definimos
$$
A=\begin{pmatrix}
t_{1} & 1 \\
t_{2} & 1 \\
\vdots & \vdots \\
t_{m} & 1
\end{pmatrix},\quad x=\begin{pmatrix}
c \\
d
\end{pmatrix},\quad y=\begin{pmatrix}
y_{1} \\
y_{2} \\

\vdots \\
y_{m}
\end{pmatrix},
$$
tenemos entonces que ${}E=\lVert y-Ax \rVert ^{2}{}$.
A continuación desarrollamos un método general para encontrar un vector ${}x_{0}\in F^{n}{}$ que minimice ${}E{}$. Primero, tomemos en cuenta que, si ${}x,y{}$ son vectores columna, entonces tenemos que ${}\langle x,y \rangle=y^{*}x{}$, donde ${}\langle \cdot,\cdot \rangle{}$ es el producto interno de ${}F^{n}{}$. Para encontrar una forma general de minimizar ${}E{}$, primero necesitamos dos lemas:
#### Lema 1:
Sean ${}A\in M_{m\times n}(F){}$, ${}x \in F^{n}{}$, y ${}y\in F^{m}{}$. Entonces 
$$
\langle Ax,y \rangle_{m}=\langle x,A^{*}y \rangle _{n}. 
$$
##### Demostración:
De forma directa se tiene que 
$$
\langle Ax,y \rangle _{m}=y^{*}(Ax)=(y^{*}A)x=(A^{*}y)^{*}x=\langle x,A^{*}y \rangle _{n}.\quad\square
$$

#### Lema 2:
Sea ${}A\in M_{m\times n}(F){}$. Entonces ${}\mathrm{rank}(A^{*}A)=\mathrm{rank}(A){}$.

