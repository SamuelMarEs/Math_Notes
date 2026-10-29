#Calculo 
#### Costo Marginal
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
