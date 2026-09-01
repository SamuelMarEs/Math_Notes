##### Definición:
Sean $V,W$ [[EspaciosVectoriales|espacios vectoriales]] sobre un campo $F$. Y sea $T:V\to W$ [[TransformacionesLineales|lineal]]. Decimos que la función $U:W\to V$ es ***inversa*** de $T$ si:
1. $TU=I_{W}$. (La transformación $TU$ es la identidad de $W$).
2. $UT=I_{V}$. (La transformación $UT$ es la identidad de $V$).

Si recordamos todo lo que sabemos de funciones inversas, existen varias propiedades que ya conocemos.
- La inversa es única  y la denotamos $T^{-1}$.
- $(T^{-1})^{-1}=T$. La inversa de la inversa es la función original.
- $T$ tiene inversa si y sólo si $T$ es biyectiva.

##### Definición:
Sean $V,W$ espacios vectoriales sobre un campo $F$. Decimos que $V$ y $W$ son ***isomorfos*** si $\exists\quad T:V\to W$ lineal e invertible, la cual llamamos un ***isomorfismo***. Denotamos que dos espacios son isomorfos como $V\cong W$.

##### Teorema 2.17.
Sean $V,W$ espacios vectoriales sobre $F$. Sea $T:V\to W$ lineal e invertible. Entonces $T^{-1}W:\to V$ también es lineal.
##### Demostración:
Sean $y_{1},y_{2}\in W$ y $c\in F$. Vamos a demostrar que $T^{-1}(cy_{1}+y_{2})=cT^{-1}(y_{1})+T^{-1}(y_{2})$.
Por definición, existen $x_{1},x_{2}\in V$ únicos tales que $T^{-1}(y_{1})=x_{1}$ y $T^{-1}(y_{2})=x_{2}$, así como también $T(x_{1})=y_{1}$ y $T(x_{2})=y_{2}$.
Entonces tenemos que 
$$
	\begin{align}
	T^{-1}(cy_{1}+y_{2})&=T^{-1}(cT(x_{1})+T(x_{2})) \\
	&=T^{-1}(T(cx_{1}+x_{2})) \\
	&=cx_{1}+x_{2} \\
	&=cT^{-1}(y_{1})+T^{-1}(y_{2}).\quad\square
	\end{align}
$$

##### Lema:
Sean $V$ y $W$ espacios vectoriales sobre $F$, y $T:V\to W$ lineal e invertible. Entonces $V$ es de dimensión finita si y sólo si la dimensión de $W$ también es finita. Más aún, $\text{dim}(V)=\text{dim}(W).$
##### Demostración:
Supongamos $V$ es de dimensión finita, es decir que $\text{dim}(V)=n$ para algún $n$. Entonces existe $\beta=\{ v_{1},\dots,v_{n} \}$ una base de $V$. Sabemos que el conjunto 
$$
	T(\beta)=\{ T(v_{i}):1\leq i\leq n \}
$$
genera a $\text{rank}(T)$, por lo tanto, $R(T)$ es de dimensión finita. Además, dado que $T$ es invertible, es suprayectiva, y por lo tanto $\text{rank}(T)=\text{dim}(W)$, por lo tanto $W$ tiene dimensión finita.
La demostración del regreso es análoga pero tomando una base $\gamma$ para $W$, y la transformación $T^{-1}$. 
Dado que ambos son de dimensión finita, por el [[TeoremaDimension|teorema de la dimensión]], sabemos que 
$$
	\text{rank}(T)+\text{nullity}(T)=\text{dim}(V).
$$
Además, dado que $T$ es invertible, es biyectiva, y por lo tanto $\text{dim}(W)=\text{rank}(T)$ y $\text{nullity}(T)=0$, por lo tanto tenemos que 
$$
	\text{dim}(W)=\text{dim}(V).\quad\square
$$

##### Teorema 2.18.
Sean $V$ y $W$ espacios vectoriales de dimensión finita sobre $F$ con bases ordenadas $\beta$ y $\gamma$. Sea $T:V\to W$ lineal. Entonces $T$ es invertible si y sólo si $[T]_{\beta}^{\gamma}$ es invertible. Más aún 
$$
	[T^{-1}]_{\gamma}^{\beta}=([T]_{\beta}^{\gamma})^{-1}.
$$
##### Demostración:
$\Rightarrow$ 

$\Leftarrow$ Supongamos que $[T]_{\beta}^{\gamma}$ es invertible, es decir que existe $([T]_{\beta}^{\gamma})^{-1}$ tal que $[T]_{\beta}^{\gamma}([T]_{\beta}^{\gamma})^{-1}=I$.

##### Teorema 2.19.
Sean $V$ y $W$ espacios vectoriales sobre $F$ de dimensión finita. $\exists$ un *isomorfismo* de $V$ en $W$ si y sólo si $\text{dim}(V)=\text{dim}(W)$.
Es decir $V\cong W\Longleftrightarrow\text{dim}(V)=\text{dim}(W)$.
##### Demostración:
$\Rightarrow$ Dado que existe un isomorfismo, sabemos que existe una transformación $T:V\to W$ lineal e invertible. Entonces por el lema tenemos inmediatamente que $\text{dim}(W)=\text{dim}(V)$.

$\Leftarrow$ Supongamos que $\text{dim}(V)=\text{dim}(W)$. Queremos demostrar que existe $T:V\to W$ lineal e invertible, o en otras palabras, lineal y biyectiva. Sean $\beta=\{ v_{1},\dots,v_{n} \}$ y $\gamma=\{ w_{1},\dots,w_{n} \}$ bases ordenadas para $V$ y $W$. Por el [[BasesOrdenadas|teorema 2.6]] existe una transformación lineal $T:V\to W$ tal que $T(v_{i})=w_{i}$ para $i=1,\dots,n$. Entonces solo basta probar que $T$ es biyectiva. Para esto basta probar que $N(T)=\{ 0 \}$, y el resto es por el [[TeoremaDimension|teorema 2.5]].
Sea $x\in N(T)$, tenemos que $T(x)=0$. Sabemos que existen escalares $a_{1},\dots,a_{n}$ tales que $x=\sum_{i=1}^{n}a_{i}v_{i}$, por lo tanto 
$$
	0=T(x)=T\left( \sum_{i=1}^{n} a_{i}v_{i} \right)=\sum_{i=1}^{n}a_{i}w_{i}.
$$
Sin embargo, como $\{ w_{1},\dots,w_{n} \}$ es una base, tenemos que 
$$
	\sum_{i=1}^{n}a_{i}w_{i}=0\Longleftrightarrow a_{i}=0\quad\forall i.
$$
Por lo tanto tenemos que $x=0$, y por lo tanto $N(T)=\{ 0 \}$. Entonces, por el ***teorema 2.5*** sabemos que $T$ es biyectiva. $\quad\square$



#AlgebraLineal