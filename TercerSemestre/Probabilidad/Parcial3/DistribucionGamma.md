#Probabilidad
#### Definición:
Sea ${}X{}$ una [[V.A.Continuas|v.a. continua]] con función de densidad dada por 
$$
f(x)=\begin{cases}
\frac{\beta^{\alpha}}{\Gamma(\alpha)}x^{\alpha-1}e^{-\beta x}, & x,\alpha,\beta>0 \\

0, & \text{en otro caso}
\end{cases},
$$
dónde 
$$
\Gamma(\alpha)=\int_{0}^{\infty}t^{\alpha-1}e^{-t}dt.
$$
El término ${}x^{\alpha-1}e^{-\beta x}{}$ es el ***kernel*** de la función, mientras que el término ${}\frac{\beta^{\alpha}}{\Gamma(\alpha)}{}$ es la constante de normalización.

La función ${}\Gamma{}$ tiene las siguientes propiedades:
- ${}\Gamma(\alpha+1)=\alpha \Gamma(\alpha){}$,
- ${}\Gamma(\alpha+1)=\alpha{}$ si ${}\alpha{}$ es un entero positivo,
- ${}\Gamma(2)=\Gamma(1)=1{}$,
- ${}\Gamma(1 / 2)=\sqrt{ \pi }{}$.

El parámetro ${}\beta{}$ se conoce como parámetro de tasa, y ${}\frac{1}{\beta}=\lambda{}$ se conoce como parámetro de escala. Por otro lado, el parámetro ${}\alpha{}$ es un parámetro de forma. Se puede demostrar que 
- ${}\mathbb{E}(X)=\frac{\alpha}{\beta}{}$, o si reparametrizamos ${}\mathbb{E}(X)=\alpha \lambda{}$,
- ${}\mathrm{Var}(X)=\frac{\alpha}{\beta^{2}}{}$, o alternativamente ${}\mathrm{Var}(X)=\alpha \lambda^{2}{}$.
Para la [[ComulativeDensityFunction|función de distribución acumulada]] no hay una forma cerrada.

El modelo gamma es muy usado para modelar cantidades positivas como tiempo, longitud, velocidad, peso, concentración, etc.

#### Proposición
Sean ${}X_{1},\dots,X_{n}{}$ v.a. exponenciales independientes e idénticamente distribuidas con parámetro ${}\lambda{}$. Luego, la v.a. ${}Y=\sum_{i=1}^{n}X_{i}\sim \mathrm{Gamma}(\mathrm{forma}=n, \mathrm{tasa}=\lambda){}$.

