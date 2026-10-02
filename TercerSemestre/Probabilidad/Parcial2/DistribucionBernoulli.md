#Probabilidad 
Sea $X$ una [[VariablesAleatorias|v.a.]] binaria con valores 
$$
	X=\begin{cases}
	1, & \text{éxito}; \\
	0, & \text{fracaso}.
	\end{cases}
$$
(La definición de éxito y fracaso dependerá del experimento aleatorio).
Supongamos que la probabilidad de éxito es $p$, y consecuentemente la probabilidad de fracaso es $1-p$.
Entonces, la [[FuncionDeProbabilidad|función de probabilidad]] de $X$ se puede escribir como 
$$
	f(x)=P(X=x)=\begin{cases}
	p^{x}(1-p)^{1-x}, & x=0,1 & p\in(0,1); \\
	0, & \text{en otro caso.}
	\end{cases}
$$
A esta v.a. se le conoce como una v.a. ***Bernoulli*** con prámetro $p$, y se denota como 
$$
	X\sim\text{Bernoulli}(p),
$$
que se lee como que $X$ sigue una distribución Bernoulli con parámetro $p$.
Se tiene una familia de modelos determinados por el parámetro $p$, que se conoce como probabilidad de éxito.
Se sigue entonces que la [[FuncionDeDistribucion|función de distribución]] es 
$$
	F(x)=\begin{cases}
	0, & x<0; \\
	1-p, & 0\leq x<1; \\
	1, & x\geq 1.
	\end{cases}
$$
Además, es fácil calcular el [[ValorEsperado|valor esperado]] y la [[Varianza_DesviacionEstandar|varianza]]: 
$$
	E(X)=p,\quad Var(X)=p(1-p).
$$
Esto pues 
$$
	E(X)=\sum_{x}xP(X=x)=0(1-p)+1(p)=p,
$$
y 
$$
	\begin{align}
	Var(X)=\sum_{x}(x-p)^{2}P(X=x)&=(0-p)^{2}(1-p)+(1-p)^{2}p \\
	&=(1-p)p^{2}+(1-p)^{2}p \\
	&=p(1-p)[p+1-p] \\
	&=p(1-p).
	\end{align}
$$

Esto sirve principalmete para estudiar la presencia de una cierta característica en un individuo.
Conocer el valor de $p$ nos indica el porcentaje de la población que cumple esa característica.

##### Ejemplo
Sea $Y$ la v.a. que indica si un correo es spam o no, y supongamos que la probabilidad de que un correo sea spam es $p=0.07$. Es decir que $Y\sim\text{Bernoulli}(p=0.07)$.
Esto implica que el 7% de los correos son spam (en promedio). Que tal que queremos crear un clasificador que nos indique si un correo es spam o no. El simple hecho de conocer $p$ no nos sirve de mucho.
Definamos 
- $X_{1}$ que indica si el correo contiene la palabra "dinero". (Binaria)
- $X_{2}$ que indica si el correo contiene la palabra "crédito". (Binaria)
- $X_{3}$ el número de caracteres del correo. (No binaria).
Entonces, nuestro clasificador puede intentar calcular 
$$
	P(Y=1|X_{1}=1,X_{2}=0,X_{3}=230).
$$
Si lo generalizamos aún mas, supongamos que tenemos $n$ v.a. que nos caracterícen un correo, (es decir $n$ características), entonces podemos asumir que 
$$
	Y|X_{1},\dots,X_{k}\sim\text{Bernoulli}(p(x_{1},\dots,x_{k})).
$$
Una forma clásica de estimar la probabilidad es mediante regresión logística, es decir 
$$
	p(x_{1},\dots,x_{n})=\frac{\exp(\beta_{0}+\beta_{1}x_{1}+\dots+\beta_{n}x_{n})}{1 +\exp(\beta_{0}+\beta_{1}x_{1}+\dots+\beta_{n}x_{n})}.
$$
