69.- Un dado equilibrado se lanza 6 veces consecutivas. ¿Cuál es la probabilidad de que:
- aparezcan las seis caras del dado en orden creciente o decreciente?
  **Sol:** 
  Sea $\Omega=\{ (a_{1},a_{2},a_{3},a_{4},a_{5},a_{6}):a_{i}=1,2,3,4,5,6 \}$. Sea $A=$ salen las seis caras en orden creciente o decreciente. Existen dos formas para que aparezcan las 6 caras en orden decreciente o creciente, $(1,2,3,4,5,6)$ y $(6,5,4,3,2,1)$. Entonces tenemos que 
  $$
	P(A)=\frac{\#A}{\#\Omega}=\frac{2}{6^{6}}=\frac{1}{23328}=0.000042.
  $$
- aparezcan las seis caras del dado en cualquier orden?
  **Sol:** 
  Sea $\Omega$ como definido en el inciso anterior, y $B=$ salen las seis caras en cualquier orden. Entonces $\#B=6!$ son todas las formas en las que pueden salir las seis caras. Entonces 
  $$
	P(B)=\frac{\#B}{\#\Omega}=\frac{6!}{6^{6}}=\frac{5}{324}=0.0152.
  $$
- sólo aparezcan números pares?
  **Sol:** 
  Nuevamente tomamos $\Omega$ como definido anteriormente, y $C=\{ (a_{1},a_{2},a_{3},a_{4},a_{5},a_{6}):a_{i}=2,4,6 \}$, y tenemos que $\#C=3^{6}$, de forma que tenemos que 
  $$
	P(C)=\frac{\#C}{\#\Omega}=\frac{3^{6}}{6^{6}}=\frac{3^{6}}{3^{6}2^{6}}=\frac{1}{2^{6}}=\frac{1}{64}=0.015.
  $$
- aparezcan números pares e impares alternados?
  **Sol:** 
  Ahora definamos dos eventos $D=\{ (a_{1},a_{2},a_{3},a_{4},a_{5},a_{6}):a_{i}=2,4,6\text{ para }i\text{ par, }a_{i}=1,3,5\text{ para }i\text{ impar} \}$, y $E=\{ (a_{1},a_{2},a_{3},a_{4},a_{5},a_{6}):a_{i}=2,4,6\text{ para }i\text{ impar, }a_{i}=1,3,5\text{ para }i\text{ par} \}$. $D$ y $E$ son eventos ajenos, ambos con la misma cardinalidad $\#E=\#D=3^{6}$, entonces tenemos que 
  $$
	P(D\cup E)=P(D)+P(E)=\frac{3^{6}}{6^{6}}+\frac{3^{6}}{6^{6}}=\frac{1}{32}=0.031.
  $$


70.- ¿Cuántos enteros positivos de a lo sumo cinco dígitos son divisibles por 2? ¿Y de ellos, cuántos hay que empiecen con el dígito 1?
**Sol:**
La pregunta se puede ver como: ¿cuántos enteros entre 1 y 99999 son divisibles entre dos?. Para esto basta dvidir la cantidad de enteros (99999) dividida entre dos, y tomar la parte entera, es decir 
$$
	\left\lfloor  \frac{99999}{2}  \right\rfloor =49999.
$$
Para contar los que empiezan por el dígito 1, dividimos en los de dos, tres, cuatro y cinco dígitos. 
De dos dígitos, son aquellos entre 10 y 19, que son 5 enteros divisibles entre dos.
De tres dígitos, son aquellos entre 100 y 199, que son 50 enteros divisibles entre dos.
De cuatro dígitos, son aquellos entre 1000 y 1999, que son 500 enteros divisibles entre dos.
Por ultimo, de 5 dígitos, son entre 10000 y 19999, que son 5000 enteros divisibles entre dos.
Entonces en total hay 
$$
	5+50+500+5000=5555
$$
enteros de a lo sumo cinco dígitos que empiezen por el 1.

76.- Corredores. ¿De cuántas maneras diferentes pueden clasificarse los tres primeros lugares de una carrera de $n$ corredores? Suponga que no hay empates.
**Sol:**
El orden sí nos importa, entonces la cantidad de formas en que pueden clasificarse los primeros tres lugares es $$n\text{P} 3=\frac{n!}{(n-3)!}.$$

79.- Rumores. En un pueblo de $n+1$ habitantes, uno de ellos le rumorea algo a una segunda persona, ésta, a su vez, se lo cuenta a una tercera persona (que puede ser la primera persona), y así sucesivamente. Determine la probabilidad de que el rumor se transmita $r$ veces sin que regrese a la primera persona.
**Sol:**
Se puede ver como la probabilidad de que ninguna persona se lo cuente a la primera de nuevo. Quien empieza, se lo puede contar a cualquiera, entonces, sea $M_{i}$ el evento de que la $i$-ésima persona no se lo cuente a la primera, queremos calcular 
$$
	P\left( \bigcap_{i=1}^{n}M_{i} \right)=P(M_{1})P(M_{2}|M_{1})\dots P(M_{n}|M_{1}\cap M_{2}\cap\dots \cap M_{n-1}).
$$
Observemos que para cada $i$, se cumple que $P(M_{i}|M_{1}\cap\dots \cap M_{i-1})=\frac{n-i+1}{n}$, de forma que, sea $M=\bigcap_{i=1}^{n}M_{i}$, tenemos que 
$$
	P(M)= \frac{n(n-1)(n-2)\dots(2)(1)}{n^{n}}=\frac{n!}{n^{n}}.
$$

81.- Funciones. Sean $A$ y $B$ dos conjuntos finitos con cardinalidades $n$ y $m$, respectivamente, como se muestra en la figura 1.25. 
![[Fig1_25_TareaProba2]]
Determine el número total de funciones $f$ de $A$ en $B$ tal que 
- no tienen restricción alguna.
  **Sol:**
  Podemos ver a todas las funciones como una eneada que nos indica a dónde va cada $a_{i}$. Es decir $\{ (f(a_{1}),f(a_{2}),\dots,f(a_{n})):f(a_{i})=b_{1},\dots b_{n}\}$. Por lo tanto, cada función tiene $m$ valores posibles, es decir que hay $n^{m}$ funciones posibles de $A$ a $B$.
- son inyectivas (uno a uno), suponiendo $n\leq m$.
  **Sol:**
  Podemos ver las funciones de la misma forma, pero ahora, el número de resultados posibles se reduce con cada 
- son suprayectivas (sobre), suponiendo $m\leq n$.


82.- Un panadero elabora 100 panes en un día, en donde 10 de ellos pesan menos de lo que deberían. Un inspector pesa 5 panes tomados al azar. Calcule la probabilidad de que el inspector encuentre en su muestra exactamente un pan de peso incorrecto.

95.- Zapatos. Una mujer tiene $n$ pares de zapatos en desorden y en un viaje intempestivo escoge al azar $2r$ zapatos ($2r\leq 2n$). Calcule la probabilidad de que en el conjunto escogido:
- no haya ningún par completo.
- haya exactamente un par completo.
- haya $r$ pares completos.

96.- Llaves. Una persona tiene $n$ llaves, de las cuales únicamente una ajusta a la cerradura pero no sabe cuál de ellas es la correcta. Procede a tomar las llaves al azar, una por una, hasta encontrar la correcta. Calcule la probabilidad de encontrar la llave correcta en el $n$-ésimo intento suponiendo que 
- retira las llaves que no funcionaron.
- no retira las llaves que no funcionaron.


