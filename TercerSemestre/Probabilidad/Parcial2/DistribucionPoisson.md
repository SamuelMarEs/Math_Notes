#Probabilidad 
Supongamos que se observa la ocurrencia de un evento en un cierto intervalo. Supongamos también que las ocurrencias del evento en intervalos de tiempo disjuntos son independientes y el tiempo que transcurre entre la ocurrencia de dos eventos sigue una [[DistribucionExponencial|distribución exponencial]].

##### Ejemplo:
Estudiar las solicitudes de acceso a un servidor en un intervalo de tiempo, digamos de 6:00 am a 10:00 am. Si tenemos otro intervalo de tiempo disjunto, como el intervalo 12:00 pm a 16:00 pm.
Las hipótesis que hacemos con el modelo Poisson es que las ocurrencias de un evento dentro del intervalo de 6 a 10 am, son independientes de las ocurrencias del mismo evento dentro del intervalo de 12 a 4 pm.

#### Definición:
Sea $X$ la [[VariablesAleatorias|v.a.]] que indica el número de ocurrencias en el intervalo $(0,t]$ de un cierto evento. Entonces $X$ pude tomar valores $\{ 0,1,2,\dots \}$. La [[FuncionDeProbabilidad|función de probabilidad]] de $X$ está dada por 
$$
	f(x)=P(X=x)=
	\frac{\lambda^{x}e^{-\lambda}}{x!}, \quad x=0,1,2,\dots
$$
A este tipo de variables se les conoce como variables aleatoria Poisson de parámetro $\lambda$, donde $\lambda>0$ se interpreta como el número de ocurrencias promedio por unidad de tiempo.
Se puede demostrar que 
$$
	E(X)=Var(X)=\lambda.
$$
##### Ejemplo:
El número de mutaciones en una cierta región del ADN por generación se puede modelar con una v.a. Poisson de parámetro $\lambda=7$.
a) ¿Cómo se interpreta $\lambda$?
b) ¿Qué tan probable es que el número de mutaciones por generación exceda 10?
c) Aproximadamente, que porcentaje de la población presenta 0 mutaciones.
**Sol:**
Sea $X$ el número de mutaciones por generación. El ejercicio nos dice que $X\sim\text{Poisson}(\lambda=7)$.
a) $\lambda$ se puede interpretar como el número promedio de mutaciones por cada generación.
b) Queremos calcular $P(X> 10)$, o en otras palabras 
$$
	P(X>10)=\sum_{x=11}^{\infty}P(X=x)=1-P(X\leq 10)=1-\sum_{x=0}^{11}P(X=x)\approx 0.098.
$$
c) Esto se traduce como la probabilidad de que que haya 0 mutaciones en una generación, es decir 
$$
	P(X=0)=\frac{7^{0}e^{-7}}{0!}=e^{-7}\approx 0.000912.
$$

##### Ejemplo:
Supongamos que el número de plantas con plaga en una parcela de 10 m x 10 m se puede modelar con una distribución Poisson de parámetro $\lambda=2.5$.
En este caso, $\lambda$ indica el número promedio de plantas con plaga por parcela de 100 $m^{2}$.
En una hectárea, ¿cuál es el número esperado de plantas con plaga? (Una hectárea tiene una medida de 100 m x 100 m, es decir, una hectárea son 100 parcelas).
**Sol:**
Sea $X_{i}$ la v.a. del número de plantas con plaga de una parcela $i$. Por el supuesto de que $X_{i}\sim \text{Poisson}(2.5)$, tenemos que los eventos en cada parcela son independientes. Entonces podemos definir $Y$ el número de plantas con plaga en una hectárea, de forma que $Y=\sum_{i=1}^{100}X_{i}$. Tenemos entonces que 
$$
	E(Y)=E\left( \sum_{i=1}^{100}X_{i} \right)=\sum_{i=1}^{100}E(X_{i})=\sum_{i=1}^{100}\lambda=100(2.5)=250.
$$
De cierta forma, esto se generaliza a que $Y\sim\text{Poisson}(\lambda'=250)$.
Ahora, supongamos que queremos calcular la probabilidad de que haya 300 plantas con plaga en una hectárea, es decir 
$$
	P(Y=300)=\frac{(250)^{300}e^{-250}}{300!}.
$$

##### Ejemplo:
Sea $D(t)$ el número de casos de una cierta enfermedad infecciosa al día $t$, $t=0,1,2,\dots$ Si suponemos que $D(t)\sim\text{Poisson}(\lambda_{t})$. Es decir que $\lambda_{t}$ depende del modelo epidemiológico $D(t)$. Se pude llegar a una ecuación diferencial que modele al parámetro $\lambda_{t}$:
$$
	\frac{d}{dt}\lambda_{t}=r\lambda_{t}\left( 1-\frac{\lambda_{t}}{k} \right).
$$

