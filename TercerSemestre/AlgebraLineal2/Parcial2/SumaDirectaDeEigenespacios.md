#AlgebraLineal #Teorema
#### Teorema 5.10
Sean $W_{1},W_{2},\dots,W_{k}$ subespacios vectoriales de un espacio de dimensión finita $V$.
Los siguientes enunciados son equivalentes:
a) $V=W_{1}\oplus W_{2}\oplus\dots \oplus W_{k}$.

b) $V=\sum_{i=1}^{k}W_{i}$ y para cualesquiera vectores $v_{1},\dots,v_{k}$ tales que $v_{i}\in W_{i}$, $1\leq i\leq k$. Si $v_{1}+\dots+v_{k}=0$ entonces $v_{i}=0$ para todo $i$.

c) Cada vector $v\in V$es escrito de manera única $v=v_{1}+\dots+v_{k}$ con $1\leq i\leq k$ y $v_{i}\in W_{i}.$

d) Si $\gamma_{i}$ es una base ordenada de $W_{i}$,$1\leq i\leq k$, entonces $\gamma_{1}\cup \gamma_{2}\cup\dots\cup \gamma_{k}$ es una base ordenada de $V$.

e) Para cada $i=1,2,\dots,k$, existe una base ordenada $\gamma_{i}\subset W_{i}$ tal que $\gamma_{1}\cup \gamma_{2}\cup\dots\cup \gamma_{k}$ es una base ordenada de $V$.
##### Demostración:
a)$\implies$b)
Supongamos que $V=W_{1}\oplus W_{2}\oplus\dots \oplus W_{k}$. Esto implica que $V=\sum_{i=1}^{k}W_{i}$ y $W_{i}\cap W_{j}=\emptyset$, por lo que ya tenemos la primera parte de b).
Sabemos que $v_{i}\in W_{i}$ para cualquier $1\leq i\leq k$. Entonces 
$$
	v_{1}=-(v_{2}+v_{3}+\dots+v_{k})
$$
con $v_{1}\in W_{1}$ y $(v_{2}+v_{3}+\dots+v_{k})\in \sum_{j\neq 1}W_{j}$, pero la intersección de estos dos es únicamente el vector cero (por ser suma directa), por lo tanto $v_{1}=0$. De forma análoga se demuestra que los demás vectores son también cero. $\quad\square$

b)$\implies$c)
Supongamos que $V=\sum W_{i}$ y que $v_{1}+v_{2}+\dots+v_{k}=0\implies v_{i}=0$ para $1\leq i\leq k$.
Supongamos que $v=v_{1}+\dots+v_{k}$ con $v_{i}\in W_{i}$, y además supongamos que se puede escribir como $v=w_{1}+\dots+w_{k}$ con $w_{i\in W_{k}}$. Entonces tenemos que 
$$
	0=(v_{1}-w_{1})+(v_{2}-w_{2})+\dots+(v_{k}-w_{k}),
$$
y por hipótesis esto implica que $v_{i}=w_{i}$ para $1\leq i\leq k$.

c)$\implies$d)
Supongamos que cada vector en $V$ se puede escribir de manera única usando vectores de los subespacios $W_{i}$. Para cada $i$, construimos una base ordenada $\gamma_{i}$ de $W_{i}$. Entonces tenemos que 
$$
	\gamma_{1}\cup \gamma_{2}\cup\dots\cup \gamma_{k}
$$
genera a $V$, pues independientemente cada base genera a $W_{i}$.
(Pendiente)

d)$\implies$e)
Sabemos que para cualquier conjunto de bases ordenadas $\gamma_{i}$ de $W_{i}$, se cumple que $\gamma_{1}\cup \gamma_{2}\cup\dots\cup \gamma_{k}$, y por lo tanto existe alguna en particular, probando e).

e)$\implies$a)


#### Teorema 5.11
Un operador lineal $T$ en un espacio vectorial de dimensión finita $V$ es [[Diagonalizabilidad|diagonalizable]] si y sólo si $V$ es suma directa de los [[Eigenespacios|eigenespacios]] de $T$.
##### Demostración:
Sean $\lambda_{1},\lambda_{2},\dots,\lambda_{k}$ [[Eigenvectores_Eigenvalores|eigenvalores]] distintos de $T$.
$\Rightarrow)$ Para cada $i$ escogemos una base ordenada $\gamma_{i}$ de $E_{\lambda i}$. Por el teorema 5.9 tenemos que $\gamma_{1}\cup\dots\cup \gamma_{k}$ es una base de $V$, y entonces por el teorema 5.10 tenemos que 
$$
	V=E_{\lambda_{1}}\oplus \dots \oplus E_{\lambda k}.
$$
$(\Leftarrow$ Ahora supongamos que $V=E_{\lambda_{1}}\oplus\dots \oplus E_{\lambda k}$, y escogamos una base $\gamma_{i}$ de $E_{\lambda i}$, que necesariamente tiene que ser una base de eigenvectores. Entonces, nuevamente por el teorema 5.10, sabemos que 
$$
	\gamma_{1}\cup \gamma_{2}\cup\dots\cup \gamma_{k}
$$
es una base de $V$, además de que como cada una es una base de eigenvectores, entonces la unión también es una base de eigenvectores, y por lo tanto $T$ es diagonalizable. $\quad\square$
