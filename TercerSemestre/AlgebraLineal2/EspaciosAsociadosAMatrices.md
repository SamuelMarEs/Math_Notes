Sea $A\in M_{m\times n}(F)$ con coeficientes $a_{ij}$ de la forma 
$$
	A=\begin{pmatrix}
	a_{11} & \dots & a_{1n} \\
	\cdot & \dots & \cdot  \\
	a_{m 1} & \dots & a_{mn}
	\end{pmatrix}.
$$
- Sean $c_{1},\dots,c_{n}$ los vectores columna de $A$ y $span(c_{1},\dots,c_{n})=C_{A}$. 
  $C_{A}$ es un [[EspaciosVectoriales|subespacio]] de $F^{m}$, cuya dimensión es el ***rango por columnas***.
- Seam $r_{1},\dots r_{m}$ los vectores renglón de $A$ y $span(r_{1},\dots,r_{m})=R_{A}$.
  $R_{A}$ es un subespacio de $F^{n}$, cuya dimensión es el ***rango por renglones***.
- Definimos la ***imagen*** $$
  	im(A)=\{ y\in F^{m}|Ax=y \quad\text{para algún}\quad x\in F^{n} \}
  $$ la cual es un subespacio de $F^{m}$.
- Definimos el [[KernelYRango|kernel]], *espacio nulo*, o *núcleo* como $$
  	ker(A)\{ x\in F^{n}|Ax=0 \}
  $$ el cual es un subespacio de $F^{n}$.

##### Teo:
Llamamos el [[KernelYRango|rango]] de una matriz $A$ a 
$$
	dim(im(A))=dim(C_{A})=dim(R_{A}).
$$

#AlgebraLineal 