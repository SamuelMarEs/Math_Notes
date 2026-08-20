### Sección 2.1 Friedberg
Para los ejercicios 2-6, probar que $T$ es una transformación lineal, encontrar bases de $N(T)$ y $R(T)$, calcular sus dimensiones, y verificar si $T$ es inyectiva o suprayectiva.
2. $T:R^{3}\to R^{2}$ definida por $T(a_{1},a_{2},a_{3})=(a_{1}-a_{2},2a_{3})$.
   **Sol:**
   Sean $(a_{1},a_{2},a_{3}),(b_{1},b_{2},b_{3})\in R^{3}$ y $\lambda\in R$. Entonces $$
	\begin{align}
	T(\lambda a_{1}+b_{1},\lambda a_{2}+b_{2},\lambda a_{3}+b_{3})&=(\lambda a_{1}+b_{1}-\lambda a_{2}-b_{2},2\lambda a_{3}+2b_{3}) \\
	&=\lambda( a_{1}-a_{2},2a_{3})+(b_{1}-b_{2},2b_{3}) \\
	&=\lambda T(a_{1},a_{2},a_{3})+T(b_{1},b_{2},b_{3}).
	\end{align}
   $$
   Además tenemos que $N(T)=\{ (a,a,0):a\in R \}$ y una base es $\{ (1,1,0)\}$, por lo tanto $\text{dim}(N(T))=1$, es decir que $\text{dim}(R(T))=2$, y una base es la canónica $\{ (1,0),(0,1) \}$.
   Dado que $N(T)\neq \{ 0 \}$, entonces $T$ no es inyectiva. Por otro lado, tenemos que $R(T)=R^{2}$, por lo tanto $T$ es suprayectiva.
   
3. $T:R^{2}\to R^{3}$ definida por $T(a_{1},a_{2})=(a_{1}+a_{2},0,2a_{1}-a_{2})$.
   **Sol:**
   Sean $(a_{1},a_{2}),(b_{1},b_{2})\in R^{2}$ y $\lambda\in R$. Entonces $$
	\begin{align}
	T(\lambda a_{1}+b_{1},\lambda a_{2}+b_{2})&=(\lambda a_{1}+b_{1}+\lambda a_{2}+b_{2},0,2(\lambda a_{1}+b_{1})-\lambda a_{2}-b_{2}) \\
	&=\Lambda(a_{1}+a_{2},0,2a_{1}-a_{2})+(b_{1}+b_{2},0,2b_{1}-b_{2}) \\
	&= \lambda T(a_{1},a_{2})+\lambda T(b_{1},b_{2}).
	\end{align}
   $$
   Tenemos entonces que $N(T)=\{ (a_{1},a_{2}):a_{1}=-a_{2},2a_{1}=a_{2} \}=\{ 0 \}$, por lo tanto $\text{dim}(N(T))=0$, y entonces $\text{dim}(R(T))=2$. Dado que $N(T)=\{ 0 \}$, entonces $T$ es inyectiva. Sin embargo, no existe $x\in R^{2}$ tal que $T(x)=(0,1,0)$, por lo tanto $T$ no es suprayectiva.
   
4. $T:M_{2\times 3}(F)\to M_{2\times 2}(F)$ definida por $$
   	T\begin{pmatrix}
	a_{11} & a_{12} & a_{13} \\
	a_{21} & a_{22} & a_{23}
	\end{pmatrix}=\begin{pmatrix}
	2a_{11}-a_{12} & a_{13}+2a_{12} \\
	0 & 0
	\end{pmatrix}.
   $$
   **Sol:**
   La transformación no involucra a la segunda fila de la matriz, entonces podemos verla como una transformación $T:R^{3}\to R^{2}$, al menos para verificar que sea lineal. Sean $(a_{1},a_{2},a_{3}),(b_{1},b_{2},b_{3})\in R^{3}$ y $\lambda\in R$, tenemos que $$
	\begin{align}
	T(\lambda a_{1}+b_{1},\lambda a_{2}+b_{2},\lambda b_{3}+b_{3})&=(2(\lambda a_{1}+b_{1})+\lambda a_{2}+b_{2},\lambda a_{3}+b_{3}+2(\lambda a_{2}+b_{2})) \\
	&=\lambda(2a_{1}+a_{2},a_{3}+2a_{2})+(2b_{1}+b_{2},b_{3}+2b_{2}) \\
	&=\lambda T(a_{1},a_{2},a_{3})+T(b_{1},b_{2},b_{3}).
	\end{align}
   $$
   $N(T)=\{ A\in M_{2\times 3}(F):4a_{11}=2a_{12}=-a_{13}\}$ y una base es 
   $$
	\{ \begin{pmatrix}
	4 & 2 & -1 \\
	0 & 0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 & 0 \\
	1 & 0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 & 0 \\
	0 & 1 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 & 0 \\
	0 & 0 & 1
	\end{pmatrix} \},
   $$
   por lo tanto $\text{dim}(N(T))=4$, y entonces $\text{dime}(R(T))=2$. Dado que $N(T)\neq \{ 0 \}$, $T$ no es inyectiva. Además $\text{dim}(R(T))\neq\text{dim}(M_{2\times 2}(F))$, por lo tanto tampoco es suprayectiva.
   
