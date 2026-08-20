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


#AlgebraLineal #Teorema