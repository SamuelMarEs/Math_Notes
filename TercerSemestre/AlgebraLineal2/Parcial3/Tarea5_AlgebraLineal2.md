Samuel Márquez Estrada
#### Sección 6.2 Friedberg
2.- En cada parte, aplicar el proceso Gram-Schmidt a los subconjuntos $S$ del espacio de producto interno $V$ para obtener una base ortogonal para $\mathrm{span}(S)$. Después, normaliza los vectores de la base para obtener una base ortonormal $\beta$ para $\mathrm{span}(S)$. Calcula los coheficientes de Fourier para cualquier vector relativo a $\beta$. Usa el Teorema 6.5 para verificar tu resultado.
a) $V=R^{3}$, $S=\{ (1,0,1),(0,1,1),(1,3,3) \}$, y $x=(1,1,2)$.
b) $V=R^{3}$, $S=\{ (1,1,1),(0,1,1),(0,0,1) \}$, y $x=(1,0,1)$.
c) $V=P_{2}(R)$ con producto interno $\langle f(x),g(x)\rangle=\int_{0}^{1}f(t)g(t)dt$, $S=\{ 1,x,x^{2} \}$, y $h(x)=1+x$.
d) $V=\mathrm{span}(S)$, $S=\{ (1,i,0),(1-i,2,4i) \}$, y $x=(3+i,4i,-4)$.
e) $V=R^{4}$, $S=\{ (2,-1,-2,4),(-2,1,-5,5),(-1,3,7,11) \}$, y $x=(-11,8,-4,18)$.
f) $V=R^{4}$, $S=\{ (1,-2,-1,3),(3,6,3,-1),(1,4,2,8) \}$, y $x=(-1,2,1,1)$.
g) $V=M_{2 \times 2}(R)$, $S=\left\{ \begin{pmatrix}3 & 5 \\  -1 & 1\end{pmatrix} , \begin{pmatrix}-1 & 9 \\  5 & -1\end{pmatrix}, \begin{pmatrix}7 & -17 \\  2 & -6\end{pmatrix}\right\}$, y $A=\begin{pmatrix}-1 & 2 \\  -4 & 8\end{pmatrix}$.
h) $V=M_{2\times 2}(R)$, $S=\left\{ \begin{pmatrix}2 & 2 \\  2 & 1\end{pmatrix} , \begin{pmatrix}11 & 4 \\  2 & 5\end{pmatrix}, \begin{pmatrix}4 & -12 \\  3 & -16\end{pmatrix}\right\}$, y $A=\begin{pmatrix}8 & 6 \\  25 & -13\end{pmatrix}$.
i) $V=\mathrm{span}(S)$ con producto interno $\langle f,g\rangle=\int_{0}^{\pi}f(t)g(t)dt$, $S=\{ \sin t, \cos t, 1, t \}$, $h(t)=2t+1$.
j) $V=C^{4}$, $S=\{ (1, i, 2-i, -1),(2+3i, 3i, 1-i, 2i),(-1+7i,6+10i,11-4i,3+4i) \}$, y $x=(-2+7i,6+9i,9-3i,4+4i)$.
k) $V=C^{4}$, $S=\{ (-4,3-2i,i,1-4i),(-1-5i,5-4i,-3+5i,7-2i),(-27-i,-7-6i,-15+25i,-7-6i) \}$, y $x=(-13-7i, -12+3i, -39-11i,-26+5i)$.
l) $V=M_{2 \times 2}(C), S=\left\{ \begin{pmatrix}1-i & -2-3i \\  2+2i & 4+i\end{pmatrix}, \begin{pmatrix}8i & 4 \\  -3-3i & -4+4i\end{pmatrix}, \begin{pmatrix}-25-38i & -2-13i \\  12-78i & -7+24i\end{pmatrix} \right\}$, y $A=\begin{pmatrix}-2+8i & -13+i \\  10-10i & 9-9i\end{pmatrix}.$
m) $V=M_{2 \times 2}(C), S=\left\{ \begin{pmatrix}-1+i & -i \\  2-i & 1+3i\end{pmatrix}, \begin{pmatrix}-1-7i & -9-8i \\  1+10i & -6-2i\end{pmatrix}, \begin{pmatrix}-11-132i & -34-31i \\  7-126i & -71-5i\end{pmatrix} \right\}$ y $A=\begin{pmatrix}-7+5i & 3+18i \\  9-6i & -3+7i\end{pmatrix}$.
**Sol:**
a) El primer vector de nuestra base es $v_{1}=(1,0,1)$. El segundo vector va a ser 
$$
	v_{2}=(0,1,1)-\frac{\langle(0,1,1),(1,0,1)\rangle}{\lvert \lvert (1,0,1) \rvert  \rvert ^{2}}(1,0,1)=(0,1,1)-\frac{1}{2}(1,0,1)=\left( -\frac{1}{2}, 1, \frac{1}{2} \right).
