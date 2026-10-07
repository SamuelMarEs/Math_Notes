#Probabilidad 
Suponga que se tienen $K$ objetos de tipo 1, y $N-K$ objetos de tipo 2. Se toma una muestra de tamaño $n$ de esta población sin repetición y sin orden.
Sea $X$ la [[VariablesAleatorias|v.a.]] que indica el número de individuos de tipo 1, tenemos que $X$ puede tomar valores $\{ 0,1,2,\dots,\min(n.K) \}$.
La [[FuncionDeProbabilidad|función de probabilidad]] de esta v.a., es decir la probabilidad de que haya $x$ objetos de tipo 1 en nuestra muestra de tamaño $n$, va a estar dada por 
$$
	P(X=x)=\frac{{K\choose x}{N-K\choose x-n}}{{N\choose n}},\quad x\in \{ 0,1,\dots,\min(n,K) \}.
$$
A este tipo de v.a. se les conoce como variables aleatorias Hipergeométricas de parámetros $(n,N,K)$.
Se puede demostrar que 
$$
	E(X)=n \frac{K}{N},\quad Var(X)= n \frac{K}{N} \frac{N-K}{N} \frac{N-n}{N-1}.
$$
