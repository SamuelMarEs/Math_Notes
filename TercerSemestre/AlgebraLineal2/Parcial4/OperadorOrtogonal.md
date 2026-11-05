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
##### Demostración:
${}(a)\implies(b){}$

${}(b)\implies(c){}$

${}(c)\implies(d){}$

${}(d)\implies(e){}$. Esta implicación es OBVIA.

${}(f)\implies(a){}$

#### Corolario 1:
Sea ${}T{}$ un operador lineal en un espacio vectorial ${}V{}$ sobre ${}\mathbb{R}{}$. Entonces ${}T{}$ es [[OperadorHermitiano|auto-adjunto]] y ortogonal si y sólo si existe una base ${}\beta{}$ de ${}V{}$ formada por eigenvectores, con eigenvalores ${}1,-1{}$.

#### Corolario 2:
Un operador lineal ${}T{}$ en un espacio vectorial ${}V{}$ sobre ${}\mathbb{C}{}$ es unitario si y sólo si existe una base ortonormal ${}\beta{}$ de ${}V{}$ formada por eigenvectores, de modo que sus eigenvalores asociados tienen norma 1 (i.e. ${}\lvert \lambda_{i} \rvert=1{}$).

#### Definición:
Sea ${}L{}$ un subespacio de dimensión 1 en ${}\mathbb{R}^{2}{}$ (aunque chance se generaliza a ${}\mathbb{R}^{n}{}$). Podemos ver a ${}L{}$ como una recta sobre el plano. Un operador lineal ${}T{}$ se llama la reflexión de ${}\mathbb{R}^{2}{}$ respecto a ${}L{}$ si ${}T(x)=x{}$ para todo ${}x \in L{}$, y ${}T(x)=-x{}$ para todo ${}x \in L^{\perp}{}$.

#### Definición:
Una matriz ${}A{}$ es unitaria equivalente a ${}D\in M_{n\times n}(\mathbb{C}){}$ (o ortogonal equivalente a ${}D\in M_{n\times n}(\mathbb{R}){}$) si existe una matriz ${}Q{}$ tal que 
$$
D=Q^{-1}AQ.
$$

