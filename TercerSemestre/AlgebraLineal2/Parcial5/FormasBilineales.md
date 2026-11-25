#AlgebraLineal 
#### Definición
Sea ${}V{}$ un espacio vectorial sobre un campo ${}F{}$. Una función ${}H{}$ del conjunto ${}V\times V{}$ en ${}F{}$ se llama una forma ***bilineal*** sobre ${}V{}$ si ${}H{}$ es lineal en cada variable cuando la otra se mantiene fija.
El conjunto de todas las funciones bilineales sobre ${}V{}$ se denota como ${}\mathcal{B}(V){}$.
Notese que el producto interno sobre un espacio vectorial es bilineal si el campo son los reales, pero no si son los complejos.

Las formas bilineales se pueden asociar a una matriz de forma similar a las transformaciones lineales. 
Para ${}A\in M_{n\times n}(F){}$, y ${}V=F^{n}{}$, definimos la forma bilineal ${}H:V\times V\to F{}$ mediante 
$$
H(x,y)=x^{t}Ay,\quad \text{para todo }x,y\in V.
$$
La matriz asociada a una forma bilineal ${}H{}$ respecto a una base ordenada ${}\beta{}$ se denota ${}\psi_{\beta}(H){}$. 
Si ${}\beta=\{ v_{1},\dots,v_{n} \}{}$, entonces las entradas de la matriz ${}A=\psi_{\beta}(H){}$ están dadas de la forma 
$$
(A)_{ij}=H(v_{i},v_{j}).
$$
Se puede demostrar que esta matriz es única.

#### Propiedades
Para cualquier forma bilineal ${}H{}$ sobre un espacio vectorial ${}V{}$ sobre un campo ${}F{}$, se cumplen las siguientes propiedades:
1.- Si, para cualquier ${}x \in V{}$ definimos 
$$
L_{x}(y)=H(x,y),\quad R_{x}(y)=H(y,x),
$$
para todo ${}y\in V{}$, entonces ${}L_{x}{}$ y ${}R_{x}{}$ son lineales.
2.- ${}H(0,x)=H(x,0)=0{}$ para todo ${}x \in V{}$.
3.- Para todos ${}x,y,z,w\in V{}$, 
$$
H(x+y,z+w)=H(x,z)+H(x,w)+H(y,z)+H(y,w).
$$
4.- Si ${}J:V\times V \to F{}$ esta definida como ${}J(x,y)=H(y,x){}$, entonces ${}J{}$ es una forma bilineal.


#### Definición
Sea ${}V{}$ un espacio vectorial, y sean ${}H_{1}{}$ y ${}H_{2}{}$ dos formas bilineales sobre ${}V{}$, y sea ${}a\in F{}$ un escalar, la suma ${}(H_{1}+H_{2}){}$ y el producto escalar ${}aH_{1}{}$ se definen como para cualquier función.

Entonces, tenemos una suma y un producto escalar de formas bilineales, lo que nos lleva a pensar en si el conjunto de formas bilineales es un espacio vectorial, que se responde con el siguiente teorema:
#### Teorema 6.31
Para cualquier espacio vectorial ${}V{}$, la suma de dos formas bilineales y el producto escalar por una forma bilineal sobre ${}V{}$ son nuevamente formas bilineales sobre ${}V{}$.
Este teorema nos asegura que entonces ${}\mathcal{B}(V){}$ es un a espacio vectorial con respecto a esas operaciones.

La demostración debería ser casi trivial.

#### Teorema 6.32
Para cualquier espacio vectorial ${}V{}$ de dimensión finita sobre ${}F{}$ y cualquier base ordenada ${}\beta \subset V{}$, ${}\psi_{\beta}:\mathcal{B}(V)\to M_{n\times n}(F){}$ es un isomorfismo.
Como corolario, esto nos dice que la dimensión de ${}\mathcal{B}(V){}$ es ${}n^{2}{}$.

