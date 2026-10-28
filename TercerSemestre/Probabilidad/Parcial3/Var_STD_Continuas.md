#Probabilidad 
#### Definición:
Sea $X$ una [[V.A.Continuas|v.a. continua]] con pdf $f(x)$ y $\mu=\mathbb{E}(X)$. La varianza de $X$ está dada por 
$$
	\mathrm{Var}(X)=\int_{-\infty}^{\infty}(x-\mu)^{2}f(x)dx\geq0.
$$
De igual forma que en el caso [[Varianza_DesviacionEstandarDiscretas|discreto]], esta se denota como $\sigma^{2}$.

##### Ejemplo
Sea $X$ una v.a. uniforme en el intervalo $(0,1)$ con pdf 
$$
	f(x)=\begin{cases}
	1, & x\in(0,1) \\
	0, & \text{en otro caso}
	\end{cases}.
$$
Anteriormente vimos que $\mathbb{E}(X)=1 / 2$, por lo que podemos hacer el cálculo de la varianza y ver que 
$$
	\mathrm{Var}(X)=\int_{0}^{1}\left( x-\frac{1}{2} \right)^{2}(1)dx=\frac{1}{12}.
$$

#### Propiedades
De forma similar al [[ValorEsperadoContinuo|valor esperado]], todas las propiedades del caso continuo se siguen cumpliendo para la varianza de una v.a. continua:
- $\mathrm{Var}(c)=0$;
- $\mathrm{Var}(cX)=c^{2}\mathrm{Var}(X)$;
- $\mathrm{Var}(cX+b)=c^{2}\mathrm{Var}(X)$;
- $\mathrm{Var}(X+Y)=\mathrm{Var}(X)+\mathrm{Var}(Y)+2\mathrm{Cov}(X,Y)$, dónde $\mathrm{Cov}(X,Y)$ denota la covarianza, y se calcula de la forma 
  $$
  	\mathrm{Cov}(X,Y)=\mathbb{E}[(X-\mathbb{E}(X))(Y-\mathbb{E}(Y))].
  $$
  Si $X$ y $Y$ son independientes, entonces $\mathrm{Var}(X+Y)=\mathrm{Var}(X)+\mathrm{Var}(Y)$.


