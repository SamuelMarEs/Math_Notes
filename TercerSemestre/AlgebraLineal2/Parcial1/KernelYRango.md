##### Definición:
Sean $V$ y $W$ [[EspaciosVectoriales|espacios vectoriales]] sobre un campo $F$, y sea $T:V\to W$ [[TransformacionesLineales|lineal]].
1. $N(T)=\{ \vec{x}\in V:T(\vec{x})=\vec{0}_{W} \}$ es el ***espacio nulo*** de $T$. (Kernel o núcleo).
2. $R(T)=\{ T(\vec{x})\in W: \exists \vec{x}\in V \}$ es el ***rango*** o ***imagen*** de $T$.
##### Ejemplo:
Sea $T:\mathbb{R}^{3}\to \mathbb{R}^{2}$ definida por $T(a_{1},a_{2},a_{3})=(a_{1}-a_{2},2a_{3})$ una transformación lineal. Encontrar $N(T)$ y $R(T)$.
$N(T)=\{ (a_{1},a_{2},a_{3})\in\mathbb{R}^{3}: a_{1}-a_{2}=0,a_{3}=0\}=\{ (a,a,0):a\in\mathbb{R} \}$. $R(T)=\mathbb{R}^{2}$, pues para cualquier $(x,y)$ basta tomar la terna $(x,0, y/2)$.


##### Teroema 2.1
Sean $V$ y $W$ espacios vectoriales sobre $F$ y sea $T:V\to W$ una transformación lineal. 
Entonces tanto $N(T)$ es un subespacio vectorial de $V$, y $R(T)$ es un subespacio vectorial de $W$.
##### Demostración:
Primero vamos a demostrar que $N(T)$ es un subespacio de $V$. 
Por ser $T$ lineal, entonces $T(\vec{0}_{V})=\vec{0}_{W}$, por lo tanto $\vec{0}_{V}\in N(T)$.
Sean $v,u\in N(T)$, entonces $T(v+w)=T(v)+T(w)=\vec{0}_{W}$, por lo tanto $v+w\in N(T)$.
Sea además $\lambda\in F$, entonces $T(\lambda v)=\lambda T(v)=\lambda \cdot \vec{0}_{W}=\vec{0}_{W}$.

Ahora, para demostrar que $R(T)$ es un subespacio de $W$.
Por ser $T$ lineal, $\exists \vec{0}_{V}\in V$ tal que $T(\vec{0}_{V})=\vec{0}_{W}$, por lo tanto $\vec{0}_{W}\in R(T)$.
Sean $w,u\in R(T)$, entonces $\exists x,y\in V$ tales que $T(x)=w$ y $T(y)=u$. Sabemos que $x+y\in V$, por lo tanto $T(x+y)=T(x)+T(y)=w+u$, y entonces $w+u\in R(T)$.
Sea además $\lambda\in F$. Sabemos que $\lambda x\in V$, lo que implica que $T(\lambda x)=\lambda T(x)=\lambda w$, por lo tanto $w\in R(T)$.

Con esto concluye la demostración de que tanto $N(T)$ como $R(T)$ son subespacios de $V$ y $W$ respectivamente. $\quad\square$


##### Teorema 2.2
Sean $V$ y $W$ espacios vectoriales sobre $F$ y sea $T:V\to W$ una transformación lineal. Sea $B=\{ v_{1},\dots,v_{n} \}$ una base de $V$. 
Entonces $span(T(B))=R(T)$.
##### Demostración:
Sea $w\in R(T)$. Sabemos que $\exists v\in V$ tal que $T(v)=w$. Como $B$ es una base para $V$, entonces 
$$
	v=a_{1}v_{1}+\dots+a_{n}v_{n}\quad\text{para}\quad a_{1},\dots,a_{n}\in F.
$$
Por lo tanto, tenemos que 
$$
	w=T(v)=T(a_{1}v_{1}+\dots+a_{n}v_{n})=a_{1}T(v_{1})+\dots+a_{n}T(v_{n}),
$$
es decir que $w$ se puede escribir como combinación lineal de $T(B)$ para cualquier $w\in R(T)$, por lo tanto 
$$
	R(T)=span(T(B)).\quad\square
$$


#AlgebraLineal #Teorema