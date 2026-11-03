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