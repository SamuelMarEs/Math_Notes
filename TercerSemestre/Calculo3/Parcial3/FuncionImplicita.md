#Calculo 
#### Teorema de la función implícita
Sea ${}F:\mathbb{R}^{n+1}\to \mathbb{R}{}$ con derivadas parciales continuas y ${}(x_{0},z_{0})\in \mathbb{R}^{n+1}{}$ con ${}x_{0} \in \mathbb{R}^{n}{}$ y ${}z_{0}\in \mathbb{R}{}$ tal que 
$$
F(x_{0},z_{0})=0, \frac{\partial F}{\partial z}(x_{0},z_{0})\neq0.
$$
Entonces existe una bola ${}U\subset \mathbb{R}^{n}{}$ que contiene a ${}x_{0}{}$ y una vecindad ${}V{}$ de ${}z\in \mathbb{R}{}$ tal que existe ${}g(x)=z{}$ definida para ${}x \in U{}$ y ${}z\in V{}$ (i.e. ${}g:U\to V{}$) que satisface ${}F(x,g(x))=0{}$. Más aún, si ${}x \in U{}$ y ${}z\in V{}$ entonces ${}F(x,z)=0{}$ y ${}z=g(x){}$. 
Finalmente, ${}z=g(x){}$ es continuamente diferenciable y 
$$
D_{g}(x)=\frac{-1}{\frac{\partial F(x,z)}{\partial z}}D_{x}F(x,z)|_{z=g(x)}.
$$
Aquí ${}D_{x}F{}$ denota la derivada parcial de ${}F{}$ con respecto a ${}x{}$ como vector, es decir 
$$
D_{x}F=\left[ \frac{\partial F}{\partial x_{1}},\dots, \frac{\partial F}{\partial x_{n}} \right].
$$
Coordenada a coordenada se tiene que 
$$
\frac{\partial g}{\partial x_{i}}=\frac{-\frac{\partial F}{\partial x_{i}}}{\frac{\partial F}{\partial z}},\quad i=1,\dots,n.
$$
Entonces se puede aproximar ${}z{}$ en términos del plano tangente a la curva ${}g{}$ usando sus parciales, lo que es, si ${}F(x_{0},g(x_{0}))=0{}$, entonces 
$$
z=z_{0}+\left( \nabla g(x_{0}) \right)(x-x_{0}).
$$
##### Demostración:
Algunos resultados previos importantes:
1.- Como ${}F\in C^{1}{}$, ${}\frac{\partial F}{\partial z}{}$ es continua. Si suponemos ${}F_{z}(x_{0},z_{0})>0{}$. Sea ${}c>0{}$ tal que ${}\frac{\partial F}{\partial z}=F_{z}=c{}$. Para ${}{}$


##### Ejemplo
Sea ${}F(x,z)=x^{2}+z^{2}-1{}$. Tenemos que ${}\frac{\partial F}{\partial z}=2z{}$ que es distinto de cero para ${}z\neq 0{}$.
Por el teorema de la función implícita, existe ${}g:U\to U{}$ tal que ${}z=g(x){}$ siempre que 
$$
x^{2}+(g(x))^{2}-1=0,\text{ y } z\neq 0,
$$
y entonces podemos tomar ${}g(x)=\sqrt{ 1-x^{2} }{}$ para ${}z>0{}$ o ${}g(x)=-\sqrt{ 1-x^{2} }{}$ para ${}z<0{}$, de modo que tenemos que 
$$
U=\{ x:\lvert x \rvert <1 \}.
$$