$$
Entonces de momento nuestra base es $\{ (1,0,1),(-1 / 2, 1, 1 / 2) \}$. Nuestro último vector es 
$$
	\begin{align}
	v_{3}&=(1,3,3)- \frac{\langle (1,3,3),(1,0,1)\rangle}{\lvert \lvert (1,0,1) \rvert  \rvert^{2} }(1,0,1)- \frac{\langle (1,3,3),(-1 /2,1,1 / 2)\rangle}{\lvert \lvert (-1 / 2,1,1 / 2) \rvert  \rvert^{2} }(-1 / 2,1,1 / 2) \\
	&= (1,3,3)-\frac{4}{2}(1,0,1)- \frac{4}{3 / 2}(-1 / 2, 1, 1/2) \\
	&=\left( 1-2+\frac{4}{3}, 3-\frac{8}{3}, 3-2-\frac{4}{3} \right)=\left( \frac{1}{3}, \frac{1}{3}, - \frac{1}{3} \right).
	\end{align}
$$
Entonces nuestra base es $S'=\left\{  (1,0,1),\left( -\frac{1}{2}, 1, \frac{1}{2} \right), \left( \frac{1}{3}, \frac{1}{3}, -\frac{1}{3} \right)  \right\}$, que normalizada es 
$$
	\left\{  \left( \frac{1}{\sqrt{ 2 }}, 0, \frac{1}{\sqrt{ 2 }} \right), \left( -\frac{\sqrt{ 6 }}{6}, \frac{\sqrt{ 6 }}{3} , \frac{\sqrt{ 6 }}{6}  \right), \left( \frac{\sqrt{ 3 }}{3}, \frac{\sqrt{ 3 }}{3}, -\frac{\sqrt{ 3 }}{3} \right) \right\}.
$$


4.- Sea $S=\{ (1,0,i),(1,2,1) \}$ en $C^{3}$. Calcula $S^{\perp}$.
**Sol:**
Para encontrar el complemento ortogonal tenemos que resolver el sistema 
$$
	\langle (1,0,i),(a,b,c)\rangle=0,\qquad\text{y}\qquad \langle(1,2,1),(a,b,c)\rangle=0.
$$
Es decir, tenemos el sistema $a-ic=0$ y $a+2b+c=0$, que podemos expresar de la forma 
$$
	a=ic,\quad b=-\frac{c}{2}(1+i), 
$$
entonces tenemos que $S^{\perp}=\left\{  c\left( i, -\frac{1}{2}-\frac{i}{2}, 1 \right):c\in C  \right\}$.


5.- Sea $S_{0}=\{ x_{0} \}$, donde $x_{0}$ es un vector no cero en $R^{3}$. Describe $S_{0}^{\perp}$ geométricamente. Ahora supón que $S=\{ x_{1},x_{2} \}$ es un subconjunto linealmente independiente de $R^{3}$. Describe $S^{\perp}$ geométricamente.
**Sol:**
Para $S_{0}=\{ x_{0} \}$, su complemento ortogonal es el conjunto de vectores $v$ tales que $\langle x_{0}, v\rangle=0$, y al estar en $R^{3}$, el producto interno es el producto punto, por lo tanto $S_{0}^{\perp}$ es el plano normal al vector $x_{0}$.
Para $S=\{ x_{1},x_{2} \}$ linealmente independientes, cualquier vector ortogonal a ambos es ortogonal a cualquier combinación lineal de ellos, por lo tanto, sea $u=ax_{1}+bx_{2}$, el complemento ortogonal son los vectores tales que $v\cdot u=0$, es decir el conjunto generado por el vector normal al plano generado por $\{ x_{1},x_{2} \}$.


