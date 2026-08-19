Existen tres tipos de operaciones elementales sobre [[Matrices|matrices]]:
1. Multiplicar un renglón por un escalar no cero.
2. Intercambiar dos renglones.
3. Sumar un múltiplo de un renglón a otro.
Las mismas tres operaciones elementales se pueden realizar para columnas.

***Nota:*** cada operación elemental se puede ver como el producto matricial con una matriz elemental. Aunque esto se generaliza con el teorema siguiente.

##### Teorema
Sea $A\in M_{m\times n}(F)$, y supongamos que $B$ es obtenida a partir de $A$ mediante operaciones elementales de renglones o columnas. Existe una $m\times m\quad[n\times n]$ matriz elemental $E$ tal que $B=EA\quad [B=AE]$. De hecho, $E$ es obtenible de $I_{m}\quad[I_{n}]$ mediante las mismas operaciones elementales utilizadas en $A$ para obtener $B$. 
De la misma forma, si $E$ es una matriz elemental $m\times m\quad[n\times n]$, entonces $EA\quad[AE]$ es la matriz obtenida a partir de $A$ al realizar las mismas operaciones elementales para obtener $E$ a partir de $I_{m}\quad[I_{n}]$.


Si una matriz es invertible se puede llevar mediante operaciones elementales a la matriz $I$ (identidad). Es decir, una matriz $A$ es invertible si existen $E_{1},\dots,E_{n}$ tales que 
$$
	A=\prod_{i=1}^{n}E_{n}I.
$$
Esto es lo que se conoce como el método Gauss Jordan.


#AlgebraLineal