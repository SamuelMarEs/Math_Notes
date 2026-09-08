Samuel Márquez Estrada

### Sección 2.1 Friedberg
Para los ejercicios 2-6, probar que $T$ es una transformación lineal, encontrar bases de $N(T)$ y $R(T)$, calcular sus dimensiones, y verificar si $T$ es inyectiva o suprayectiva.
2. $T:R^{3}\to R^{2}$ definida por $T(a_{1},a_{2},a_{3})=(a_{1}-a_{2},2a_{3})$.
   **Sol:**
   Sean $(a_{1},a_{2},a_{3}),(b_{1},b_{2},b_{3})\in R^{3}$ y $\lambda\in R$. Entonces $$
	\begin{align}
	T(\lambda a_{1}+b_{1},\lambda a_{2}+b_{2},\lambda a_{3}+b_{3})&=(\lambda a_{1}+b_{1}-\lambda a_{2}-b_{2},2\lambda a_{3}+2b_{3}) \\
	&=\lambda( a_{1}-a_{2},2a_{3})+(b_{1}-b_{2},2b_{3}) \\
	&=\lambda T(a_{1},a_{2},a_{3})+T(b_{1},b_{2},b_{3}).
	\end{align}
   $$
   Además tenemos que $N(T)=\{ (a,a,0):a\in R \}$ y una base es $\{ (1,1,0)\}$, por lo tanto $\text{dim}(N(T))=1$, es decir que $\text{dim}(R(T))=2$, y una base es la canónica $\{ (1,0),(0,1) \}$.
   Dado que $N(T)\neq \{ 0 \}$, entonces $T$ no es inyectiva. Por otro lado, tenemos que $R(T)=R^{2}$, por lo tanto $T$ es suprayectiva.
   
3. $T:R^{2}\to R^{3}$ definida por $T(a_{1},a_{2})=(a_{1}+a_{2},0,2a_{1}-a_{2})$.
   **Sol:**
   Sean $(a_{1},a_{2}),(b_{1},b_{2})\in R^{2}$ y $\lambda\in R$. Entonces $$
	\begin{align}
	T(\lambda a_{1}+b_{1},\lambda a_{2}+b_{2})&=(\lambda a_{1}+b_{1}+\lambda a_{2}+b_{2},0,2(\lambda a_{1}+b_{1})-\lambda a_{2}-b_{2}) \\
	&=\Lambda(a_{1}+a_{2},0,2a_{1}-a_{2})+(b_{1}+b_{2},0,2b_{1}-b_{2}) \\
	&= \lambda T(a_{1},a_{2})+\lambda T(b_{1},b_{2}).
	\end{align}
   $$
   Tenemos entonces que $N(T)=\{ (a_{1},a_{2}):a_{1}=-a_{2},2a_{1}=a_{2} \}=\{ 0 \}$, por lo tanto $\text{dim}(N(T))=0$, y entonces $\text{dim}(R(T))=2$. Dado que $N(T)=\{ 0 \}$, entonces $T$ es inyectiva. Sin embargo, no existe $x\in R^{2}$ tal que $T(x)=(0,1,0)$, por lo tanto $T$ no es suprayectiva.
   
4. $T:M_{2\times 3}(F)\to M_{2\times 2}(F)$ definida por $$
   	T\begin{pmatrix}
	a_{11} & a_{12} & a_{13} \\
	a_{21} & a_{22} & a_{23}
	\end{pmatrix}=\begin{pmatrix}
	2a_{11}-a_{12} & a_{13}+2a_{12} \\
	0 & 0
	\end{pmatrix}.
   $$
   **Sol:**
   La transformación no involucra a la segunda fila de la matriz, entonces podemos verla como una transformación $T:R^{3}\to R^{2}$, al menos para verificar que sea lineal. Sean $(a_{1},a_{2},a_{3}),(b_{1},b_{2},b_{3})\in R^{3}$ y $\lambda\in R$, tenemos que $$
	\begin{align}
	T(\lambda a_{1}+b_{1},\lambda a_{2}+b_{2},\lambda b_{3}+b_{3})&=(2(\lambda a_{1}+b_{1})+\lambda a_{2}+b_{2},\lambda a_{3}+b_{3}+2(\lambda a_{2}+b_{2})) \\
	&=\lambda(2a_{1}+a_{2},a_{3}+2a_{2})+(2b_{1}+b_{2},b_{3}+2b_{2}) \\
	&=\lambda T(a_{1},a_{2},a_{3})+T(b_{1},b_{2},b_{3}).
	\end{align}
   $$
   $N(T)=\{ A\in M_{2\times 3}(F):4a_{11}=2a_{12}=-a_{13}\}$ y una base es 
   $$
	\{ \begin{pmatrix}
	4 & 2 & -1 \\
	0 & 0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 & 0 \\
	1 & 0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 & 0 \\
	0 & 1 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 & 0 \\
	0 & 0 & 1
	\end{pmatrix} \},
   $$
   por lo tanto $\text{dim}(N(T))=4$, y entonces $\text{dime}(R(T))=2$. Dado que $N(T)\neq \{ 0 \}$, $T$ no es inyectiva. Además $\text{dim}(R(T))\neq\text{dim}(M_{2\times 2}(F))$, por lo tanto tampoco es suprayectiva.
   
