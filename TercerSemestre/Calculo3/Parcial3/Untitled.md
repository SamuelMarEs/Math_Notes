#Calculo 
¿Cómo podemos extender la noción de una integral a funciones de varias variables? Si para funciones de una variable la integral mide el área bajo la curva, es natural querer extender esta noción de modo que la integral de una función $f:\mathbb{R}^{2}\to \mathbb{R}$ mida el volumen bajo la superficie generada por la función.
Denotemos 
- $x$: la posición respecto al eje $x$ (a lo largo),
- $y$: la posición respecto al eje $y$ (a lo ancho),
- $z=f(x,y)$: la altura de cada punto.
Notemos que en cada punto $y_{0}$, (i.e. para $y$ constante), podemos definir una integral como 
$$
	A(y_{0})=\int_{a}^{b}f(x,y_{0})dx,
$$
de modo que tenemos que 
$$
A(y)\approx \sum_{i=1}^{n}f(c,y)\Delta x,\quad \text{para }c\in[x_{i+1},x_{i}].
$$
Como el área puede cambiar para cada una de las secciones transversales, se puede definir el volumen total como la suma (integral) de todas las áreas: 
$$
V=\int_{c}^{d}A(y)dy,
$$
lo cual sustituyendo nos da que 
$$
V=\int_{c}^{d}\left( \int_{a}^{b}f(x,y)dx \right)dy.
$$
Notemos que ${}V\approx \sum_{j=1}^{m}A(y^{*})\Delta y{}$, entonces, de cierta forma, tenemos que ${}\Delta V_{ij}\approx f(x_{i}^{*},y_{j}^{*})\Delta x\Delta y{}$ lo que nos lleva a 
$$
V=\lim_{ m \to \infty } \lim_{ n \to \infty } \sum_{j=1}^{m}\sum_{i=1}^{n}f(x_{i}^{*},y_{j}^{*})\Delta x\Delta y.
$$
***Nota:*** Es importante darnos cuenta que aquí solo estaríamos calculando el área de una forma similar a un prisma, pues estamos restringidos al rectángulo ${}[a,b]\times[c,d]{}$.