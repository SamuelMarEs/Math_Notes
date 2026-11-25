#AlgebraLineal 
#### Definición
Sean ${}A,B\in M_{n\times n}(F){}$. Se dice que ${}B{}$ es ***congruente*** con ${}A{}$ si existe una matriz invertible ${}Q\in M_{n\times n}(F){}$ tal que 
$$
B=Q^{t}AQ.
$$
Se puede mostrar que la relación de congruencia es una relación de equivalencia.

#### Teorema 6.33
Sea ${}V{}$ un espacio vectorial de dimensión finita con bases ordenadas ${}\beta=\{ v_{1},\dots,v_{n} \}{}$ y ${}\gamma=\{ w_{1},\dots,w_{n} \}{}$. Sea ${}Q{}$ la matriz de cambio de base de ${}\gamma{}$ a ${}\beta{}$. Entonces para cualquier [[FormasBilineales|forma bilineal]] ${}H\in \mathcal{B}(V){}$, se tiene que 
$$
\psi_{\gamma}(H)=Q^{t}\psi_{\beta}(H)Q.
$$
Por lo tanto, las matrices asociadas a una forma bilineal en distintas bases son congruentes.

A partir de la relación de congruencia entre matrices, surge el problema de determinar aquellas formas bilineales que admiten representaciones matriciales diagonales. Veremos que existe una estrecha relación entre la simetría de una matriz y las formas bilineales diagonalizables.

####