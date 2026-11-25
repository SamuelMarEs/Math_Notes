#AlgebraLineal 
#### Definición 
Sea ${}V{}$ un espacio vectorial sobre un campo ${}F{}$ de característica distinta de dos. Una función ${}K:V\to F{}$ se llama una ***forma cuadrática*** sobre ${}V{}$ si existe una forma bilineal simétrica ${}H\in \mathcal{B}(V){}$ tal que 
$$
K(x)=H(x,x),\quad\text{para todo }x \in V.
$$

Si conocemos la forma de una forma cuadrática asociada a una forma bilineal simétrica ${}H{}$ sobre ${}V{}$, entonces podemos recuperar ${}H{}$ a partid de ${}K{}$ mediante 
$$
H(x,y)=\frac{1}{2}[K(x+y)-K(x)-K(y)].
$$

El ejemplo más clásico de una forma cuadrática es un polinomio homogéneo de segundo grado de varias variables.
Dadas las variables ${}t_{1},\dots,t_{n}{}$ que toman valores sobre un campo ${}F{}$ de característica distinta de dos, y dados los escalares ${}a_{ij}{}$ (no necesariamente distintos), con ${}1\leq i,j\leq n{}$, definimos el polinomio 
$$
f(t_{1},\dots,tt_{n})=\sum_{i\leq j}a_{ij}a_{ij}t_{i}t_{j},
$$
y todo polinomio de esta forma es una forma cuadrática.

Si ${}\beta$ es la base ordenada estándar de ${}F^{n}{}$, entonces la forma bilineal simétrica ${}H{}$ correspondiente a la forma cuadrática ${}f{}$ definida anteriormente, tiene como matriz asociada ${}\psi_{\beta}(H)=A{}$ con entradas