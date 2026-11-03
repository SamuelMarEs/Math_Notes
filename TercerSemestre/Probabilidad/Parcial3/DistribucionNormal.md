#Probabilidad 
#### Definición:
Sea ${}X{}$ una [[V.A.Continuas|v.a. continua]] que toma valores en todo ${}\mathbb{R}{}$ y con función de densidad dada por 
$$
f(x)=\frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( -\frac{(x-\mu)^{2}}{2\sigma^{2}} \right),\quad \forall x \in \mathbb{R}.
$$
Al parámetro ${}\mu {}$ se le conoce como “media” o parámetro de centralidad, y a ${}\sigma{}$ se le conoce como parámetro de escala.
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