5. $T:P_{2}(R)\to P_{3}(R)$ definida por $T(f(x))=xf(x)+f'(x)$.
   **Sol:**
   Sean $f(x)=a_{1}x^{2}+b_{1}x+c_{1},g(x)=a_{2}x^{2}+b_{2}x+c_{2}\in P_{2}(R)$ y $\lambda\in R$, tenemos que $$
	\begin{align}
	T(f(x)+g(x))&=(\lambda a_{1}+a_{2})x^{3}+(\lambda b_{1}+b_{2})x^{2}+(\lambda c_{1}+c_{2})x+2(\lambda a_{1}+a_{2})x+(\lambda b_{1}+b_{2}) \\
	&=\lambda[(a_{1}x^{3}+ b_{1}x^{2}+ c_{1}x)+(2a_{1}x+ b_{1})]+[(a_{2}x^{3}+b_{2}x^{2}+c_{1}x)+(2a_{2}x+b_{2})] \\
	&=\lambda T(f(x))+T(g(x)).
	\end{align}
   $$
   La única forma de que $T(f)=0$ es si $f=0$, por lo tanto $N(T)=\{ 0 \}$, por lo tanto la transformación es inyectiva. Sin embargo, por el teorema de la dimensión tenemos que $\text{dim}(R(T))=3$, por lo tanto no es suprayectiva, ya que $\text{dim}(P_{3}(R))=4$. En particular, no se puede cubrir ningún polinomio de la forma $g(x)=ax^{3}+bx^{2}+cx$ para $a,b,c\neq 0$.
   Una base de $R(T)$ es $\{ x^{3},x^{2},x \}$.
   
6. $T:M_{n\times n}(F)\to F$ definida por $T(A)=\text{tr}(A)$. La traza de $A$ dada por $$
   	\text{tr}(A)=\sum_{i=1}^{n}a_{ii}.
   $$
   **Sol:**
   Sean $A,B\in M_{n\times n}(F)$ con $A=[a_{ii}]$ y $B=[b_{ii}]$, y sea $\lambda \in R$, entonces   $$
	T(\lambda A+B)=\sum_{i=1}^{n}\lambda a_{ii}+b_{ii}=\lambda \sum_{i=1}^{n}a_{ii}+\sum_{i=1}^{n}b_{ii}=\lambda T(A)+T(B).
   $$
   El la base del kernel $N(T)$ tiene $n^{2}-n$ matrices, cada una con un uno en una posición distinta de la diagonal, además de $\begin{pmatrix}n-1 \\  1\end{pmatrix}=n-1$ matrices obtenidas de colocar un 1 en la posición 11, y todas las formas de colocar un $-1$ en las demás posiciones, i.e. $\text{dim}(N(T))=n^{2}-1$, y por lo tanto $\text{dim}(R(T))=1=\text{dim}(R)$, por lo tanto la transformación es suprayectiva, pero no es inyectiva. Una base de $R(T)$ es $\{ 1 \}$.

