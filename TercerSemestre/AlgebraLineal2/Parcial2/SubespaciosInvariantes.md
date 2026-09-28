#AlgebraLineal 
Queremos demostrar que toda matriz es solución de su polinomio característico.
Es decir, sea $f(t)=a_{0}+a_{1}t+\dots+a_{k}t^{k}$ el polinomio característico de una transformación $T$, entonces tenemos que $f([T]_{\beta})=0=T_{0}$ la transformación cero.

#### Definición:
Sea $T$ un operador lineal sobre un espacio vectorial de dimensión finita $V$. Un subespacio $W$ de $V$ se llama ***subespacio $T$-invariante***  de $V$ si 
$$
	T(v)\in W,\forall v\in W.
$$
Algunos ejemplos son:
- $\{ 0 \}$. (Trivial)
- $V$. (Trivial)
- $R(T)$, si tomas un elemento de la imagen, su imagen esta en la imagen, duh uh.
- $N(T)$, todos mandan al cero, que esta en $N(T)$.
- $E_{\lambda}$, es decir que los [[Eigenespacios|eigenespacios]] son subespacios invariantes. $v\in W\implies T(v)=\lambda v\in W.$

##### Ejemplo:
Sea $T$ sobre $R^{3}$ definida como 
$$
	T(a,b,c)=(a+b,b+c,0),
$$
el plano $xy=\{ (x,y,0)|x,y\in R \}$ y el eje $x=\{ (x,0,0)|x\in R \}$ son subespacios $T$-invariantes de $V$. Es facil verlo si transformamos cualquier vector genérico dentro de ellos.

#### Definición:
Sea $x\neq 0$. El subespacio $W=\text{span}\{ x,T(x),T^{2}(x),\dots \}$ se llama el ***subespacio $T$-ciclico*** generado por $x$.
Es el subespacio $T$-invariante más pequeño que contiene a $x$. Es decir que cualquier otro subespacio $T$-invariante que contenga a $x$, también contiene a $W$.

#### Teorema 5.20
Sea $T$ un operador lineal sobre un espacio de dimensión finita $V$, y sea $W$ un subespacio $T$-invariante de $V$. Entonces, el polinomio característico de $[T_{W}]$ divide al polinomio característico de $T$.
##### Demostración:
Sea $\gamma=\{ v_{1},v_{2},\dots,v_{k} \}$ una base ordenada de $W$, y la extendemos a una base $\beta=\{ v_{1},\dots,v_{k},v_{k+1},\dots,v_{n} \}$ una base de $V$. Sea $A=[T]_{\beta}$ y $B=[T_{W}]_{\gamma}$. Sabemos que $A$ se puede escribir como 
$$
	A=\begin{pmatrix}
	B_{1} & B_{2} \\
	0 & B_{3}
	\end{pmatrix}
$$
Como $W$ es un subespacio $T$-invariante, tenemos que $T(v_{1})$ es combinación de $\gamma$.
Sea $f(t)$ el polinomio característico de $T$, y $g(t)$ el polinomio característico de $T_{W}$. Tenemos que 
$$
	f(t)=\det(A-tI)=\det(B_{1}-tI)\det(B_{3}-tI),
$$
pero como $B_{1}$ esla matriz asociada a $T_{W}$, tenemos que 
$$
	f(t)=g(t)q(t),
$$
dónde $q(t)=\det(B_{3}-tI)$, aunque no nos interesa en específico su forma. Con esto, tenemos que $g(t)$ divide a $f(t).\quad\square$
