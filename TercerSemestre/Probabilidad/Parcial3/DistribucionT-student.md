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