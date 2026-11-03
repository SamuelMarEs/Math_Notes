#AlgebraLineal 
1.- Determine si las siguientes afirmaciones son verdaderas o falsas. Suponga que los espacios de producto interno son de dimensión finita.
a) Todo operador lineal tiene un adjunto.
b) Todo operador lineal sobre ${}V{}$ tiene la forma ${}x\to \langle x,y \rangle{}$ para algún ${}y\in V{}$.
c) Para todo operador lineal ${}T{}$ sobre ${}V{}$ y toda base ordenada ${}\beta{}$ de ${}V{}$, tenemos que ${}[T^{*}]_{\beta}=[T]_{\beta}^{*}{}$.
d) El adjunto de un operador lineal es único.
e) Para cualesquiera operadores lineales ${}T{}$ y ${}U{}$ y escalares ${}a,b{}$, 
$$
(aT+bU)^{*}=aT^{*}+bU^{*}.
$$
f) Para toda matriz ${}A{}$ de ${}n\times n{}$, se tiene que ${}(L_{A})^{*}=L_{A^{*}}{}$.
g) Para todo operador lineal ${}T{}$, se tiene que ${}(T^{*})^{*}=T{}$.
**Sol:**
a) Verdadero.
b) Verdadero.
c) Falso.
d) Verdadero.
e) Falso.
f) Verdadero.
g) Verdadero.


2.- En cada caso, encuentre el vector ${}y{}$ tal que ${}g(x)=\langle x,y \rangle{}$ para todo ${}x \in V{}$.
a) ${}V=\mathbb{R}^{3},g(a_{1},a_{2},a_{3})=a_{1}-2a_{2}+4a_{3}{}$.
b) ${}V=\mathbb{C}^{2}, g(z_{1},z_{2})=z_{1}-2z_{2}{}$.
c) ${}V=P_{2}(\mathbb{R}){}$ con ${}\langle f,h \rangle=\int_{0}^{1}f(t)h(t)dt{}$, y ${}g(f)=f(0)+f´(1){}$.
**Sol:**
a) Sea ${}\beta=\{ e_{1},e_{2},e_{3} \}{}$, entonces 
$$
y=g(e_{1})e_{1}+g(e_{2})e_{2}+g(e_{3})e_{3}=e_{1}-2e_{2}+4e_{3}=(1,-2,4).
$$
b) Sea $\beta=\{ e_{1},e_{2} \}{}$, entonces tenemos que 
$$
y=\overline{g(e_{1})}e_{1}+\overline{g(e_{2})}e_{2}=e_{1}-2e_{2}=(1,-2).
$$
c) Sea ${}\beta=\{ 1,x,x^{2} \}{}$

3.- Para cada uno de los siguientes, calcula ${}T^{*}{}$ en el vector dado.
a) ${}V=\mathbb{R}^{2},T(a,b)=(2a+b,a-3b),x=(3,5){}$.
b) ${}V=\mathbb{C}^{2},T(z_{1},z_{2})=(2z_{1}+iz_{2},(1-i)z_{1}),x=(3-i,1+2i){}$.
c) ${}V=P_{1}(\mathbb{R}){}$ con ${}\langle f,g \rangle=\int_{-1}^{1}f(t)g(t)dt{}$, ${}T(f)=f’+3f{}$, ${}f(t)=4-2t{}$.

10.- Sea ${}T{}$ un operador lineal sobre ${}V{}$ un espacio de producto interno. Pruebe que ${}\lVert T(x) \rVert=\lVert x \rVert{}$ para todo ${}x{}$ si y sólo si ${}\langle T(x),T(y) \rangle=\langle x,y \rangle{}$ para todo ${}x,y\in V{}$. *Hint*: use el ejercicio 20 de la sección 6.1.

12.- Sea ${}V{}$ un espacio de producto interno, y sea ${}T{}$ un operador lineal sobre ${}V{}$. pruebe los siguientes resultados:
a) ${}R(T^{*})^{\perp}=N(T){}$.
b) Si ${}V{}$ es de dimensión finita, entonces ${}R(T^{*})=N(T)^{\perp}{}$. *Hint*: Use el ejercicio 13(c) de la sección 6.2.

20.- Para cada uno de los siguientes conjuntos de datos, use aproximación por mínimos cuadrados para encontrar la mejor aproximación lineal y cuadrática. Calcule el error en ambos casos.
a) ${}\{ (-3,9),(-2,6),(0,2),(1,1) \}{}$
b) ${}\{ (1,2),(3,4),(5,7),(7,9),(9,12) \}{}$
c) ${}\{ (-2,4),(-1,3),(0,1),(1,-1),(2,-3) \}{}$
