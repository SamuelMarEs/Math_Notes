#Calculo #Teorema 
Al estudiar funciones de varias variables, también nos interesa encontrar máximos y mínimos, y para esto ocupamos un criterio que nos permita detectar punto extremos, de forma similar al cálculo de una variable.
Para funciones suaves de una variable, el teorema de Taylor (el mismo de las series) asegura que 
$$
	f(x)=f(a)+f'(a)(x-a)+\frac{f''(a)}{2!}(x-a)^{2}+\dots+ \frac{f^{(k)(a)}}{k!}(x-a)^{k}+R_{k}(x,a),
$$
donde 
$$
	R_{k}(x,a)=\int_{a}^{x} \frac{(x-t)^{k}}{k!}f^{(k+1)}(t)dt
$$
es el residuo de la aproximación usando una serie de Taylor finita.
Queremos generalizar este resultado a funciones de varias variables. Dada una función diferenciable en un punto $x_{0}$, $f:R^{n}\to R$, ya podemos dar un caso inicial del teorema de Taylor. De forma similar a un plano tangente, definamos 
$$
	R_{1}(x,x_{0})=f(x)-f(x_{0})-Df(x_{0})\cdot(x-x_{0}),
$$
de modo que tenemos que 
$$
	f(x)=f(x_{0})+Df(x_{0})\cdot(x-x_{0})+R_{1}(x,x_{0}),
$$
donde por la definición de diferenciabilidad (i.e. confirmando que $R_{1}$ es el plano tangente a la curva), tenemos que 
$$
	\frac{\lvert R_{1}(x,x_{0}) \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert}\to 0\quad\text{cuando}\quad x\to x_{0}.
$$

Lo siguiente, de acuerdo al libro, constituye un abuso de notación, pero definamos $h=x-x_{0}$, de modo que $R_{1}(x,x_{0})=R_{1}(h,x_{0})$.
Entonces tenemos los siguientes dos teoremas:

#### Teorema 1. Fórmula de Taylor de primer orden
Sea $f:U\subset R^{n}\to R$ diferenciable en $x_{0}\in U$. Entonces podemos escribir 
$$
	f(x_{0}+h)=f(x_{0})+\sum_{i=1}^{n}h_{i} \frac{\partial f}{\partial x_{i}}(x_{0})+R_{1}(h,x_{0}),
$$
donde $\frac{R_{1}(h,x_{0})}{\lvert \lvert h \rvert \rvert}\to 0$ cuando $h\to 0$.
Este teorema es básicamente lo que se acaba de enunciar anteriormente.

#### Teorema 2. Fórmula de Taylor de segundo orden
Sea $f:U\subset R^{n}\to R$ con derivadas parciales continuas hasta de tercer orden. Entonces podemos escribir 
$$
	f(x_{0}+h)=f(x_{0})+\sum_{i=0}^{n}h_{i} \frac{\partial f}{\partial x_{i}}(x_{0})+ \frac{1}{2}\sum_{i,j=1}^{n}h_{i}h_{j} \frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}(x_{0})+R_{2}(h,x_{0}),
$$
dónde se tiene que 
$$
	\frac{R_{2}(h,x_{0})}{\lvert \lvert h \rvert  \rvert ^{2}}\to 0\quad\text{cuando}\quad h\to 0. 
$$
La fórmula explícita del residuo $R_{2}$ se obtiene durante la demostración.
##### Demostración:
Primero, restringimos nuestra función a la recta $x_{0}+th$ para $h,x_{0}$ constantes. Usando la regla de la cadena, llegamos a que 
$$
	\frac{d}{dt}f(x_{0}+th)=Df(x_{0}+th)\cdot h=\sum_{i=1}^{n} \frac{\partial f}{\partial x_{i}}(x_{0}+th)\cdot h_{i},
