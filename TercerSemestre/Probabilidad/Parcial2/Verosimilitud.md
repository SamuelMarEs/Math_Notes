#Probabilidad 
Suponga que se tiene una muestra independiente de tamaño $n$ de una [[VariablesAleatorias|v.a.]] discreta $X$ con [[FuncionDeProbabilidad|función de probabilidad]] $f(x)$.
Se desea estimar la proporción de la población que cumple cierta característica, y calcular la probabilidad de observar una cierta secuencia de resultados.
Sea 
$$
	X_{i}=\begin{cases}
	1, & \text{si tiene la condicicón} \\
	0, & \text{en otro caso}.
	\end{cases}
$$
Entonces definimos $P(X_{i}=1)=p$ y $P(X_{i}=0)=1-p$, de modo que nuestra función de probabilidad es 
$$
	f(x)=\begin{cases}
	p^{x}(1-p)^{1-x}, & x=0,1 \\
	0, & \text{en otro caso}.
	\end{cases}
$$
Supongamos que queremos, por ejemplo, la secuencia $1,0,0,1,0,0,\dots,1$, o en general cualquier secuencia de resultados.
Entonces, la probabilidad de observar esta secuencia es 
$$
	\begin{align}
	P(X_{1}=1,X_{2}=0,X_{3}=0,X_{4}=0,\dots,X_{n}=1)&=\prod_{i=1}^{n} P(X_{i}=x_{i}) \\
	&=\prod_{i=1}^{n} p^{x_{i}}(1-p)^{1-x_{i}} \\
	&=p^{\sum x_{i}}(1-p)^{n-\sum x_{i}}
	\end{align}
$$
dónde $\sum x_{i}$ es el número de veces que aparece la condición, y $n-\sum x_{i}$ el resto de veces en las que no se cumple.

A la probabilidad de observar una muestra se le conoce como ***función de verosimilitud***, y únicamente depende de los parámetros del modelo de probabilidad, en este caso, de $p$. 
$$
	\mathcal{L}(p)=p^{s}(1-p)^{n-s},
$$
dónde en este caso, $s=\sum x_{i}$.

Observemos que podemos definir la función del logaritmo de la verosimilitud para encontrar $p$, es decir 
$$
	\ell(p)=\ln(\mathcal{L}(p))=s\ln(p)+(n-s)\ln(1-p).
$$
Si tomamos la derivada con respecto a $p$, tenemos que 
$$
	\frac{d\ell(p)}{dp}=\frac{s}{p}+\frac{n-s}{1-p}(-1)=0,
$$
y por lo tanto $p=s / n$.

De forma más general, la verosimilitud se define como 
$$
	L(\theta|x)=\prod_{i=1}^{N}f(x|\theta),
$$
para $\theta$ un conjunto de parámetros, y $x$ una muestra o conjunto de observaciones.

