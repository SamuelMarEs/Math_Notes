##### Definición:
Sea $V$ un espacio vectorial de dimensión finita. Sea $\{ v_{1},\dots,v_{n} \}$ una base de $V$, decirmos que esa base en particular es una ***base ordenada*** de $V$ si nos importa el orden de los vectores. 
(Hay $n!$ bases ordenadas distintas dada una base).
Por ejemplo, las bases $v_{1},v_{2},\dots,v_{n}$ y $v_{n},v_{1},v_{2},\dots ,v_{n-1}$, si bien son una misma base, no son iguales como bases ordenadas.

##### Teorema 2.6
Sean $V$ y $W$ [[EspaciosVectoriales|espacios vectoriales]] sobre $F$ y $\{ v_{1},v_{2},\dots,v_{n} \}$ una base ordenada de $V$. Dada $w_{1},w_{2},\dots,w_{n}\in W$, existe una única $T:V\to W$ lineal tal que $T(v_{i})=w_{i}$ para todo $1\leq i\leq n$.
##### Demostración:
Recordemos que si $x\in V\implies x=\sum_{i=1}^{n}a_{i}v_{i}$ dónde $a_{i}\in F$ son únicos (dada la base ordenada). Sea $T:V\to W$ definida por $T(x)=\sum_{i=1}^{n}a_{i}w_{i}$ dónde $a_{i}$ son los mismos que generan a $x$ dada la base ordenada.
1.- Primero vamos a demostrar que $T$ es lineal. Sean $x,y\in V$ caracterizados por los escalares $a_{i},b_{i}$, y sea además $\lambda\in F$ entonces 
$$
	T(\lambda x+y)=\sum_{i=1}^{n}(\lambda a_{i}+b_{i})w_{i}=\lambda \sum_{i=1}^{n}a_{i}w_{i}+\sum_{i=1}^{n}b_{i}w_{i}=\lambda T(x)+T(y),
$$
por las propiedades de la suma sobre $V$ y sobre $F$.
2.- Ahora vamos a verificar que $T(v_{i})=w_{i}$. Sabemos que $v_{i}=\sum_{k=1}^{n}a_{k}v_{k}$ donde $a_{k}=0$ para todo $k\neq i$, y $a_{i}=1$. Entonces tenemos que 
$$
	T(v_{i})=\sum_{k=1}^{n}a_{k}w_{k}=w_{i}.
$$
3.- Por último, queremos demostrar que $T$ es única. Supongamos que existe otra transformación lineal $U:V\to W$ tal que $U(v_{i})=w_{i}$ para todo $i$. Sea $x\in V$, entonces tenemos que 
$$
	T(x)=\sum_{i=1}^{n}a_{i}w_{i}=\sum_{i=1}^{n}a_{i}U(v_{i})=U\left( \sum_{i=1}^{n}a_{i}v_{i} \right)=U(x).\quad\square
$$  
###### Corolario:
Sean $V$ y $W$ espacios vectoriales sobre $F$ y $\beta=\{ v_{1},\dots,v_{n} \}$ una base ordenada de $V$. Si $T$ y $U$ son transformaciones lineales de $V$ en $W$ y $T(v_{i})=U(v_{i})$ para todo $i$, entonces $T=U$.
###### Demostración:
Sean $\{ w_{1},\dots,w_{n}\}$ vectores arbitrarios tales que $w_{i}=T(v_{i})$, entonces, por el teorema 2.6, $T$ es única, es decir que $T(v_{i})=U(v_{i})\implies T=U.\quad\square$


#AlgebraLineal #Teorema