5. $T:P_{2}(R)\to P_{3}(R)$ definida por $T(f(x))=xf(x)+f'(x)$.
6. $T:M_{n\times n}(F)\to F$ definida por $T(A)=\text{tr}(A)$. La traza de $A$ dada por 
   $$
   	\text{tr}(A)=\sum_{i=1}^{n}a_{ii}.
   $$

7.- Probar las propiedades:
   - Si $T:V\to W$ es lineal, entonces $T(\vec{0}_{v})=\vec{0}_{w}$. 
   - $T(r\vec{x}+\vec{y})=rT(\vec{x})+T(\vec{y})$.
   - $T(\vec{x}-\vec{y})=T(\vec{x})-T(\vec{y})$.
   - $T\left( \sum_{i=1}^{n}a_{i}x_{i} \right)=\sum_{i=1}^{n}a_{i}T(x_{i})$.
    **Solución:**
     Sea $T:V\to W$ una transformación lineal. Dado que $F$ es un campo, entonces $0\in F$, por lo tanto tenemos que $0\vec{x}=\vec{0}_{W}$ para todo $\vec{x}\in W$. Por lo tanto tenemos que 
   $$
   	T(\vec{0}_{V})=T(0\vec{x})=0T(\vec{x})=\vec{0}_{W}.\quad \square 
   $$
	Como $T$ es lineal, entonces tenemos que 
   $$
   	\begin{align}
	T(r\vec{x}+\vec{y})&=T(r\vec{x})+T(\vec{y}) \\
	&= rT(\vec{x})+T(\vec{y}).\quad\square
	\end{align}
   $$
	Podemos reescribirlo de la forma 
   $$
   	T(\vec{x}-\vec{y})=T(\vec{x}+(-1\cdot\vec{y}))=T(\vec{x})+T(-1\cdot \vec{y})=T(\vec{x})-T(\vec{y}).\quad\square
   $$
	Es inmediato que, dado que $T$ es lineal, entonces  $$
	     	T\left( \sum_{i=1}^{n}a_{i}x_{i} \right)=T(a_{1}x_{1}+\dots+a_{n}x_{n})=a_{1}T(x_{1})+\dots+a_{n}T(x_{n})=\sum_{i=1}^{n}a_{i}T(x_{i}).\quad\square
	     $$


11.- Probar que existe una transformación lineal $T:R^{2}\to R^{2}$ tal que $T(1,1)=(1,0,2)$ y $T(2,3)=(1,-1,4)$.

13.- Sean $V$ y $W$ espacios vectoriales, sea $T:V\to W$ lineal y sea $\{ w_{1},w_{2},\dots,w_{k} \}$ un conjunto de $k$ vectores linealmente independientes de $R(T)$. Probar que si $S=\{ v_{1},\dots,v_{k} \}$ se eligen tal que $T(v_{i})=w_{i}$ para $i=1,\dots,k$, entonces $S$ es linealmente independiente.

15.- Definamos 
$$
	T:P(R)\to P(R) \quad\text{como}\quad T(f(x))=\int_{0}^{x}f(t)dt.
$$
Probar que $T$ es linear e inyectiva, pero no suprayectiva.

16.- Sea $T:P(R)\to P(R)$ definida como $T(f(x))=f'(x)$. $T$ es lineal. Probar que $T$ es suprayectiva, pero no inyectiva.


 