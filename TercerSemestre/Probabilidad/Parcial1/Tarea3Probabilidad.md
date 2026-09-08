103.- Sean $A, B$ dos eventos tales que $P(A)=1 / 4$,$P(B|A)=1 / 2$ y $P(A|B)=1 / 2$. Determine y justifique si las siguientes afirmaciones son verdaderas o falsas.
- $A$ y $B$ son ajenos.
  **Sol:**
  Falso, pues $A\cap B=\emptyset\Rightarrow P(A|B)=\frac{P(A\cap B)}{P(B)}=\frac{P(\emptyset)}{P(B)}=0\neq \frac{1}{2}$.
- $A=B$.
  **Sol:**
  Falso, ya que $A=B\Rightarrow P(A|B)=\frac{P(A\cap B)}{P(B)}==\frac{P(B)}{P(B)}=1\neq \frac{1}{2}$.
- $P(B)=1 / 4$.
  **Sol:**
  Verdadero, pues $P(A|B)=\frac{P(B|A)P(A)}{P(B)}\Rightarrow P(B)=\frac{(1 / 2)(1 / 4)}{(1 / 2)}=\frac{1}{4}$.
- $P(A^{c}|B^{c})=5 / 6$.
  **Sol:**
  Verdadero, ya que 
  $$
	\begin{align}
	P(A^{c}|B^{c})&=\frac{P(A^{c}\cap B^{c})}{P(B^{c})}=\frac{1-P(A\cup B)}{1-P(B)} \\
	&=\frac{1-(P(A)+P(B)-P(A\cap B))}{1-P(B)} \\
	&=\frac{1-(P(A)+P(B)-P(A|B)P(B))}{1-P(B)} \\
	&=\frac{4}{3}\left( 1-\frac{1}{4}-\frac{1}{4}+\frac{1}{2} \frac{1}{4} \right)=\frac{5}{6}.
	\end{align}
  $$
- $P(B^{c}|A^{c})=5 / 6$.
  **Sol:** 
  Verdadero, pues por Bayes
  $$
	P(B^{c}|A^{c})=\frac{P(A^{c}|B^{c})P(B^{c})}{P(A^{c})}=\frac{5 / 6(1- 1 / 4)}{(1- 1 / 4)}=\frac{5}{6}.
  $$
  
- $P(A|B)+P(A|B^{c})= 2 / 3$.
  **Sol:**
  Falso pues $P(A|B)+P(B|A)=\frac{1}{2}+ \frac{1}{2}=1\neq \frac{2}{5}$.


117.- Se tiene un arreglo lineal de tres cajas como se muestra en la Figura 1.30, en donde en cada caja hay 1 canica blanca y 1 azul. Se toma una canica al azar de la primera caja y, sin verla, se coloca en la segunda caja. Después se toma una canica al azar de la segunda caja y, sin verla, se coloca en la tercera caja. Finalmente se toma una canica al azar de la tercera caja. Calcule la probabilidad de que la canica escogida sea azul.
![[Figura1_30_Tarea3Proba.png]]
**Sol:**
Sean $A_{1},A_{2},A_{3}$ los eventos de sacar una canica azul de las cajas 1,2,3, respectivamente. Sean además $B_{1},B_{2},B_{3}$ definidos de forma análoga pero para las bolas blancas.
Aplicando la ley de probabilidad total, tenemos que 
$$
	P(A_{3})=P(A_{3}|A_{2})P(A_{2})+P(A_{3}|B_{2})P(B_{2}).
$$
Pero, de la misma forma, tenemos que 
$$
	P(A_{2})=P(A_{2}|A_{1})P(A_{1})+P(A_{2}|B_{1})P(B_{1}),
$$
y que 
$$
	P(B_{2})=P(B_{2}|A_{1})P(A_{1})+P(B_{2}|B_{1})P(B_{1}).
$$
Sabemos que $P(A_{1})=P(B_{1})=\frac{1}{2}$. Dado $A_{1}$, en la caja dos hay dos canicas azules y una blanca, entonces $P(A_{2}|A_{1})=\frac{2}{3}=P(B_{2}|B_{1})$, y además $P(A_{2}|B_{1})=\frac{1}{3}=P(B_{2}|A_{1})$. Entonces tenemos que 
$$
	P(A_{2})=\left( \frac{2}{3} \right)\left( \frac{1}{2} \right)+\left( \frac{1}{3}\right)\left( \frac{1}{2} \right) =\frac{1}{2}.
$$
De la misma forma tenemos que 
$$
	P(B_{2})=\left( \frac{1}{3} \right)\left( \frac{1}{2} \right)+\left( \frac{2}{3} \right)\left( \frac{1}{2} \right)=\frac{1}{2}.
$$
De la misma forma que para $P(A_{2}|A_{1})$, tenemos que $P(A_{3}|A_{2})=\frac{2}{3}$ y $P(A_{3}|B_{2})=\frac{1}{3}$. Entonces tenemos que 
$$
	P(A_{3})=\left( \frac{2}{3} \right)\left( \frac{1}{2} \right)+\left( \frac{1}{3}\right)\left( \frac{1}{2} \right) =\frac{1}{2}.
$$


118.- Se cuenta con cuatro monedas marcadas con "cara" y "cruz" tal que para la $i$-ésima moneda $P(\text{"cara"})=0.2i,i=1,2,3,4$. Si se escoge una moneda al azar y se lanza al aire, encuentre la probabilidad de que ésa caiga cruz.
**Sol:**
Estamos trabajando con la ley de probabilidad total. Sea $M_{i}$ el evento de escoger la moneda $i=1,2,3,4$, entonces 
$$
	P(\text{"cara"})=P(\text{cara}|M_{1})P(M_{1})+P(\text{cara}|M_{2})P(M_{2})+P(\text{cara}|M_{3})P(M_{3})+P(\text{cara}|M_{4})P(M_{4}).
