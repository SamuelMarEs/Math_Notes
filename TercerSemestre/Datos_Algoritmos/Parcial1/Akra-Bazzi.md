#Algoritmos #Teorema 
Un método para calcular la complejidad de [[Recursion|recursiones]] que es aún más general que el [[MetodoMaestro]].
Sean $n\geq 1,m\geq 1,a_{i}>0,b_{i}>0,d>0$: 
$$
	T(n)=\begin{cases}
	d, & 1\leq n\leq n_{0} \\
	\sum_{i=1}^{m}a_{i}T(n / b_{i})+f(n), & n>n_{0}.
	\end{cases}
$$
Condición de crecimiento: Existen constantes $C_{1},C_{2}>0$ tales que, para todo $i$ y $n>n_{0}$, 
$$
	C_{1}f(n)\leq f(u)\leq C_{2}f(n),\quad \frac{n}{b_{i}}\leq u\leq n.
$$

#### Teorema de Akra-Bazzi
Bajo las hipótesis anteriores, existe un único $p\in\mathbb{R}$ que satisface 
$$
	\sum_{i=1}^{m} \frac{a_{i}}{b_{i}^{p}}=1.
$$
Entonces 
$$
	T(n)\in \Theta\left( n^{p}\left( 1+\int_{1}^{n} \frac{f(u)}{u^{p+1}}du \right) \right).
$$

- $p$ es una constante determinada por los coeficientes y los factores de reducción, no depende de $n$.
- $u$ es la variable de integración. Usamos la misma función de costo no recursivo $g$.

###### Ejemplo: división desigual
Esta recurrencia no tiene la forma del [[MetodoMaestro|teorema maestro]]: 
$$
	T(n)=T(n / 3)+T(2n / 3)+cn,\quad n>3,c>0.
$$
Nuestro parámetros son $a_{1}=1,b_{1}= 3,a_{2}=1,b_{2}= 3 / 2,$ y $f(n)=cn$.
Tomamos $T(n)=d>0$ para $1\leq n\leq 3$. El costo $f(u)=cu$ satisface la condición de crecimiento.
1.- Encontrar $p$. Con $a_{1}=a_{2}=1,b_{1}=3$ y $b_{2}=3 / 2$: 
$$
	(1 / 3)^{p}+(2 / 3)^{p}=1\implies p=1.
$$
2.- Calcular la integral. 
$$
	\int_{1}^{n} \frac{cu}{u^{1+1}}du=c\int_{1}^{n} \frac{1}{u}du=c\ln n.
$$
3.- Sustituir. 
$$
	T(n)\in \Theta(n(1+c\ln n))=\Theta(n\log n).
$$
$\ln n$ y $\log n$, en cualquier base fija mayor que 1, difieren por un valor constante.