$$
y podemos integrar ambos lados en el intervalo $[0,1]$ para obtener que 
$$
	f(x_{0}+h)-f(x_{0})=\int_{0}^{1}\sum_{i=1}^{n} \frac{\partial f}{\partial x_{i}}(x_{0}+th)h_{i}dt=\sum_{i=1}^{n}\int_{0}^{1} \frac{\partial f}{\partial x_{i}}(x_{0}+th)h_{i}dt.
$$
Se puede aplicar integración por partes para resolver la integral, tomando $u=\frac{\partial f}{\partial x_{i}}(x_{0}+th)h_{i}$, y tomando $v=t+1$ (para un día vi una vaca vestida de uniforme). Esto nos permite llegar a que 
$$
	\sum_{i=1}^{n}\int_{0}^{1} \frac{\partial f}{\partial x_{i}}(x_{0}+th)h_{i}dt=\sum_{i,j=1}^{n}\int_{0}^{1}(1-t) \frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}(x_{0}+th)h_{i}h_{j}dt+\sum_{i=1}h_{i} \frac{\partial f}{\partial x_{i}}(x_{0}).
$$
Esto es suficiente para probar el Teorema 1, pues llegamos a que 
$$
		f(x_{0}+h)=f(x_{0})+\sum_{i=1}^{n}h_{i} \frac{\partial f}{\partial x_{i}}(x_{0})+R_{1}(h,x_{0}),
$$
donde la expresión para el residuo es 
$$
	R_{1}(h,x_{0})=\sum_{i,j=1}^{n}\int_{0}^{1}(1-t) \frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}(x_{0}+th)h_{i}h_{j}dt.
$$
Si volvemos a integrar por partes este residuo, nuevamente por pares, pero ahora tomando 
$$
	u = \frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}(x_{0}+th)h_{i}h_{j}\quad\text{y}\quad v=-\frac{(t-1)^{2}}{2},
$$
llegamos a que 
$$
	R_{1}(h,x_{0})=\sum_{i,j,k=1}^{n}\int_{0}^{1} \frac{(t-1)^{2}}{2} \frac{\partial^{3}f}{\partial x_{i}\partial x_{j}\partial x_{k}}(x_{0}+th)h_{i}h_{j}h_{k}dt+\sum_{i,j=1}^{n} \frac{1}{2} \frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}(x_{0})h_{i}h_{j},
$$
donde podemos ver que ya tenemos completa la expresión que buscábamos, y tenemos que nuestro nuevo residuo es 
$$
	R_{2}(h,x_{0})=\sum_{i,j,k=1}^{n}\int_{0}^{1} \frac{(t-1)^{2}}{2} \frac{\partial^{3}f}{\partial x_{i}\partial x_{j}\partial x_{k}}(x_{0}+th)h_{i}h_{j}h_{k}dt.
$$
Para probar que este residuo satisface que $\lvert R_{2}(h,x_{0}) \rvert / \lvert \lvert h \rvert  \rvert ^{2}\to 0$, basta ver que estamos integrando una función continua de $t$, y por lo tanto la podemos acotar dentro de una pequeña vecindad de $x_{0}.\quad\square$ 


No es difícil tratar de generalizar el teorema de Taylor a mayores órdenes, pues esto se puede seguir haciendo de forma casi idéntica al caso de funciones de una sola variable, solo hace falta seguir agregando $\partial x_{i}\partial x_{j}\partial x_{k}\dots \partial x_{l}$, y así sucesivamente.

##### Ejemplos:
1.- Encontrar Taylor de segundo orden alrededor de $x_{0}=(0,0)$, para $f(x,y)=\sin(x+2y)$.
**Sol:**
Las primeras derivadas parciales son
$$
	\frac{\partial f}{\partial x}=\cos(x+2y),\quad \frac{\partial f}{\partial y}=2\cos(x+2y).