$$
Notemos que los eventos de elegir cada moneda son equiprobables, es decir que $P(M_{1})=P(M_{2})=P(M_{3})=P(M_{4})=\frac{1}{4}$. Y además sabemos que $P(\text{cara}|M_{i})=0.2i$. Entonces tenemos que 
$$
	P(\text{"cara"})=\frac{1}{4}(0.2+0.4+0.6+0.8)=\frac{1}{2}.
$$


122.- Examen de opción múltiple. Un estudiante contesta un examen de opción múltiple, en el cual cada pregunta tiene cuatro opciones como respuesta pero sólo una es correcta. Cuando el estudiante conoce la respuesta correcta, la selecciona, en caso contrario, selecciona una de las opciones al azar. Suponga que con probabilidad 0.6 el estudiante conoce la respuesta correcta de cualquiera de las preguntas.
- Calcule la probabilidad de que el estudiante tenga correcta una de las preguntas escogida al azar.
  **Sol:**
  Sea el evento $C=$ escoger la respuesta correcta, $S=$ el estudiante sabe la respuesta, $S^{c}=$ el estudiante no sabe la respuesta. Entonces el ejercicio nos dice que $P(S)=0.6$, $P(S^{c})=0.4,$ $P(C|S)=1$ y $P(C|S^{c})=\frac{1}{4}$. Entonces por la ley de probabilidad total, tenemos que la probabilidad de escoger la respuesta correcta de una pregunta al azar es 
  $$
	\begin{align}
	P(C)&=P(C|S)P(S)+P(C|S^{c})P(S^{c}) \\
	&=(1)(0.6)+(0.25)(0.4)&=0.7.
	\end{align}
  $$
  
- Si el estudiante obtuvo la respuesta correcta a una pregunta escogida al azar, ¿cuál es la probabilidad de que haya sabido verdaderamente la respuesta?
  **Sol:**
  Queremos calcular $P(S|C)$. Por el teorema de Bayes esto es 
  $$
	P(S|C)=\frac{P(C|S)P(S)}{P(C)}=\frac{(1)(0.6)}{0.7}=\frac{6}{7}.
  $$
  
- Si el examen consta de 10 pregunta y es necesario tener por lo menos 6 respuestas correctas para acreditar, ¿cuál es la probabilidad de que el estudiante pase el examen?
  **Sol:**
  Tenemos que calcular la probabilidad de tener al menos 6 respuestas correctas


125.- El problema de los tres prisioneros. A tres prisioneros, a quienes llamaremos $A,B$ y $C$, les informa su celador que se ha escogido al azar a uno de ellos para ser ejecutado, dejando a los otros dos en libertad. El prisionero $A$ sabe que tiene probabilidad $1 / 3$ de ser ejecutado y le pide al celador que le diga en secreto cuál de sus compañeros saldrá libre argumentando que por lo menos uno de ellos saldrá en libertad y que saber esa información no cambia su probabilidad de ser ejecutado. El celador, por el contrario, piensa que si el prisionero $A$ sabe cuál de sus compañeros saldrá en libertad, la probabilidad de ser ejecutado aumenta a $1 / 2$. ¿Quién tiene la razón? Justifique su respuesta.


126.- El problema de las tres puertas (Monty Hall). Se le presentan a un concursante tres puertas cerradas, detrás de cada una de las cuales hay un premio. El concursante debe adivinar la puerta que contiene el premio para ganarlo. Una vez que el concursante elige una puerta, y antes de abrirla, el presentador del concurso abre alguna de las puertas restantes, de la cual sabe que no contiene ningún premio. Entonces le pregunta al concursante si desea cambiar su decisión. ¿Qué debe hacer el concursante? Justifique su respuesta.


128.- Una persona toma al azar uno de los número 1,2 o 3, con idéntica probabilidad cada uno de ellos, y luego tira un dado equilibrado tantas veces como indica el número escogido. Finalmente suma los resultados de las tiradas del dado. Calcule la probabilidad de que
- se obtenga un total de 5.
- se haya escogido el número 2 dado que la suma de las tiradas del dado es 8.


133.- Sean $A$ y $B$ eventos tales que $P(A)=4 / 10$ y $P(A\cup B)=7 / 10$. Encuentre la probabilidad de $B$ suponiendo que 
- $A$ y $B$ son independientes.
- $A$ y $B$ son ajenos.
- $P(A|B)=1 / 2$.


154.- Un cierto componente de una máquina falla el 5% de las veces que se enciende. Para obtener una mayor confiabilidad se colocan $n$ componentes de las mismas características en un arreglo en paralelo, como se muestra en la Figura 1.36, de tal forma que ahora el conjunto de componentes falla cuando todos fallan. Suponga que el comportamiento de cada componente es independiente uno del otro. Determine el mínimo valor de $n$ a fin de garantizar el funcionamiento de la máquina por lo menos el 99% de las veces.
![[Figura1_36_Tarea3Proba.png]]


155.- Basketbol. Dos jugadores de basketbol alternan turnos para efectuar tiros libres hasta que uno de ellos enceste. En cada intento, la probabilidad de encestar es $p$ para el primer jugador y $q$ para el segundo jugador, siendo los resultados de los tiros independientes unos de otros. Calcule la probabilidad de encestar primero de cada uno de los jugadores.