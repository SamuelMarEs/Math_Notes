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
M(t)=E(e^{tx}),\quad M_{X_{1}+X_{2}}(t)=M_{X_{1}}(t)M_{X_{2}}(t).
$$
**Sol:**
La función generadora de momentos va a estar dada por 


3.- Si ${}X\sim\mathcal{N}(5,7){}$, calcular:
a) ${}P(X<7){}$,
b) ${}P(X>4){}$,
c) ${}P(\lvert X-2 \rvert\leq 3){}$,
d) ${}P(\lvert X-6 \rvert>1){}$.
**Sol:**
Sea ${}X\sim N(5,7){}$, definamos ${}Z=\frac{X-5}{7}{}$, de modo que ${}Z\sim N(0,1){}$. Entonces tenemos que:
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
Sea ${}X\sim N(20000,500){}$, definamos ${}Z=\frac{X-20000}{500}{}$ tal que ${}Z\sim N(0,1){}$. Entonces tenemos que:
a) ${}P(X>21000)=1-P(X\leq 21000)=1-P(Z\leq 2){}$
b) ${}P(X>21500|X>21000)=\frac{P(X>21500, X>21000)}{P(X>21000)}=\frac{P(X>21500)}{P(X>21000)}=\frac{1-P(X\leq 21500)}{1-P(X\leq 21000)}=\frac{1-P(Z\leq 3)}{1-P(Z\leq 2)}{}$.
c) Queremos encontrar ${}c{}$ que satisfaga ${}P(X\leq c)=0.05{}$, lo que es lo mismo que ${}P\left( Z\leq \frac{c-21000}{500} \right)=0.05{}$.

5.- Si ${}X\sim\mathcal{N}(\mu,\sigma){}$, encuentre, de forma aproximada, el valor de ${}c{}$ que cumple 
$$
P(\mu-c\sigma\leq X\leq \mu+c\sigma)=0.99.
$$
**Sol:**
Por lo visto en clase, sea ${}X\sim N(\mu,\sigma){}$, tenemos ${}{}$


6.- Sean ${}a<b{}$ y ${}Z\sim\mathcal{N}(0,1){}$. Demuestra que 
$$
P(a\leq Z^{2}\leq b)=2(F_{Z}(\sqrt{ b })-F_{Z}(\sqrt{ a })).
$$

7.- Use software para verificar las siguientes aproximaciones:
a) Para ${}n{}$ grande, la distribución ${}\mathrm{Binomial}(n,p){}$ puede aproximarse con una distribución ${}\mathcal{N}(np, \sqrt{ np(1-p) }){}$.
b) Para ${}\lambda{}$ grande, la distribución Poisson puede aproximarse por una distribución ${}\mathcal{N}(\lambda,\sqrt{ \lambda }){}$.
De un ejemplo de donde estas aproximaciones podrías ser útiles.