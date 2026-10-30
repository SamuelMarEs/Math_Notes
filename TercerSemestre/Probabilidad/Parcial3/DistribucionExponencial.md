#Probabilidad 
#### Definición
Sea $X$ una [[V.A.Continuas|v.a. continua]] con función de densidad dada por 
$$
	f(x)=\begin{cases}
	\frac{1}{\lambda}e^{- x / \lambda}, & x>0, \lambda>0; \\
	0, & \text{en otro caso}
	\end{cases}.
$$
A este tipo de variables aleatorias se les conoce como variables *exponenciales* de parámetro $\lambda$, y se denota por 
$$
	X\sim \mathrm{Exp}(\lambda).
$$
##### Propiedades
Se puede demostrar de forma sencilla que 
- $F(x)=1-e^{-x / \lambda}$,
- $\mathbb{E}(X)=\lambda$,
- $\mathrm{Var}(X)=\lambda^{2}$,
- De la [[ComulativeDensityFunction|cdf]] se sigue que $F^{-1}(\alpha)=-\lambda \ln(1-\alpha)$, para $\alpha\in(0,1)$, lo que nos permite calcular [[Metricas|cuantiles]].

##### Re-parametrización
Existe otra parametrización de la función de densidad dada por 
$$
	f(x)=\begin{cases}
	\theta e^{\theta x}, & x,\theta>0; \\
	0, & \text{en otro caso}
	\end{cases}.
$$
En esta versión, $\theta$ se conoce como parámetro de tasa, mientras que $\lambda$ se conoce como parámetro de escala. Es evidente que $\theta=1 / \lambda$.
Dependiendo del tipo de aplicación con la que se esté trabajando, a veces se usa el parámetro de tasa, y a veces se utiliza el parámetro de escala.
En programas como R, se debe de especificar cual parámetro se está utilizando al usar funciones que trabajen con la distribución exponencial.
Si se trabaja con el parámetro de tasa, se tiene que 
$$
	\mathbb{E}(X)=1 / \theta,\quad \mathrm{Var}(X)=\frac{1}{\theta^{2}},\quad F(x)=1-e^{-\theta x},\quad F^{-1}(\alpha)=-\frac{\ln(1-\alpha)}{\theta}.
$$

##### Ejemplos:
1.- Suponga que en una cierta región, el consumo de electricidad por casa se puede modelar con una v.a. $\mathrm{Exp}(\lambda=170)$, donde la medición se hace en $\mathrm{kw}/ \mathrm{h}$ (kilowatts por hora) al mes.
¿Cuál es el consumo medio (esperado) de electricidad por casa? 
¿Qué proporción de la población consume más de 250 kw/h al mes?
**Sol:**
Sea $X\sim \mathrm{Exp}(\lambda=170)$. Para resolver la primera pregunta, basta encontrar el valor esperado, es decir 
$$
	\mathbb{E}(X)=\lambda=170.
$$
Para responder a la segunda pregunta, lo que queremos encontrar es $P(X>250)=1-P(X\leq 250)$, o lo que es lo mismo $1-F(250)=1-(1-e^{-250 / 170})=e^{-250 / 170}\approx 0.22$. Es decir, alrededor del 22% de la población consume más de 250 kw/h al mes.