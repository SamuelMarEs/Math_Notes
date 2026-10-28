#Probabilidad
#### Definición: 
Dos [[V.A.Continuas|variables aleatorias]] $X$ y $Y$ son independientes si 
$$
	F_{X,Y}(x,y)=F_{X}(x)\cdot F_{Y}(y),
$$
es decir si 
$$
	P(X\leq x,Y\leq y)=P(X\leq x)\cdot P(Y\leq y).
$$
En el caso continuo, esto es equivalente a 
$$
	f_{X,Y}(x,y)=f_{X}(x)\cdot f_{Y}(y).
$$
##### Ejemplos:
1.- Sea $f_{XY}(x,y)=\begin{cases}\lambda^{2} e^{-\lambda(x+y)}, & x,y\geq 0,\lambda>0 \\  0, & \text{otro caso}\end{cases}.$  Para encontrar las funciones de distribución de cada una de las variables, lo podemos hacer integrando sobre la otra variable, es decir 
$$
	f_{Y}(y)=\int_{0}^{\infty}\lambda^{2} e^{-\lambda(x+y)}dx=\lambda e^{-\lambda y},
$$
y de manera análoga se puede llegar a que $f_{X}(y)=\lambda e^{-\lambda x}$, de modo que podemos ver que 
$$
	f_{Y}(y)f_{X}(x)=\lambda e^{-\lambda y}\lambda e^{-\lambda y}=\lambda^{2}e^{-\lambda(x+y)},
$$
de modo que tenemos que las dos variables aleatorias son independientes.

2.- Suponga que se tiene una muestra de tamaño $n$ de una v.a. con función de densidad dada por 
$$
	f(x)=\begin{cases}
	\frac{1}{\theta}, & x\in(0,\theta) \\
	0, & \text{en otro caso},
	\end{cases}
$$
donde $\theta$ es una constante desconocida. Supongamos que tenemos las muestras 
$$
	x_{1}=3,x_{2}=7,x_{3}=1.2,x_{4}=4.7,x_{5}=6.1.
$$
La función de verosimilitud en este ejemplo se obtiene: 
$$
	\mathcal{L}(\theta)=\prod_{i=1}^{n}f(x_{i}).
$$
$\mathcal{L}(\theta)$ representa una aproximación a la probabilidad de observar la muestra: $$P(X_{1}\in(x_{1}-\varepsilon, x_{1}+\varepsilon), X_{2}\in(x_{2}-\varepsilon,x_{2}+\varepsilon), \dots, X_{5}\in(x_{5}-\varepsilon,x_{5}+\varepsilon)).$$
Nuestra función de verosimilitud va a estar dada por 
$$
	\mathcal{L}(\theta)=\prod_{i=1}^{n} \frac{1}{\theta}I_{(0,\theta)}(x_{i}),
$$
donde $I_{(0,\theta)}(x)=\begin{cases}1, & x\in(0,\theta) \\  0, & \text{en otro caso}\end{cases}$ se conoce como una función indicadora. Entonces, siempre y cuando todos los $x$ estén en el intervalo, la función es $\mathcal{L}(\theta)=1 / \theta^{5}$, tomando en cuenta que esto se satisface (para nuestra muestra) siempre que $\theta\geq 7$.
Si queremos maximizar la verosimilitud, no lo podemos hacer derivando, puesto que la función no presenta puntos criticos. Sin embargo, con la restricción de $\theta\geq7$, y dado que la función $1 / \theta^{5}$ es estrictamente decreciente, el punto de máximo es $\theta=7=\max\{x_{1},\dots,x_{5}\}$.
El uso de la función de verosimilitud funciona siempre que supongamos que las muestras son independientes.
