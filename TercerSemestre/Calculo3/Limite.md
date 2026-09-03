Recordemos que, sea $f:R\to R$, decimos que $\lim_{ x \to a }f(x)=L$ si y sólo si 
$$
	\forall \varepsilon>0,\exists \delta>0:|x-a|<\delta\Rightarrow|f(x)-L|<\varepsilon.
$$
Además sabemos que 
$$
	\lim_{ x \to a }f(x)=L\Longleftrightarrow\lim_{ x \to a^{-} }f(x)=\lim_{ x \to a^{+} } f(x) = L  .
$$
La noción de que una [[Funciones|función]] tienda a algo cuando es de una variable es bastante intuitiva. Sin embargo, queremos generalizar esta noción de "acercarse" a otras dimensiones. 

##### Definición:
Sea $f:R^{n}\to R$ con dominio $A\subset R^{n}$, donde $A$ es un [[ConjuntosAbiertos|conjunto abierto]]. Sea $x_{0}\in A$ ó $x_{0}$ un punto en la frontera de $A$ y $N$ una vecindad de $b\in R$.
Decimos que $b$ es límite de $f$ cuando $x$ tiende a $x_{0}$ si existe una vecindad $U$ de $x_{0}$ tal que $x\neq x_{0}$, con $x\in U$ y $x\in A$ implica $f(x)\in N$, y escribimos 
$$
	\lim_{ x \to x_{0} } f(x)=b,
$$
es decir $\exists U\subset R^{n}$ tal que $x_{0}\in U$ y $f(U\setminus\{ x_{0} \})\subset N,\forall N$ tal que $b\in N$. 
La misma noción se puede extender para una función $f:R^{n}\to R^{m}$ de forma análoga.

#### Teorema
Si $\lim_{ x \to x_{0} }f(x)=L$, entonces para cualquier función continua $\gamma:(-\varepsilon,\varepsilon)\to R$ tal que $\gamma(0)=x_{0}$ y $\gamma(t)\neq x_{0}$ si $t\neq 0$, se cumple que 
$$
	\lim_{ t \to 0 } f(\gamma(t))=L.
$$
A esta función $\gamma$ le llamamos una trayectoria, y la noción es que todas las trayectorias que pasen por el punto $x_{0}$ deben converger al mismo límite.
La demostración requiere conceptos que no hemos visto.
![[LimitesPorTrayectorias]]
#### Ejercicios
1.- Encuentre, si existe $\lim_{ (x,y) \to (0,0) } \frac{x^{2}-y^{2}}{x^{2}+y^{2}}$.
**Sol:** Observemos que a lo largo de $y=x$, tenemos 
$$
	\lim_{ x \to 0 }= \frac{x^{2}-x^{2}}{x^{2}+x^{2}} =0.
$$
Por otro lado, a lo largo de $y=2x$, tenemos que 
$$
	\lim_{ x \to 0 } \frac{x^{2}-4x^{2}}{x^{2}+4x^{2}}=-\frac{3}{5}.
$$
Entonces, por el teorema anterior tenemos que el límite no existe.

2.- Encuentre, si existe $\lim_{ (x,y) \to (0,0) } \frac{\sin(x^{2}+y^{2})}{x^{2}+y^{2}}$.
**Sol:** Podemos definir $u=x^{2}+y^{2}$, de forma que tenemos el límite 
$$
	\lim_{ u \to 0 } \frac{\sin(u)}{u}=1, 
$$
pues es un límite que ya conocemos.
En realidad, la forma correcta sería demostrar el límite por definicón, porqué no hemos demostrdo que la comosición de funciones continuas es continua para funciones de multiples variables.
Es decir, queremos demostrar que: 
$$
	\forall V\text{ abierto en $R$ tq }1\in V,\exists U\text{ abierto en $R^{2}$ tq }(0,0)\in U \text{ y }f(U\setminus(0,0))\subset V.
$$

Para poder simplificar la definición a la hora de querer demostrar un límite, vamos a demostrar primero el siguiente teorema:
#### Teorema
Sea $f:R^{n}\to R$, entonces $$\lim_{ x \to x_{0} }f(x)=L$$ si y sólo si 
$$
	\forall\varepsilon>0,\exists \delta>0\text{ tq }0\leq \lvert x-x_{0} \rvert <\delta\implies \lvert f(x)-L \rvert <\varepsilon.
$$
##### Demostración
$\Rightarrow$ Dado $\varepsilon>0$, el conjunto $V=(L-\varepsilon,L+\varepsilon)$ es un abierto en $R$ que contiene a $L$. Por la definición de límite (en $R^{n}$), existe un abierto $U\in R^{n}$ tal que $x_{0}\in U$ y $f(U\setminus \{ x_{0} \})\subset U$.
Como $U$ es abierto, entonces existe un $r>0$ tal que $B_{r}(x_{0})\subset U$. Entonces definimos a $\delta=r$, y vamos a demostrar que, en efecto, 
$$
	0\leq \lvert x-x_{0} \rvert<\delta\Rightarrow \lvert f(x)-L \rvert <\varepsilon. 
$$
Sabemos que $x\in B_{\delta}(x_{0})$, y por definición tenemos que $\lvert x-x_{0} \rvert<r=\delta$. Entonces sea $x\in B_{\delta}(x_{0})$ o equivalentemente $\lvert x-x_{0} \rvert<\delta$, tenemos entonces que $f(x)\in V$ por la definición de límite, es decir que $f(x)\in B_{\varepsilon}(L)$ que es equivalente al intervalo $(L-\varepsilon,L+\varepsilon)$, es decir que 
$$
	\lvert f(x)-L \rvert<\varepsilon. \quad\square
$$

$\Leftarrow$ Sea $V$ un abierto en $R$ con $L\in V$. Queremos demostrar que existe un $U\in R^{n}$ con $x_{0}\in U$ tal que $f(U\setminus \{ x_{0} \})\subset V$.
Cualquier abierto $V\subset R$ que contenga a $L$, sabemos que $B_{\varepsilon}(L)\subset V$ para algún $\varepsilon$, es decir que $L-\varepsilon<c<L+\varepsilon\Rightarrow x\in V$ para cualquier $c$. Sabemos que $\forall\varepsilon>0$ va a existir un $\delta$ que satisfaga la definición de límite, entonces definamos el abierto $U=B_{\delta}(x_{0})$. Entonces tenemos que $\forall x\in U\setminus \{ x_{0} \}$ se satisface que $0\leq\lvert x-x_{0} \rvert<\delta$, y por la definición de limite esto implica que $\lvert f(x)-L \rvert<\varepsilon$, que a su vez implica que $L-\varepsilon < f(x)<L+\varepsilon$, y por lo tanto $f(x)\in V.\quad\square$ 

Esta demostración se generaliza de igual forma a funciones de $R^{n}$ en $R^{m}$, pero ahora en vez de trabajar con $\varepsilon$ y $\delta$ escalares, serían puntos en $R^{m}$.


#Calculo