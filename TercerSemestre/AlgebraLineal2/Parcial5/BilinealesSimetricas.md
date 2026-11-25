#AlgebraLineal 
#### Definición
Una [[FormasBilineales|forma bilineal]] ${}H{}$ sobre un espacio ${}V{}$ es simétrica si 
$$
H(x,y)=H(y,x)
$$
para todo ${}x,y\in V{}$.
Como el nombre lo indica, no es difícil demostrar que una forma bilineal ${}H{}$ es simétrica si y sólo si ${}\psi_{\beta}(H){}$ es una matríz simétrica. (Teorema 6.34).
Así mismo, la siguiente definición también es intuitiva dado el nombre:
#### Definición:
Una forma bilineal ${}H{}$ sobre un espacio ${}V{}$ de dimensión finita se llama ***diagonalizable*** si existe una base ordenada ${}\beta \subset V{}$ tal que ${}\psi_{\beta}(H){}$ es una matriz diagonal.

Además, es trivial ver que si ${}H{}$ es diagonalizable, entonces ${}H{}$ es simétrica. Sin embargo, el regreso de esta afirmación no necesariamente se satisface, y de hecho puede depender hasta del campo ${}F{}$. Pero aún así, si ponemos algunas restricciones sobre ${}F{}$ (básicamente que no sea ${}\mathbb{Z}_{2}{}$), entonces tenemos el siguiente teorema

#### Teorema 6.35
Sea ${}V{}$ un espacio vectorial de dimensión finita sobre un campo ${}F{}$ de característica distinta de dos. Entonces toda forma bilineal simétrica sobre ${}V{}$ es diagonalizable.
Como corolario, si ${}A{}$ es simétrica, entonces ${}A{}$ es congruente con una matriz diagonal.

Ya que tenemos este teorema, podemos pasar las cuentitas, como encontramos una matriz diagonal congruente con una matriz simétrica. 
Sabemos que si ${}A{}$ es simétrica, existen ${}Q,D{}$ tales que ${}Q{}$ es invertible y ${}D{}$ diagonal, y 
$$
Q^{t}AQ=D.
$$
Esto se hace mediante el mismo proceso que llevamos haciendo desde secciones anteriores para hallar matrices ortogonalmente equivalentes:

1.- Encontramos los eigenvalores de ${}A{}$ encontrando las raíces de ${}\det(A-\lambda I)=0{}$.
2.- Encontramos los eigenvectores asociados a cada eigenvalor resolviendo el sistema ${}(A-\lambda_{i}I)(x)=0{}$.
3.- Ortonormalizamos la base de eigenvectores ${}\{ x_{1},\dots,x_{n} \}{}$ en una base ortonormal ${}\{ v_{1},\dots,v_{n} \}{}$.
4.- Fijamos ${}Q=[v_{1},\dots,v_{n}]{}$ y ${}D=\mathrm{diag}(\lambda_{1},\dots,\lambda_{n}){}$.