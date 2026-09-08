##### Definición:
Sean $N(T)$ y $R(T)$ el [[KernelYRango|kernel y la imagen]] de una transformación $T:V\to W$.
Definimos la ***nulidad*** como la dimensión del kernel $\text{dim}(N(T))$, y el ***rango*** como la dimensión de la imagen $\text{dim}(R(T))$.
Se pueden denotar como $\text{nullity}(T)$ y $\text{rank}(T)$.

##### Teorema 2.3. Teorema de la dimensión
Sean $V, W$ [[EspaciosVectoriales|espacios vectoriales]] sobre un campo $F$. Sea $T:V\to W$ una [[TransformacionesLineales|transformación lineal]]. Entonces 
$$
	\text{nullity}(T)+\text{rank}(T)=\text{dim}(V.)
$$
##### Demostración:
Sea $\text{nullity}(T)=k$ y $\text{dim}(V)=n$, vamos a demostrar que $\text{rank}(T)=n-k$.
Sea $S=\{ v_{1},v_{2},\dots,v_{k} \}$ una base de $N(T)$. Sabemos que podemos extender $S$ a una base de $V$ al añadir los vectores $\{ v_{k+1},\dots,v_{n} \}$, de forma que tenemos como resultado la base $S_{1}=\{ v_{1},\dots,v_{n} \}$.
Sabemos que $T(span(S_{1}))$ genera $R(T)$, es decir que  $span(T(S_{1}))=R(T)$. Por lo tanto
$$
	T\left( \sum_{i=1}^{n}a_{i}v_{i} \right)=\sum_{i=1}^{n}a_{i}T(v_{i})\in R(T).
$$
Pero además, $T(v_{i})=0$ para todo $i\leq k$, por lo tanto $\sum_{i=1}^{n}a_{i}T(v_{i})=\sum_{i=k+1}^{n}a_{i}T(v_{i})$. Es decir, tenemos un conjunto con $n-k$ vectores que genera a $R(T)$. Si demostramos que es una base, demostraremos que $\text{rank}(T)=n-k$, por lo tanto solo nos falta mostrar que son linealmente independientes.
Sea
$$
	0=\sum_{i=k+1}^{n}a_{i}T(v_{i})=T(\sum_{i=k+1}^{n}a_{i}v_{i}),
$$
esto implica que $\sum_{i=k+1}^{n}a_{i}v_{i}\in N(T)$, por lo tanto existen $b_{1},b_{2},\dots,b_{k}$ tales que 
$$
	\sum_{i=k+1}^{n}a_{i}v_{i}=\sum_{i=1}^{n}b_{i}v_{i}\implies\sum_{i=1}^{n}(-b_{i})v_{i}+\sum_{i=k+1}^{n}a_{i}v_{i}=0,
$$
pero como todos estos vectores son parte de nuestra base $S_{1}$, son linealmente independientes, lo que implica que $a_{k+1}=\dots=a_{n}=0$, por lo tanto $\{ T(v_{k+1}),\dots,T(v_{n}) \}$ son linealmente independientes, lo que concluye nuestra demostración. $\quad\square$


##### Teorema 2.4
Sean $V$ y $W$ espacios vectoriales sobre $F$. Sea $T:V\to W$ lineal. Entonces $T$ es inyectiva (uno a uno) si y sólo si $N(T)=\{ 0 \}$.
##### Demostración:
Por ser $T$ lineal, sabemos que $T(0)=0$. Además, por definición de inyectividad, sea $x\in N(T)$, entonces $T(x)=0\implies x=0$, por lo tanto $N(T)=\{ 0 \}$.
Para el regreso, supongamos que $N(T)=\{ 0 \}$. Sean $x,y\in V$ tales que $T(x)=T(y)$. Entonces tenemos que $T(x-y)=T(x)-T(y)=0$, lo que implica que $x-y\in N(T)$, y por lo tanto $x-y=0$, es decir que $x=y$, y por lo tanto $T$ es inyectiva. $\quad\square$


##### Teorema 2.5
Sean $V$ y $W$ espacios vectoriales de dimensión finita con la misma dimensión. Sea $T:V\to W$ lineal. Entonces las siguientes afirmaciones son equivalentes:
- $T$ es inyectiva.
- $T$ es suprayectiva.
- $\text{rank}(T)=\text{dim}(V)$.
##### Demostración:
Sea $T$ inyectiva, entonces $N(T)=\{ 0 \}$, entonces $\text{nullity}(T)=0$, por lo tanto $\text{rank}(T)=\text{dim}(V)=\text{dim}(W)$, es decir que $\text{rank}(T)=\text{dim}(W)$, la cual es la definición de suprayectividad. $\quad\square$

#AlgebraLineal #Teorema