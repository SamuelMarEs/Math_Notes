##### Definición:
Sean $V$ y $W$ [[EspaciosVectoriales|espacios vectoriales]] sobre un campo $F$. Sean $\vec{x}, \vec{y}\in V$ y $r\in F$.
Una transformación lineal entre $V$ y $W$ es una función $T:V\to W$ que satisface
1. $T(\vec{x}+\vec{y})=T(\vec{x})+T(\vec{y})$.
2. $T(r\vec{x})=rT(\vec{x})$.
Esto se puede interpretar como que $T$ es una función que "preserva la estructura".

#### Primeras consecuencias:
1. Si $T:V\to W$ es lineal, entonces $T(\vec{0}_{v})=\vec{0}_{w}$. 
2. $T(r\vec{x}+\vec{y})=rT(\vec{x})+T(\vec{y})$.
3. $T(\vec{x}-\vec{y})=T(\vec{x})-T(\vec{y})$.

##### Demostración:
1. Sea $T:V\to W$ una transformación lineal. Dado que $F$ es un campo, entonces $0\in F$, por lo tanto tenemos que $0\vec{x}=\vec{0}_{w}$ para todo $\vec{x}\in W$. Por lo tanto tenemos que 
   $$
   	T(0\vec{x})=0T(\vec{x})=\vec{0}_{w}.\quad \square 
   $$
2. Como $T$ es lineal, entonces tenemos que 
   $$
   	\begin{align}
	T(r\vec{x}+\vec{y})&=T(r\vec{x})+T(\vec{y}) \\
	&= rT(\vec{x})+T(\vec{y}).\quad\square
	\end{align}
   $$
3. Podemos reescribirlo de la forma 
   $$
   	T(\vec{x}-\vec{y})=T(\vec{x}+(-1\cdot\vec{y}))=T(\vec{x})+T(-1\cdot \vec{y})=T(\vec{x})-T(\vec{y}).\quad\square
   $$

#### Ejemplos
1. Sean $V=W=\mathbb{R}^{2}$:
	1. $T(a_{1},a_{2})=(a_{1},-a_{2})$ es una transformación que refleja a los vectores sobre el eje $y$. Se le llama una ***reflexión*** sobre el eje $y$.
	2. $T(a_{1},a_{2})=(a_{1},0)$ es una transformación lineal que "aplasta" los vectores sobre el eje $x$. Recibe el nombre de una ***proyección*** sobre el eje $x$.
	3. $T(a_{1},a_{2})=$ que es una ***rotación*** por el ángulo $\theta$.
2. Sea $V=M_{n\times m}$ y $W=M_{m\times n}$. Podemos definir $T(A)=A^{t}$ la transpuesta de la matriz $A$.
3. $T:P_{n}(\mathbb{R})\to P_{n-1}(\mathbb{R})$ tal que $T(p)=p'$ la derivada.
4. $T:C(\mathbb{R})\to C(\mathbb{R})$ donde $C(\mathbb{R})$ denota las funciones continuas sobre los reales, y $T(f)=\int f$.

#AlgebraLineal