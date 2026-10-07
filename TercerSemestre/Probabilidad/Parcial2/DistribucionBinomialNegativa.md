#Probabilidad 
Suponga que se tiene una sucesión de [[VariablesAleatorias|v.a.]] [[DistribucionBernoulli|Bernoulli]] [[V.A.Independientes|independientes]] con probabilidad de éxito $p$ constante. 
Definimos la v.a. $X$ como el número de fallas hasta el $r$-ésimo éxito. Es decir, cuantas veces fallamos hasta obtener $r$ éxitos. Notemos que la [[DistribucionGeometrica|distribución geométrica]] es un caso especial de esta v.a. para $r=1$.
Tenemos que $X$ puede tomar valores en $\{ 0,1,2,\dots \}$, y su [[FuncionDeProbabilidad|función de probabilidad]] va a estar dada por 
$$
	 f(x)=P(X=x)=\begin{cases}
	 {x+r-1\choose x}p^{x}(1-p)^{x}, & x=0,1,\dots \\
	 0, & \text{en otro caso.}
	 \end{cases}
$$
Se puede entonces demostrar que 
$$
	E(X)=\frac{r(1-p)}{p},\quad Var(X)=\frac{r(1-p)}{p^{2}}.
$$
A este tipo de variables se les conoce como variables aleatorias Binomiales Negativas de parámetros $r$ y $p$.