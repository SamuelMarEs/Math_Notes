##### Definición:
Dados dos conjuntos $A$ y $B$, una ***función*** de $A$ en $B$ es una relación $f$ tal que si $(a,b)\in f$ y $(a,c)\in f$ entonces $b=c$.
Decimos que $f$ es ***sobreyectiva*** si para cada $b\in B$ existe $a\in A$ tal que $(a,b)\in f$.
Decimos que $f$ es ***inyectiva*** si cuando $(a_{1},b),(a_{2},b)\in f$, entonces se tiene que $a_{1}=a_{2}$.
Denotamos la relación $f$ entre $A$ y $B$ como 
$$
	f:A\to B,
$$
y para decir que $(x,y)\in f$ escribimos $f(x)=y$.

Vamos a estudiar las funciones cuyo dominio es un conjunto $A\subset\mathbb{R}^{n}$ y toman valores en $\mathbb{R}^{m}$ 
$$
	f:\mathbb{R}^{n}\to\mathbb{R}^{m}\quad n,m\in\mathbb{N}.
$$
Si $m=1$ decimos que es una función con **valores escalares**, y si $m>1$ decimos que es una función con **valores vectoriales**.


##### Ejemplos:
1. Sea $f:\mathbb{R}^{3}\to\mathbb{R}$ dada por $f(x,y,z)=(x^{2}+y^{2}+z^{2})^{-3/2}$. El dominio de $f$ es $\mathbb{R}^{3}\setminus \{ (0,0,0) \}$.
2. $g:\mathbb{R}^{6}\to\mathbb{R}^{2}$ dada por $g(x_{1},x_{2},x_{3},x_{4},x_{5},x_{6})=(x_{1}x_{2}x_{3}x_{4}x_{5}x_{6},\sqrt{ x_{1}^{2}+x_{6}^{2} })$.


### [[ConjuntoDeNivel|Conjuntos de nivel]]
Supongamos que $f:\mathbb{R}^{3}\to\mathbb{R}$ esta dada por $f(x,y,z)=x^{2}+y^{2}+z^{2}$.
El conjunto $\{ (x,y,z)\in\mathbb{R}^{3}:f(x,y,z)=r^{2} ,r>0\}$ es la esfera con centro en el origen y radio $r$. Estas esferas son las *superficies de nivel*.
De forma similar, si tenemos $f:\mathbb{R}^{2}\to\mathbb{R}$, podemos tomar las *curvas de nivel* como el conjunto $\{ (x,y,a)\in\mathbb{R}^{3}:f(x,y)=a \}$. 


#Calculo 