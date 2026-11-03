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
Tomamos ${}A[i]{}$ como *clave* y desplazamos a la derecha los valores mayores