#Calculo 
Sea $U\subset R^{n}$ un abierto.
##### Teorema:
Sea $f:U\to R^{m}$ diferenciable en $x_{0}$ y sea $c$ un número real. Entonces $h(x)=cf(x)$ es diferenciable en $x_{0}$, y 
$$
	Dh(x_{0})=cDf(x_{0}).
$$
###### Demostración:
Supongamos que $f:U\to R^{m}$ es diferenciable en $x_{0}$, entonces 
$$
	\lim_{ x \to x_{0} } \frac{\lvert f(x)-f(x_{0})-Df(x_{0})(x-x_{0}) \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }=0.
$$
Entonces tenemos que 
$$
	\lim_{ x \to x_{0} } \frac{\lvert cf(x)-cf(x_{0})-cDf(x_{0})(x-x_{0}) \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }=\lim_{ x \to x_{0} } \frac{\lvert c \rvert \lvert f(x)-f(x_{0})-Df(x_{0})(x-x_{0}) \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }=\lvert x \rvert 0=0. 
$$
##### Teorema:
Sean $f:U\to R^{m}$ y $g:U\to R^{m}$ diferenciables en $x_{0}$. Entonces $h(x)=f(x)+g(x)$ es diferenciable en $x_{0}$, y 
$$
	Dh(x_{0})=Df(x_{0})+Dg(x_{0}).
$$
###### Demostración:
Queremos demostrar que 
$$
	\lim_{ x \to x_{0} } \frac{\lvert \lvert (f(x)+g(x))-(f(x_{0})+g(x_{0}))-Df(x_{0})(x-x_{0})-Dg(x_{0})(x-x_{0}) \rvert  \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }=0.
$$
Este límite lo podemos expresar como 
$$
	\lim_{ x \to x_{0} } \frac{\lvert \lvert [f(x)-f(x_{0})-Df(x_{0})(x-x_{0})]+[g(x)-g(x_{0})-Dg(x_{0})(x-x_{0})] \rvert  \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert },
$$
y por desigualdad tirangular tenemos que esto es menor o igual que 
$$
	\leq\lim_{ x \to x_{0} } \frac{\lvert f(x)-f(x_{0})-Df(x_{0})(x-x_{0}) \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }+\lim_{ x \to x_{0} } \frac{\lvert g(x)-g(x_{0})-Dg(x_{0})(x-x_{0}) \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }=0+0=0.
$$
Entonces tenemos que 
$$
	0\leq\lim_{ x \to x_{0} } \frac{\lvert \lvert (f(x)+g(x))-(f(x_{0})+g(x_{0}))-Df(x_{0})(x-x_{0})-Dg(x_{0})(x-x_{0}) \rvert  \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }\leq0,
$$
es decir que 
$$
	\lim_{ x \to x_{0} } \frac{\lvert \lvert (f(x)+g(x))-(f(x_{0})+g(x_{0}))-Df(x_{0})(x-x_{0})-Dg(x_{0})(x-x_{0}) \rvert  \rvert }{\lvert \lvert x-x_{0} \rvert  \rvert }=0.\quad\square
$$

##### Teorema:
Sean $f:U\to R$ y $g:U\to R$ diferenciables en $x_{0}$. Entonces $h(x)=f(x)g(x)$ es diferenciable en $x_{0},$ y 
$$
	Dh(x_{0})=g(x_{0})Df(x_{0})+f(x_{0})Dg(x_{0}).
$$
###### Demostración:

##### Teorema:
Sean $f:U\to R$ y $g:U\to R$ diferenciables en $x_{0}$, supongamos que $g$ nunca es cero en $U$. Entonces $h=\frac{f(x)}{g(x)}$ es diferenciable en $x_{0}$ y 
$$
	Dh(x_{0})=\frac{g(x_{0})Df(x_{0})-f(x_{0})Dg(x_{0})}{g^{2}(x_{0})}.
$$
###### Demostración:
(A lo mejor es más sencillo demostrar primero el caso para $D\frac{1}{g}$).
