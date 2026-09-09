Sea $f:R^{2}\to R$ tal que las [[Diferenciacion|derivadas parciales]] $\frac{\partial f}{\partial x}$ y $\frac{\partial f}{\partial y}$ existen. Tomemos $P=(x_{0},y_{0},z_{0})$ en la gráfica de $f$. (Es decir $z_{0}=f(x_{0},y_{0})$). 
Vamos a considerar las curvas sobre la [[Graficas|gráfica]] de $f$ determinadas por los planos $x=x_{0}$ y $y=y_{0}.$
Sea $L_{1}$ la línea que pasa por $P$ con pendiente $\frac{\partial f}{\partial x}(x_{0},y_{0})$ y $L_{2}$ la recta que pasa por $P$ con pendiendte $\frac{\partial f}{\partial y}(x_{0},y_{0})$.
![[PlanoTangente]]
Vamos a decir que el plano que contiene a $L_{1}$ y $L_{2}$ es el plano tangente a la gráfica de $f$ en $P$.

Por otro lado sabemos que la ecuación general de un plano en $R^{3}$ que pasa por $P$ es 
$$
	a(x-x_{0})+b(y-y_{0})+c(z-z_{0})=0,
$$
donde $z_{0}=f(x_{0},y_{0})$.
Si asumimos que $c\neq 0$, de la ecuación obtenemos 
$$
	z-z_{0}=-\frac{a}{c}(x-x_{0})-\frac{b}{c}(y-y_{0}).
$$
Vamos a tomar $x=x_{0}$ en la ecuación del plano para obtener 
$$
	z-z_{0}=-\frac{b}{c}(y-y_{0}),
$$
que es la ecuación de la recta contenida en el plano $x=x_{0}$ que pasa por $P$ y con pendiente $-\frac{b}{c}$.
Entonces si la recta es tangente a la gráfica de $f$, debe cumplir que $$-\frac{b}{c}=\frac{\partial f}{\partial y}(x_{0},y_{0}).$$
De manera análoga, si tomamos en su lugar $y=y_{0}$, llegamos a la ecuación de la recta contenida en el plano $y=y_{0}$ que pasa por $P$, y que para ser tangente a la gráfica de $f$ debe satisfacer que 
$$
	-\frac{a}{c}=\frac{\partial f}{\partial x}(x_{0},y_{0}).
$$
Entonces una ecuación para el plano tangente es 
$$
	z-z_{0}=\frac{\partial f}{\partial x}(x_{0},y_{0})(x-x_{0})+\frac{\partial f}{\partial y}(x_{0},y_{0})(y-y_{0}).
$$

### Aproximaciones lineales
Sea $f:R^{2}\to R$ tal que las derivadas parciales $\frac{\partial f}{\partial x}=f_{x}$ y $\frac{\partial f}{\partial y}=f_{y}$ existen.
Sabemos que la ecuación del plano tangente en $P=x_{0},y_{0},f(x_{0},y_{0})$ esta dado por 
$$
	L(x,y)=f(x_{0},y_{0})+f_{x}(x_{0},y_{0})(x-x_{0})+f_{y}(x_{0},y_{0})(y-y_{0}).
$$
A la función $L(x,y)$ le vamos a llamar la ***aproximación lineal*** de $f(x,y)$ alrededor de $(x_{0},y_{0})$.


#Calculo #Geometria