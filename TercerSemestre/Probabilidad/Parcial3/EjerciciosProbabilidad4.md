#Probabilidad 
1.- Si ${}X\sim\mathcal{N}(\mu,\sigma){}$, encontrar la distribución de ${}Y=aX+b{}$, ${}a>0{}$.
**Sol:**
Sea ${}\psi(x)=ax+b{}$ para ${}a>0{}$, esta función es creciente, y su inversa es ${}\psi ^{-1}(y)=\frac{y-b}{a}{}$, con derivada ${}\frac{d}{dy}\psi ^{-1}(y)=\frac{1}{a}{}$. Entonces, por el teorema de cambio de variable, tenemos que 
$$
\begin{aligned}
F_{Y}(y)&=F_{X}(\psi ^{-1}(y))\left\lvert  \frac{d}{dy}\psi ^{-1}(y)  \right\rvert  \\
&=\frac{1}{a\sqrt{ 2\pi }\sigma}\exp\left( -\frac{\left( \frac{y-b}{a}-\mu \right)^{2}}{2\sigma^{2}} \right).
\end{aligned}
$$

2.- Encontrar la función generadora de momentos de ${}X\sim \mathcal{N}(\mu,\sigma){}$. Usar esta función para demostrar que la suma de dos v.a. independientes Normales es Normal. 
$$
M(t)=\mathbb{E}(e^{tx}),\quad M_{X_{1}+X_{2}}(t)=M_{X_{1}}(t)M_{X_{2}}(t).
$$
**Sol:**
La función generadora de momentos de la distribución normal esta dada por 
$$
\begin{aligned}
M(t)=\mathbb{E}(e^{tx})&=\int_{-\infty}^{\infty}e^{tx} \frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( - \frac{(x-\mu)^{2}}{2\sigma^{2}} \right)dx \\
&=\int_{-\infty}^{\infty} \frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( - \frac{(x-\mu)^{2}}{2\sigma^{2}}+tx \right)dx.
\end{aligned}
$$
Concentrémonos únicamente en el término de la exponencial, que al desarrollarlo tenemos que 
$$
\begin{aligned}
-\frac{(x-\mu)^{2}}{2\sigma^{2}}+tx&=\frac{-x^{2}+2x(\mu+\sigma^{2}t)-\mu^{2}+(\mu+\sigma^{2}t)^{2}-(\mu+\sigma^{2}t)^{2}}{2\sigma^{2}} \\
&=\frac{-(x^{2}-2x(\mu+\sigma^{2}t)+(\mu+\sigma^{2}t)^{2})-\mu^{2}+(\mu \sigma^{2}t)}{2\sigma^{2}} \\
&=\frac{-(x-\mu+\sigma^{2}t)^{2}+\sigma^{2}(2\mu t+\sigma^{2}t^{2})}{2\sigma^{2}} \\
&=-\frac{(x-(\mu-\sigma^{2}t))^{2}}{2\sigma^{2}}+\mu t+\frac{\sigma^{2}t^{2}}{2}.
\end{aligned}
$$
Por lo tanto, tenemos que podemos llevar la integral a 
$$
M(t)=\exp\left( \mu t+\frac{\sigma^{2}t^{2}}{2} \right)\int_{-\infty}^{\infty} \frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( - \frac{(x-(\mu-\sigma^{2}t))^{2}}{2\sigma^{2}} \right)dx,
$$
donde podemos ver a 
$$
g(x)=\frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( - \frac{(x-(\mu-\sigma^{2}t))^{2}}{2\sigma^{2}} \right)
$$
como la función de densidad de una variable aleatoria ${}X_{1}\sim \mathcal{N}(\mu-\sigma^{2}t,\sigma){}$, y por lo tanto satisface que 
$$
\int_{-\infty}^{\infty}g(x)dx=1,
$$
de modo que tenemos que 
$$
M(t)=\exp\left( \mu t+\frac{\sigma^{2}t^{2}}{2} \right).
$$
Para la segunda parte del ejercicio, sean ${}X_{1}\sim \mathcal{N}(\mu_{1},\sigma_{1}){}$ y ${}X_{2}\sim \mathcal{N}(\mu_{2},\sigma_{2}){}$, tenemos que 
$$
M_{X_{1}}(t)=\exp\left( \mu_{1}t+\frac{\sigma_{1}^{2}t^{2}}{2} \right)\quad\text{y}\quad M_{X_{2}}(t)=\exp\left( \mu_{2}t+\frac{\sigma_{2}^{2}t^{2}}{2} \right),
$$
por lo que se sigue que 
$$
\begin{aligned}
M_{X_{1}+X_{2}}(t)&=M_{X_{1}}(t)M_{X_{2}}(t) \\
&=\exp\left( \mu_{1}t+\frac{\sigma_{1}^{2}t^{2}}{2} \right)\exp\left( \mu_{2}t+\frac{\sigma_{2}^{2}t^{2}}{2} \right) \\
&=\exp\left( (\mu_{1}+\mu_{2})t+\frac{(\sigma_{1}^{2}+\sigma_{2}^{2})t^{2}}{2} \right).
\end{aligned}
$$
Podemos observar que ${}M_{X_{1}+X_{2}}(t){}$ es la función generadora de momentos de otra v.a. normal, más aún, esto nos dice que 
$$
X_{1}+X_{2}=Z\sim \mathcal{N}\left(\mu_{1}+\mu_{2},\sqrt{ \sigma_{1}^{2}+\sigma_{2}^{2} }\right).
$$


