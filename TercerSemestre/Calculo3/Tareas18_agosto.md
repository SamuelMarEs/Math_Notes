### Determinante 2x2
Encontrar la forma general de la inversa de una matriz de $2\times 2$ mediante el sistema de ecuaciones. 
Sea $A\in M_{2\times 2}$ de la forma 
$$
	A=\begin{pmatrix}
	a & b \\
	c & d
	\end{pmatrix},
$$
y suponiendo que exista la inversa $A^{-1}$ de la forma 
$$
	A^{-1}=\begin{pmatrix}
	x & y \\
	z & w
	\end{pmatrix},
$$
vamos a resolver la ecuación $AA^{-1}=I$, o de otra forma 
$$
	\begin{pmatrix}
	a & b \\
	c & d
	\end{pmatrix}\begin{pmatrix}
	x & y \\
	z & w
	\end{pmatrix}=\begin{pmatrix}
	1 & 0 \\
	0 & 1
	\end{pmatrix},
$$
mediante el siguiente sistema de ecuaciones:
$$
	\begin{cases}
	ax+bz=1 \\
	cx+dz=0 \\
	ay+bw=0 \\
	cy+dw=1.
	\end{cases}
$$
##### Solución:
De la segunda ecuación tenemos que $x=-\frac{dz}{c}$, que se puede reemplazar en la primera ecuación para obtener que 
$$
	\begin{align}
	a\left( -\frac{dz}{c} \right)+bz&=1 \\
	z&=\frac{c}{bc-ad}.
	\end{align}
$$
A partir de esto es inmediato que 
$$
	x=\frac{d}{ad-bc}.
$$
Repitiendo el mismo proceso, pero con las dos ecuaciones de abajo, obtenemos que 
$$
	y=\frac{b}{bc-ad}\quad\text{y}\quad w=\frac{a}{ad-bc}.
$$
Entonces llegamos a que 
$$
	A^{-1}=\begin{pmatrix}
	\frac{d}{ad-bc} & \frac{b}{bc-ad} \\
	\frac{c}{bc-ad} & \frac{a}{ad-bc}
	\end{pmatrix}=\frac{1}{ad-bc}\begin{pmatrix}
	d & -b \\
	-c & a
	\end{pmatrix}.
$$
### Método de Cramer
Sea $A\in M_{n\times n}$ con coeficientes $a_{ij}$. Si $\det(A)\neq 0$, entonces el sistema $Ax=b$ tiene solución $x=(x_{1},\dots,x_{n})^{T}$ tal que 
$$
	x_{i}=\frac{\det(B_{i})}{\det(A)},
$$
donde $B_{i}$ es la matriz obtenida al intercambiar la $i$-ésima columna de $A$ por el vector columna $b$.
##### Demostración:
Dado el sistema $Ax=b$ con $\det(A)\neq 0$, sabemos que la solución única es de la forma 
$$
	x=A^{-1}b,
$$
lo cual se puede reescribir usando la igualdad $A^{-1}=\frac{1}{\det(A)}\text{adj}(A)$, de forma que tenemos: 
$$
	x=\frac{1}{\det(A)}\text{adj}(A)b.
$$
El $i$-ésimo valor del vector solución $x$ está dado por multiplicar la $i$-ésima columna de la matriz adjunta (que tiene los cofactores $C_{ki}$) por el vector columna $b=(b_{1},\dots,bn)$, es decir 
$$
	x_{i}=\frac{C_{1i}b_{1}+C_{2i}b_{2}+\dots+C_{ni}b_{i}}{\det(A)},
$$
donde el numerador es el determinante de $A$ al remplazar la $i$-ésima columna por el vector $b$. Por lo tanto tenemos 
$$
	x_{i}=\frac{\det(B_{i})}{\det(A)}.\quad\square
$$

### Software para encontrar inversas
En el lenguaje de programación Python, usando la libreria numpy (np), se puede calcular la inversa de una matriz de la siguiente forma:
~~~python
import numpy as np
# Definimos una matriz
A = np.array([1,2],
			 [3,4])
# Calculamos la inversa
A_inv = np.linalg.inv(A)
~~~

### Balanceo de ecuaciones químicas
Plantear un sistema para resolver 
$$
	pC_{3}H_{4}O_{3}+qO_{2}=rCO_{2}+sH_{2}O,
$$
y hallar la menor solución entera positiva posible para $p,q,r$ y $s$. Decir si es consistente, inconsistente, determinado o indeterminado.
##### Solución:
Podemos plantear un sistema de 3 ecuaciones y 4 incógnitas, donde los coeficientes son las cantidades de cada elemento: 
$$
	\begin{cases}
	3p=r \quad\text{(Carbono)}\\
	4p=2s \quad\text{(Hidrógeno)}\\
	3p+2q=2r+s \quad\text{(Oxígeno)}.
	\end{cases}
$$
Sustituyendo $s$ y $r$ en la última ecuación, tenemos 
$$
	3p+2q=6p+2p \implies 5p=2q.
$$
Estas ecuaciones forman un sistema consistente indeterminado, pues si bien tiene solución, esta no es única.
Entonces, escribiendo todas las variables en términos de $p$ tenemos: 
$$
	r=3p,\quad s=2p,\quad\text{y}\quad q=\frac{5}{2}p.
$$
Dado que queremos una solución entera, y como $q=\frac{5}{2}p$, entonces $p$ debe ser par. El entero par más chico es $p=2$, con el cual obtenemos la solución 
$$
	p=2,\quad r=6,\quad s=4,\quad\text{y}\quad q=5.
$$
Por lo tanto nuestra ecuación balanceada es 
$$
	2C_{3}H_{4}O_{3}+5O_{2}=6CO_{2}+4H_{2}O.
$$


#Calculo #AlgebraLineal 