7.- Probar las propiedades:
   - Si $T:V\to W$ es lineal, entonces $T(\vec{0}_{v})=\vec{0}_{w}$. 
   - $T(r\vec{x}+\vec{y})=rT(\vec{x})+T(\vec{y})$.
   - $T(\vec{x}-\vec{y})=T(\vec{x})-T(\vec{y})$.
   - $T\left( \sum_{i=1}^{n}a_{i}x_{i} \right)=\sum_{i=1}^{n}a_{i}T(x_{i})$.
    **Solución:**
     Sea $T:V\to W$ una transformación lineal. Dado que $F$ es un campo, entonces $0\in F$, por lo tanto tenemos que $0\vec{x}=\vec{0}_{W}$ para todo $\vec{x}\in W$. Por lo tanto tenemos que 
   $$
   	T(\vec{0}_{V})=T(0\vec{x})=0T(\vec{x})=\vec{0}_{W}.\quad \square 
   $$
	Como $T$ es lineal, entonces tenemos que 
   $$
   	\begin{align}
	T(r\vec{x}+\vec{y})&=T(r\vec{x})+T(\vec{y}) \\
	&= rT(\vec{x})+T(\vec{y}).\quad\square
	\end{align}
   $$
	Podemos reescribirlo de la forma 
   $$
   	T(\vec{x}-\vec{y})=T(\vec{x}+(-1\cdot\vec{y}))=T(\vec{x})+T(-1\cdot \vec{y})=T(\vec{x})-T(\vec{y}).\quad\square
   $$
	Es inmediato que, dado que $T$ es lineal, entonces  $$
	     	T\left( \sum_{i=1}^{n}a_{i}x_{i} \right)=T(a_{1}x_{1}+\dots+a_{n}x_{n})=a_{1}T(x_{1})+\dots+a_{n}T(x_{n})=\sum_{i=1}^{n}a_{i}T(x_{i}).\quad\square
	     $$


11.- Probar que existe una transformación lineal $T:R^{2}\to R^{3}$ tal que $T(1,1)=(1,0,2)$ y $T(2,3)=(1,-1,4)$. ¿Qué es $T(8,11)$? 
**Sol:**
Sea $T(a_{1},a_{2})=(2a_{1}-a_{2} , a_{1}-a_{2}, 2a_{1})$, tenemos que $T(1,1)=(2-1,1-1,2)=(1,0,2)$, y $T(2,3)=(4-3,2-3,4)=(1,-1,4)$.
Además tenemos que para $(a_{1},a_{2}),(b_{1},b_{2})\in R^{2}$ y $\lambda\in R$, se cumple que 
$$
	\begin{align}
	T(\lambda a_{1}+b_{1},\lambda a_{2}+b_{2})&=(2(\lambda a_{1}+b_{1})-(\lambda a_{2}+b_{2}), (\lambda a_{1}+b_{1})-(\lambda a_{2}+b_{2}), 2(\lambda a_{1}+b_{1})) \\
	&=\lambda(2a_{1}-a_{2},a_{1}-a_{2},2a_{2})+(2b_{1}-b_{2},b_{1}-b_{2},2b_{1}) \\
	&=\lambda T(a_{1},a_{2})+T(b_{1},b_{2}),
	\end{align}
$$
por lo que $T$ es lineal. 
Además, $T(8,11)=(5,-3,16)$.


13.- Sean $V$ y $W$ espacios vectoriales, sea $T:V\to W$ lineal y sea $\{ w_{1},w_{2},\dots,w_{k} \}$ un conjunto de $k$ vectores linealmente independientes de $R(T)$. Probar que si $S=\{ v_{1},\dots,v_{k} \}$ se eligen tal que $T(v_{i})=w_{i}$ para $i=1,\dots,k$, entonces $S$ es linealmente independiente.
**Sol:**
**Prueba por contradicción:**
Supongamos que $S=\{ v_{1},\dots,v_{k} \}$ es un conjunto linealmente dependiente, esto quiere decir que existen $a_{1},\dots,a_{k}$ no todos ceros tales que 
$$
	a_{1}v_{1}+\dots+a_{k}v_{k}=0.
$$
Si tomamos la transformación lineal de esta combinación, tenemos que 
$$
	0=T\left( \sum_{i=1}^{k} a_{i}v_{i}\right)=a_{1}T(v_{1})+\dots+a_{k}T(v_{k})=a_{1}w_{1}+\dots+a_{k}w_{k,}
$$
es decir, tenemos una combinación lineal de $\{ w_{1},w_{2},\dots,w_{k} \}$ con $a_{1},\dots,a_{k}$ no todos ceros, que es igual a cero, es decir que $\{ w_{1},w_{2},\dots,w_{k} \}$ es linealmente independiente, pero esto es una contradicción.
Por lo tanto, $S$ tiene que ser linealmente independiente.


15.- Definamos 
$$
	T:P(R)\to P(R) \quad\text{como}\quad T(f(x))=\int_{0}^{x}f(t)dt.
