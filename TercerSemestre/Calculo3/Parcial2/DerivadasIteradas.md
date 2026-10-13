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

###### Ejercicio 19
La fuerza gravitacional sobre una masa $m$ en $(x,y,z)$ inducida por una masa $M$ en el origen está dada por la ley de gravitación de Newton: 
$$
	F= -\frac{GmM}{r^{2}}\vec{u},
$$
dónde $G$ es constante, $r$ la distancia entre las masas, y $\vec{u}$ un vector unitario en la dirección de $m.$
Notese que podemos escribir a $\vec{u}=\frac{1}{r} (x i+y j+z k)$.
El potencial gravitacional $V$ de la masa $m$ en $(x,y,z)$ provocado por una masa $M$ en el origen se define como 
$$
	V=- \frac{GmM}{r},
$$
y se tiene que $F=-\nabla V$.
Mostrar que el potencial $V$ de Newton satisface la ecuación de Laplace: 
$$
	\frac{\partial^{2}V}{\partial x^{2}}+ \frac{\partial^{2}V}{\partial y^{2}}+ \frac{\partial ^{2}V}{\partial z^{2}}=0\quad\text{para}\quad (x,y,z)\neq 0.
$$
**Sol:**
La expresión que más nos sirve del potencial en este caso sería 
$$
	V(r)=-\frac{GMm}{r},\quad r=\sqrt{ x^{2}+y^{2}+z^{2} }.
$$
Entonces tenemos que 
$$
	\frac{\partial V}{\partial x}=\frac{dV}{dr} \frac{\partial r}{\partial x}=\frac{GMm}{r^{2}} \frac{1}{2}(x^{2}+y^{2}+z^{2})^{-1 / 2}2x=\frac{GmM}{(x^{2}+y^{2}+z^{2})^{3 / 2}}x.
$$
Si volvemos a derivar obtenemos que 
$$
	\frac{\partial^{2}V}{\partial x^{2}}=GmM\left( \frac{(x^{2}+y^{2}+z^{2})^{3 / 2} - x (3 / 2)(x^{2}+y^{2}+z^{2})^{1 / 2}2x}{(x^{2}+y^{2}+z^{2})^{3}} \right)=GmM \left( \frac{-2x^{2}+y^{2}+z^{2}}{(x^{2}+y^{2}+z^{2})^{ 5 / 2}} \right).
$$
De forma análoga se llega a que 
$$
	\frac{\partial^{2}V}{\partial y^{2}}=GmM \left( \frac{x^{2}-2y^{2}+z^{2}}{(x^{2}+y^{2}+z^{2})^{5/ 2}} \right),
$$
y 
$$
	\frac{\partial^{2}V}{\partial z^{2}}=GmM \left( \frac{x^{2}+y^{2}-2z^{2}}{(x^{2}+y^{2}+z^{2})^{5/ 2}} \right).
$$
Simplemente queda hacer la suma, y obtener que 
$$
		\frac{\partial^{2}V}{\partial x^{2}}+ \frac{\partial^{2}V}{\partial y^{2}}+ \frac{\partial ^{2}V}{\partial z^{2}}=GmM\left( \frac{-2x^{2}+y^{2}+z^{2}+x^{2}-2y^{2}+z^{2}+x^{2}+y^{2}-2z^{2}}{(x^{2}+y^{2}+z^{2})^{5/ 2}} \right)=0.
$$

###### Ejemplo 6
La ecuación diferencial parcial $u_{t}+u_{x x x}+uu_{x}=0$ llamada ecuación de Korteweg-de Vries describe el movimiento de ondas de agua en un canal poco profundo.
Mostrar que para cualquier constante positiva $c$, la función 
$$
	u(x,t)=3c\text{sech}^{2}\left( \frac{1}{2} (x-ct)\sqrt{ c }\right)
$$
es solución de la ecuación diferencial.
**Sol:**
El problema consiste simplemente en calcular las derivadas implicadas en la ecuación diferencial, y ver que en efecto su suma es cero.
