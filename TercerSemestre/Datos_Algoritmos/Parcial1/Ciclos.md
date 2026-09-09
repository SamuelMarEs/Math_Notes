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


#Algoritmos