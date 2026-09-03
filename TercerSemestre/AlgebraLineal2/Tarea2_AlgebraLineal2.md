### Sección 2.2 Friedberg
2.- Sea $\beta$ y $\gamma$ las bases canónicas ordenadas para $R^{n}$ y $R^{m}$, respectivamente. Para cada transformación lineal $T:R^{n}\to R^{m}$ calcule $[T]_{\beta}^{\gamma}$.
- $T:R^{2}\to R^{3}$ definida como $T(a_{1},a_{2})=(2a_{1}-a_{2},3a_{1}+4a_{2},a_{1})$.
  **Sol:** 
  Primero vamos a calcular la imagen de los vectores de la base $\beta$.
  $T(1,0)=(2,3,1)$, $T(0,1)=(-1,4,0)$. Entonces la representación matricial de nuestra transformación es 
  $$
	[T]_{\beta}^{\gamma}=\begin{pmatrix}
	2 & -1 \\
	3 & 4 \\
	1 & 0
	\end{pmatrix}.
  $$
  
- $T:R^{3}\to R^{2}$ definida como $T(a_{1},a_{2},a_{3})=(2a_{1}+3a_{2}-a_{3},a_{1}+a_{3})$.
  **Sol:**
  La imagen de la base canónica es $T(1,0,0)=(2,1)$, $T(0,1,0)=(3,0)$, y $T(0,0,1)=(-1,1)$.
  Entonces tenemos que la representación matricial es 
  $$
	[T]_{\beta}^{\gamma}=\begin{pmatrix}
	2 & 3 & -1 \\
	1 & 0 & 1
	\end{pmatrix}.
  $$
  
- $T:R^{3}\to R$ definida como $T(a_{1},a_{2},a_{3})=2a_{1}+a_{2}-3a_{3}$.
  **Sol:**
  La imagen de la base es $T(1,0,0)=2$, $T(0,1,0)=1$ y $T(0,0,1)=-3$. Por lo tanto 
  $$
	[T]_{\beta}^{\gamma}=(2,1,-3).
  $$
- $T:R^{3}\to R^{3}$ definida como $T(a_{1},a_{2},a_{3})=(2a_{2}+a_{3},-a_{1}+4a_{2}+5a_{3},a_{1}+a_{3}).$
  **Sol:**
  La imagen de la base es $T(1,0,0)=(0,-1,1)$, $T(0,1,0)=(2,4,0)$ y $T(0,0,1)=(1,5,1)$.
  Entonces la matriz es 
  $$
	[T]_{\beta}=\begin{pmatrix}
	0 & 2 & 1 \\
	-1 & 4 & 5 \\
	1 & 0 & 1
	\end{pmatrix}.
  $$
  
- $T:R^{n}\to R^{n}$ definida como $T(a_{1},\dots,a_{n})=(a_{1},\dots,a_{1})$.
  **Sol:**
  La imagen de cualquier vector de la base canónica es $T(e_{1})=(1,\dots,1)$ y $T(e_{i})=(0,\dots,0)$ si $i\neq 1$. Entonces la matriz resultante es la matriz de $n\times n$ dada por 
  $$
	[T]_{\beta}=\begin{pmatrix}
	1 & 0 & \dots & 0 \\
	1 & 0 & \dots & 0 \\
	\vdots  &  &  & \vdots \\
	1 & 0 & \dots & 0
	\end{pmatrix}.
  $$
  
- $T:R^{n}\to R^{n}$ definida como $T(a_{1},\dots,a_{n})=(a_{n},a_{n-1},\dots,a_{1})$.
  **Sol:**
  La imagen de cualquier vector de la base es $T(e_{i})=e_{n-i+1)}$, y lo que esta haciendo la transformación es "invetir" la base. Entonces la matriz asociada es 
  $$
	[T]_{\beta}=\begin{pmatrix}
	0 & \dots & 0 & 1 \\
	0 & \dots & 1 & 0 \\
	\vdots &  &  & \vdots \\
	1 & \dots & 0 & 0
	\end{pmatrix}.
  $$
  
