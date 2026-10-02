#Probabilidad 
Así como previamente estudiamos la [[Independencia|independencia]] de dos eventos, también podemos extender la idea a variables aleatorias.
Supongamos que tenemos dos [[VariablesAleatorias|v.a.]] $X$ y $Y$ definidas sobre un mismo espacio de probabilidad. Entonces tenemos la siguiente definición:
#### Definición:
Se dice que las variables aleatorias $X$ y $Y$ son independientes si los eventos $(X\leq x)$ y $(Y\leq y)$ son independientes para cualesquiera valores reales de $x$ y $y$, es decir, si se cumple la igualdad 
$$
	P[(X\leq x)\cap(Y\leq y)]=P(X\leq x)P(Y\leq y).
$$
El lado izquierdo también se puede escribir como $P(X\leq x,Y\leq y)$, o también como $F_{X,Y}(x,y)$.
Esta recibe el nombre de ***distribución conjunta*** de $X$ y $Y$ evaluada en $(x,y)$.

De forma natural se extiende la idea de que la independencia de dos variables aleatorias discretas se cumple si 
$$
	P(X=x,Y=y)=P(X=x)P(Y=y),
$$
en donde, por la [[LeyProbabilidadTotal|ley de probabilidad total]] tenemos que 
$$
	P(X=x)=\sum_{y}P(X=x,Y=y),
$$
y 
$$
		P(Y=y)=\sum_{x}P(X=x,Y=y).
$$
En otras palabras, la probabilidad de que $X$ tome un valor $x$ es la probabilidad de que tome el mismo valor, dado que conocemos el valor que toma para cada uno de los valores de $Y$.
Denotamos que dos variables aleatorias son independientes como $X\bot Y$.

***Note:*** Basta con que la condición $f_{x,y}(x,y)=f_{x}(x)f_{y}(y)$ no se cumple para una sola pareja $(x,y)$ para que no haya independencia.

Para cualquier colección de variables aleatorias discretas, decimos que es una colección independiente si se cumple la condición de independencia para cualquier subconjunto de variables aleatorias. (La condición de independencia por pares no es suficiente para garantizar independencia de la colección completa, aunque si toda la colección es independiente, entonces las v.a. son independientes por pares).

###### Ejemplo:
Sean $X$ y $Y$ dos v.a. independientes e idénticamente distribuidas (tienen la misma función de probabilidad).
Definamos $Z=\max\{ X,Y \}$. 
Queremos encontrar la función de distribución de $Z$: 
$$
	\begin{align}
	F_{Z}(z)=P(Z\leq z)&=P(\max\{ X,Y \}\leq z) \\
	&=P(X\leq z, Y\leq z) \\
	&=P(X\leq z)P(Y\leq z) \\
	&=[F(z)]^{2}
	\end{align}
$$
