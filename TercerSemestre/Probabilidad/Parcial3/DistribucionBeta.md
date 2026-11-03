#Probabilidad 
#### Definición:
Sea ${}X{}$ una [[V.A.Continuas|v.a. continua]] que sólo toma valores en el intervalo ${}(0,1){}$ y con función de densidad 
$$
f(x)=\begin{cases}
\frac{1}{B(\alpha,\beta)}x^{\alpha-1}(1-x)^{\beta-1}, & x \in(0,1),\alpha,\beta>0, \\
0, & \text{en otro caso}
\end{cases},
$$
dónde 
$$
B(a,b)=\int_{0}^{1}x^{a-1}(1-x)^{b-1}dx.
$$
De forma similar a la [[DistribucionGamma|distribución gamma]], el término ${}x^{\alpha-1}(1-x)^{\beta-1}{}$ es el kernel de la función de densidad, y ${}1 / B(\alpha,\beta){}$ es la constante de normalización.
La distribución beta es muy versátil, ya que se pueden encontrar funciones muy diferentes variando los parámetros ${}\alpha,\beta{}$.
A este tipo de variables aleatorias se les denota de la forma 
$$
X\sim \mathrm{Beta}(\alpha,\beta).
$$
Se puede demostrar que 
- ${}\mathbb{E}(X)=\frac{\alpha}{\alpha+\beta}{}$,
- ${}\mathrm{Var}(X)=\frac{\alpha \beta}{(\alpha+\beta+1)(\alpha+\beta)^{2}}{}$.

Este modelo se usa principalmente para modelar proporciones.
##### Ejemplo
Sea ${}X{}$ una v.a. ${}\text{Beta}(\alpha=3,\beta=10){}$ que describe la proporción de personas que sufren accidentes cardiacos en una cierta población