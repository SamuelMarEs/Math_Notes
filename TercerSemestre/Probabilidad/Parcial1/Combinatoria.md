Para poder utilizar la [[ProbabilidadClasica|probabilidad clásica]], tenemos que poder contar los elementos de cada conjunto.
A continuación se enlistan alguno métodos de conteo:

#### Principio de multiplicación
Si se tiene un procedimiento que tiene $n$ formas de realizarse, y un segundo procedimiento con $m$ formas, entonces el número total de formas en las que se pueden realizar ambos procesos, uno seguido del otro es $n\cdot m$.

#### Coeficiente binomial
Suponga que se tienen $n$ elementos y se desea tomar $r$ de ese grupo *sin repetición* y *sin orden*. ¿De cuántas formas se puede hacer?
La solución es el coeficiente binomial, dado por 
$$
	nCr=\begin{pmatrix}
	n \\
	r
	\end{pmatrix}=\frac{n!}{r!(n-r)!}.
$$
También se le llaman las *combinaciones* de $n$ en $r$.

#### Permutaciones
Suponga que el muestro se realiza *sin repetición*, pero *con orden*. Entonces la forma de hacerlo es 
$$
	nPr=\frac{n!}{(n-r)!}.
$$
Estas son las *permutaciones* de $n$ en $r$. Cuando el muestreo es exhaustivo, es decir, cuando $r=n$, entonces  tenemos $n!$.

#### Combinaciones con repetición
Si queremos elegir $r$ elementos de $n$, pero ahora si hay *repetición*, pero no *orden*. Entonces la forma de hacer este cálculo es 
$$
	\begin{pmatrix}
	n+r-1 \\
	r
	\end{pmatrix}=\frac{(n-1+r)!}{r!(n-1)!}.
$$


#Combinatoria #Probabilidad