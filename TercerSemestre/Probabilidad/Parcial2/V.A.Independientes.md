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

De forma natural se extiende la idea de que la independencia de dos variables aleatorias de cumple si 
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