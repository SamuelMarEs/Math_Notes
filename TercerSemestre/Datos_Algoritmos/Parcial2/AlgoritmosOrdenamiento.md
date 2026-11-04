#Algoritmos 
#### Problema de ordenamiento
Dado un arreglo ${}A{}$ de ${}n{}$ elementos comparables, reorganizarlos para obtener 
$$
A[0]\leq A[1]\leq\dots\leq A[n-1].
$$
El resultado debe conservar todos los elementos originales y sus repeticiones.
El procedimiento modificará el arreglo recibido. El arreglo vacío y el arreglo de un elemento ya están ordenados.
#### Algoritmo estable
Un algoritmo de ordenamiento es estable si conserva el orden relativo de los elementos con la misma clave.
Por ejemplo, si la entrada es ${}[2_{a},1,2_{b}]{}$, un ordenamiento estable (que conserva el orden entre estables) regresaría ${}[1,2_{a},2_{b}]{}$, mientras que uno no estable lo invierte ${}[1,2_{b},2_{a}]{}$.
### Insertion Sort
El prefijo ${}A[0:i]{}$ ya está ordenado.
Tomamos ${}A[i]{}$ como *clave* y desplazamos a la derecha los valores mayores.
La clave ocupa el espacio que queda libre. 
$$
[2,5,4,6,1,3]\implies[2,5,5,6,1,3]\implies[2,4,5,6,1,3].
$$
Después, tocaría mover el 1, por lo que habría que repetir los mismos tres pasos un total de cuatro veces.
```python
def insertion_sort(A):
    n = len(A)
    for i in range(1, n):
        clave = A[i]
        j = i - 1
        while j >= 0 and A[j] > clave
            a[j+1] = A[j]
            j -= 1
        A[j+1] = clave
```
No es difícil ver que en el peor de los casos, el algoritmo tiene complejidad ${}\Theta(n^{2}){}$.
### Selection Sort
Buscamos el mínimo del sufijo ${}A[i:n]{}$ y lo intercambiamos con ${}A[i]{}$.
Después de cada iteración del ciclo exterior, una posición más queda en su lugar definitivo.
El prefijo contiene los menores elementos, en orden. 
$$
[5,2,4,6,1,3]\implies[1,2,4,6,5,3]\implies[1,2,3,6,5,4]\implies \dots\implies[1,2,3,4,5,6].
$$
Buscamos el mínimo de los siguientes, y reemplazamos con el actual.
```python
def selection_sort(A):
    n = len(A)
    for i in range(n - 1):
        m = i
        for j in range(i+1, n):
            if A[j] < A[m]:
                m = j
        A[i], A[m] = A[m], A[i]
```
Sin importar si se trata del mejor o el pero caso, el algoritmo tiene complejidad ${}\Theta(n^{2}){}$.
Este algoritmo resulta ser no estable, pues ${}[2_{a},2_{b},1]\implies[1,2_{b},2_{a}]{}$, y ahí acaba el algoritmo.
### Bubble Sort
Comparamos vecinos de derecha a izquierda e intercambiamos si están invertidos.
El mínimo del sufijo avanza hasta la posición ${}i{}$.
Al terminar una iteración del ciclo exterior, el prefijo ordenado crece una posición.
```python
def bubble_sort(A):
    n = len(A)
    for i in range(n-1):
        for j in range(n-1, i, -1):
            if A[i] < A[j]:
                A[i], A[j] = A[j], A[i]
```
Es fácil ver que la complejidad del Bubble Sort es ${}\Theta(n^{2}){}$.
### Shell Sort
Ordenamos por inserción las subsecuencias separadas por una distancia ${}h{}$. Un arreglo está ${}h{}$-ordenado si ${}A[j-h]\leq A[j]{}$ para todo ${}j\geq h{}$.
Por ejemplo, si ${}h=4{}$, las posiciones 0, 4, 8 forman una subsecuencia: 
$$
[9,8,7,6,5,4,3,2,1]\implies[1,4,3,2,5,8,7,6,9].
$$
```python
def shell_sort(A):
    n = len(A)
    h = 1
    while h < n // 3:
        h = 3*h + 1
    while h >= 1:
        for i in range(h, n):
            j = i
            while (j >= h and A[j]<A[j-h]):
                A[j], A[j-h] = A[j-h], A[j]
                j -= h
        h //= 3
```
Existen distintas sucesiones que se pueden usar para determinar ${}h{}$:

| Sucesión       | Primeros términos | Mejor caso               | Peor caso |
| -------------- | ----------------- | ------------------------ | --------- |
| Shell original |                   | ${}\Theta(n\log_{2}n){}$ |           |
| Hibbard        |                   | ${}\Theta(n\log_{2}n){}$ |           |
| Knuth          |                   | ${}\Theta(n\log_{2}n){}$ |           |
| Pratt          |                   |                          |           |
| Sedgewick      |                   | ${}\Theta(n\log_{2}n){}$ |           |
### Heap Sort
El máximo del [[Heap|heap]] está en la raíz. Lo intercambiamos con el último elemento activo y reservamos esa posición para el resultado.
Si tenemos un max-heap incial 
$$
[16,14,10,8,7,9,3,2,4,1],
$$
intercambiamos el primero con el último, y lo hundimos 
$$
[14,8,10,4,7,9,3,2,1,16].
$$
La última posición deja de pertenecer al heap (de lo contrario la tendríamos que flotar, y no queremos eso).
```python
def heap_sort(A):
	construir_heap(A)
	n = len(A)
	for i in range(n - 1, 0, -1):
	    A[0], A[i], = A[i], A[0]
	    n -= 1
	    hundir(A, n, 0)
```
La complejidad de hundir es ${}\Theta(\log_{2}(n+1)){}$, mientras que construir_heap tiene complejidad lineal. Dado que hundir está dentro de un ciclo, tenemos que la complejidad de heap sort será de ${}\Theta(n\log_{2}(n+1)){}$.
### Merge Sort
Ordenamiento por mezcla. Dividimos el intervalo, ordenamos cada mitad y mezclamos sus resultados.
![[MergeSort]]
```python
def mergesort(A, p, r):
    if p >= r
        return
    q = (p + r) // 2
    mergesort(A, p, q)
    mergesort(A, q+1, r)
    mezclar(A, p, q, r)
```
