#Algoritmos 

Un algoritmo recursivo resuelve un problema llamándolse a sí mismo sobre una o más instancias más pequeñas del mismo problema. La idea es reducir el problema hasta llegar a un caso que podamos resolver directamente. 
$$
	\text{problema grade}\to\text{problemas pequeños}\to\text{caso base}.
$$
Todo algoritmo recursivo debe dejar claras tres partes:
- **Caso base:** instancia que se resuleve directamente, sin hacer una llamada.
- **Caso recursivo:** reducción del problema original a una o más instancias del mismo tipo.
- **Progresión:** debe haber un progreso, es decir que debe "avanzar" y no atorarse para siempre.

Hay dos tipos principales 
- **Directa:** Una función se llama a sí misma.
- **Indirecta:**: Una función llama a otra función que, directa o indirectamente, vuelve a la original.

##### Ejemplo:
El factorial de un entero $n\geq 0$ se define por:
$$
	n! = \begin{cases}
	1,\quad n=0 \\
	n\cdot(n-1)!\quad n>0.
	\end{cases}
$$
**Caso base** $0! = 1$, **caso recursivo** llama $n!$ usando $(n-1)!$, **progresión** pues $n-1<n$.

#### Recursión e iteración

| Recursión                                                                  | Iteración                                                                 |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Expresa naturalmente problemas definidos en términos de sí mismos.         | Suele evitar el costo extra de las llamadas a función.                    |
| Es útil en árboles, búsqueda, divide y vencerás y definiciones inductivas. | Suele ser már directa cuando el problema es una repetición lineal.        |
| Puede aumentar complejidad si se usa sin cuidado.                          | Puede requerir variables auxiliares que oculten la estructura matemática. |
La recursión se conecta naturalmente con las ideas de [[CorreccionAlgoritmica|corrección]] tanto parcial como total.
- Parcial: si la función termina, entonces devuelve el resultado.
- Total: toda cadena de llamadas recursiva llega al caso base en un número finito de pasos

#### Divide y vencerás
Es una estrategia de diseño algorítmico que resuelve un problema descomponiéndolo recursivamente:
- **Dividir:** separar el problema en subproblemas más pequeños del mismo tipo.
- **Conquistar:** resolver los subproblemas de forma recursiva (o directa si son pequeños).
- **Combinar:** unir las soluciones parciales para formar la solución global.
$$
	T(n)=aT\left( \frac{n}{b} \right)+f(n),\quad T(1)=\Theta(1).
$$
$a$ es el número de subproblemas en cada división $a\geq 1$, $b$ es el factor de reducción de tamaño $b>1$, y $f(n)$ es el costo no recursivo de dividir y combinar.
##### Ejemplo: potenciación entera
Dados $x\in\mathbb{R}$ y un entero $n\geq 0$, calcular la potencia $x^{n}$.
El enfoque iterativo es 
$$
	x^{n}=x\cdot x\cdot\dots \cdot x
$$
que requiere $n-1$ operaciones, es decir $T(n)\in \Theta(n)$.
Idea de divide y vencerás: aprovechamos propiedades algebraicas:
$$
	x^{n}=\begin{cases}
	1,\quad n=0 \\
	(x^{n / 2})^{2},\quad n\text{ par} \\
	x\cdot (x^{n / 2})^{2},\quad n\text{ impar}.
	\end{cases}
$$
~~~Python
def potencia(x, n):
	if n == 0:
		return 1
	mitad = potencia(x, n // 2)
	if n % 2 == 0:
		return mitad * mitad
	else:
		return x * mitad * mitad
~~~
**Dividir:** calcular `n//2` en tiempo $\Theta(1)$.
**Conquistar:** $a=1$ subproblema de tamaño `n/2` $(b=2)$.
**Combinar:** a lo sumo 2 multiplicaciones en tiempo $\Theta(1)$.