#AlgebraLineal 
Sabemos que, para que un operador sobre ${}V{}$ sea diagonalizable, es necesario y suficiente que ${}V{}$ tenga una base de eigenvectores asociados al operador. Si trabajamos con ${}V{}$ un espacio de producto interno, es natural querer buscar una base ortonormal de ${}V{}$ compuesta de eigenvectores, y preguntarnos que condiciones son necesarias para que esta base exista. A continuación vemos algunos resultados importantes para responder estas dudas.
#### Lema
Sea ${}T{}$ un operador lineal sobre un espacio de producto interno de dimensión finita ${}V{}$. Si ${}T{}$ tiene un eigenvector, entonces también ${}T^{*}{}$.
##### Demostración:
Supongamos que ${}v{}$ es un eigenvector de ${}T{}$ con eigenvalor ${}\lambda{}$. Entonces para cualquier ${}x \in V{}$, 
$$
0=\langle 0,x \rangle =\langle (T-\lambda I)(v),x \rangle =\langle v,(T-\lambda)^{*}(x) \rangle =\langle v,(T^{*}-\overline{\lambda}I)(x) \rangle ,
$$
y por lo tanto ${}v{}$ es ortogonal a la imagen de ${}T^{*}-\overline{\lambda}I{}$