3.- Si ${}X\sim\mathcal{N}(5,7){}$, calcular:
a) ${}P(X<7){}$,
b) ${}P(X>4){}$,
c) ${}P(\lvert X-2 \rvert\leq 3){}$,
d) ${}P(\lvert X-6 \rvert>1){}$.
**Sol:**
Sea ${}X\sim \mathcal{N}(5,7){}$, definamos ${}Z=\frac{X-5}{7}{}$, de modo que ${}Z\sim \mathcal{N}(0,1){}$. Entonces tenemos que:
a) ${}P(X<7)=P(Z<2 / 7){}$
b) ${}P(X>4)=1-P(X\leq 4)=1-P(Z\leq -1 / 7){}$
c) ${}P(\lvert X-2 \rvert\leq 3)=P(-3\leq X\leq 3)=P(-1\leq X\leq 5)=P(- 6 / 7\leq Z \leq 0)=P(Z\leq 0)-P(Z\leq- 6 / 7){}$.
d) ${}P(\lvert X-6 \rvert>1)=P(X-6>1\cup X-6<-1)=P(X-6>1)+P(X-6<-1)=1-P(X\leq 7)+P(X<5)=1-P(Z\leq 2 / 7)+P(Z<0){}$.
Estas probabilidades son fáciles de calcular con una tabla o una computadora.


4.- Suponga que el tiempo de vida útil ${}X{}$, medido en horas, de un componente electrónico se puede modelar de forma aproximada con una distribución Normal con media ${}\mu=20,000{}$ y ${}\sigma=500{}$ horas.
a) ¿Cuál es la probabilidad de que un componente dure más de 21,000 horas?
b) Dado que el componente ha vivido 21,000 horas, ¿qué tan probable es que dure otros 500?
c) ¿Qué garantía debería dar el fabricante para garantizar que sólo recibirá reclamaciones por el 5% de productos que venda?
**Sol:**
Sea ${}X\sim \mathcal{N}(20000,500){}$, definamos ${}Z=\frac{X-20000}{500}{}$ tal que ${}Z\sim \mathcal{N}(0,1){}$. Entonces tenemos que:
a) ${}P(X>21000)=1-P(X\leq 21000)=1-P(Z\leq 2){}$
b) ${}P(X>21500|X>21000)=\frac{P(X>21500, X>21000)}{P(X>21000)}=\frac{P(X>21500)}{P(X>21000)}=\frac{1-P(X\leq 21500)}{1-P(X\leq 21000)}=\frac{1-P(Z\leq 3)}{1-P(Z\leq 2)}{}$.
c) Queremos encontrar ${}c{}$ que satisfaga ${}P(X\leq c)=0.05{}$, lo que es lo mismo que ${}P\left( Z\leq \frac{c-21000}{500} \right)=0.05{}$.


