#Calculo 
### Costo Marginal
Si $x$ es el número de unidades de algún producto, y $C(x)$ el costo de producir $x$ unidades.
Llamamos *costo marginal* al cambio que se produce en el costo por producir una unidad más. Es decir que el costo marginal sería $C'(x)$.
De igual forma, si definimos a $G(x)$ como la ganancia/utilidades/beneficio de producir y vender $x$ unidades, podemos también definir el *beneficio marginal*, que se puede interpretar como la "ganancia" que se produce de aumentar una unidad a las producidas.

##### Ejercicio:
Supongamos que una empresa produce $x,y$ cantidades de dos productos. El precio de venta del producto $x$ es $50$ y el del producto $y$ es 30.
Sea $C(x,y)=10x+10y+x^{2}+y^{2}$ la función de costo, y sea $V(x,y)=50x+30y$ la función de ingreso por cantidad vendida. 
Sea $G(x,y)=V(x,y)-C(x,y)=40x+20y-x^{2}-y^{2}$ la función de ganancia.
¿Cuál es el número óptimo de $x$ y $y$?
**Sol:**
Tenemos que $\nabla G(x,y)=(40-2x, 20-2y)$, y por lo tanto el punto crítico de nuestra gunción es $(20,10)$, por lo tanto este es el valor óptimo de ventas.

Y si nos restringimos a vender únicamente 20 unidades, es decir nos restringimos a la recta $x+y=20$. Esto nos da $y=20-y$, entonces podemos expresar nuestra función de ganancia en términos de una sola variable como $G(x)=400+60x-2x^{2}$, que nos lleva al resultado $x=15,y=5$.

### Modelo de producción Cobb-Douglas
Sea $Q(K,L)=AK^{\alpha}L^{\beta}$ donde $Q$ -> Producción, $K$ -> Capital (materia prima, maquinaria), $L$ -> Trabajo (fuerza laboral, empleados), y $A$ es una constante que describe la productividad total.
Por simplicidad, vamos a asumir $A=1$. Las constantes $\alpha,\beta$ miden la elasticidad para que no sea simplemente una relación lineal entre la producción y sus entradas.

Si tomamos el gradiente, lo podemos interpretar como la producción [[ProblemasOptimizacion2|marginal]] 
$$
	\nabla Q=\left( \frac{\partial Q}{\partial K}, \frac{\partial Q}{\partial L} \right).
$$
Por ahora vamos a suponer $\alpha=\beta=1 / 2$. Entonces tenemos $Q(K,L)=K^{1 / 2}L^{1 / 2}$,  y por lo tanto nuestra producción marginal será 
$$
	\nabla Q=\frac{1}{2}\begin{pmatrix}
	K^{-1 / 2}L^{1 / 2}, & K^{1 / 2}L^{- 1 / 2}
	\end{pmatrix}.
$$
En general, sin indagar de más en las especificaciones del modelo, se suele tener que $\alpha+\beta=1$->Rendimiento constante, $\alpha+\beta >1$->Rendimiento creciente, $\alpha+\beta<1$->Rendimiento decreciente.

##### Ejercicio:
Sea $Q(x,y)=\sqrt{ xy }$, encontrar los máximos de la función sujeto a $x+y=100$.
**Sol:**
Sea $g(x,y)=x+y$, nos estamos restringiendo a la curva de nivel $g(x,y)=100$. Primero, los gradientes son 
$$
	\nabla Q=\frac{1}{2}\left( \left( \frac{y}{x} \right)^{1 / 2}, \left( \frac{x}{y} \right)^{1 / 2} \right),\quad \nabla g=(1,1).
$$
La función $Q$ no tiene puntos críticos (ni $x$ ni $y$ pueden ser cero). Ahora procedemos a encontrar los [[MultiplicadoresDeLagrange|multiplicadores de Lagrange]] mediante el sistema 
$$
	x+y=100,\quad \frac{\sqrt{ y }}{\sqrt{ x }}=2\lambda,\quad \frac{\sqrt{ x }}{\sqrt{ y }}=2\lambda,
$$
lo que nos da que $\frac{\sqrt{ y }}{\sqrt{ x }}=\frac{\sqrt{ x }}{\sqrt{ y }}$, lo que nos da que $y^{2}=x^{2}$, y pensando en la interpretación del modelo, tendríamos que esto implica que $x=y$, y por la restricción, esto nos dice que $2x=2y=100$, es decir que $x=y=50$.
Para verificar que es un máximo, hace falta calcular la [[MaxMinAbsolutos|Hessiana de frontera]]. Definamos $h(x,y)=\sqrt{ xy }-\lambda(x+y)$, y de la igualdad $x=y$ obtenemos que $\lambda= 1 / 2$, por lo tanto las parciales de $h$ son 
$$
	h_{x}=\frac{1}{2} \frac{\sqrt{ y }}{\sqrt{ x }}-\frac{1}{2}, h_{y}=\frac{1}{2} \frac{\sqrt{ x }}{\sqrt{ y}}-\frac{1}{2}, h_{x x}=-\frac{\sqrt{ y }}{4} \frac{1}{x^{ 3 / 2}}, h_{yy}=-\frac{\sqrt{ x }}{4} \frac{1}{y^{ 3 / 2}} ,\quad h_{xy}=\frac{1}{4\sqrt{ xy }}.
$$
Si en base a esto se calcula el determinante de la Hessiana de frontera, se llega en efecto a un determinante positivo, por lo tanto en efecto el punto encontrado es un máximo.
Si se generaliza la restricción a $x+y=B$, entonces el punto óptimo es $\left( \frac{B}{2} , \frac{B}{2}\right)$.

¿Qué sucede si definimos $\alpha = 1 / 2,\beta = 1 / 3$, y sostenemos la restricción $x+y=B$? Notese que en este caso tenemos $\alpha+\beta=\frac{1}{2}+\frac{1}{3}=5 / 6<1$, por lo que estaríamos trabajando con un rendimiento decreciente.

### Condiciones KKT para problemas de min-max
Karush Kuhn Tucker.
Para un problema de optimización de encontrar un mínimo restringido a $g_{i}(x)\leq 0$ y $h_{j}(x)=0$, sea
$$
	\mathcal{L}= f(x)-\sum_{i=1}^{n}\lambda_{i}g_{i}(x)-\sum_{j=1}^{m}\mu_{j}h_{j}(x),
$$
dadas las restricciones, si $x_{0}$ es tal que $\nabla\mathcal{L}(x_{0})=0$, $g_{i}(x_{0})\leq 0$ y $h(x_{0})=0$, entonces $x_{0}$ es una solución del problema.
Notese que tenemos 
$$
	\nabla\mathcal{L}=\nabla f-\sum \lambda_{i}\nabla g_{i}-\sum \mu_{j}\nabla h_{j},
$$
con $\lambda_{i}\geq 0$. Si $g_{i}(x_{0})<0$ decimos que es una restricción inactiva, si $g_{i}(x_{0})=0$, decimos que es una restricción activa