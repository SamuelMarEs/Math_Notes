#AlgebraLineal
Para trabajar el producto interno de [[ProductoInterno|Frobenius]], definimos la matriz adjunta de ${}A{}$ como 
$$
(A_{ij}^{*})=\overline{(A_{ji})},
$$
es decir, como la matriz transpuesta conjugada. Para matrices sobre los reales, esta es únicamente la matriz transpuesta.
Sea ${}T{}$ un operador lineal sobre un espacio de producto interno ${}V{}$, definimos el operador adjunto de ${}T{}$, cuya representación matricial respecto a una base ${}\beta{}$ es ${}[T]_{\beta}^{*}{}$.

Observemos primero que podemos definir una operación lineal ${}g:V\to F{}$ de la forma ${}g(x)=\langle x,y\rangle{}$ para ${}y{}$ un vector fijo. Veremos que, si ${}V{}$ es de dimensión finita, entonces todas las transformaciones lineales de ${}V{}$ en ${}F{}$ se pueden expresar de esta forma:
#### Teorema 6.8
Sea ${}V{}$ un espacio de producto interno de dimensión finita sobre un campo ${}F{}$, y sea ${}g:V\to F{}$ una transformación lineal. Entonces existe un único vector ${}y\in V{}$ tal que ${}g(x)=\langle x,y\rangle{}$ para todo ${}x\in V{}$.
##### Demostración:
Sea ${}\beta=\{ v_{1},\dots,v_{n} \}{}$ una base ortonormal de ${}V{}$, y sea 
$$
y=\sum_{i=1}^{n}\overline{g(v_{i})}v_{i}.
$$
Definamos ${}h:V\to F{}$ como ${}h(x)=\langle x,y\rangle{}$, tenemos que para ${}1\leq j\leq n{}$:
$$
\begin{aligned}
h(v_{j})&=\langle v_{j}, y\rangle=\langle v_{j}, \sum_{i=1}^{n}\overline{g(v_{i})}v_{i}\rangle \\
&=\sum_{i=1}^{n}g(v_{i})\langle v_{j},v_{i}\rangle \\
&=\sum_{i=1}^{n}g(v_{i})\delta_{ji}=g(v_{j}).
\end{aligned}
$$
Para demostrar la unicidad, basta ver que, de existir otro ${}y’{}$, se tendría que ${}\langle x,y\rangle=\langle x,y’\rangle{}$ para todo ${}x{}$, por lo tanto ${}y=y’.\quad\square$

Volviendo al tema del operador adjunto, tenemos el siguiente teorema para definirlo: 
#### Teorema 6.9
Sea ${}V{}$ un espacio de producto interno de dimensión finita, y sea ${}T{}$ un operador lineal sobre ${}V{}$. Entonces existe una única función ${}T^{*}:V\to V{}$ tal que ${}\langle T(x), y \rangle=\langle x,T^{*}(y) \rangle{}$ para todo ${}x,y\in V{}$. Más aún, ${}T^{*}{}$ es lineal.
##### Demostración:
Sea ${}y\in V{}$. Definamos ${}g:V\to F{}$ como ${}g(x)=\langle T(x),y \rangle{}$ para todo ${}x \in V{}$. No es difícil de ver que ${}g{}$ es lineal, y aplicando el teorema anterior, tenemos que existe ${}y’{}$ tal que ${}g(x)=\langle x, y’ \rangle=\langle T(x),y \rangle{}$ para toda ${}x \in V{}$. Si definimos a ${}T^{*}:V\to V{}$ como ${}T^{*}(y)=y’{}$, entonces tenemos que ${}\langle T(x), y \rangle=\langle x,T^{*}(y) \rangle{}$. No es complicado ver que ${}T^{*}{}$ es lineal, y la unicidad se demuestra tomando otra ${}U:V\to V{}$ que satisfaga ${}\langle T(x),y \rangle=\langle x,U(y) \rangle{}$, de modo que tendríamos ${}\langle x,T^{*}(y) \rangle=\langle x,U(y) \rangle{}$, por lo que ${}T^{*}=U.\quad\square{}$

Este teorema nos da la definición del operador adjunto como aquel que satisface que ${}\langle T(x),y \rangle=\langle x,T^{*}(y) \rangle{}$ para todo ${}x,y\in V{}$, y no es difícil mostrar que ${}\langle x,T(y) \rangle=\langle T^{*}(x),y \rangle{}$. Si ${}V{}$ es un espacio vectorial de dimensión infinita, entonces no podemos garantizar la existencia del operador adjunto, aunque se mantiene la unicidad y linearidad.
Pero, ¿cómo podemos encontrar este operador adjunto? El siguiente teorema nos da una herramienta para encontrarlo:
#### Teorema 6.10
Sea ${}V{}$ un espacio de producto interno de dimensión finita, y sea ${}\beta{}$ una base ortonormal de ${}V{}$. Si ${}T{}$ es un operador lineal sobre ${}V{}$, entonces 
$$
[T^{*}]_{\beta}=[T]_{\beta}^{*}.
$$
Es decir, la matriz asociada al operador adjunto, es la matriz adjunta de la matriz asociada al operador original.
##### Demostración:
Sean ${}A=[T]_{\beta}{}$, ${}B=[T^{*}]_{\beta}{}$, y ${}\beta=\{ v_{1},\dots,v_{n} \}{}$. Entonces tenemos que 
$$
B_{ij}=\langle T^{*}(v_{j}),v_{i} \rangle =\overline{\langle v_{i},T^{*}(v_{j}) \rangle }=\overline{\langle T(v_{i}),v_{j} \rangle }=\overline{A_{ji}}=(A^{*})_{ij}.
$$
Por lo tanto se tiene que ${}B=A^{*}.\quad\square{}$

#### Propiedades (Teo 6.11)
Sea ${}V{}$ un espacio de producto interno, y sean ${}T{}$ y ${}U{}$ operadores lineales cuyos operadores adjuntos existen. Entonces 
a) ${}(T+U)^{*}=T^{*}+U^{*}{}$;
b) ${}(cT)^{*}=\overline{c}T^{*}{}$ para todo ${}c\in F{}$;
c) ${}(TU)^{*}=U^{*}T^{*}{}$;
d) ${}T^{**}=T{}$;
e) ${}I^{*}=I{}$.
Estas mismas propiedades se extienden a matrices adjuntas.
