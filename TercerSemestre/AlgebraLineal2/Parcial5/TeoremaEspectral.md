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
c) 