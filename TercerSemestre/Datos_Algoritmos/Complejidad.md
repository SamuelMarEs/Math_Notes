Si queremos resolver un problema, pueden existir distintos algoritmos que nos sirvan.
¿Cómo elegimos entre estos algoritmos?
En general hay dos enfoques:
- Empírico, consiste en programar las opciones y probarlas en distintos casos.
- Teórico, consiste en determinar matemáticamente la cantidad de recursos necesarios (tiempo de cómputo y espacio de almcenamiento).
---
##### Tabla de comparación de complejidades

| Entrada $n$ | Logarítmica | Lineal | Cuadrática | Exponencial |
| ----------- | ----------- | ------ | ---------- | ----------- |
| 10          | 3           | 10     | 100        | 1024        |
| 100         | 7           | 100    | 10000      | $100!$      |
| 1000        | 10          | 1000   | $10^{6}$   | $1000!$     |
| 10000       | 14          | 10000  | $10^{8}$   | $10000!$    |

---
### Modelo RAM
Usamos una computadora idealizada para contar operaciones de forma consistente, llamada ***Random Access Machine (RAM)***. Este modelo es una [[TDA|abstracción]]. 

| Supuesto del modelo RAM                           | En una máquina real                               |
| ------------------------------------------------- | ------------------------------------------------- |
| Operación básica = un paso                        | Algunas operaciones cuestan más que otras         |
| Ciclos y subrutinas se descomponen en operaciones | Compilador y paralelismo alteran los tiempos      |
| Acceso a memoria = un paso                        | La jerarquía de memoria cambia el costo de acceso |
	***Notas:*** Se mide la cantidad de operaciones en lugar del tiempo o espacio.
	Siempre va a interesar el peor caso. La complejidad se mide en función del tamaño de la entrada.
##### Ejemplo 1:
```pseudocodigo
Entrada: n entero positivo
Inicializar x <- 0, i <- 1
Repetir mientras i<=n:
	x <- x+1
	i <- i+1
```
Que en python se ve como 
```Python
def algoritmo_ejemplo(n):
	x = 0
	for i = 1 to n:
		x += 1
```
Esto el modelo RAM lo trabaja como sigue:

| Operación | Veces |
| --------- | ----- |
| $x=0$     | 1     |
| $i=1$     | 1     |
| $i\leq n$ | n+1   |
| $x = x+1$ | 2n    |
| $i=i+1$   | 2n    |
	***Nota:*** $i\leq n$ se ejecuta $n+1$ veces. Las $n$ veces especificadas explicitamente, y una extra para salir del ciclo. Por otro lado, $x = x+1$ son dos operaciones. Una asignación, y una suma, por eso se ejecuta $2n$ veces.

Entonces tenemos que $T(n)=1+1+(n+1)+2n+2n=5n+3$. Este es el modelo de complejidad RAM.
##### Ejemplo 2:
```pseudocodigo
Entrada: A[0],...,A[n-1], con n entero positivo
Inicializar total <- 0, i <- 1
Repetir mientras i<n:
	total <- total + A[i]
	i <- i+1
Regresar total
```
En python esto se puede implementar como
```Python
def suma_elementos(A, n):
	total = 0
	i = 0
	while i < n:
		total = total + A[i]
		i = i + 1
```
El modelo de complejidad es de la forma:

| Operación            | Veces |
| -------------------- | ----- |
| total = 0            | 1     |
| i = 0                | 1     |
| i < n                | n+1   |
| total = total + A[i] | 3n    |
| i = i +1             | 2n    |
| return total         | 1     |
Entonces tenemos que $T(n)=1+1+(n+1)+3n+2n+1=6n+4$.

---
#### Cotas de crecimiento
En vez de conservar una función exacta complicada, buscamos funciones simples que la acoten para $n$ grande. 
$$
	c_{1}g(n)\leq f(n)\leq c_{2}g(n).
$$
- $c_{2}g(n)$: cota superior, $O(g(n))$.
- $c_{1}g(n)$: cota inferior, $\Omega(g(n))$.
- Ambas cotas: mismo orden, $\Theta(g(n))$.
##### Definición:
Sean $f,g:\mathbb{N}\to\mathbb{R}_{\geq 0}$, con $g(n)> 0$ para $n$ suficientemente grande. Entonces 
$$
	\begin{align}
	f\in O(g)&\Longleftrightarrow \exists c>0,\quad\exists n_{0}\in\mathbb{N},\forall n\geq n_{0}:0\leq f(n)\leq cg(n). \\
	f\in \Omega (g)&\Longleftrightarrow \exists c>0,\quad\exists n_{0}\in\mathbb{N},\forall n\geq n_{0}:0\leq cg(n)\leq f(n). \\
	f\in \Theta(g)&\Longleftrightarrow \exists c_{1},c_{2}>0,\quad\exists n_{0}\in\mathbb{N},\forall n\geq n_{0}:0\leq c_{1}g(n)\leq f(n)\leq c_{2}g(n).
	\end{align}
$$

##### Teorema: relación entre $O,\Omega$ y $\Theta$
Para $f,g:\mathbb{N}\to\mathbb{R}_{\geq 0}$, tenemos que 
$$
	f\in \Theta(g)\Longleftrightarrow f\in O(g)\quad\text{y}\quad f\in \Omega(g).
$$
Equivalentemente, $\Theta(g)=O(g)\cap \Omega(g)$.
##### Demostración:
$\Rightarrow$ Si $f\in \Theta(g)$, existen $c_{1},c_{2}>0$ y $n_{0}$ tales que, para todo $n\geq n_{0}$, tenemos que 
$$
	c_{1}g(n)\leq f(n)\leq c_{2}g(n).
$$
La desigualdad de la izquierda prueba que $f\in \Omega(g)$, y la de la derecha que $f\in O(g)$.
$\Leftarrow$ Si $f\in O(g)$ y $f\in \Omega(g)$, entonces tenemos que $\exists c_{1},c_{2}>0$ y $\exists n_{1},n_{2}\in\mathbb{N}$ tales que $\forall n\geq n_{1}$ se tiene que $0\leq f(n)\leq c_{1}g(n)$, y $\forall n\geq n_{2}$ tenemos que $0\leq c_{2}g(n)\leq f(n)$. Entonces, basta tomar a $n_{0}=\text{max}(n_{1},n_{2})$, tal que $\forall n\geq n_{0}$ se van a cumplir ambas contenciones al mismo tiempo, es decir que 
$$
	0\leq c_{2}g(n)\leq f(n)\leq c_{1}g(n).\quad\square
$$

