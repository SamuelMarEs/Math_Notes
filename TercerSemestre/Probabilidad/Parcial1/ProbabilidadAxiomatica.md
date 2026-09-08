##### Axiomas de Kolmogorov
1. $P(A)\geq 0$.
2. $P(\Omega)=1$.
3. Sean $A_{1}, A_{2}, A_{3} \dots$ conjuntos disjuntos $A_{i}\cap A_{j}=\emptyset\quad\forall i\neq j$, entonces 
   $$
   	P\left( \bigcup_{i=1}^{\infty}A_{i} \right)=\sum_{i=1}^{\infty}P(A_{i}).
   $$

##### Definición:
Una ***medida de probabilidad*** es una función $P:\mathcal{A}\to[0,1]$ que satisface los axiomas de Kolmogorov, donde $\mathcal{A}\subset 2^{\Omega}$ es una [[SigmaAlgebra|sigma álgebra]] done $\Omega$ es el [[PrincipiosDeProbabilidad|espacio muestral]].

Se puede demostrar que la [[ProbabilidadClasica|probabilidad clásica]], [[ProbabilidadGeometrica|probabilidad geométrica]] y la [[ProbabilidadFrecuentista|probabilidad frecuentista]] satisfacen los axiomas de Kolmogorov.

##### Proposición:
$P(\emptyset)=0$.
**Sol:**
Sean $A_{1}=A_{2}=\dots=\emptyset$, entonces 
$$
	P\left( \bigcup_{i=1}^{\infty}A_{i} \right)=P(\emptyset)=\sum_{i=1}^{\infty}P(A_{i}),
$$
es decir que $P(\emptyset)$ es igual a una suma infinita de si mismo, lo cual solo es posible si 
$$
	P(\emptyset)=0. \quad \square
$$
##### Proposición:
$P(A)=1-P(A^{c})$.
**Sol:**
Sabemos que $A\cup A^{c}=\Omega$ y $A\cap A^{c}=\emptyset$, por lo tanto 
$$
	1=P(\Omega)=P(A\cup A^{c})=P(A)+P(A^{c})\implies P(A)=1-P(A^{c}). \quad\square
$$
##### Proposición:
Si $A\subset B$ entonces $P(A)\leq P(B)$.
**Sol:**
Sabemos que $A\cup(B-A)=B$, y que $A\cap(B-A)=\emptyset$, por lo tanto 
$$
	P(B)=P(A)+P(B-A)\geq 0\implies P(B)-P(A)=P(B-A)\geq 0 \implies P(B)\geq P(A).\quad\square
$$
##### Otras propiedades:
1. Si $A\subset B$, entonces $P(B-A)=P(B)-P(A)$.
2. Para todo $A$ se cumple $0\leq P(A)\leq 1$.
3. $P(A\cup B)=P(A)+P(B)-P(A\cap B)$.
4. $P(A\cup B\cup C)=P(A)+P(B)+P(C)-P(A\cap B)-P(A\cap C)-P(B\cap C)+P(A\cap B\cap C)$.


##### Ejercicio:
Si $P$ y $Q$ son medidas de probabilidad sobre $\mathcal{A}$, y $\alpha\in(0,1)$ entonces 
$$
	\alpha P+(1-\alpha)Q
$$
es una medida de probabilidad.
Esto se llama una ***mezcla*** de distribuciones de probabilidad.
**Sol:**
Vamos a demostrar que esta satisface los tres axiomas de Kolmogorov.
1. P.d. que $\alpha P(A)+(1-\alpha)Q(A)\geq 0$.
   Sabemos que $1\geq\alpha\geq 0$, por lo tanto también $1-\alpha$ esta en el mismo rango. Además, al ser $P$ y $B$ medidas de probabilidad, entonces son positivas. Y la suma de número positivos es positvia.
2. P.d. que $\alpha P(\Omega)+(1-\alpha)Q(\Omega)= 1$.
   Al ser $P$ y $Q$ medidas de probabilidad, entonces $P(\Omega)=Q(\Omega)=1$, por lo tanto tenemos 
   $$
	\alpha P(\Omega)+(1-\alpha)Q(\Omega)=\alpha+1-\alpha=1.
   $$
3. P.d. que es $\sigma$-aditiva. 
   Sea $Z=\alpha P+(1-\alpha)Q$, sabemos que $P\left( \bigcup_{i=1}^{\infty}A_{i} \right)=\sum_{i=1}^{\infty}P(A_{i})$ y $Q\left( \bigcup_{i=1}^{\infty}A_{i} \right)=\sum_{i=1}^{\infty}Q(A_{i})$ para $A_{i}$ disjuntos, entonces 
   $$
	\begin{align}
	Z\left( \bigcup_{i=1}^{\infty}A_{i} \right)&=\alpha P\left( \bigcup_{i=1}^{\infty}A_{i} \right)+(1-\alpha)Q\left( \bigcup_{i=1}^{\infty}A_{i} \right) \\
	&=\alpha(\sum_{i=1}^{\infty}P(A_{i}))+(1-\alpha)(\sum_{i=1}^{\infty}Q(A_{i})) \\
	&=\sum_{i=1}^{\infty}\alpha P(A_{i})+(1-\alpha)Q(A_{i}) \\
	&=\sum_{i=1}^{\infty}Z(A_{i}).\quad\square
	\end{align}
	
   $$

#Probabilidad

