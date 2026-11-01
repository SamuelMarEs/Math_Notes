#Calculo 
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
${}{}$