$$
Probar que $T$ es linear e inyectiva, pero no suprayectiva.
**Sol:**
Por las propiedades de la integral, dados $f,g\in P(R)$ y $\lambda\in R$, tenemos que 
$$
	T(\lambda f+g)=\int_{0}^{x}\lambda f(t)+g(t)dt=\lambda\int_{0}^{x}f(t)dt+\int_{0}^{x}g(t)dt=\lambda T(f)+T(g).
$$
Además tenemos que la única forma de que la integral definida de un polinomio sea cero es que el polinomio sea el polinomio nulo, es decir que $N(T)=\{ 0 \}$, y por lo tanto la transformación es inyectiva.
Sin embargo, no existe ningún polinomio $g$ tal que $T(g)=1$, o en general cualquier constante distinta de cero, pues $\int_{0}^{x}g(t)dt$ nunca va a tener un término constante.


16.- Sea $T:P(R)\to P(R)$ definida como $T(f(x))=f'(x)$. $T$ es lineal. Probar que $T$ es suprayectiva, pero no inyectiva.
**Sol:**
Para cualquier polinomio $g\in P(R)$, podemos tomar $\int g=f$ tal que $T(f)=\left( \int g \right)'=g$, por lo tanto $T$ es suprayectiva.
Sea $h=1\in P(R)$, tenemos que $T(h)=0\implies h\in N(T)\implies N(T)\neq \{ 0 \}$, por lo tanto $T$ no puede ser inyectiva.$\square$


17.- Sean $V,W$ espacios vectoriales de dimensión finita y $T:V\to W$ lineal.
- Pruebe que si $\text{dim}(V)<\text{dim}(W)$ entonces $T$ no puede ser sobreyectiva.
  **Sol:** Sea $k=\text{dim}(V)$ y $n=\text{dim}(W)$, con $k<n$. Sabemos que $T$ es sobreyectiva si y sólo si $\text{rank}(T)=\text{dim}(W)$. Además, sabemos que, dada la base $S=\{ v_{1},\dots,v_{k} \}$, tenemos que $T(\text{span}(S))=R(T)$ la imagen de $T$. Es decir, tenemos un conjunto de $k$ vectores que genera a $R(T)$, por lo tanto $\text{rank}(T)\leq k<n$, es decir $\text{rank}(T)<\text{dim}(W)$, por lo que $T$ no puede ser sobreyectiva. $\square$
  
- Pruebe que si $\text{dim}(V)>\text{dim}(W)$ entonces $T$ no puede ser inyectiva.
  **Sol:** Nuevamente, sea $k=\text{dim}(V)$ y $n=\text{dim}(W)$ con $k>n$. Sabemos que $T$ es inyectiva si y sólo si $N(T)=\{ 0_{V} \}$. Dada una base de $V$, $S_{v}=\{ v_{1},\dots,v_{k} \}$, sabemos que el conjunto $S_{w}=\{ T(v_{1}),\dots,T(v_{n}) \}$ genera a $W$. Y además sabemos que se puede reducir a una base de tamaño $n$ para $W$. Es decir que, existen $k-n>0$ vectores que se pueden expresar como combinación lineal de los otros. Tomemos, sin pérdida de generalidad, un vector $j$ de este tipo, es decir un vector $v_{j}\in V$. Si $T(v_{j})=0$ ya acabamos, pues eso implica que $v_{j}\in N(T)$, y por ser parte de la base de $V$, sabemos que $v_{j}\neq 0$ y por lo tanto $T$ no puede ser inyectiva. Si $T(v_{j})\neq 0$ tenemos entonces que 
  $$
	T(v_{j})=a_{1}T(v_{1})+\dots+a_{j-1}T(v_{j-1})+a_{j+1}T(v_{j+1})+\dots+a_{k}T(v_{k}),
  $$
  con $a_{i}\in F$ y no todos ceros, y por lo tanto 
  $$
	\begin{align}
	0&=a_{1}T(v_{1})+\dots+a_{j-1}T(v_{j-1})+a_{j+1}T(v_{j+1})+\dots+a_{k}T(v_{k})-T(v_{j}) \\
	&=T(a_{1}v_{1}+\dots+a_{j-1}v_{j-1}+a_{j+1}v_{j+1}+\dots+a_{k}v_{k}-v_{j})
	\end{align},
  $$
  es decir que existe un vector $s=a_{1}v_{1}+\dots+a_{j-1}v_{j-1}+a_{j+1}v_{j+1}+\dots+a_{k}v_{k}-v_{j}$ distinto de cero (porque está generado por $S$ con algunos coeficientes distintos de cero), tal que $T(s)=0$, por lo tanto $s\in N(T)$, y por esto $T$ no es inyectiva. $\square$


