#Algoritmos
Otro de los tipos de [[Recursion|recursión]].
Cada nodo representa una llamada. Su etiqueta indica el trabajo realizado fuera de las llamadas recursivas.
- **Raiz:** la llamada inicial.
- **Ramas**: las llamadas a subproblemas.
- **Hojas**: las llamadas que resuelven un caso base.
- **Nivel**: llamadas a la misma profundidad; la raíz está en el nivel 0.
$$
	\text{costo total}=\sum_{\text{niveles internos}}\text{costo del nivel}+\text{costo de las hojas}.
$$
###### Ejemplo: una rama
$T(n)=T(n-1)+cn$, $T(1)=d$, y $c,d>0$.
Hay $n-1$ niveles internos y una hoja. 
$$
	\begin{align}
	T(n)&=cn+c(n-1)+\dots+2c+d \\
	&=c\sum_{j=2}^{n}j+d \\
	&=c\left(  \frac{n(n+1)}{2}-1 \right)+d.
	\end{align}
$$
Por tanto, 
$$
	T(n)\in \Theta(n^{2}).
$$
![[ArbolUnaRama]]

###### Ejemplo: dos ramas
$T(n)=2T(n/4)+cn^{2},T(1)=d$ y $c,d>0$.
Suponemos $n=4^{h}$. Estos son los primeros niveles internos:
![[Arbol2Ramas]]
Nivel interno $i$, con $0\leq i\leq h$, tal que:
Nodos $2^{i}$, 
Tamaño por nodo $n / 4^{i}$,
Costo por nodo $cn^{2} / 16^{i}$,
Costo por nivel $cn^{2} / 8^{i}$.
De nuestro supuesto inicial tenemos que $h=\log_{4}n$. La raíz está en el nivel 0, y las hojas en el nivel $h$. Hay en total $h+1$ niveles.
En cada división se generan dos llamadas $2^{h}=2^{\log_{4}n}=\dots=\sqrt{ n }$.
Entonces, para calcular el costo total, sumamos los niveles internos y después las hojas: 
$$
	T(n)=cn^{2}\sum_{i=0}^{h-1}\left( \frac{1}{8} \right)^{i}+d\sqrt{ n },
$$
cuyo orden dominante es $n^{2}$, es decir que podemos concluir que $T(n)\in \Theta(n^{2})$.