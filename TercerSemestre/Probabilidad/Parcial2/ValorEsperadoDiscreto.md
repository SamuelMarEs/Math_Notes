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
1.- Sea $X$ una v.a. constante, es decir, $X(w)=c$ para todo $w\in \Omega$. Tenemos entonces que 
$$
	E(c)=E(X)=\sum_{x}xP(X=x).
$$
Por ser una variable aleatoria constante, $x=c$ para cualquier $w\in \Omega$, por lo tanto la variable aleatoria únicamente toma ese valor, es decir que 
$$
	E(c)=E(X)=cP(X=c),
$$
pero además $P(X=c)=1$, por lo tanto 
$$
	E(c)=c.
$$

2.- Sea $X$ una v.a.. Entonces tenemos que 
$$
	E(cX)=\sum_{x}cxP(X=x)=c\sum_{x}xP(X=x)=cE(X).
$$

3.- Sea $X\geq 0$, es decir que $x=X(w)\geq 0\forall w\in \Omega$. Notemos además que $P(X=x)\geq 0$ para cualquier $x$, esto por las propiedades de una medida de probabilidad. Entonces tenemos que $xP(X=x)\geq 0$ para todo $x$, y como la suma de números no negativos es no negativa, tenemos que $E(X)\geq 0$.

4.- Sean $X$ y $Y$ dos variables aleatorias discretas. Entonces tenemos que 
$$
	E(X+Y)=\sum_{x,y}(x+y)P(X=x,Y=y)=\sum_{x}\sum_{y}xP(X=x,Y=y)+yP(X=x,Y=y).
$$
Notemos que esto lo podemos reorganizar de la siguiente forma: 
$$
	\left(\sum_{x}x\sum_{y}P(X=x,Y=y)\right)+\left( \sum_{y}y\sum_{x}P(X=x,Y=y) \right),
$$
y por la idea de [[V.A.Independientes|probabilidad conjunta]], sabemos que $\sum_{y}P(X=x,Y=y)=P(X=x)$, y análogamente para $P(Y=y)$, por lo tanto tenemos 
$$
	\sum_{x}xP(X=x)+\sum_{y}yP(Y=y)=E(X)+E(Y).
$$

5.- Sean $X$ y $Y$ dos v.a. discretas independientes. Entonces tenemos que $P(X=x,Y=y)=P(X=x)P(Y=y)$, y por lo tanto tenemos que 
$$
	\begin{align}
	E(XY)=\sum_{x,y}xyP(X=x,Y=y)&=\sum_{x,y}xP(X=x)yP(Y=y) \\
	&=\left( \sum_{x}xP(X=x) \right)\left( \sum_{y}yP(Y=y) \right) \\
	&=E(X)E(Y).
	\end{align}
$$

