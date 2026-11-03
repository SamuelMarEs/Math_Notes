#Probabilidad 
#### Definición:
Sea ${}X{}$ una [[V.A.Continuas|v.a. continua]] que toma valores en todo ${}\mathbb{R}{}$ y con función de densidad dada por 
$$
f(x)=\frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( -\frac{(x-\mu)^{2}}{2\sigma^{2}} \right),\quad \forall x \in \mathbb{R}.
$$
Al parámetro ${}\mu {}$ se le conoce como “media” o parámetro de centralidad, y a ${}\sigma{}$ se le conoce como parámetro de escala y ${}\sigma >0{}$.
A este tipo de v.a. se le conoce como variable Normal o Gaussiana de parámetros ${}\mu{}$ y ${}\sigma{}$, y se denota como 
$$
X\sim \mathcal{N}(\mu,\sigma).
$$
Se puede demostrar que 
- ${}\mathbb{E}(X)=\mu{}$;
- ${}\mathrm{Var}(X)=\sigma^{2}{}$.

Para toda distribución Normal, sin importar sus parámetros, se cumple lo siguiente:
- ${}P(\mu-\sigma\leq X\leq \mu+\sigma)\approx 0.68{}$,
- ${}P(\mu-2\sigma\leq X\leq \mu+2\sigma)\approx 0.95{}$,
- ${}P(\mu-3\sigma\leq X\leq \mu+3\sigma)\approx 0.99{}$.

#### Proposición:
Si ${}X\sim\mathcal{N}(\mu,\sigma){}$, entonces 
$$
Z=\frac{X-\mu}{\sigma}\sim\mathcal{N}(0,1).
$$
A ${}Z{}$ se le conoce como una v.a. Normal *estándar*.
##### Demostración:
Usando el [[ComulativeDensityFunction|teorema de cambio de variable]] para variables continuas, podemos encontrar la función de densidad de la v.a. ${}Z{}$.
Sea ${}\psi(x)=\frac{x-\mu}{\sigma}{}$, esta es una función creciente con inversa ${}\psi ^{-1}(z)=\sigma z+\mu{}$, cuya derivada es ${}\frac{d}{dz}\psi ^{-1}(z)=\sigma{}$. Si recordamos el teorema, tenemos que 
$$
f_{Z}(z)=f_{X}(\psi ^{-1}(z))\left\lvert  \frac{d}{dz}\psi ^{-1}(z)  \right\rvert ,
$$
es decir que 
$$
f_{Z}(z)=\frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( -\frac{(\sigma z+\mu-\mu)^{2}}{2\sigma^{2}} \right)\sigma=\frac{1}{\sqrt{ 2\pi }}\exp\left( -\frac{z^{2}}{2} \right),
$$
es decir que ${}Z{}$ es una v.a. Normal con media ${}\mu=0{}$ y desviación estándar ${}\sigma=1.\quad\square{}$
