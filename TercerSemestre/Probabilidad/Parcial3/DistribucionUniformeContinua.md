#Probabilidad
#### Definición:
Sea $X$ una [[V.A.Continuas|v.a. continua]] con función de densidad dada por 
$$
	f(x)=\begin{cases}
	\frac{1}{b-a}, & x\in(a,b); \\
	0, & \text{en otro caso}
	\end{cases}.
$$
A este tipo de variable aleatoria se le conoce como v.a. *uniforme* en el intervalo $(a,b)$ y se denota como 
$$
	X\sim \mathrm{Uniforme}(a,b),\quad X\sim U(a,b).
$$
El caso particular en el que $X\sim U(0,1)$ se utiliza mucho para generación de números aleatorios y como distribución a priori en procesos de estimación Bayesiana para proporciones.

##### Propiedades:
No es difícil demostrar que 
- $F(x)=\begin{cases}0, & x\leq a \\  \frac{x-a}{b-a}, & a<x\leq b \\  1 , & x>b\end{cases}$.
- $\mathbb{E}(X)=\frac{b+a}{2}$.
- $\mathrm{Var}(X)=\frac{(b-a)^{2}}{12}$.
- Recordando que para obtener el [[Metricas|cuantil]] $c_{\alpha}$ necesitamos la función inversa $F^{-1}(\alpha)$, que es sencillo mostrar que es $F^{-1}(\alpha)=(b-a)\alpha+a$

##### Ejemplos:
1.- Supongamos que se quieren generar valores aleatorios de una [[DistribucionBernoulli|distribución Bernoulli]] de parámetro $p=0.5$ (lanzamiento de una moneda).
Consideremos el siguiente algoritmo:
1. Generar $u\sim U(0,1)$ (un número $u$ bajo una distribución uniforme entre 0 y 1).
2. Definir $x=\begin{cases}1, & u\leq0.5; \\  0, & u>0.5\end{cases}$. De este modo, no es difícil ver que $P(X=1)=P(U\leq 0.5)=F(0,5)=0.5=p$. De forma análoga se puede ver que $P(X=0)=0.5=1-p$.

En general, si se desea simular de una v.a. continua con función de distribución $F_{1}$, el siguiente algoritmo funciona:
1. $u\sim U(0,1)$.
2. $x=F^{-1}(u)$.

2.- Estimación de la probabilidad de éxito de una v.a. $\mathrm{Bernoulli}(p)$.
Tenemos 5 resultados del lanzamiento de una moneda: águila, sol, sol, sol, sol. ¿Es una moneda justa?
Si definimos un éxito como águila, entonces la probabilidad de éxito es $p$. Podemos pensar que los lanzamientos vienen de un modelo $\mathrm{Bernoulli}(p)$. En la práctica realmente no conocemos el valor de $p$, pero podemos estimarlo. Podemos estimarlo, por ejemplo, como 
$$
	\hat{p}= \frac{\mathrm{\#éxitos}}{\mathrm{\#lanzamientos}}= \frac{1}{5}=0.2.
$$
Si repetimos el experimento de lanzar la moneda 5 veces, y obtenemos a, s, s, a, s, entonces tendríamos una nueva aproximación 
$$
	\hat{p}_{2}=\frac{2}{5}=0.4.
$$
Para dar una mejor aproximación, podemos utilizar el [[TeoremaDeBayes|teorema de Bayes]] para intentar dar otra aproximación de la distribución de $p$ dados los datos, de la siguiente forma 
$$
	f(p|X_{1},\dots,X_{5})=\frac{P(X_{1}=x_{1},\dots,X_{5}=x_{5}|p)f(p)}{\int_{0}^{1}P(X_{1}=x_{1},\dots,X_{5}=x_{5}|p)f(p)dp}.
$$
Supongamos que, a priori, $p \sim U(0,1)$.
La función $P(X_{1}=x_{1},\dots,X_{5}=x_{5}|p)$ se conoce como función de verosimilitud, y si suponemos que las variables aleatorias $X_{i}$ son Bernoulli e independientes, entonces 
$$
	P(X_{1}=x_{1},\dots,X_{5}=x_{5}|p)=\prod_{i=1}^{5}P(X_{i}=x_{i}|p)=\prod_{i=1}^{5}p^{x_{i}}(1-p)^{1-x_{i}}.
$$
Dados los datos de nuestro primer experimento, tendríamos entonces que 
$$
	f(p|X_{1},\dots,X_{5})=\frac{p(1-p)^{4}(1)}{\int_{0}^{1}p(1-p)^{4}(1)dp}=\dots=\frac{1}{B(2,5)}p^{2-1}(1-p)^{5-1},
$$
donde $B(a,b)=\int_{0}^{1}x^{a-1}(1-x)^{b-1}dx$.
Al resultado encontrado se le conoce como [[DistribucionBeta]].