5.- Si ${}X\sim\mathcal{N}(\mu,\sigma){}$, encuentre, de forma aproximada, el valor de ${}c{}$ que cumple 
$$
P(\mu-c\sigma\leq X\leq \mu+c\sigma)=0.99.
$$
**Sol:**
Por lo visto en clase, sea ${}X\sim \mathcal{N}(\mu,\sigma){}$, tenemos que para ${}c=3{}$ se cumple que 
$$
P(\mu-3\sigma\leq X\leq \mu+3\sigma \approx 0.99.
$$


6.- Sean ${}a<b{}$ y ${}Z\sim\mathcal{N}(0,1){}$. Demuestra que 
$$
P(a\leq Z^{2}\leq b)=2(F_{Z}(\sqrt{ b })-F_{Z}(\sqrt{ a })).
$$
**Sol:**
Sean ${}Z\sim \mathcal{N}(0,1){}$ y ${}a<b\in \mathbb{R}{}$. Sabemos que ${}P(a\leq Z^{2}\leq b)=P(Z^{2}\leq b)-P(Z^{2}\leq a){}$. Notemos que ${}Z^{2}\geq 0{}$, por lo tanto podemos tomar ${}0\leq a<b{}$. 
Tenemos entonces que 
$$
P(Z^{2}\leq b)=P(\lvert Z \rvert \leq \sqrt{ b })=P(-\sqrt{ b }\leq Z\leq \sqrt{ b })=P(Z\leq \sqrt{ b })-P(Z \leq -\sqrt{ b }).
$$
Observemos que ${}Z\sim \mathcal{N}(0,1){}$ es simétrica respecto a ${}0{}$, por lo tanto ${}P(Z\leq -\sqrt{ b })=P(Z\geq \sqrt{ b })=1-P(Z\leq \sqrt{ b }){}$, y por lo tanto 
$$
\begin{aligned}
P(Z^{2}\leq b)&=P(Z\leq \sqrt{ b })-P(Z\leq -\sqrt{ b }) \\
&=P(Z\leq \sqrt{ b })-(1-P(Z \leq \sqrt{ b })) \\
&=2P(Z \leq \sqrt{ b }) -1.
\end{aligned}
$$
De forma análoga, se llega a que ${}P(Z^{2}\leq a)=2P(Z\leq \sqrt{ a })-1{}$, por lo tanto tenemos que 
$$
\begin{aligned}
P(a\leq Z^{2}\leq b)&=P(Z^{2}\leq b)-P(Z^{2}\leq a) \\
&=(2P(Z \leq \sqrt{ b }) -1)-(2P(Z \leq \sqrt{ a }) -1) \\
&=2P(Z \leq \sqrt{ b }) -2P(Z \leq \sqrt{ a })  \\
&=2(F_{Z}(\sqrt{ b })-F_{Z}(\sqrt{ a })).\quad\square
\end{aligned}
$$


7.- Use software para verificar las siguientes aproximaciones:
a) Para ${}n{}$ grande, la distribución ${}\mathrm{Binomial}(n,p){}$ puede aproximarse con una distribución ${}\mathcal{N}(np, \sqrt{ np(1-p) }){}$.
b) Para ${}\lambda{}$ grande, la distribución Poisson puede aproximarse por una distribución ${}\mathcal{N}(\lambda,\sqrt{ \lambda }){}$.
De un ejemplo de donde estas aproximaciones podrías ser útiles.