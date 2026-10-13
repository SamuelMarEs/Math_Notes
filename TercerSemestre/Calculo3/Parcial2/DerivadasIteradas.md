#Calculo
Lo que queremos hacer al iterar las derivadas, es generalizar el concepto de una derivada de orden superior para funciones de varias variables.

#### Definición:
Sea $f:\mathbb{R}^{3}\to\mathbb{R}$ tal que las parciales $\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z}$ existen y son continuas, es decir la función es diferenciable. Entonces decimos que $f\in C^{1}$.
Si parciales $g_{1}= \frac{\partial f}{\partial x},g_{2}=\frac{\partial f}{\partial y},g_{3}=\frac{\partial f}{\partial z}$ son diferenciables y sus parciales son continuas, entonces decimos que $f\in C^{2}$.
Si $f$ es diferenciable $n$ veces y con derivada (parciales) continuas, entonces $f\in C^{n}$.

Hay que tener en cuenta que $g_{i}:\mathbb{R}^{3}\to\mathbb{R}$. Como estamos trabajando nuevamente con parciales, la notación es de cierto modo intercalable, algo como 
$$
	\frac{\partial^{2}f}{\partial x\partial y}=\frac{\partial}{\partial x}\left( \frac{\partial f}{\partial y} \right),
$$
y de forma análoga para aplicar las demás derivadas parciales en cualquier orden. (El orden si importa).

##### Ejercicio
$f(x,y)$ una función $f:\mathbb{R}^{2}\to\mathbb{R}$. Sean $x=g(s,t)$, $y=h(s,t)$. Si $k(s,t)=f(g(s,t),h(s,t))$, calcule $D_{s}k$, $D_{t}(D_{s}k)$.
Primero, tenemos que 
$$
	D_{s}k=\frac{\partial f}{\partial g} \cdot\frac{\partial g}{\partial s}+\frac{\partial f}{\partial h} \cdot \frac{\partial h}{\partial s}.
$$
Ahora, si tomamos $D_{t}$, tenemos lo siguiente: 
$$
	\begin{align}
	D_{t}(D_{s}k)&=D_{t}\left(\frac{\partial f}{\partial g} \cdot\frac{\partial g}{\partial s}+\frac{\partial f}{\partial h} \cdot\frac{\partial h}{\partial s}\right) \\ 
	
	&=D_{t}\left(\frac{\partial f}{\partial g} \cdot\frac{\partial g}{\partial s}\right)+D_{t}\left(\frac{\partial f}{\partial g} \cdot\frac{\partial g}{\partial s}\right) \\
	
	&=\left[ \frac{\partial}{\partial t} \frac{\partial f}{\partial g} \right] \cdot\frac{\partial g}{\partial s}+ 
	\left[ \frac{\partial}{\partial t} \frac{\partial g}{\partial s} \right] \cdot\frac{\partial f}{\partial g}+
	\left[ \frac{\partial}{\partial t} \frac{\partial f}{\partial h} \right] \cdot\frac{\partial h}{\partial s}+
	\left[ \frac{\partial}{\partial t} \frac{\partial h}{\partial s} \right] \cdot\frac{\partial f}{\partial h}  \\ 
	
	&=\left[ \frac{\partial}{\partial t} \frac{\partial f}{\partial g} \right] \cdot\frac{\partial g}{\partial s}+ 
	\left[ \frac{\partial^{2}g}{\partial t\partial s} \right] \cdot\frac{\partial f}{\partial g}+
	\left[ \frac{\partial}{\partial t} \frac{\partial f}{\partial h} \right] \cdot\frac{\partial h}{\partial s}+
	\left[ \frac{\partial^{2}h}{\partial t\partial s} \right] \cdot\frac{\partial f}{\partial h}
	\end{align}
$$
Por simplicidad, cambiemos la notación, de modo que $\frac{\partial f}{\partial g}=D_{g}$ y $D_{h}$ definido de forma análoga. Entonces tenemos que $D_{g}(g(s,t),h(s,t))$, y por lo tanto tenemos que 
$$
	\begin{align}
	\frac{\partial}{\partial t}D_{g}&=\frac{\partial D_{g}}{\partial g} \cdot\frac{\partial g}{\partial t}+ \frac{\partial D_{g}}{\partial h}\cdot \frac{\partial h}{\partial t} \\ 
	
	&= \frac{\partial^{2}f}{\partial g^{2}}\cdot \frac{\partial g}{\partial t}+ \frac{\partial^{2}f}{\partial h\partial g}\cdot \frac{\partial h}{\partial t}.
	\end{align}
$$
De forma análoga se puede llegar a que 
$$
	\frac{\partial}{\partial t}D_{h}= \frac{\partial^{2}f}{\partial g \partial h}\cdot \frac{\partial g}{\partial t}+ \frac{\partial^{2}f}{\partial h^{2}}\cdot \frac{\partial h}{\partial t}.
$$
 

#### Teorema 
Sea $f$ una función de dos variables definida en $U$ un abierto. Si existe $D_{1}f,D_{2}f,D_{1}D_{2}f,D_{2}D_{1}f$ y son continuas (es decir $f\in C^{2}(\mathbb{R}^{2})$), entonces 
$$
	D_{1}D_{2}f=D_{2}D_{1}f.
$$
O lo que es lo mismo 
$$
	\frac{\partial^{2}f}{\partial x\partial y}=\frac{\partial^{2}f}{\partial y\partial x}.
$$
Esto se extiende, de cierto modo, a que la composición de derivadas parciales es conmutativa.
Es decir, podemos caracterizar cualquier derivada como 
$$
	D^{m_{1}}_{x}D_{y}^{m_{2}}D_{z}^{m_{3}}f,
$$
que sería una derivada de orden $m_{1}+m_{2}+m_{3}$.
