##### Definición:
Sea $f:R^{n}\to R$ con dominio $D$ [[ConjuntosAbiertos|abierto]]. Decimos que $f$ es continua en $x_{0}\in D$ si se cumple el siguiente [[Limite|limite]] que 
$$
	\lim_{ x \to x_{0} }f(x)=f(x_{0}). 
$$
Esto es equivalente a decir que $f$ es continua en $x_{0}$ si para todo abierto $V$ que contenga a $f(x_{0})$, existe un abierto $U$ que contiene a $x_{0}$ tal que $f(U)\subset V$.

Al igual quela mayoria de definiciones y teoremas, esto se puede extender de forma análoga a funciones de $R^{n}$ en $R^{m}$.

#### Teorema
Sea $f:R^{n}\to R$ con dominio $D$ abierto. La función $f$ es continua en todo punto de $D$ si y solo si para todo conjunto abierto $V\subset R$ su preimagen 
$$
	f^{-1}(V)=\{ x\in D:f(x)\in V \}
$$
es un conjunto abierto en $D$.

#### Ejemplos
1.- $f(x,y)=\begin{cases} \frac{x^{3}-y^{3}}{x^{2}+y^{2}},\quad(x,y)\neq(0,0) \\  0,\quad (x,y)=(0,0)\end{cases}$. ¿Es continua en $(0,0)$?
**Sol:** 
No sabemos en sí como resolver el límite de forma directa, pero podemos usar un cambio a coordenadas polares de la forma 
$$
	x=r\cos \theta,\quad y=r\sin \theta
$$
para simplificar la función como 
$$
	\frac{x^{3}-y^{3}}{x^{2}+y^{2}}=\frac{r^{3}\cos ^{3} \theta-r^{3}\sin ^{3}\theta}{r^{2}\cos ^{2}\theta+r^{2}\sin ^{2}\theta}=r(\cos ^{3}\theta-\sin^{3}\theta).
$$
Además, para cualquier $\theta$, podemos acotar esto de la forma 
$$
	-2r\leq r(\cos ^{3}\theta-\sin ^{3}\theta)\leq 2r,
$$
por lo tanto tenemos que 
$$
	0=\lim_{ (r,\theta) \to (0,\theta) } -2r\leq\lim_{ (r,\theta) \to (0,\theta) }r(\cos ^{3}\theta-\sin ^{3}\theta) \leq \lim_{ (r,\theta) \to (0,\theta) }2r=0,
$$
por lo tanto tenemos que 
$$
	\lim_{ (x,y) \to (0,0) } \frac{x^{3}-y^{3}}{x^{2}+y^{2}}=\lim_{ (r,\theta) \to (0,\theta) }r(\cos ^{3}\theta-\sin ^{3}\theta)=0.
$$

2.- Usar un cambio a [[SistemasCoordenadas|coordenadas polares]] para encontrar $\lim_{ (x,y) \to (0,0) } \frac{x^{2}y}{x^{2}+y^{2}}$.

#Calculo