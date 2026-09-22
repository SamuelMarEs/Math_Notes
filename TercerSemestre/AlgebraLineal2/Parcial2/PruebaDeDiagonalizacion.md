#AlgebraLineal
Sea $T$ un operador lineal en un espacio $n$-dimensional $V$. Entonces $T$ es diagonalizable si y sólo si ambas condiciones se cumplen:
1. El polinomio característico de $T$ se descompone sobre $F$.
2. Para cada eigenvalor $\lambda$ de $T$, la multiplicidad de $\lambda$ es igual a $n-\text{rank}(T-\lambda I).$

#### Ejemplos:
1.- Sea $A=\begin{pmatrix}3 & 1 & 0 \\  0 & 3 & 0 \\  0 & 0 & 4\end{pmatrix}$, ¿es diagonalizable?
**Sol:**
El polinomio característico es $f(t)=(3-t)^{2}(4-t)$, entonces los valores propios son $\lambda_{1}=3$ y $\lambda_{2}=4$ con multiplicidades de $m_{1}=2$ y $m_{2}=1$ respectivamente. Notemos que el rango de $T-3I$ es el rango de 
$$
	\text{rank}\begin{pmatrix}
	0 & 1 & 0 \\
	0 & 0 & 0 \\
	0 & 0 & 1
	\end{pmatrix}=2,
$$
pero tenemos que $n=3$, por lo tanto $3-2=1\neq m_{1}$. Por lo tanto $A$ no es diagonalizable.


2.- Sea $T$ un operador lineal sobre $P_{2}(R)$ definido como 
$$
	T(f(x))=f(1)+f'(0)x+(f'(0)+f''(0))x^{2}.
$$
¿Es diagonalizable? Encuentra la base de eigenvectores 
**Sol:**
Observemos que $T(1)=1, T(x)=1+1x+1x^{2}$ y $T(x^{2})=1+0x+2x^{2}$, por lo tanto 
$$
	[T]_{\beta}=\begin{pmatrix}
	1 & 1 & 1 \\
	0 & 1 & 0 \\
	0 & 1 & 2
	\end{pmatrix}.
$$
El polinomio característico es $f(t)=(1-t)^{2}(2-t)$, y por lo tanto los eigenvalores son $\lambda_{1}=1,\lambda_{2}=2$ con multiplicidades $m_{1}=2,m_{2}=1$.
Para $\lambda_{1}=1$, tenemos que 
$$
	\text{rank}\begin{pmatrix}
	0 & 1 & 1 \\
	0 & 0 & 0 \\
	0 & 1 & 1
	\end{pmatrix}=1,
$$
y $n=3$, de modo que tenemos que $3-1=2=m_{1}$.
Ahora para $\lambda_{2}=2$, tenemos que 
$$
	\text{rank}\begin{pmatrix}
	-1 & 1 & 1 \\
	0 & -1 & 0 \\
	0 & 1 & 0
	\end{pmatrix}=2,
$$
y entonces tenemos que $3-2=1=m_{2}$.
Es decir que las multiplicidades coinciden, por lo tanto $T$ si es diagonalizable.
Ahora vamos a encontrar la base de eigenvectores.
Para $\lambda_{1}=1$, tenemos 
$$
	\begin{pmatrix}
	0 & 1 & 1 \\
	0 & 0 & 0 \\
	0 & 1 & 1
	\end{pmatrix}\begin{pmatrix}
	x \\
	y \\
	z
	\end{pmatrix}=\bar{0}.
$$
Esto nos da la ecuación $y=-z$, entonces podemos fijar parámetros $s$ y $t$ tales que $x=t,y=-s,z=s$, de modo que los eigenvectores son 
$$
	v_{1}=\begin{pmatrix}
	0 \\
	-1 \\
	1
	\end{pmatrix}, \quad v_{2}=\begin{pmatrix}
	1 \\
	0 \\
	0
	\end{pmatrix}.
$$
Ahora, para $\lambda_{2}=2$, tenemos 
$$
	\begin{pmatrix}
	-1 & 1 & 1 \\
	0 & -1 & 0 \\
	0 & 1 & 0
	\end{pmatrix}\begin{pmatrix}
	x \\
	y \\
	z
	\end{pmatrix}=\bar{0},
$$
de lo que obtenemos que $y=0$ y $x=z$, entonces tenemos el vector $v_{3}=\begin{pmatrix}1 \\  0 \\  1\end{pmatrix}$. Entonces una base de eigenvectores es como en la siguiente matriz 
$$
	Q=\begin{pmatrix}
	1 & 0 & 1 \\
	0 & -1 & 0 \\
	0 & 1 & 1
	\end{pmatrix},
$$
y entonces si hacemos $D=Q^{-1}[T]_{\beta}Q$, tenemos que 
$$
	D=\begin{pmatrix}
	1 & 0 & 0 \\
	0 & 1 & 0 \\
	0 & 0 & 2
	\end{pmatrix}.
$$