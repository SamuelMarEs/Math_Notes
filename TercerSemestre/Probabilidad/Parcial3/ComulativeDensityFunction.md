#Probabilidad 
La función de distribución acumulada de una [[V.A.Continuas|v.a. continua]] cumple:
a) $\lim_{ x \to \infty }F(x)=1$;
b) $\lim_{ x \to -\infty }F(x)=0$;
c) $F(x)$ es no decreciente, es decir, sean $x_{1},x_{2}\in\mathbb{R}$ tal que $x_{1}<x_{2}$, entonces $F(x_{1})\leq F(x_{2})$.
d) $F(x)$ es continua.

Una consecuencia directa del teorema fundamental del cálculo es que la función de densidad $f(x)$ se puede encontrar a partir de $F(x)$ mediante la siguiente operación: 
$$
	f(x)=\frac{d}{dx}F(x).
$$
##### Ejemplo:
Sea $X$ una v.a. continua con función de distribución $F(x)=\begin{cases}1-e^{-\lambda x}, & x>0,\lambda>0 \\  0, & \text{en otro caso}\end{cases}$. Si queremos encontrar la función de densidad, basta realizar la operación:
$$
	f(x)=\frac{d}{dt}F(x)=\frac{d}{dx}1-e^{-\lambda x}=\lambda e^{-\lambda x}.
$$
Más concretamente tenemos que $f(x)=\begin{cases}\lambda e^{-\lambda x}, & x>0,\lambda >0 \\  0, & \text{en otro caso}\end{cases}$.


#### Teorema de Cambio de Variable (v.a. continuas)
Sea $X$ una v.a. continua con función de densidad $f_{x}(x)$ y función de distribución $F_{x}(x)$, y sea $\psi$ una transformación de $\mathbb{R}$ en $\mathbb{R}$ monótona creciente o decreciente. Sea $Y=\psi(X)$. La función de densidad de $Y$ está dada por 
$$
	f_{y}(y)=f_{x}(\psi ^{-1}(y))\cdot \left\lvert  \frac{d}{dy}\psi ^{-1}(y)  \right\rvert ,
$$
si $y\in \mathrm{Rango}(\psi(X))$, y es cero en otro caso.
Aquí, $\psi ^{-1}(X)$ es la función inversa de $\psi(X)$.
##### Demostración:
Primero consideremos el caso en el que $\psi$ es creciente. Notar que 
$$
	F_{y}(y)=P(Y\leq y)=P(\psi(X)\leq y)=P(X\leq \psi ^{-1}(y)),
$$
este último paso se garantiza dado que $\psi$ es monótona creciente. Entonces tenemos que 
$$
	F_{y}(y)=P(X\leq \psi ^{-1}(y))=F_{x}(\psi ^{-1}(y)).
$$
Ahora, solo tenemos que derivar para obtener que 
$$
	f_{y}(y)=\frac{d}{dy}F_{y}(y)=\frac{d}{dy}F_{x}(\psi ^{-1}(y))=f_{x}(\psi ^{-1}(y))\cdot \frac{d}{dy}\psi ^{-1}(y).
$$
Ahora, consideremos el caso donde $\psi$ es monótona decreciente. Siguiendo una lógica similar, tenemos que 
$$
	F_{y}(y)=1-P(Y>y)=1-P(\psi(X)>y)=1-P(X\leq \psi ^{-1}(y))=1-F_{x}(\psi ^{-1}(y)).
$$
Por lo tanto, nuevamente basta con que derivemos para obtener que 
$$
	f_{y}(y)=\frac{d}{dy}F_{y}(y)=\frac{d}{dy}1-F_{x}(\psi ^{-1}(y))=-f_{x}(\psi ^{-1}(y))\cdot \frac{d}{dy}\psi ^{-1}(y).
$$
Como $\psi ^{-1}$ es decreciente, su derivada es negativa, por lo que $-\frac{d}{dy}\psi ^{-1}(y)=\left\lvert  \frac{d}{dy}\psi ^{-1}(y)  \right\rvert$. Por lo tanto tenemos que en ambos casos 
$$
	f_{y}(y)=f_{x}(\psi ^{-1}(y))\cdot \left\lvert  \frac{d}{dy}\psi ^{-1}(y)  \right\rvert .\qquad\square
$$
##### Ejemplos:
1.- Sea $X$ una v.a. continua con pdf $f(x)=\begin{cases}1, & x\in(0,1) \\  0, & \text{en otro caso}\end{cases}$. Encontrar la función de densidad de $Y=x^{2}$.
**Sol:**
Nuestra función $\psi(x)=x^{2}$ es monótona creciente en el intervalo $(0,1)$, y la función inversa es $\psi ^{-1}(x)=\sqrt{ x }$. Si aplicamos directamente el teorema, tenemos que 
$$
	f_{y}(y)=f_{x}(\psi ^{-1}(x))\cdot \left\lvert  \frac{d}{dt}\psi ^{-1}(y)  \right\rvert =1\cdot\left( \frac{1}{2\sqrt{ y }} \right),
