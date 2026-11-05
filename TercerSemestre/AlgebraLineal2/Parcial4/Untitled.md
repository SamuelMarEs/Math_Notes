#AlgebraLineal 
#### Definición:
Sea ${}T{}$ un [[OperadoresNormales|operador normal]] tal que ${}T^{*}T=TT^{*}=I{}$, entonces decimos que ${}T{}$ es un ***operador unitario*** (si es sobre ${}\mathbb{C}{}$), o ***ortogonal*** (si es sobre ${}\mathbb{R}{}$).

Si se trata de operadores lineales (i.e. matrices de ${}n\times n{}$), entones básicamente estamos definiendo un operador lineal cuyo adjunto es su inverso.

#### Teorema 6.18
Sea ${}T{}$ un operador lineal sobre un espacio de producto interno ${}V{}$ de dimensión finita. Entonces las siguientes afirmaciones son equivalentes:
a) ${}TT^{*}=I{}$.
b) ${}T^{*}T=I{}$.
c) ${}\langle T(x),T(y) \rangle=\langle x,y \rangle{}$ para todo ${}x,y\in V{}$.
d) Si ${}\beta{}$ es una base ortonormal de ${}V{}$, entonces ${}T(\beta){}$ es una base ortonormal de ${}V{}$.
e) Existe una base ortonormal ${}\beta{}$ de ${}V{}$ tal que ${}T(\beta){}$ es una base ortonormal de ${}V{}$.
f) ${}\lVert T(x) \rVert=\lVert x \rVert{}$ para todo ${}x \in V{}$.
Es decir, todas las condiciones anteriores son equivalentes a la definición de un operador ortogonal/unitario.