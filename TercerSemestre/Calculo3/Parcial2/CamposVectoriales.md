#Calculo 
Un ***campo vectorial*** es una función $F:\mathbb{R}^{n}\to \mathbb{R}^{n}$ tal que a cada punto $x$ en el dominio de la función se le asigna un vector $F(x)$.
Se representan gráficamente como vectores $F(x)$ con base en $x$. ![[CampoVectorial1]]
##### Ejemplo:
1.- El campo vectorial $F(x,y)=(-y,x)$
![[EjemploCampoVectorial1.png|458]]

2.- $F(x,y)=\left( \frac{y}{x^{2}+y^{2}}, \frac{-x}{x^{2}+y^{2}} \right)$
![[EjemploCampoVectorial2.png|458]]

### Campo vectorial gradiente
¿Hay un campo vectorial que se pueda ver como el gradiente de una función? Es decir que $\nabla f$ le asigna el vector $\left( \frac{\partial f}{\partial x_{1}},\dots, \frac{\partial f}{\partial x_{n}} \right)$ para $f:\mathbb{R}^{n}\to\mathbb{R}$.
Por ejemplo si $f:\mathbb{R}^{2}\to\mathbb{R}$, entonces podemos tomar $\nabla f:\mathbb{R}^{2}\to\mathbb{R}^{2}$. 
Recordemos que el gradiente es perpendicular al plano tangente (o recta tangente) a la superficie de nivel (curva de nivel).

##### Ejemplo: Campo Gravitacional
La fuerza de atracción entre dos cuerpos está dada por 
$$
	F=\frac{mMG}{r^{3}}\bar{r},
$$
donde $m$ es la masad del objeto más chico, $M$ la masa del objeto más grande, $G$ es la constante gravitacional, y $\bar{r}=(x,y,z)$ es un vector, con $r=\lvert \lvert \bar{r} \rvert \rvert$ que es la distancia entre ambos cuerpos.
Entonces, el potencial gravitatorio está definido como 
$$
	F=-\nabla V,
$$
con $V=\frac{mMG}{r}$. (Es decir que $V:\mathbb{R}^{3}\to\mathbb{R}$).

#### Definición:
Si $F$ es un campo vectorial, una ***línea de flujo*** para $F$ es una curva $c(t)$ tal que la derivada en cada punto de la curva coincide con el elemento del campo vectorial correspondiente al punto. Es decir que 
$$
	c'(t)=F(c(t)).
$$
Podemos ver a $c(t)$ como la solución de un sistema de ecuaciones diferenciales. Por ejemplo si $c(t)=(x(t),y(t),z(t))$ y $F(c(t))=(P(c(t)),Q(c(t)),R(c(t)))$, entonces el sistema es
$$
	x'(t)=P(x(t),y(t),z(t)),\quad y'(t)=Q(x(t),y(t),z(t)),\quad z'(t)=R(x(t),y(t), z(t)).
$$

###### Ejemplo:
$c(t)=(\cos t,\sin t)$ es una línea de flujo de $F(x,y)=(-y,x)$. Esto pues 
$x(t)=\cos t\implies x'(t)=-\sin t=-y(t)$, y además $y(t)=\sin t\implies y'(t)=\cos t=x(t)$.