- $T:R^{n}\to R$ definida como $T(a_{1},\dots,a_{n})=a_{1}+a_{n}.$
  La imagen de la base es $T(e_{i})=1$ si $i=1,n$, $T(e_{i})=0$ para $i\neq 1,n$. Entonces nuestra matriz es el vector 
  $$
	[T]_{\beta}^{\gamma}=(1,0,\dots,0,1).
  $$


3.- Sea $T:R^{2}\to R^{3}$ definida como $T(a_{1},a_{2})=(a_{1}-a_{2},a_{1},2a_{1}+a_{2})$. Sea $\beta$ la base canónica ordenada para $R^{2}$ y $\gamma=\{ (1,1,0),(0,1,1),(2,2,3) \}$. Calcula $[T]_{\beta}^{\gamma}$. Si $\alpha=\{ (1,2),(2,3) \}$, calcula $[T]_{\alpha}^{\gamma}$.
**Sol:**
La imagen de la base canónica $\beta$ es $T(1,0)=(1,1,2)=-\frac{1}{3} (1,1,0)+0(0,1,1)+\frac{2}{3} (2,2,3)$ y $T(0,1)=(-1,0,1)=-1(1,1,0)+1(0,1,1)+0(2,2,3)$. Entonces nuestra matriz asociada a la transformación es 
$$
	[T]_{\beta}^{\gamma}=\begin{pmatrix}
	-\frac{1}{3} & -1 \\
	0 & 1 \\
	\frac{2}{3} & 0
	\end{pmatrix}.
$$
Si en su lugar tomamos la base $\alpha=\{ (1,2),(2,3) \}$, entonces tenemos que la imagen de la transformación es $T(1,2)=(-1,1,4)=-\frac{7}{3}(1,1,0)+2(0,1,1)+\frac{2}{3}(2,2,3)$, y para el otro vector tenemos $T(2,3)=(-1,2,7)=-\frac{11}{3}(1,1,0)+3(0,1,1)+\frac{4}{3}(2,2,3)$, entonces la representación matricial queda como 
$$
	[T]_{\alpha}^{\gamma}=\begin{pmatrix}
	-\frac{7}{3} & -\frac{11}{3} \\
	2 & 3 \\
	\frac{2}{3} & \frac{4}{3}
	\end{pmatrix}.
$$


4.- Define $T:M_{2\times 2}(R)\to P_{2}(R)$ como
$$
	T\begin{pmatrix}
	a & b \\
	c & d
	\end{pmatrix}=(a+b)+(2d)x+bx^{2}.
$$
Sean 
$$
	\beta=\left\{ \begin{pmatrix}
	1 & 0 \\
	0 & 0
	\end{pmatrix},\begin{pmatrix}
	0 & 1 \\
	0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 \\
	1 & 0
	\end{pmatrix},
	\begin{pmatrix}
	0 & 0 \\
	0 & 1
	\end{pmatrix}\right\}\quad\text{y}\quad \gamma=\{ 1,x,x^{2} \}.
	
$$
Calcula $[T]_{\beta}^{\gamma}$.
**Sol:**
Sea $\beta=\{  e_{1},e_{2},e_{3},e_{4} \}$ la base canónica del espacio $M_{2\times 2}(R)$. Entonces tenemos que 
$$
	T(\beta)=\{ 1,1+x^{2},0,2x \},
$$
entonces tenemos que 
$$
	[T]_{\beta}^{\gamma}=\begin{pmatrix}
	1 & 1 & 0 & 0 \\
	0 & 0 & 0 & 2 \\
	0 & 1 & 0 & 0
	\end{pmatrix}.
$$


5.- Sean 
$$
	\alpha=\left\{ \begin{pmatrix}
	1 & 0 \\
	0 & 0
	\end{pmatrix},\begin{pmatrix}
	0 & 1 \\
	0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 0 \\
	1 & 0
	\end{pmatrix},
	\begin{pmatrix}
	0 & 0 \\
	0 & 1
	\end{pmatrix}\right\},\quad \beta=\{ 1,x,x^{2} \},\quad\text{y}\quad\gamma=\{ 1 \}.
