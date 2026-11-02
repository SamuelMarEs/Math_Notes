#AlgebraLineal 
Sabemos que, para que un operador sobre ${}V{}$ sea diagonalizable, es necesario y suficiente que ${}V{}$ tenga una base de eigenvectores asociados al operador. Si trabajamos con ${}V{}$ un espacio de producto interno, es natural querer buscar una base ortonormal de ${}V{}$ compuesta de eigenvectores, y preguntarnos que condiciones son necesarias para que esta base exista. A continuación vemos algunos resultados importantes para responder estas dudas.
#### Lema
Sea ${}T{}$ un operador lineal sobre un espacio de producto interno de dimensión finita ${}V{}$. Si ${}T{}$ tiene un eigenvector, entonces también ${}T^{*}{}$.
##### Demostración:
Supongamos que ${}v{}$ es un eigenvector de ${}T{}$ con eigenvalor ${}\lambda{}$. Entonces para cualquier ${}x \in V{}$, 
$$
0=\langle 0,x \rangle =\langle (T-\lambda I)(v),x \rangle =\langle v,(T-\lambda)^{*}(x) \rangle =\langle v,(T^{*}-\overline{\lambda}I)(x) \rangle ,
$$
y por lo tanto ${}v{}$ es ortogonal a la imagen de ${}T^{*}-\overline{\lambda}I{}$, por lo que este operador no puede ser suprayectivo ni inyectivo, y por lo tanto su espacio nulo es distinto del vector cero, y cualquier vector no cero cuya imagen sea el cero es un eigenvector de ${}T^{*}{}$ con eigenvalor ${}\overline{\lambda}.\quad\square{}$

#### Teorema de Schur (6.14)
Sea ${}T{}$ un operador lineal sobre un espacio de producto interno de dimensión finita ${}V{}$. Supongamos que el polinomio característico de ${}T{}$ es descomponible. Entonces existe una base ortonormal ${}\gamma{}$ de ${}V{}$ tal que la matriz ${}[T]_{\gamma}{}$ es triangular superior.
##### Demostración:
Por un ejercicio que o no recuerdo o no hice (12(a) sección 5.2, revisarlo luego, o sea nunca), existe una base ordenada ${}\beta=\{ w_{1},\dots,w_{n} \}{}$ tal que ${}[T]_{\beta}{}$ es triangular superior. Si aplicamos el proceso Gram-Schmidt para obtener una base ortogonal ${}\beta’=\{ v_{1},\dots,v_{n} \}{}$, y definimos 
$$
S_{k}=\{ w_{1},\dots,w_{k} \},S’_{k}=\{ v_{1},\dots,v_{k} \},\quad \text{para }1\leq k\leq n,
$$
entonces ${}\mathrm{span}(S_{k})=\mathrm{span}(S’_{k}){}$ para toda ${}k{}$, y por algún detalle del mismo ejercicio, esto nos lleva a que ${}[T]_{\beta’}{}$ es también una matriz triangular, y normalizarla a ${}\gamma=\{ z_{1},\dots,z_{n} \}{}$ se mantiene tal que ${}[T]_{\gamma}{}$ es triangular superior. ${}\quad\square{}$

