¿Qué significa que un algoritmo sea correcto? 
Cada algoritmo se diseña para cumplir una tarea específica.
Decimos que un algoritmo es correcto sí, para cada entrada permitida por su especificación, termina y produce una salide que cumple lo especificado.
La **corrección** depende de una especificación.

##### Definición:
El ***estado*** es la asignación de un valor actual a cada variable del programa.

Por ejemplo, en el estado $x=3,y=6$: 
$$
	x\geq 0, y=2x
$$
son afirmaciones verdaderas. 
Después de ejecutar $x=x+1$, el estado es $x=4,y=6$, tenemos que la primera condición sigue siendo verdadera, pero la segunda no, pues $y\neq 2x$.

##### Definición:
Una ***precondición*** es una propiedad que suponemos verdadera antes de ejecutar el algoritmo.
Una ***postcondición*** es la propiedad que debe cumplirse al culminar el algoritmo.

Por ejemplo, para la división entera: 
$$
	P:a,d\in\mathbb{Z},\quad a\geq 0, b\geq 0,
$$
es una precondición.

#### Correción parcial y total
##### Definición
Para toda entrada que satisface la precondición, si el algoritmo termina, entonces su estado final satisface la postcondición. Esta es una ***corrección parcial***.

##### Definición
Para toda entrada que satisface la precondición, el algoritmo **termina** y su estado final satisface la postcondición. Esta es una ***corrección parcial***.

La condición parcial no garantiza que la ejecución del algoritmo culmine.

#### Tripletas de Horae
Una espacificación formada por una precondición $P$, un fragmento de código $C$ y una postcondición $Q$: 
$$
	\{ P \}C\{ Q \}.
$$
En este caso, la tripleta representa [[Clases|corrección parcial]].Es válida si, desde cualquier estado que satisface $P$, toda ejecución de $C$ que dermina deja un estado que satisface $Q$.
Por ejemplo 
$$
	\{ x<4 \} x=x+1 \{ x<5 \}
$$
**Estado inicial**: $x=1$, que satisface la precondición $x<4$.
**Instrucción**: $x=x+1$.
**Estado final**: $x=2$, que satisface la postcondición $x<5$.
La tripleta vale siempre que valga la precondición.

#### Aserciones
Afirmación sobre los valores de las variables en un punto concreto de la ejecución. 
$$
	\begin{matrix}
	\{ A_{1} \} & \text{Precondición del algoritmo} \\
	C_{1} & \text{Primer fragmento de instrucciones} \\
	\{ A_{2} \} & \text{Aserción intermedia} \\
	C_{2} & \text{Siguiente fragmento de instrucciones} \\
	\vdots & \vdots \\
	\{ A_{k-1} \} & \text{Última aserción intermedia} \\
	C_{k-1} & \text{Último fragmento de instrucciones} \\
	\{ A_{k} \} & \text{Postcondición del algoritmo}
	\end{matrix}
$$
Cada par de aserciones **sucesivas** funciona como precondición y postcondición del fragmento situado entre ellas.

Para cada $i=1,2,\dots,k-1$, debemos demostrar:
$$
   \{ A_{i} \}C_{i}\{ A_{i+1} \}.
$$
Si $A_{i}$ es verdadera, y el fragmento $C_{i}$ termina, entonces $A_{i+1}$ debe ser verdadera. 
Debemos justificar *todas las transiciones*.

#### Expresiones
Combinaciones de valores, variables y operaciones que se evalúa para obtener un valor, como $x+1$ o $2x+y$.

Decimos que una expresión está ***bien definida*** si puede evaluarse para los valores considerados. Por ejemplo $x+1$ esta definida para cualquier entero $x$, en cambio, $1 / x$ requiere $x\neq 0$.
Decimos que es ***sin efectos secundarios*** si evaluarla no modifica el estado del programa. Por ejemplo, si $x=4$, evaluar $x+1$ produce 5, pero no estamos alterando el estado de $x$, que sigue valiendo 4. Al ejecutar $x\leftarrow x+1$, primero evaluamos la expresión, y luego modificamos el estado.

#### Sustitución
Denotamos $Q[E / x]$ que se llama como "la fórmula $Q$, sustituyendo $x$ por $E$".

#### Regla de la asignación
Para una expresión $E$ bien definida y sin efectos secundarios: 
$$
	\{ Q[E / x] \}x\leftarrow E\{ Q \}.
$$
##### Ejemplo
Queremos ejecutar $x\leftarrow x+1$ y garantizar que después se cumpla $x>5$.
**Valor anterior y valor nuevo**
Sea $a$ el valor de $x$ antes de la asignación, entonces
1. Antes, $x$ vale $a$.
2. Calculamos $a+1$.
3. Guardamos el resultado: ahora $x$ vale $a+1$.
**Condición necesaria antes**
Para que el valor nuevo sea mayor que cinco necesitamos: 
$$
	a+1>5\Longleftrightarrow a>4.
$$
En la regla, $Q$ es $x>5$, y $E$ es $x+1$. Al sustituir obtenemos que $Q[E / x]:x+1>5$. (La regla $Q$ ($x>5$) sustituyendo $x$ por $E$ ($x+1$)).
Entonces tenemos 
$$
	\{ x>4 \}x\leftarrow x+1\{ x>5 \}
$$
nuestra tripleta de Horae. Notese que $Q[E / x]=\{ x+1>5 \}=\{ x>4 \}$.




#Algoritmos 