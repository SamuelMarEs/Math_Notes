Usaremos llamadas [[Recursion|recursivas]] para explorar decisiones y construir soluciones. Este método usa [[ArbolesDeRecursion|árboles]] para encontrar una solución.
#### Definición:
La búsqueda con retroceso (backtracking) construye soluciones de forma incremental, explora alternativas y descarta estados parciales que no pueden conducir a una solución válida.

- **Construir**: elegir una alternativa para extender la solución parcial.
- **Podar**: descartar una posibilidad que ya contradice las restricciones.
- **Retroceder**: restaurar el estado anterior para probar otra alternativa, también después de encontrar una solución.
El proceso del algoritmo se ve algo de la forma:
Elegir -> explorar -> deshacer.


###### Ejemplo: decisiones
Construir secuencias binarias de longitud 3 sin dos unos consecutivos. Cada nodo muestra un prefijo de la secuencia.
![[BusquedaRetroceso]]
Después de registrar 000, retiramos el último 0, y probamos 001.
Soluciones: 000, 001, 010, 100, 101. El prefijo 11 se descarta sin generar 110 ni 111.

#### Estados y poda
Un estado parcial es 
$$
	X=(x_{1},\dots,x_{k}),\quad 0\leq k\leq n,\quad x_{i}\in S_{i},
$$
donde los conjuntos $S_{i}$ son finitos. En el ejemplo anterior, $S_{i}=\{ 0,1 \}$.
Admisibilidad de $P(X)$:
- Si $P(X)$ es falso, ninguna extensión de $X$ debe ser una solución válida. Podemos podar sin perder soluciones.
- Si $P(X)$ es verdadero y $k<n$, todavía hay decisiones por explorar; esto no garantiza encontrar una solución.
- Para $k=n$, $P(X)$ comprueba que la solución completa cumple las restricciones.
Sin poda, el número de candidatos completos es 
$$
	\prod_{i=1}^{n}\lvert S_{i} \rvert ;\quad \text{si todos tienen $m$ elementos, son $m^{n}$}.
$$
La poda puede evitar trabajo, pero no garantiza evitar un peor caso exponencial.

###### Ejemplo de algoritmo