Volviendo al tema de encontrar una base ortonormal de vectores. Si suponemos que esa base existe, y la llamamos ${}\beta{}$, entonces ${}[T]_{\beta}{}$ es una matriz diagonal, y por lo tanto ${}[T^{*}]_{\beta}=[T]_{\beta}^{*}{}$ también es una matriz diagonal, y dado que las matrices diagonales son conmutativas, tenemos que ${}TT^{*}=T^{*}T{}$ si ${}V{}$ posee una base ortonormal de eigenvectores de ${}T{}$.
Esto nos lleva a la definición del nombre de la nota:
#### Definición:
Sea ${}V{}$ un espacio de producto interno, y sea ${}T{}$ un operador lineal sobre ${}V{}$. Decimos que ${}T{}$ es ***normal*** si ${}TT^{*}=T^{*}T{}$. Una matriz ${}A{}$ de ${}n\times n{}$ sobre los complejos o los reales es normal si ${}AA^{*}=A^{*}A{}$.
#### Propiedades (Teo 6.15)
Sea ${}V{}$ un espacio de producto interno, y sea ${}T{}$ un operador normal sobre ${}V{}$. Entonces las siguientes propiedades son ciertas:
a) ${}\lVert T(x) \rVert=\lVert T^{*}(x) \rVert{}$ para todo ${}x \in V{}$;
b) ${}T-cI{}$ es normal para todo ${}c\in F{}$;
c) Si ${}x{}$ es un eigenvector de ${}T{}$ correspondiente al eigenvalor ${}\lambda{}$, entonces ${}x{}$ también es un eigenvector de ${}T^{*}{}$ correspondiente al eigenvalor ${}\overline{\lambda}{}$. Es decir, si ${}T(x)=\lambda x{}$, entonces ${}T^{*}(x)=\overline{\lambda}x{}$;
d) Si ${}\lambda_{1}{}$ y ${}\lambda_{2}{}$ son eigenvalores distintos de ${}T{}$ con sus correspondientes eigenvectores ${}x_{1}{}$ y ${}x_{2}{}$, entonces ${}x_{1}{}$ y ${}x_{2}{}$ son ortogonales.
##### Demostración:
a) Para todo ${}x \in V{}$, tenemos que 
$$
\lVert T(x) \rVert ^{2}=\langle T(x),T(x) \rangle =\langle T^{*}T(x),x \rangle =\langle TT^{*}(x),x \rangle =\langle T^{*}(x),T^{*}(x) \rangle =\lVert T^{*}(x) \rVert ^{2}. 
$$
b) Sea ${}c\in F{}$, queremos mostrar que ${}(T-cI)^{*}(T-cI)=(T-cI)(T-cI)^{*}{}$. Sabemos que tanto ${}T{}$ como ${}cI{}$ son normales para cualquier constante ${}c{}$ (esto pues ${}I{}$ es diagonal y su adjunto es ella misma). Además, por ser lineales, tenemos que 
$$
\begin{aligned}
(T-cI)^{*}(T-cI)&=T^{*}(T-cI)-\overline{c}I(T-cI) \\
&=T^{*}T-cT^{*}I-\overline{c}IT+\overline{c}cII
\end{aligned}
$$ 

c) Supongamos que ${}T(x)=\lambda x{}$ para algún ${}x \in V{}$. Sea ${}U=T-\lambda I{}$, entonces ${}U(x)=0{}$, y por el inciso anterior, ${}U{}$ es normal, por lo tanto 
$$
0=\lVert U(x) \rVert =\lVert U^{*}(x) \rVert =\lVert (T^{*}-\overline{\lambda}I)(x) \rVert =\lVert T^{*}(x)-\overline{\lambda}x \rVert .
$$
Por lo tanto tenemos que ${}T^{*}(x)=\overline{\lambda}x{}$.

d) Sean ${}\lambda_{1}{}$ y ${}\lambda_{2}{}$ eigenvalores distintos de ${}T{}$ con eigenvectores correspondientes ${}x_{1}{}$ y ${}x_{2}{}$. Entonces, por el inciso (c), tenemos que 
$$
\lambda_{1}\langle x_{1},x_{2} \rangle =\langle \lambda_{1}x_{1},x_{2} \rangle =\langle T(x_{1}),x_{2} \rangle =\langle x_{1},T^{*}(c_{2}) \rangle =\langle x_{1},\overline{\lambda_{2}}x_{2} \rangle =\lambda_{2}\langle x_{1},x_{2} \rangle. 
$$
Dado que ${}\lambda_{1}\neq \lambda_{2}{}$, la única forma posible para que se cumpla la igualdad es si ${}\langle x_{1},x_{2} \rangle=0{}$, por lo tanto son ortogonales. ${}\quad\square{}$