$$
Para calcular las segundas parciales, dado que el orden de estas no importa, tenemos que 
$$
	\frac{\partial^{2} f}{\partial x^{2}}=-\sin(x+2y),\quad \frac{\partial^{2}f}{\partial y^{2}}=-4\sin(x+2y),\quad \frac{\partial^{2}f}{\partial x\partial y}=-2\sin(x+2y).
$$
Entonces 
$$
    \begin{align}
	f(h)&=\sin(0)+h_{1}\cos(0)+2h_{2}\cos(0)+\frac{1}{2}h_{1}^{2}(-\sin(0))+\frac{1}{2}h_{2}^{2}(-4\sin(0))+h_{1}h_{2}(-2\sin(0)) \\
	&=0+h_{1}+2h_{2}+0+0+0 \\
	&=h_{1} +2h_{2}.
	\end{align}
$$
(Todo esto más el residuo).

2.- Ahora para $f(x,y)=e^{x}\cos y$.
**Sol:**
Las primeras parciales son 
$$
	\frac{\partial f}{\partial x}=e^{x}\cos y,\quad \frac{\partial f}{\partial y}=-e^{x}\sin y.
$$
Y las segundas parciales son 
$$
	\frac{\partial^{2}f}{\partial x^{2}}=e^{x}\cos y,\quad \frac{\partial^{2} f}{\partial y^{2}}=-e^{x}\cos y,\quad \frac{\partial^{2} f}{\partial x \partial y}=-e^{x}\sin y.
$$
Evaluadas en $(0,0)$ en el orden anterior, los resultados son $1,0,1,-1,0$, respectivamente. Entonces 
$$
	\begin{align}
	f(h)&=1+h_{1}+0+\frac{1}{2}h_{1}^{2}+0+0+\frac{1}{2}h_{2}^{2}(-1) \\
	&=1+h_{1}+\frac{1}{2}h_{1}^{2} -\frac{1}{2}h_{2}^{2}.
	\end{align}
$$
(más el residuo que es $R_{2}(0,h)=-\frac{h_{1}h_{2}^{2}}{2}-\frac{h_{1}^{2}h_{2}^{2}}{4}$)

3.- Sea $f(x,y)=\sin xy$, encontrar Taylor de segundo orden para $(1,\pi/2)$.
**Sol:**
Denotemos la parcial respecto a $x$ como $f_{x}$ y análogamente para las demás. Entonces tenemos que 
$$
	f_{x}=y\cos xy,\quad f_{y}=x\cos xy,\quad f_{x x}=-y^{2}\sin xy,\quad f_{yy}=-x^{2}\sin xy,\quad f_{xy}=-xy\sin xy.
$$
En ese mismo orden, los valores al evaluar en el punto $(1,\pi / 2)$ son $0,0,- \pi^{2} / 4,-1,-\pi / 2$. Además, $f(1,\pi / 2)=1$. 
Entonces tenemos que la función es: 
$$
	f\left( 1+h_{1}, \frac{\pi}{2}+h_{2} \right)=1+0h_{1}+0h_{2}- \frac{\pi^{2}}{8}h_{1}^{2}-\frac{h_{2}^{2}}{2}-\frac{\pi}{2}h_{1}h_{2}+R_{2}((1,\pi / 2),h).
$$

4.- Sea $f(x,y)=\frac{(x-1)^{2}}{(y-3)^{2}}$ para $(4,6)$.
Primero, tenemos que $f(4,6)=1$.
Ahora, las parciales son 
$$
	f_{x}=\frac{2x-2}{(y-3)^{2}}, f_{y}=- \frac{(x-1)^{2}}{(y-3)^{3}},f_{x x}=\frac{2}{(y-3)^{3}},f_{yy}=\frac{6(x-1)^{2}}{(y-3)^{4}},f_{xy}=-\frac{4(x-1)}{(y-3)^{3}},
$$
cuyos valores al evaluarlos en el punto de interés son 
$$
	\frac{2}{3}, -\frac{2}{3}, \frac{2}{9}, \frac{2}{3}, -\frac{4}{9},
$$
respectivamente.