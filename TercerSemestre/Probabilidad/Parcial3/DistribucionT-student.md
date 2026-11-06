#Probabilidad 
#### Definición:
Sea ${}X{}$ una [[V.A.Continuas|v.a. continua]] con función de densidad 
$$
f(x)=\frac{\Gamma\left( \frac{n+1}{2} \right)}{\Gamma(n/2)\sqrt{ n\pi }}\left( 1+ \frac{x^{2}}{n} \right)^{-(n+1) / 2},\quad x \in \mathbb{R},n>0.
$$
A esta v.a. se le conoce como variable t-student con ${}n{}$ grados de libertad, y se denota de la forma ${}X\sim t_{n}{}$.
La distribución t-student se parece a una [[DistribucionNormal|normal estándar]], aunque se puede pensar/interpretar que modela ligeramente más incertidumbre. De hecho, se puede demostrar que 
$$
t_{n}\underset{n\to \infty}{\to}\mathcal{N}(0,1).
$$
Además, también podemos demostrar que 
- ${}\mathbb{E}(X)=0{}$,
- ${}\mathrm{Var}(X)=\frac{n}{n-2}{}$ para ${}n>2{}$.

#### Ejemplo:
El modelo t-student se puede utilizar para calcular intervalos de confianza para la media de una v.a.
Sea ${}X{}$ el tiempo de vida de una célula. Se sabe que se puede utilizar una distribución Normal para modelar estos tiempos. No obstante, en la práctica se desconoce los valores de los parámetros de la distribución.
Supongamos que recabamos los tiempos de vida de distintas células ${}x_{1},\dots,x_{n}{}$, y estimamos ${}\mu{}$ como el promedio de nuestros datos ${}\bar{X}=\frac{1}{n}\sum_{i=1}^{n}x_{i}{}$. El principal problema con esta estimación, es que si cambiamos la muestra, el promedio seguramente va a cambiar. Una opción para lidiar con esto, podría ser repetir el experimento, y después calcular el promedio de los promedios, pues este sería una mejor estimación. Sin embargo esta solución no es viable.
En vez de repetir el experimento, podemos usar la distribución t-student para dar un intervalo de confianza para la estimación de ${}\mu{}$.
Se puede demostrar que un buen intervalo de estimación de ${}u{}$ es 
$$
\bar{X}\pm t_{1-\alpha /2} \frac{S}{\sqrt{ n }},
$$
dónde ${}t_{1- \alpha /2}{}$ es una distribución t-student con ${}n-1{}$ grados de libertad, y ${}S{}$ es la desviación estándar estimada de la forma 
$$
S=\sqrt{ \frac{1}{n-1}\sum_{i=1}^{n}(x_{i}-\bar{x}) }.
$$
Este intervalo se conoce como el intervalo de confianza de nivel ${}(1-\alpha)100\%{}$ para la media de la distribución normal, con ${}\alpha \in(0,1){}$.
Si tomamos ${}\alpha=0.05{}$, entonces el nivel del intervalo es ${}(1-0.05)100\%=95\%{}$. 
Esto se interpreta como que si repetimos el intervalo 100 veces, en 95 de esas 100 el valor del promedio caerá dentro del intervalo.