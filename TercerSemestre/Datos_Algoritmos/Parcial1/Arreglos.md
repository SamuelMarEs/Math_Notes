Un arreglo unidimensional es una colección de $n$ elementos identificados por su posición: 
$$
	A=(a_{0},a_{1},\dots,a_{n-1}),\quad A[i]=a_{i},\quad 0\leq i<n.
$$
Su operación fundamental es el acceso directo por índice.
El índice indica la posición, no el valor almacenado.
Los valores si pueden repetirse, es decir la posición importa.
Al acceder a $A[i]$ no se requiere acceder a los elementos anteriores.

El número de operaciones para acceder a un elemento del arreglo es *constante*, i.e. $T_{\text{acceso}}(n)=\Theta(1)$.

##### En Python
~~~Python
A = [10, 20, 30, 40, 50]
B = (10, 20, 30, 40, 50)

A[0]     # 10
A[3]     # 40
A[-1]    # 50
len(A)   # 5

A[2] = 99 # permitido
B[2] = 99 # TypeError
~~~
Una `list` se puede modificar, pero un `tuple` es [[TDA|inmutable]]. Sin embargo, ambos son arreglos de una dimensión.

##### Operaciones con listas
Sea una lista `A = [10, 20, 30]`

| Operación           | Python         | Efecto o resultado                  |
| ------------------- | -------------- | ----------------------------------- |
| Acceder por índice  | A[1]           | 20                                  |
| Consultar longitud  | len(A)         | 3                                   |
| Agregar al final    | A.append(40)   | A: [10, 20, 30, 40]                 |
| Insertar            | A.insert(1,99) | A: [10, 99, 20, 30]                 |
| Extraer el último   | A.pop()        | Devuelve 30. A: [10, 20]            |
| Extraer por índice  | A.pop(0)       | Devuelve 10. A: [20, 30]            |
| Eliminar por índice | del A[1]       | A: [10, 30]                         |
| Buscar un valor     | 20 in A        | True                                |
| Localizar un valor  | A.index(20)    | Devuelve el primer índice: 1        |
| Obtener un segmento | A[1:]          | Nueva lista [20, 30]; no modifica A |
##### Operaciones con tuplas
Para la tupla `T = (10, 20, 30)`

| Operación           | Python      | Efecto o resultado |
| ------------------- | ----------- | ------------------ |
| Acceder por índice  | T[1]        | 20                 |
| Consultar longitud  | len(T)      | 3                  |
| Buscar un valor     | 20 in T     | True               |
| Localizar un valor  | T.index(20) | Primer índice: 1   |
| Obtener un segmento | T[1:]       | (20, 30)           |
| Concatenar          | T + (40,)   | (10, 20, 30, 40)   |
Estas operaciones no modifican a la tupla T.

#### NumPy
La librería de `numpy` es una librería de Python enfocada en el cálculo numérico. Hay funciones matemáticas, algebra lineal, estadística, probabilidad, etc.

Un `ndarray` es un arreglo multidimensional de NumPy. Su forma, `shape`, indica el tamaño de cada eje; `dtype` indica el tipo de almacenamiento común de sus elementos.

#Algoritmos