18.- De un ejemplo de una transformación lineal $T:R^{2}\to R^{2}$ tal que $N(T)=R(T)$.
**Sol:** Sea $T(a,b)=(a-b,a-b)$, primero vamos a demostrar que $T$ es lineal.
Sean $(a_{1},b_{1}),(a_{2},b_{2})\in R^{2}$, y $\lambda\in R^{2}$, entonces 
$$
	\begin{align}
	 T(\lambda a_{1}+a_{2},\lambda b_{1}+b_{2})&=((\lambda a_{1}+a_{2})-(\lambda b_{1}+b_{2}),(\lambda a_{1}+a_{2})-(\lambda b_{1}+b_{2})) \\
	 &=(\lambda a_{1}-\lambda b_{1},\lambda a_{1}-\lambda b_{1})+(a_{2}-b_{2},a_{2}-b_{2}) \\
	 &=\lambda(a_{1}-b_{1},a_{1}-b_{1})+(a_{2}-b_{2},a_{2}-b_{2}) \\
	 &=\lambda T(a_{1},b_{2})+T(a_{2},b_{2}).
	\end{align}
$$
Entonces ya tenemos que en efecto $T$ es lineal. 
Por un lado, $N(T)=\{ (x,x)\in R^{2} \}$, y a su vez tenemos que $R(T)=\{ (x,x)\in R^{2} \}$, por lo tanto $N(T)=R(T).\quad\square$ 


22.- Sea $T:R^{3}\to R$ lineal. Pruebe que existen escalares $a,b,c$ tales que $T(x,y,z)=ax+by+cz$ para todo $(x,y,z)\in R^{3}$. ¿Se puede generaliar este resultado para $T:F^{n}\to F$? Nombre y pruebe un resultado análogo para $T:F^{n}\to F^{m}$.
**Sol:** Todo vector $(x,y,z)\in R^{3}$ se puede expresar como $(x,0,0)+(0,y,0)+(0,0,z)$ de forma que tenemos 
$$
	\begin{align}
	T((x,0,0)+(0,y,0)+(0,0,z))&=T(x,0,0)+T(0,y,0)+T(0,0,z) \\
	&=xT(1,0,0)+yT(0,1,0)+zT(0,0,1),
	\end{align}
$$
por lo que basta fijar $T(1,0,0)=a,T(0,1,0)=b$ y $T(0,0,1)=c$, de forma que tenemos 
$$
	T(x,y,z)=ax+by+cz.\quad\square
$$
El resultado se puede modificar de forma análoga para $T:F^{n}\to F$ para cualquier vector $(x_{1},\dots,x_{n})$ tomando los escalares $a_{1},\dots,a_{n}$ tales que $T(x_{1},\dots,x_{n})=a_{1}x_{1}+\dots+a_{n}x_{n}$. Basta tomar $a_{i}=T(e_{i})$ para $e_{i}=(0_{1},\dots,1_{i},\dots,0_{n})=$ el $i$-ésimo vector de la base canónica.
Para la forma general, se puede decir que, sea $T:F^{n}\to F^{m}$ lineal, existen vectores $a_{1},\dots,a_{n}\in F^{m}$ tales que 
$$
	T(x_{1},\dots,x_{n})=a_{1}x_{1}+\dots+a_{n}x_{n}.
$$
La demostración es exactamente que para el caso $m=1$, asignando $a_{i}=T(e_{i})\in F^{m}$ pues tenemos que $(x_{1},\dots,x_{n})=x_{1}e_{1}+\dots+x_{n}e_{n}.\quad\square$


23.- Sea $T:R^{3}\to R$ lineal. Describa geométricamente todas las posibilidades para el espacio nulo de $T$. $Hint:$ use el inciso 22.
**Sol:** Dados los escalares $a,b,c\in R$ que describen la transformación (por el inciso anterior), el espacio nulo $N(T)$ se puede describir de la forma $\{ (x,y,z):ax+by+cz=0 \}$, el cual es un ***PLANO*** por el origen en $R^{3}$.