$$
entonces tenemos que 
$$
	f_{y}(y)=\begin{cases}
	\frac{1}{2\sqrt{ y }}, & y\in(0,1) \\
	0, & \text{en otro caso}
	\end{cases}.
$$

2.- Sea $X$ una v.a. continua con pdf dada por $f(x)=\frac{1}{\sqrt{ 2\pi }}\exp\left( -\frac{x^{2}}{2} \right)$. Sea $Y=e^{x}$. Encontrar $f_{y}(y)$.
**Sol:**
La función $\psi(x)=e^{x}$ es monótona creciente, y su inversa es $\psi ^{-1}(x)=\ln(x)$ para $x\in(0,\infty)$. Tenemos entonces que $\frac{d}{dy}\psi ^{-1}(y)=\frac{1}{y}$. Entonces, aplicando el teorema tenemos que 
$$
	f_{y}(y)=\frac{1}{\sqrt{ 2\pi }}\exp\left( -\frac{(\ln y)^{2}}{2} \right)\cdot \frac{1}{y},\quad y\in(0,\infty).
$$
La v.a. $X$ sigue una distribución normal con media $\mu=0$ y desviación estándar $\sigma=1$, i.e. es una Gaussiana estándar o Normal estándar. La transformación se conoce como una distribución log-normal.

3.- Sea $X$ una v.a. continua con pdf dada por $f(x)=\begin{cases}e^{-x}, & x>0 \\  0, & \text{en otro caso}\end{cases}$. Sea $Y=\frac{1}{X}$. Encontrar y graficar $f_{y}(y)$.
**Sol:**
Nuestra transformación es $\psi(x)=\frac{1}{x}$ que es monótona decreciente. Su función inversa es ella misma, es decir $\psi ^{-1}(x)=\frac{1}{x}$. La derivada es $\frac{d}{dt}\psi ^{-1}(x)=-\frac{1}{x^{2}}$. Entonces 
$$
	f_{y}(y)=\begin{cases}
    \frac{e^{-1 / y}}{y^{2}}, & x>0, \\
	0, & \text{en otro caso}
	\end{cases}.
$$

4.- Sea $X$ una v.a. continua con pdf dada por $f_{x}(x)=\begin{cases}c(1-|2x-1|), & x\in(0,1) \\  0, & \text{en otro caso}\end{cases}$.
a) Encuentre el valor de $c$ que hace que $f_{x}(x)$ sea función de densidad.
b) Encuentre $f_{y}(y)$ para 
- $Y=(X-1)^{2}$,
- $Y=\frac{1}{X}$,
- $Y=\ln X$.
**Sol:**
a) Queremos encontrar $c$ tal que 
$$
	\int_{-\infty}^{\infty}c(1-\lvert 2x-1 \rvert )dx=c\int_{0}^{1}1-\lvert 2x-1 \rvert dx=1,
$$
o lo que es lo mismo que 
$$
	c\left(\int_{0}^{1}dx-\left( \int_{0}^{1 / 2}-2x+1dx+\int_{1/2}^{1}2x-1dx \right)\right)=1,
$$
que es lo mismo que 
$$
	c\left(1-\left( \left( -\frac{1}{4}+\frac{1}{2}\right) +\left( -\frac{1}{4}+\frac{1}{2} \right) \right)\right)=1\implies \frac{c}{2}=1\implies c=2.
$$
b) 
Primero, para $Y=(X-1)^{2}$, la función $\psi (x)=(x-1)^{2}$ es monótona decreciente en $(0,1)$, y su inversa es $\psi ^{-1}(y)=-\sqrt{ y }+1$, cuya derivada es $\frac{d}{dy}\psi ^{-1}(y)=-\frac{1}{2\sqrt{ y }}$. Entonces la pdf es 
$$
	f_{y}(y)=\begin{cases}
	1-\left\lvert  -2\sqrt{ y }+1 \right\rvert\cdot 1/\sqrt{ y } , & y\in(0,1) \\
	0, & \text{en otro caso}
	\end{cases}.
$$
Ahora, sea $Y=\frac{1}{X}$, entonces nuestra transformación es $\psi(x)=\frac{1}{x}$ que es monótona decreciente en $(0,1)$, y su inversa es la misma $\psi ^{-1}(y)=\frac{1}{y}$ con derivada $\frac{d}{dy}\psi ^{-1}(y)=-\frac{1}{y^{2}}$, por lo que la pdf es 
$$
	f_{y}(y)=\begin{cases}
	\left( 2-2\left\lvert  \frac{2}{y}-1  \right\rvert \right)\cdot \frac{1}{y^{2}}, & y\in(0,1) \\
	0, & \text{en otro caso}. 
	\end{cases}
$$
Por último, sea $Y=\ln X$, nuestra transformación es $\psi(x)=\ln x$, que es monótona creciente, cuya inversa es $\psi ^{-1}(y)=e^{y}$ con derivada $\frac{d}{dy}\psi ^{-1}(y)=e^{y}$, por lo tanto la función de distribución es 
$$
	f_{y}(y)=\begin{cases}
	(2-2\lvert 2e^{y}-1 \rvert )e^{y}, & y\in(-\infty,0) \\
	0, & \text{en otro caso}.
	\end{cases}
$$

