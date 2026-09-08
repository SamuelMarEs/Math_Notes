##### Vecindad
Una vecindad en $R$ de $a$ es un conjunto definido como 
$$
	\{ x\in R:x\in(a-\delta,a+\delta) \}
$$
para algún $\delta>0$.
##### Bola en $R^{n}$ (Disco $R^{n}$):
Sea $x_{0}\in R^{n}$ y $r$ un número real positivo. La ***Bola*** (disco abierto) de radio $r$ y centro en $x_{0}$ se define como el conjunto de todos los puntos $x\in R^{n}$ cuya distancia a $x_{0}$ es menor que $r$.
$$
	D_{r}=\{ x\in R^{n}:\text{d}(x,x_{0})<r \}.
$$
La bola es un concepto necesario para introducir el concepto de un conjunto abierto.
Además, una bola en $R$ es equivalente a una vecindad.
##### Definición:
Sea $U\subset R^{n}$, $U$ es un ***conjunto abierto*** si *para todo* $x_{0}\in U$, $\exists r>0$ tal que $D_{r}(x_{0})$ esta contenida en $U$, es decir que 
$$
	D_{r}(x_{0})\subset U.
$$

Entonces, para poder definir el concepto de un límite en $R^{n}$, vamos a utilizar el concepto de un conjunto abierto para extender la noción de intervalo a otras dimensiones.

##### Teorema
La bola $B_{r}(a)$ es un conjunto abierto.
###### Demostración:
Queremos demostrar que $\forall x\in B_{r}(a),\exists \delta>0$ tal que $B_{\delta}(x)\subset B_{r}(a)$.
Sea $x\in B_{r}(a)$, definamos $\delta_{1}=\text{d}(x,a)$, y entonces podemos tomar $\delta=r-\delta_{1}>0$, tal que podemos demostrar que 
$$
	B_{\delta}(x)\subset B_{r}(a).
$$
Sea $x_{0}\in B_{\delta}(x)$, sabemos que $\text{d}(x_{0},x)<\delta$, por lo tanto 
$$
	\begin{align}
	\text{d}(x_{0},a)= \lvert x_{0}-a \rvert &=\lvert x_{0}-x+x-a \rvert \\
	&\leq \lvert x_{0}-x \rvert  +\lvert x-a \rvert  \\
	&< \delta+\lvert x-a \rvert \\
	&<r-\lvert x-a \rvert+\lvert x-a \rvert   \\
	&=r. 
	\end{align}
$$
Por lo tanto $x_{0}\in B_{r}(a).\quad\square$

##### Ejemplo
Probar que $A=\{ (x,y)\in R^{2}:x>0 \}$ es un conjunto abierto.
**Sol:**
Por Demostrar que $\forall x_{0}\in A,\exists r>0$ tal que $B_{r}(x_{0})\subset A$.
Sea $x_{0}=(x,y)\in A$, tenemos que $x>0$. Tomemos como radio $r=x>0$, de forma que tenemos la bola $B_{r}(x_{0})$. Entonces para todo $(x_{1},y_{1})=v\in B_{r}(x_{0})$, tenemos que $\lvert v-x_{0} \rvert<r$. Observemos que $$\lvert v-x_{0} \rvert=\sqrt{ (x_{1}-x)^{2}+(y_{1}-y)^{2} }<r=x.$$Además tenemos que $\lvert x_{1}-x \rvert=\sqrt{ (x_{1}-x)^{2} }\leq\sqrt{ (x_{1}-x)^{2}+(y_{1}-y)^{2} }$, es decir que 
$$
	\lvert x_{1}-x \rvert<x\Rightarrow-x<x_{1}-x<x\Rightarrow_{0}<x_{1}. \quad\square
$$

##### Definición
Sea $A\subset R^{n}$. Un punto $x\in R^{n}$ se llama ***punto frontera*** de $A$ si cada vecindad (o bola) de $x$ contiene al menos un punto en $A$ y al menos un punto que no este en $A$.
	***Nota:*** Si $A$ es un abierto entonces $x\notin A$. Para demostrar esto basta darse cuenta que si $x\in A$, entonces existira una vecindad que no contenga ningun punto fuera de $A$.