#### Teorema de composición secuencial
Si las [[CorreccionAlgoritmica|tripletas]]
$$
	\{ P \}C_{1}\{ R \}\quad\text{y}\quad \{ R \}C_{2}\{ Q \}
$$
son válidas, entonces tembién lo es 
$$
	\{ P \}C_{1};C_{2}\{ Q \}.
$$
##### Demostración
Supongamos que $P$ es verdadera y que la secuencia $C_{1}:C_{2}$ termina.
Al terminar $C_{1}$, se cumple $R$, por la primera tripleta. Eses estado $R$, es el estado inicial de $C_{2}$. Al terminar $C_{2}$, se cumple $Q$, por la segunda tripleta.
Por lo tanto $\{ P \}C_{1};C_{2}\{ Q \}$ es válida. El argumento se extiende a cualquier secuencia finita de fragmentos. 

#Algoritmos #Teorema