#### Estructura
~~~
{P}: precondición del ciclo
Repetir mientras G:
	Ejecutar cuerpo C
{Q}: postcondición del ciclo
~~~
La condición $G$ se llama **guarda**. Si $G$ es verdadera, se ejecuta el ciclo. Si es falsa, se sale del ciclo. El cuerpo puede ejecutarse cero veces.
En la notación de [[CorreccionAlgoritmica|Horae]], 
$$
	\{ P \}\text{ mientras }G\text{ ejecutar }C\{ Q \}.
$$

#### Invariante de ciclo
La invariante es un predicado (condición) $I$ sobre el estado que se conserva al ejecutar el cuerpo bajo la guarda: 
$$
	\{ I\wedge G \}C\{ I \}.
$$
Si $I$ y $G$ se cumplen antes de una iteración y el cuerpo termina, $I$ vuelve a cumplirse después. Por eso es la invariante.

#### Inducción
Sea $I(k)$ la afirmación de que el estado después de $k$ iteraciones completas satisface el invariante $I$.
- **Base:** $I(0)$; se cumple antes de la primera iteración.
- **Paso inductivo:** para cada entero $k\geq 0$, si se cumplen $I(k)$ y la guarda $G$, una iteración completa establece que $I(k+1)$ (se cumple la invariante para la siguiente iteración).
Por inducción, el invariante vale después de cada número de iteraciones que se ejecuta. $k$ cuenta las iteraciones, no debe ser una variable del programa.

#### Regla del ciclo
Si es válida $\{ I\wedge G \}C\{ I \}$, entonces es válida: 
$$
	\{ I \}\text{ mientras }G\text{ ejecutar }C\{ I\wedge \neg G \}.
$$
Si el ciclo termina, la inducción garantiza $I$, y la condición de salida garantiza $\neg G$. Para conectar esta regla con una especificación de precundiciones y postcondiciones, necesitamos:
$$
	P\implies I,\quad I\wedge \neg G\implies Q.
$$
Una invariante útil debe poder establecerse al inicio y aportar suficiente información para obtener $Q$ al salir.

#### Teorema del invariante
Sea un ciclo con guarda $G$, precondición $P$ y postcondición $Q$. El ciclo es totalmente correcto si se justifican estas cuatro propiedades:
1. Propiedad base: $P$ implica $I(0)$ antes de la primera iteración.
2. Propiedad inductiva: para cada entero $k\geq 0$, si $I(k)$ y $G$ son verdaderas, una iteración completa establece $I(k+1)$.
3. Eventual falsedad de la guarda: la ejecución llega a una evaluación con $G$ falsa en un número finito de pasos.
4. Corrección de la postcondición: si $N$ es el menor número de iteraciones tras las cuales la guarda es falsa, entonces $I(N)\wedge \neg G\implies Q$.

##### Ejemplo:
Verificaremos un ciclo que incrementa $i$ desde cero hasta $n$.
```pseudocódigo
Entrada: n entero no negativo
Inicializar i <- 0
Repetir mientras i < n:
	i <- i + 1
```
Antes del ciclo: $P:n\in\mathbb{Z}_{\geq 0}\wedge i=0.$
Guarda $G: i<n$.
Postcondición: $Q:i=n$.
Invariante: $I(k):i=k\wedge 0\leq k\leq n.$

Verificando el teorema, tenemos:
1. Propiedad base. Al inicio, $i=0$ y $n\geq 0$, por lo tanto se cumple $I(0)$.
2. Propiedad inductiva. Si $I(k)$ y $G$ son verdaderas, $k<n$. Después del incremento, $i=k+1$ y $0\leq k+1\leq n$, por lo tanto se cumple $I(k+1)$.
3. Eventual falsedad de la guarda. Tras $n$ iteraciones, $i=n$, por lo que $i<n$ es falsa. Cada iterción contiene una sola asignación.
4. Postcondición. Al salir, $\neg G$ implica $i\geq n$. El invariante garantiza $i\leq n$. Por lo tanto, $i=n$.

#Algoritmos