7.- Sea $\beta$ una base del subespacio $W$ de un espacio de producto interno $V$, y sea $z\in V$. Demuestra que $z\in W^{\perp}$ si y sólo si $\langle z,v\rangle=0$ para todo $v\in \beta$.
**Sol:**
$\implies$ Sea $z\in W^{\perp}$, por demostrar que $\langle z,v\rangle=0$ para todo $v\in \beta$. Dado que $\beta$ es una base de $W$, tenemos que $\beta \subset W$, entonces por definición tenemos que $\langle z,v\rangle=0\quad\forall v\in \beta \subset W$.

$\Longleftarrow$ Sea $z\in V$ tal que $\langle z,v\rangle=0$ para todo $v\in \beta$ una base de $W$. Queremos demostrar que $z\in W^{\perp}$, es decir que $\langle z,w\rangle=0$ para todo $w\in W$. Sea $\beta=\{ v_{1},\dots, v_{n} \}$ tenemos que
$$
	\begin{align}
	\langle z,w\rangle&=\left\langle  z,\sum_{i=1}^{n}a_{i}v_{i} \right\rangle \\
	&=\sum_{i=1}^{n}\bar{a_{i}}\langle z,v_{i}\rangle=\sum_{i=1}^{n}\bar{a_{i}}0=0.\quad\square
	\end{align}
$$


19.- En cada una de las siguientes partes, encuentra la proyección ortogonal del vector dado sobre el subespacio $W$ del espacio de producto interno $V$.
a) $V=R^{2}$, $u=(2,6)$, y $W=\{ (x,y):y=4x \}$.
b) $V=R^{3}$, $u=(2,1,3)$, y $W=\{ (x,y,z):x+3y-2z=0 \}$.
c) $V=P(R)$ con producto interno $\langle f(x),g(x)\rangle=\int_{0}^{1}f(t)g(t)dt$, $h(x)=4+3x-2x^{2}$ y $W=P_{1}(R)$.
**Sol:**
a) Podemos ver que una base de $W$ es $\{ (1,4) \}$, por lo tanto la proyección de $u=(2,6)$ sobre $W$ es 
$$
	v=\frac{\langle (2,6),(1,4)\rangle}{\lvert \lvert (1,4) \rvert  \rvert ^{2}}(1,4)=\frac{26}{17}(1,4).
$$
b) El subespacio $W$ es un plano que se puede parametrizar como $P=(2z-3y, y, z)$, por lo que una base es $\{ (-3,1,0),(2,0,1) \}$. Para encontrar la proyección ortogonal, necesitamos transformar nuestra base en una base ortogonal, usando el proceso Gram-Schmidt, de modo que nuestro primer vector sigue siendo $(-3,1,0)$, y nuestro segundo vector será 
$$
	(2,0,1)-\frac{\langle (2,0,1),(-3,1,0)\rangle}{\lvert \lvert (-3,1,0) \rvert  \rvert ^{2}}(-3,1,0)=(2,0,1)-\frac{-6}{10}(-3,1,0)=\left( \frac{1}{5}, \frac{3}{5},1 \right).
$$
Entonces la proyección ortogonal de $u=(2,1,3)$ sobre $W$ es 
$$
	\begin{align}
	v&= \frac{\langle (2,1,3),(-3,1,0)\rangle}{\lvert \lvert (-3,1,0) \rvert  \rvert ^{2}}(-3,1,0)+ \frac{\langle(2,1,3),(1 / 5,3 / 5,1)\rangle}{\lvert \lvert (1 / 5,3 / 5,1) \rvert  \rvert ^{2}}\left( \frac{1}{5}, \frac{3}{5}, 1 \right) \\
	&=\frac{-1}{2}(-3,1,0)+\frac{20}{7}\left( \frac{1}{5}, \frac{3}{5}, 1 \right) \\
	&=\left( \frac{3}{2}+\frac{4}{7}, -\frac{1}{2}+\frac{12}{7}, \frac{20}{7} \right)=\left( \frac{29}{14}, \frac{17}{14}, \frac{20}{7} \right).
	\end{align}
$$
c) Sea $W=P_{1}(R)$, si queremos llevar la base $\{ 1,x \}$ a una base ortogonal, tomamos 
$$
	x-\frac{\langle x,1\rangle}{\lvert \lvert 1 \rvert  \rvert ^{2}}1=x-\frac{1}{2},
