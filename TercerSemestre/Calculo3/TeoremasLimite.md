Sean $f,g:R^{n}\to R^{m}$ dos funciones con dominio $A\subset R^{n}$ para $A$ abierto. Sea $x_{0}\in A$ o alternativamente $x_{0}$ un punto en la frontera de $A$. Sean $b\in R^{m}$ y $c\in R$. Entonces las siguientes propiedades se satisfacen:
1. Si $\lim_{ x \to x_{0} }f(x)=b$, entonces $\lim_{ x \to x_{0} }cf(x)=c b$.
2. Si $\lim_{ x \to x_{0} }f(x)=b_{1}$ y $\lim_{ x \to x_{0} }g(x)=b_{2}$, entonces 
   $$
   	\lim_{ x \to x_{0} } (f+g)(x)=b_{1}+b_{2}, \lim_{ x \to x_{0} } (fg)(x)=b_{1}b_{2},\quad\text{y}\quad\lim_{ x \to x_{0} } \frac{1}{f(x)}=\frac{1}{b}.
   $$
   La segunda igualdad tiene la condición agregada que $m=1$, es decir que las funciones están definidas como $f,g:R^{n}\to R$, puesto que no podemos trabajar el producto de dos vectores.
   La última igualdad se satisface siempre que $b\neq 0$ y $f(x)\neq 0,\forall A$.
3. Si $f(x)=(f_{1}(x),f_{2}(x),\dots,f_{m}(x))$ para cada $f_{i}:R^{n}\to R$. Entonces tenemos que 
   $$
   	\lim_{ x \to x_{0} } f(x)=b=(b_{1},\dots,b_{n})\Longleftrightarrow\lim_{ x \to x_{0} } f_{i}(x)=b_{i}.
   $$
##### Demostración:
Las primeras 2 partes del teorema se demuestran igual que para funciones de $R$ en $R$, gracias al teorema que extiende la definición a [[Limite|epsilon y deltas]].
A continuación la demostración para la tercera parte:
$\Rightarrow$ Si $\lim_{ x \to x_{0} }f(x)=b$, entonces sabemos que 
$$
	\begin{align}
	\forall\varepsilon>0,\exists \delta>0:\lvert x-x_{0} \rvert <\delta &\Rightarrow \lvert f(x)-b \rvert <\varepsilon \\
	&\Rightarrow \lvert (f_{1}(x),\dots,f_{m}(x))-(b_{1},\dots,b_{m}) \rvert<\varepsilon \\
	&\Rightarrow \sqrt{ (f_{1}(x)-b_{1})^{2}+\dots+(f_{m}(x)-b_{m})^{2} }<\varepsilon \\
	&\Rightarrow \sqrt{ (f_{i}(x)-b_{i})^{2} }<\varepsilon \\
	&\Rightarrow \lvert f_{i}(x)-b_{i} \rvert <\varepsilon. 
	\end{align}
$$
$\Leftarrow$ Si $\lim_{ x \to x_{0} }f_{i}(x)=b_{i}$, entonces, para todo $\varepsilon_{i}>0$ existen $\delta_{i}>0$ tales que 
$$
	\lvert x-x_{0} \rvert<\delta_{i}\Rightarrow \lvert f_{i}(x)-b_{i} \rvert <\varepsilon. 
$$
Queremos demostrar que, para todo $\varepsilon>0,\exists \delta>0$ tal que la definición tradicional de límite se satisface. Tomemos a cada uno de nuestros $\varepsilon_{i}$ como $\varepsilon_{i}=\frac{\varepsilon}{m}$, además tomemos a $\delta=\min\{ \delta_{i} \}$. Entonces, sea 
$$
	\lvert x-x_{0} \rvert <\delta<\delta_{i}\quad\forall i=1,\dots,m,
$$
por la existencia de cada límite, se cumple que 
$$
	\lvert f_{i}(x)-b_{i} \rvert < \frac{\varepsilon}{m},
$$
y por lo tanto 
$$
	\lvert f(x)-b \rvert =\lvert (f_{1}(x),\dots,f_{m}(x))-(b_{1},\dots,b_{m}) \rvert =\lvert f_{1}(x)-b_{1} \rvert+\dots+\lvert f_{m}(x)-b_{m} \rvert <\varepsilon.\quad\square
$$


#Calculo #Teorema