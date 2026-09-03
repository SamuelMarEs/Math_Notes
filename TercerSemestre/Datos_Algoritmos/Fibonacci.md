#### Algoritmo FibonacciRecursivo
```pseudocodigo
Entrada: entero i >= 0
Si i <= 1, regresar F <- i
En otro caso: 
	calcular a <- FibonacciRecursivo(i-1)
	calcular b <- FibonacciRecursivo(i-2)
	Regresar F <- a + b
```
Este algoritmo recursivo para calcular la secuencia de Fibonacci, es de cierto modo igual a la fórmula con la que se define: 
$$
	a_{0}=1, a_{1}=1, a_{n}= a_{n-1}+a_{n-2}.
$$
En Python se puede implementar como:
```Python
def FibonacciRecursivo(n):
	if n <= 1:
		return n
	a = FibonacciRecursivo(n-1)
	b = FibonacciRecursivo(n-2)
	return a + b
```
Si la entrada es $0, 1$, entonces tiene una complejidad constante de 2 operaciones.
Si $n=2$, entonces tiene que volver a calcular FibonacciRecursivo(0) y FibonacciRecursivo(1) (2 operaciones por cada uno), asignarlas, y retornar la suma (4 operaciones más), lo que son en total 6 operaciones.
Si $n=3$, debe calcular FibonacciRecursivo(1) y FibonacciRecursivo(2) (8 operaciones), y le sumamos las 4 de asignar y retornar la suma para un total de 12 operaciones.
Si $n=4$, debe calcular FibonacciRecursivo(2) y FibonacciRecursivo(3) (20 operaciones totales), para un total de 24 operaciones.
Así, para calcular cualquier $n$, la función debe hacer todos los calculos anteriores para calcular $n-1$ y $n-2$, casi duplicando la complejidad.

Este algoritmo recursivo tiene el problema de tener una complejidad de orden $O(2^{n})$.

#### Algoritmo FibonacciIterativo
```pseudocodigo
Entrada: entero i >= 0
Si i <= 1, regresar F <- i
Inicializar anterior <- 0, actual <- 1
Para j <- 2 hasta i:
	siguiente <- anterior + actual
	Actualizar anterior <- actual
	Actualizar actual <- siguiente
Regresar F <- actual
```
Este algoritmo itera de forma lineal, en vez de tener que calcular la función para los dos valores anteriores, y los anteriores de los anteriores, y así repetidamente.
En Python lo podemos implementar como sigue:
```Python
def FibonacciIterativo(n):
	if n <= 1:
		return n
		
	anterior = 0
	actual = 1
	for j = 2 to n:
		siguiente = anterior + actual
		anterior = actual
		actual = siguiente
		
	return actual
```
En este caso, es muchísimo más sencillo calcular la complejidad del algoritmo, de la forma siguiente (para casos $n>1$):

| Operaciones                   | Veces       |
| ----------------------------- | ----------- |
| n <= 1                        | 1           |
| anterior = 0                  | 1           |
| actual = 1                    | 1           |
| j = 2                         | 1           |
| j <= n                        | n+1         |
| siguiente = anterior + actual | 2n          |
| anterior = actual             | n           |
| actual = anterior             | n           |
| j += 1                        | n           |
| return actual                 | 1           |
Esto nos da una complejidad final de $f(n)=5n+6$, es decir que tiene una complejidad de orden $O(n)$.

#Algoritmos