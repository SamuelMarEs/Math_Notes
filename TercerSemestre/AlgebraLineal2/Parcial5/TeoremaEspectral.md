#AlgebraLineal 
###### Observación
Sea ${}V{}$ un espacio de dimensión finita y sea ${}W\subseteq V{}$ con ${}T{}$ la proyección ortogonal de ${}V{}$ sobre ${}W.{}$ Podemos escoger una base ${}\beta=\{ v_{1},\dots,v_{n} \}{}$ tal que ${}\gamma=\{ v_{1},\dots,v_{k} \}\subseteq W{}$. Además ${}V=W\oplus W^{\perp}=R(T)\oplus N(T){}$ y ${}T(v_{k+1})=0{}$, y la matriz asociada a ${}T{}$ queda de la forma 
$$
\begin{pmatrix}
I_{k} & O \\
O & O
\end{pmatrix}.
$$
#### Teorema Espectral
Supongase que ${}T{}$ es un operador lineal en un espacio con producto interno de dimensión finita ${}V{}$ sobre ${}F{}$. Suponga que ${}F{}$ es [[OperadoresNormales|normal]] si ${}F=\mathbb{C}{}$, o [[OperadorHermitiano|auto-adjunto]] si ${}F=\mathbb{R}{}$.
Si ${}\lambda_{1},\dots,\lambda_{n}{}$ son los [[Eigenvectores_Eigenvalores|eigenvalores]] distintos de ${}T{}$, y ${}W_{i}=E_{\lambda i}{}$ correspondiente a ${}\lambda_{i}{}$ y sea ${}T_{i}{}$ la proyección ortogonal de ${}V{}$ sobre ${}W_{i}{}$. Entonces 
a) ${}V=W_{1}\oplus\dots\oplus W_{n}{}$.
b) Si ${}W_{i}’=\bigoplus_{j>i}W_{j}\implies W_{i}^{\perp}=W_{i}’{}$.
c) ${}T_{i}T_{j}=\delta_{ij}T_{i}{}$ para ${}1\leq i,j\leq n{}$.
d) ${}I=T_{1}+\dots+T_{n}{}$.
e) ${}T=\lambda_{1}T_{1}+\lambda_{2}T_{2}+\dots+\lambda_{n}T_{n}{}$.
##### Demostración
a) Por los teoremas 6.16 y 6.17 ${}T{}$ es diagonalizable y por lo tanto ${}V=W_{1}\oplus\dots\oplus W_{n}{}$.
b) Sea ${}x \in W_{i}{}$ y ${}y\in W_{j}{}$, entonces ${}\langle x,y \rangle=0{}$ pues ${}W_{i}{}$ y ${}W_{j}{}$ son eigenespacios distintos, por lo tanto sus elementos son perpendiculares. ([[OperadoresNormales#^c16283|teo 6.15]]) Esto implica que ${}W_{i}’\subseteq W^{\perp}{}$
Además, por el inciso (a), tenemos que ${}\text{dim}(W_{i}’)=\text{dim}(V)-\text{dim}(W_{i}){}$, por otro lado también tenemos que ${}\text{dim}(W^{\perp})=\text{dim}(V)-\text{dim}(W_{i}){}$, por lo tanto las dimensiones de ambas son la misma, pero como uno está contenido en el otro, se tiene que necesariamente ${}W_{i}^{\perp}=W_{i}’{}$.
c) Sea ${}x \in V{}$, tenemos que ${}x=x_{1}+\dots+x_{n}{}$ donde ${}x_{i}\in W_{i}{}$. Entonces tenemos que ${}T_{j}(x)=T_{j}(x_{1})+\dots+T_{j}(x_{n})=T_{j}(x_{j})=x_{j}{}$, por lo tanto ${}T_{i}(T_{j}(x))=T_{i}(x_{j})=\delta_{ij}T_{i}{}$ pues es cero si ${}i\neq j{}$, y de lo contrario es únicamente ${}T_{i}{}$.
d) De forma directa ${}x=x_{1}+\dots+x_{n}{}={}T_{1}(x)+T_{2}(x)+\dots+T_{n}(x)=(T_{1}+\dots+T_{n})(x){}$, por lo tanto ${}I=T_{1}+\dots+T_{n}{}$.
e) Tenemos que ${}T(x)=T(x_{1}+\dots+x_{n})=T(x_{1})+\dots+T(x_{n})=\lambda_{1}x_{1}+\dots+\lambda_{n}x_{n}=\lambda_{1}T_{1}(x)+\dots+\lambda_{n}T_{n}(x){}$.


El conjunto ${}\{ \lambda_{1},\lambda_{2},\dots,\lambda_{n} \}{}$ se llama el ***espectro*** de ${}T{}$. Y ${}T=\lambda_{1}T_{1}+\lambda_{2}T_{2}+\dots+\lambda_{n}T_{n}{}$ se llama la descomposición espectral de ${}T{}$, y es única salvo el orden.
Y tenemos que ${}A=[T]_{\beta}{}$ es la matriz diagonal donde ${}A_{ii}=\lambda_{i}I_{ni}{}$ donde ${}n_{i}{}$ es la dimensión del eigenespacio ${}E_{\lambda i}{}$.

Sea ${}g(T)=g(\lambda_{1})T_{1}+\dots+g(\lambda_{n})T_{n}{}$ donde ${}g{}$ es un polinomio cualquiera. Lo que esto nos dice es que para evaluar una transformación en un polinomio basta con tomar la descomposición espectral del operador, tomando además el polinomio evaluado en cada eigenvalor.

##### Corolario 1
Si ${}F=\mathbb{C}{}$ entonces ${}T{}$ es normal si y sólo si ${}T^{*}=g(T){}$ para algún polinomio ${}g{}$.
###### Demostración:
${}\implies){}$ Supongamos que ${}T{}$ es normal, entonces por el teorema espectral tenemos que ${}T=\lambda_{1}T_{1}+\dots+\lambda_{n}T_{n}{}$, y entonces ${}T^{*}=\overline{\lambda_{1}}T_{1}+\dots+\overline{\lambda_{n}}T_{n}{}$ 