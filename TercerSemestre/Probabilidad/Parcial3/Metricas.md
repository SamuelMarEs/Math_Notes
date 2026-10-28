#Probabilidad 
#### Momentos
El $n$-ésimo momento de una [[V.A.Continuas|v.a. continua]] $X$ está dado por $\mathbb{E}(X^{n})$, i.e. 
$$
	\mathbb{E}(X^{n})=\int_{-\infty}^{\infty}x^{n}f(x)dx.
$$

#### Cuantiles
Si $X$ es una v.a. continua con función de distribución $F(x)$, entonces el cuantil de nivel $\alpha$ denotado $c_{\alpha}$ de $X$ es el valor de la variable tal que 
$$
	F(c_{\alpha})=\alpha\implies P(X\leq c_{\alpha})=\alpha,\quad \alpha\in(0,1).
$$
Gracias a las propiedades de la [[ComulativeDensityFunction|cdf]], esto se puede encontrar de forma rápida como 
$$
	c_{\alpha}=F^{-1}(\alpha).
$$
##### Ejemplo:
Sea $X$ la v.a. continua que mide el tiempo (en minutos) que tarda un estudiante en resolver un Quiz. Supongamos que la pdf de esta variable está dada por 
$$
	f_{X}(x)=\begin{cases}
	\frac{1}{10}e^{-x / 10}, & x>0; \\
	0, & \text{en otro caso}
	\end{cases}.
$$
No es difícil encontrar que $\mathbb{E}(X)=10$. 
Supongamos que queremos calcular el tiempo que se debe dar a los estudiantes para resolver el Quiz, de modo que el 95% de los estudiantes lo resuelvan. Es decir, queremos encontrar el cuantil de nivel 0.95 ($c_{0.95}$).
Para esto, necesitamos encontrar $F^{-1}(\alpha)$. No es complicado ver que 
$$
	F(x)=\begin{cases}
	1-e^{-x / 10}, & x>0; \\
	0, & \text{en otro caso}
	\end{cases}.
$$
Despejando, podemos llegar a que $F^{-1}(\alpha)=--10\ln(1-\alpha)$. Entonces para encontrar $c_{0.95}$ basta encontrar $F^{-1}(0.95)=-10\ln(0.05)\approx 29.95$. Es decir, que alrededor de 30 minutos bastan para que el 95% de los estudiantes terminen el examen.

