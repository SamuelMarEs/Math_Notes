Usaremos llamadas [[Recursion|recursivas]] para explorar decisiones y construir soluciones. Este método usa [[ArbolesDeRecursion|árboles]] para encontrar una solución.
#### Definición:
La búsqueda con retroceso (backtracking) construye soluciones de forma incremental, explora alternativas y descarta estados parciales que no pueden conducir a una solución válida.

- **Construir**: elegir una alternativa para extendaer la solución parcial.


###### Ejemplo: decisiones
Construir secuencias binarias de longitud 3 sin dos unos consecutivos. Cada nodo muestra un prefijo de la secuencia.

Después de registrar 000, retiramos el último 0, y probamos 001.
Soluciones: 000, 001, 010, 100, 101. El prefijo 11 se descarta sin generar 110 ni 111.

#### Estados y poda
Un estado parcial es 
$$
	X=(x_{1},\dots,x_{k}),\quad 0\leq k\leq n,\quad x_{i}\in S_{i},
$$
donde los conjuntos $S_{i}$ son finitos