$$
- Define $T:M_{2\times 2}(F)\to M_{2\times 2}(F)$ como $T(A)=A^{t}$. Calcula $[T]_{\alpha}$.
  **Sol:**
  Sea $T(A)=A^{t}$ la transpuesta de una matriz, tenemos que 
  $$
	T(\alpha)=\left\{ \begin{pmatrix}
	1 & 0 \\
	0 & 0
	\end{pmatrix},\begin{pmatrix}
	0 & 0 \\
	1 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 1 \\
	0 & 0
	\end{pmatrix},
	\begin{pmatrix}
	0 & 0 \\
	0 & 1
	\end{pmatrix} \right\},
  $$
  la cual es exactamente la misma base, solo que en otro orden. Nuestra matríz asociada es 
  $$
	[T]_{\alpha}=\begin{pmatrix}
	1 & 0 & 0 & 0 \\
	0 & 0 & 1 & 0 \\
	0 & 1 & 0 & 0 \\
	0 & 0 & 0 & 1
	\end{pmatrix}.
  $$
- Define 
  $$
  	T:P_{2}(R)\to M_{2\times 2}(R)\quad\text{como}\quad T(f(x))=\begin{pmatrix}
	f'(0) & 2f(1) \\
	0 & f''(3)
	\end{pmatrix},
  $$
  dónde $'$ denota la derivada. Calcule $[T]_{\beta}^{\alpha}$.
  **Sol:**
  Tenemos que la imagen de la base $\beta$ bajo $T$ es: 
  $$
	T(\beta)=\left\{ \begin{pmatrix}
	0 & 2 \\
	0 & 0
	\end{pmatrix},\begin{pmatrix}
	1 & 2 \\
	0 & 0
	\end{pmatrix}, \begin{pmatrix}
	0 & 2 \\
	0 & 2
	\end{pmatrix} \right\},
  $$
  y entonces nuestra matriz asociada va a ser 
  $$
	[T]_{\beta}^{\alpha}=\begin{pmatrix}
	0 & 1 & 0 \\
	2 & 2 & 2 \\
	0 & 0 & 0 \\
	0 & 0 & 2
	\end{pmatrix}.
  $$
  
- Define $T:M_{2\times 2}(F)\to F$ como $T(A)=\text{tr}(A)$. Calcule $[T]_{\alpha}^{\gamma}$.
  **Sol:**
  Para la base canónica $\alpha$, tenemos que su imagen bajo $T$ es: 
  $$
	T(\alpha)=\{ 1,0,0,1 \},
  $$
  y como tenemos que la imagen está contenida en $F$, entonces la imagen de la base es la misma matriz asociada. Es decir que 
  $$
	[T]_{\alpha}^{\gamma}=(1,0,0,1).
  $$
  
- Define $T:P_{2}(R)\to R$ como $T(f(x))=f(2)$. Calcule $[T]_{\beta}^{\gamma}$.
  **Sol:**
  La imagen de la base $\beta$ es 
  $$
	T(\beta) = \{ 1,2,4 \},
  $$
  y entonces, al igual que en el inciso anterior, tenemos que 
  $$
	[T]_{\beta}^{\gamma} = (1,2,4).
  $$
  
- Si $A=\begin{pmatrix}1 & -2 \\  0 & 4\end{pmatrix},$ calcula $[A]_{\alpha}$.
  **Sol:** 
  $$
	[A]_{\alpha}=\begin{pmatrix}
	1 \\
	-2 \\
	0 \\
	4
	\end{pmatrix}.
  $$
- Si $f(x)=3-6x+x^{2}$, calcule $[f(x)]_{\beta}$.
  **Sol:** 
  $$
	[f(x)]_{\beta}=\begin{pmatrix}
	3 \\
	-6 \\
	1
	\end{pmatrix}.
  $$
- Para $a\in F$, calcule $[a]_{\gamma}$.
  **Sol:** 
  $$
	[a]_{\gamma}=(a).
  $$


10.- Sea $V$ un espacio vectorial con base ordenada $\beta=\{ v_{1},v_{2},\dots,v_{n} \}$. Define $v_{0}=0$. Por el Teorema 2.6, existe una transformación lineal $T:V\to V$ tal que $T(v_{j})=v_{j}+v_{j-1}$ para $j=1,2,\dots,n$. Calcule $[T]_{\beta}$.
**Sol:**



