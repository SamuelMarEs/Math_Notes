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
a) ${}V=W_{1}\oplus\dots\oplus W_{n}{}$
b) Si ${}W_{i}’={}$