$$
entonces nuestra base ortogonal es $\left\{  1,x-\frac{1}{2}  \right\}$. Entonces la proyección de $h(x)=4+3x-2x^{2}$ es 
$$
	v=\frac{\langle h(x),1\rangle}{\lvert \lvert 1 \rvert  \rvert^{2} }1+ \frac{\langle h(x),x-1 /2\rangle}{\lvert \lvert x-1 / 2 \rvert  \rvert ^{2}}(x-1 / 2).
$$
Para calcular cada uno de los productos internos, veamos que las integrales son: 
$$
	\int_{0}^{1}4+3x-2x^{2}dx=4x+\frac{3}{2}x^{2}-\frac{2}{3}x^{3}|_{0}^{1}=4+\frac{3}{2}-\frac{2}{3}=\frac{24+9-4}{6}=\frac{29}{6}.
$$
La segunda integral que tenemos que calcular es la de $h(x)\left( x-\frac{1}{2} \right)$, que es 
$$
	\int_{0}^{1}-2+\frac{5}{2}x+4x^{2}-2x^{3}dx=-2x+\frac{5}{4}x^{2}+\frac{4}{3}x^{3}-\frac{1}{2}x^{3}|_{0}^{1}=\frac{-24+15+16-6}{12}=\frac{1}{12}.
$$
Por último, para calcular la norma de nuestro segundo vector de la base, tenemos 
$$
	\int_{0}^{1}\left( x-\frac{1}{2} \right)^{2}dx=\frac{1}{12}.
$$
Entonces tenemos que 
$$
	v=\frac{29}{6}+x-\frac{1}{2}=x+\frac{26}{6}.
$$


21.- Sea $V=C([-1,1])$ con producto interno $\langle f,g\rangle=\int_{-1}^{1}f(t)g(t)dt$ y sea $W$ el subespacio $P_{2}(R)$, visto como un espacio de funciones. Use la base ortonormal obtenida en el ejemplo 5 para calcular la "mejor" (más cercana) aproximación polinomial de segundo grado de la función $h(t)=e^{t}$ en el intervalo $[-1,1]$.
**Sol:**
La “mejor” aproximación polinomial de grado 2 de $h(t)=e^t$ en $[-1,1]$ es la proyección ortogonal de $h$ sobre $W=P_2(\mathbb R)$. Si en el ejemplo 5 se obtuvo la base ortonormal de Legendre
$$
q_0(t)=\frac1{\sqrt2},\qquad
q_1(t)=\sqrt{\frac32}\,t,\qquad
q_2(t)=\sqrt{\frac58}(3t^2-1),
$$
entonces la proyección es
$$
p(t)=\langle h,q_0\rangle q_0+\langle h,q_1\rangle q_1+\langle h,q_2\rangle q_2.
$$
Calculamos los coeficientes:$$
\langle h,q_0\rangle
=\frac1{\sqrt2}\int_{-1}^1 e^t\,dt
=\frac{e-e^{-1}}{\sqrt2},
$$

$$
\langle h,q_1\rangle
=\sqrt{\frac32}\int_{-1}^1 t e^t\,dt
=\sqrt{\frac32}\cdot \frac{2}{e},
$$

$$
\langle h,q_2\rangle
=\sqrt{\frac58}\int_{-1}^1 (3t^2-1)e^t\,dt
=\sqrt{\frac58}\left(2e-\frac{14}{e}\right).
$$
Por tanto,
$$
\begin{aligned}
p(t)
&=\frac{e-e^{-1}}{2}
+\frac{3}{e}t
+\frac54\left(e-\frac7e\right)(3t^2-1).
\end{aligned}
$$
Equivalentemente, desarrollando:
$$
\boxed{
p(t)=\frac{15}{4}\left(e-\frac7e\right)t^2
+\frac{3}{e}t
+\frac{33/e-3e}{4}
}
$$

o también
$$
\boxed{
p(t)=\frac{15}{4}\left(e-\frac7e\right)t^2
+\frac{3}{e}t
+\frac34\left(\frac{11}{e}-e\right).
}
$$
Numéricamente,
$$
p(t)\approx 0.5367\,t^2+1.1036\,t+0.9963.
$$
Ese polinomio es la proyección ortogonal de \(e^t\) sobre \(P_2(\mathbb R)\) y, por el teorema de la mejor aproximación, es el polinomio de grado \(\le 2\) que minimiza
$$
\|e^t-p(t)\|^2=\int_{-1}^1\left(e^t-p(t)\right)^2dt.
$$


