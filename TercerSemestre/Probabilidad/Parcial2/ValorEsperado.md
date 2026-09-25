#Probabilidad
#### Definición:
Sea $X$ una [[VariablesAleatorias|variable aleatoria]] discreta con valores $x_{1},x_{2},\dots$ y pdf $f(x)$. El ***valor esperado*** o ***esperanza*** (o media) de $X$ está dado por 
$$
	E(X)=\sum_{x}xP(X=x).
$$
El valor esperado nos indica cual es el resultado promedio de $X$.

##### Ejemplo:
Sea $X\sim\text{Poisson}(\lambda)$, es decir 
$$
	P(X=x)=\begin{cases}
	\frac{\lambda^{x}e^{-\lambda}}{x!}, & x=0,1,2,\dots \\
	0, & \text{otro caso}.
	\end{cases}
$$
Entonces tenemos que 
$$
	E(X)=\sum_{x=0}^{\infty}xP(X=x)=\sum_{x=0}^{\infty} \frac{x\lambda^{x}e^{-\lambda}}{x!}=\lambda.
$$
(La última igualdad no es obvia, pero no debería ser muy complicado demostrarla).

Al parámetro $\lambda$ se le conoce como parámetro de intensidad y denota el # promedio de ocurrencias de un evento en un intervalo de tiempo determinado.

#### Proposición:
Algunas de las propiedades del valor esperado.
1.- $E(c)=c$.
2.- $E(cX)=cE(X)$.
3.- Si $X\geq0$, entonces $E(X)\geq0$.
4.- $E(X+Y)=E(X)+E(Y)$.
5.- $E(aX+b)=aE(X)+b$.
6.- $E(XY)=E(X)E(Y)$ siempre que $X$ y $Y$ sean independientes.
##### Demostración:
1.-