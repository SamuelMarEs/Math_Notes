#Calculo 
1.- Dado un cartón de $10\mathrm{m}^{2}$, construya la caja rectangular que maximice el volumen.
**Sol:**
Sean $x,y,z$ son la longitud de largo, ancho y alto, respectivamente. Entonces el volumen de la caja está dado por 
$$
	V(x,y,z)=xyz,
$$
restringido a que el área es menor o igual a $10\mathrm{m}^{2}$. El área de una caja está dada por 
$$
	A(x,y,z)=2xy+2xz+2yz,
$$
entonces nuestra restricción es el conjunto de nivel $A(x,y,z)\leq 10$. Vamos a seguir nuestro algoritmo para encontrar [[MaximosMinimos|máximos y mínimos absolutos]].
Nuestro gradiente es 
$$
	\nabla V(x,y,z)=(yz,xz,xy),
$$
que se anula en todos los puntos $(0,0,a),(0,a,0),(a,0,0)$ para $a\in\mathbb{R}$. Como no tiene sentido pensar en una caja con largo, ancho y alto zero, entonces estos puntos críticos no nos interesan.
El gradiente de la función del área es 
$$
	\nabla A(x,y,z)=(2y+2z, 2x+2z, 2x+2y)=2(y+z,x+z,x+y).
$$
Ahora vamos a encontrar los coeficientes de Lagrange mediante el sistema 
$$
	xy+xz+yz=5,\quad yz=\lambda(y+z),\quad xz=\lambda(x+z),\quad xy=\lambda(y+z)
$$


2.- Y si ahora la condición es que el largo más 2 veces el ancho más 2 veces la altura sea de un máximo de 108 pulgadas. ¿Cuál es el volumen máximo que puede tener la caja?
**Sol:**
Nuevamente $V(x,y,z)=xyz$, pero ahora tenemos que $108=y+2x+2z$, para $x$ el ancho, $y$ el largo y $z$ la altura.

3.- Diseñar una lata con tapa que contenga 1 litro de agua usando el mínimo metal.
**Sol:**
Sea $f(r,h)=2\pi r^{2}+2\pi rh$ el area de la lata, y $g(r,h)=\pi r^{2}h$ es volumen, entonces la restricción que tenemos es $g(r,h)=1\implies \pi r^{2}h=1$.
Nuestros gradientes son 
$$
	\nabla f(r,h)=(2\pi r+2\pi h, 2\pi r),\quad \nabla g(r,h)=(2\pi rh, \pi r^{2}),
$$
entonces, la función que queremos minimizar es 
$$
	\mathrm{min}\mathcal{L}=f(r,h)-\lambda(g(r,h)-1).
$$