22.- Sea $V=C([0,1])$ con producto interno $\langle f,g\rangle=\int_{0}^{1}f(t)g(t)dt$. Sea $W$ es subespacio generado por el conjunto linealmente independiente $\{ t, \sqrt{ t } \}$.
a) Encuentra una base ortonormal de $W$.
b) Sea $h(t)=t^{2}$. Usa la base ortonormal para encontrar la "mejor" (más cercana) aproximación de $h$ en $W$.
**Sol:**
Sea $V=C([0,1])$ con el producto interno
$$
\langle f,g\rangle=\int_{0}^{1}f(t)g(t)\,dt,
$$
y sea $W=\operatorname{span}\{t,\sqrt t\}$.

a) Base ortonormal de \(W\)
Aplicamos Gram-Schmidt a
$$
u_1(t)=t,\qquad u_2(t)=\sqrt t.
$$
Primero,
$$
\|u_1\|^2=\int_0^1 t^2\,dt=\frac13,
$$
por lo que
$$
e_1(t)=\frac{u_1}{\|u_1\|}=\sqrt3\,t.
$$
Ahora calculamos
$$
\langle u_2,u_1\rangle
=\int_0^1 \sqrt t\,t\,dt
=\int_0^1 t^{3/2}\,dt
=\frac25.
$$
Entonces
$$
v_2=u_2-\frac{\langle u_2,u_1\rangle}{\|u_1\|^2}u_1
=\sqrt t-\frac{2/5}{1/3}t
=\sqrt t-\frac65t.
$$
Su norma es
$$
\|v_2\|^2
=\left\|\sqrt t-\frac65t\right\|^2
=\frac1{50},
$$
así que
$$
\|v_2\|=\frac1{\sqrt{50}}=\frac1{5\sqrt2}.
$$
Por tanto,
$$
e_2(t)=\frac{v_2}{\|v_2\|}
=\sqrt{50}\left(\sqrt t-\frac65t\right)
=\sqrt2\left(5\sqrt t-6t\right).
$$

Así, una base ortonormal de \(W\) es
$$
\boxed{
\left\{
e_1(t)=\sqrt3\,t,\qquad
e_2(t)=\sqrt2\left(5\sqrt t-6t\right)
\right\}.
}
$$

b) Mejor aproximación de $h(t)=t^2$ en $W$.
La mejor aproximación de $h$ en $W$ es su proyección ortogonal sobre $W$:
$$
p(t)=\langle h,e_1\rangle e_1+\langle h,e_2\rangle e_2.
$$
Calculamos los coeficientes:
$$
\langle h,e_1\rangle
=\int_0^1 t^2(\sqrt3\,t)\,dt
=\sqrt3\int_0^1 t^3\,dt
=\frac{\sqrt3}{4}.
$$
Por otro lado,
$$
\begin{aligned}
\langle h,e_2\rangle
&=\int_0^1 t^2\sqrt2\left(5\sqrt t-6t\right)dt \\
&=\sqrt2\left(5\int_0^1 t^{5/2}\,dt-6\int_0^1 t^3\,dt\right) \\
&=\sqrt2\left(5\cdot\frac27-6\cdot\frac14\right) \\
&=\sqrt2\left(\frac{10}{7}-\frac32\right)
=\sqrt2\left(-\frac1{14}\right)
=-\frac{\sqrt2}{14}.
\end{aligned}
$$
Entonces
$$
\begin{aligned}
p(t)
&=\frac{\sqrt3}{4}\left(\sqrt3\,t\right)
-\frac{\sqrt2}{14}\left[\sqrt2\left(5\sqrt t-6t\right)\right] \\
&=\frac34t-\frac17\left(5\sqrt t-6t\right) \\
&=\frac34t-\frac57\sqrt t+\frac67t \\
&=\frac{45}{28}t-\frac57\sqrt t.
\end{aligned}
$$

Por tanto, la mejor aproximación de $h(t)=t^2$ en $W$ es
$$
\boxed{
p(t)=\frac{45}{28}t-\frac57\sqrt t.
}
$$
