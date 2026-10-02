#Probabilidad 
Suponga que se tiene un experimento o fenómeno aleatorio en el que se define una [[DistribucionBernoulli|v.a. Bernoulli]]. Supongamos además que el experimento se puede repetir $n$ veces de forma independiente (el resultado de una repetición no afecta a la siguiente). Más aún, supongamos que la probabilidad de éxito no cambia entre repeticiones.

Sea $X$ la [[VariablesAleatorias|v.a.]] que cuenta el número de éxitos en las $n$ repeticiones. Entonces, es claro que $X\in \{ 0,1,\dots,n \}$.
La [[FuncionDeProbabilidad|función de probabilidad]] de $X$ está dada por 
$$
	f(x)=P(X=x)=\begin{cases}
	\begin{pmatrix}
	n  \\
	x
	\end{pmatrix}p^{x}(1-p)^{n-x}, & x\in \{ 0,1,\dots,n \} \\
	0, & \text{en otro caso},
	\end{cases}
$$
dónde $p$ es la probabilidad de tener un éxito al realizar el experimento.
A esta v.a. se le conoce como v.a. ***Binomial*** de parámetros $n$ y $p$, i.e. 
$$
	X\sim\text{Binomial}(n,p).
$$
Se puede demostrar (tarea) que el [[ValorEsperado|valor esperado]] y la [[Varianza_DesviacionEstandar|varianza]] son 
$$
	E(X)=np,\quad Var(X)=np(1-p).
$$
r