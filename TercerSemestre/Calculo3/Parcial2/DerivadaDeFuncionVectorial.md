#Calculo
Si $f:\mathbb{R}\to\mathbb{R}^{n}$, podemos escribirla en términos de sus componentes 
$$
	f(a)=(f_{1}(a),f_{2}(a),\dots,f_{n}(a)),
$$
dónde $f_{i}:\mathbb{R}\to\mathbb{R}$ para $i=1,2,\dots,n$.
Decimos que $f$ es diferenciable si $f_{i}(x)$ es diferenciable para $i=1,\dots,n$.
Sabemos que 
$$
	\begin{align}
	\frac{f(a+h)-f(a)}{h}&=\frac{(f_{1}(a+h),f_{2}(a+h),\dots,f_{n}(a+h))-(f_{1}(a),\dots,f_{n}(a))}{h} \\
	&=\left( \frac{f_{1}(a+h)}{h}, \frac{f_{2}(a+h)}{h}, \dots, \frac{f_{n}(a+h)}{h} \right),
	\end{align}
$$
entonces basta tomar el límite cuando $h\to 0$, de como que tenemos que 
$$
	\begin{align}
	\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}&=\lim_{ h \to 0 } \left( \frac{f_{1}(a+h)}{h}, \frac{f_{2}(a+h)}{h}, \dots, \frac{f_{n}(a+h)}{h} \right) \\
	&=\left( \frac{d}{dx}f_{1}(a), \dots, \frac{d}{dx}f_{n}(a) \right).
	\end{align}
$$

Sabemos que una función $c:\mathbb{R}\to\mathbb{R}^{n}$ representa una curva parametrizada. Entonces para una curva $c(t)=(x_{1}(t), x_{2}(t), \dots, x_{n}(t))$, definimos el vector tangente en el punto $c(t)$ como 
$$
	c'(t)=(x_{1}'(t), x_{2}'(t), \dots, x_{n}'(t)).
$$
![[VectorTangente]]

Si $c'(t_{0})\neq0$, definimos la recta tangenta a $c(t_{0})$ como la recta que pasa por $c(t_{0})$ en la dirección $c'(t_{0})$:
$$
	\ell(s)=c(t_{0})+sc'(t_{0}).
$$
##### Propiedades
Si $c_{1}:\mathbb{R}\to\mathbb{R}^{n}$ y $c_{2}:\mathbb{R}\to\mathbb{R}^{n}$ son diferenciables, entonces:
1. $\frac{d}{dt}(c_{1}(t)+c_{2}(t))=\frac{d}{dt} c_{1}(t)+ \frac{d}{dt}c_{2}(t)$.
2. Si $p:\mathbb{R}\to\mathbb{R}$ es diferenciable, entonces $\frac{d}{dt}(p(t)c(t))=p(t) \frac{d}{dt}c(t) + c(t) \frac{d}{dt}p(t)$.
3. $\frac{d}{dt}(c_{1}(t)\cdot c_{2}(t))=c_{1}(t)\cdot \frac{d}{dt}c_{2}(t) + c_{2}(t)\cdot \frac{d}{dt}c_{1}(t).$
4. Si $n=3$, entonces podemos definir de forma análoga que para al producto punto, con el producto cruz: 
   $$
   	\frac{d}{dt}(c_{1}(t)\times c_{2}(t))=c_{1}(t)\times \frac{d}{dt}c_{2}(t)+\frac{d}{dt}c_{1}(t)\times c_{2}(t).
   $$

###### Ejercicio:
Si $c:\mathbb{R}\to\mathbb{R}^{n}$ es diferenciable. Si $\lvert \lvert c(t) \rvert \rvert$ es constante, demuestra que $c'(t)$ y $c(t)$ son perpendiculares.
**Sol:**
Por demostrar que $c'(t)\cdot c(t)=0$.
Sea $r=\lvert \lvert c(t) \rvert \rvert= \sqrt{ c(t)\cdot c(t) }$ para $r\in\mathbb{R}$. Si elevamos al cuadrado ambos lados, nos queda que: 
$$
	r^{2}=c(t)\cdot c(t),
$$
entonces podemos tomar la derivada de ambos lados, de modo que tenemos que 
$$
	0=\frac{d}{dt}r^{2}=\frac{d}{dt}c(t)\cdot c(t)=2c(t)\cdot c'(t),
$$
es decir que $c(t)\cdot c'(t)=0$, por lo tanto son perpendiculares. $\quad\square$