15.- Sea $V=P(R)$, y para $j\geq 1$ define $T_{j}(f(x))=f^{j}(x)$ la $j$-ésima derivada de $f(x)$. Pruebe que el conjunto $\{ T_{1},T_{2},\dots,T_{n} \}$ es un subconjunto linealmente independiente de $\mathcal{L}(V)$ para cualquier entero positivo $n$.
**Sol:**


### Sección 2.3 Friedberg
###### Teorema 2.10
Sea $V$ un espacio vectorial. Sean $T,U_{1},U_{2}\in\mathcal{L}(V)$. Entonces se satisfacen las siguientes:
- $T(U_{1}+U_{2})=TU_{1}+TU_{2}$ y $(U_{1}+U_{2})T=U_{1}T+U_{2}T$.
- $T(U_{1}U_{2})=(TU_{1})U_{2}$.
- $TI=IT=T$. (Dónde $I$ es la identidad).
- $a(U_{1}U_{2})=(aU_{1})U_{2}=U_{1}(aU_{2})$ para cualquier escalar $a$.
###### Teorema 2.11
Sean $V,W,Z$ espacios vectoriales de dimensión finita con bases ordenadas $\alpha,\beta,\gamma$ respectivamente. Sean $T:V\to W$ y $U:W\to Z$ transformaciones lineales. Entonces 
$$
	[UT]_{\alpha}^{\gamma}=[U]_{\beta}^{\gamma}[T]_{\alpha}^{\beta}.
$$
###### Teorema 2.14
Sean $V,W$ espacios vectoriales de dimensión finita con bases ordenadas $\beta$ y $\gamma$ respectivamente. Sea $T:V\to W$ lineal. Entonces para cada $u\in V$ tenemos que 
$$
	[T(u)]_{\gamma}=[T]_{\beta}^{\gamma}[u]_{\beta}.
$$


3.- Sea $g(x)=3+x$. Sean $T:P_{2}(R)\to P_{2}(R)$ y $U:P_{2}(R)\to R^{3}$ transformaciones lineales definidas respectivamente como 
$$
	T(f(x))=f'(x)g(x)+2f(x)\quad\text{y}\quad U(a+bx+x^{2})=(a+b,c,a-b).
$$
Sean $\beta$ y $\gamma$ las bases ordenadas de $P_{2}(R)$ y $R^{3}$ respectivamente.
- Calcule $[U]_{\beta}^{\gamma},[T]_{\beta}$ y $[UT]_{\beta}^{\gamma}$ directamente. Después use el Teorema 2.11 para verificar su resultado.
- Sea $h(x)=3-2x+x^{2}$. Calcule $[h(x)]_{\beta}$ y $[U(h(x))]_{\gamma}$. Entonces use $[U]_{\beta}^{\gamma}$ de la parte (a) del Teorema 2.14 para verificar sus resultados.


4.- Para cada una de las siguientes, sea $T$ la transformación lineal definida en el Ejercicio 5 de la sección 2.2. Use el Teorema 2.14 para calcular los siguientes vectores.
- $[T(A)]_{\alpha}$ donde $A=\begin{pmatrix}1 & 4 \\  -1 & 6\end{pmatrix}$.
- $[T(f(x))]_{\alpha}$, donde $f(x)=4-6x+3x^{2}$.
- $[T(A)]_{\gamma}$, donde $A=\begin{pmatrix}1 & 3 \\  2 & 4\end{pmatrix}$.
- $[T(f(x))]_{\gamma}$, dónde $f(x)=6-x+2x^{2}$.


8.- Pruebe el Teorema 2.10. Ahora nombra y prueba un resultado más general que involucre transformaciones lineales con dominio diferente a su codominio.

 
12.- Sean $V,W$ y $Z$ espacios vectoriales, y sean $T:V\to W$ y $U:W\to Z$ lineales.
- Pruebe que si $UT$ es intectiva, entonces $T$ es inyectiva. ¿Debe $U$ también ser inyectiva?
- Pruebe que si $UT$ es suprayectiva, entonces $U$ es suprayectiva. ¿Debe $T$ también ser suprayectiva?
- Pruebe que si $U$ y $T$ son inyectivas y suprayectivas, entonces $UT$ también lo es.