25.- Sea $T:R^{2}\to R^{2}$. Incluya figuras para cada una de las siguientes:
- Encuentre una fórmula para $T(a,b)$, donde $T$ representa la proyección sobre el eje $y$ a lo largo del eje $x$.
  **Sol:** Sea $(a,b)\in R^{2}$, podemos reescribir nuestro vector de la forma $(a,0)+(0,b)$ dónde $(a,0)\in$ eje $x$, y $(0,b)\in$ eje $y$.
  Entonces, podemos dar la siguiente forma para la transformación lineal: 
  $$
	T(a,b)=(0,b).
  $$
  Geométricamente, esta transformación se puede ver como "comprimir" el espacio $R^{2}$ sobre el eje $y$.
  ![[ProyeccionSobreYdeX]]


- Encuentre una fórmula para $T(a,b)$, donde $T$ representa la proyección sobre el eje $y$ a lo largo de la recta $L=\{ (s,s):s\in R \}$.
  **Sol:** Sea $(a,b)\in R^{2}$, podemos reescribir el vector como $(a,b)=(a,a)+(0,b-a)$ donde $(a,a)\in L$ y $(0,b-a)\in$ eje $y$. Entonce, podemos dar la fórmula para la transformación lineal de la siguiente forma: 
  $$
	T(a,b)=(0,b-a).
  $$
  Geométricamente, está es la proyección de la recta identidad sobre el eje $y$.
![[ProyeccionSobreYdeL]]

















37.- Sean $V$ el espacio vectorial de todas las secuencias $(a_{n})$ sobre $F$ con las operaciones $(a_{n})+(b_{n})=(a_{n}+b_{n})$ y $t(a_{n})=(ta_{n})$. Sea además $T:V\to V$ definida como 
$$
	T(a_{1},a_{2},\dots)=(a_{2},a_{3},\dots),
$$
lineal y suprayectiva, pero no inyectiva.
- Pruebe que $V=R(T)+N(T)$, pero $V$ no es la suma directa de ambos espacios. 
  **Sol:** Primero vamos a demostrar que $R(T)\cap N(T)\neq \{ (0) \}$. Si tomamos la secuencia $(a,0,0,\dots)$, tenemos que $T(a,0,0,\dots)=(0,0,\dots)=(0)$, por lo tanto $(a,0,0,\dots)\in N(T)$. Adicionalmente, dado que $T$ es suprayectiva, tenemos que existe una secuencia $(a_{n})$ en $V$ tal que $T(a_{n})=(a,0,0,\dots)$, en particular basta tomar por ejemplo $(d,a,0,0,\dots)$.
  Entonces, tenemos que nuestra secuencia $(a,0,\dots)\in R(T)\cap N(T)$, por lo tanto $V$ no puede ser suma directa de ambos espacios.
  Sin embargo, dado que $T$ es suprayectiva, tenemos que $R(T)=V$, y por esto es trivial que $V=R(T)+N(T)$ ya que basta tomar $(a_{n})\in R(T)=V$ y $(0)\in N(T).\quad\square$ 
  
- Encuentre una operación lineal $T_{1}$ sobre $V$ tal que $R(T_{1})\cap N(T_{1})=\{ 0 \}$ pero $V$ no es la suma directa de $R(T_{1})$ y $N(T_{1})$.
  **Sol:** Podemos tomar la otra transformación del ejercicio 21, es decir 
  $$
	T_{1}(a_{1},a_{2},\dots)=U(a_{1},a_{2},\dots)=(0,a_{1},\dots).
  $$
  Es evidente que $N(T_{1})=\{ 0 \}$, pues cualquier sucesión no cero no va transformarse en cero. Por esto es que se satisface que $R(T_{1})\cap N(T_{1})=\{ 0 \}$.
  Sabiendo esto, se tendría que cumplir que $R(T_{1})=V$ para que $V=R(T_{1})\oplus N(T_{1})$. Sin embargo, cualquier sucesión $(b_{1},b_{2},\dots)$ con $b_{1}\neq 0$ no puede estar en la imagen $R(T)$. Supongamos que si estuviera, entonces existiría $(a_{1},a_{2},\dots)$ tal que $T_{1}(a_{1},a_{2},\dots)=(0,a_{1},\dots)=(b_{1},b_{2},\dots)$, por lo que tendríamos que $b_{1}= 0$, lo cual es una contradicción. Por lo tanto $R(T)\neq V$, y por esto $V$ no es suma directa de la imagen y el espacio nulo. $\quad\square$



 