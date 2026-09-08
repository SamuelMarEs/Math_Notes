##### Definición
Decimos que los eventos $A$ y $B$ son independientes si se cumple que 
$$
	P(A\cap B)=P(A)P(B).
$$

Esto tiene la siguiente implicación directa: si dos eventos son independientes, entonces 
$$
	P(A|B)=P(A)\quad\text{y}\quad P(B|A)=P(B).
$$
Esto se deduce inmediatamente de la definición de [[ProbabilidadCondicional|probabilidad condicional]].

##### Ejemplo:
Supongamos que se lanzan dos dados distinguibles y se calcula la suma.
Definamos los eventos $D_{1}=$ dado 1 salió 4, $S_{6}=$ suma es 6. Intuitivamente es inmediato que ambos eventos NO son independientes.
Si fueran independientes, debería cumplirse que: 
$$
	P(D_{1}\cap S_{6})=P(D_{1})P(S_{6}).
$$
Sabemos que $P(D_{1})=\frac{1}{6}$ y $P(S_{6})=\frac{5}{36}$.  Además es fácil calcular que $P(D_{1}\cap S_{6})=\frac{1}{36}$, sin embargo vemos inmediatamente que $\frac{1}{6} \frac{5}{36}\neq \frac{1}{36}$. Por lo tanto los eventos no son independientes.

Ahora que sucede con $S_{7}=$ suma es 7. Vamos a ver que $D_{1}$ y $S_{7}$ SI son independientes.
Sabemos que $P(D_{1})=\frac{1}{6}$, y $P(S_{7})=\frac{6}{36}=\frac{1}{6}$. Pero además tenemos que $P(D_{1}\cap S_{7})=\frac{1}{6}$, por lo tanto tenemos que 
$$
	P(D_{1})P(S_{7})=\frac{1}{6} \frac{1}{6}=\frac{1}{36}=P(D_{1}\cap S_{7}).
$$
¿Por qué sucede esto?. Para el caso $S_{6}$, el resultado del primer dado si condiciona a la probabilidad de que la suma sea seis, pues, si sale seis en el primer lanzamineto, en el segundo no importa que pase, no se puede sumar 6. Pero en el caso de $S_{7}$, no importa que salga en el primer dado, siempre podemos conseguir un resultado con el segundo dado que nos de 7, por esto que la suma sea 7 es indpendiente del resultado del primer lanzamiento.

##### Ejercicio
Supongamos que se tienen 3 radios para detectar el paso de un avión por una cierta zona. Los radares trabajan de manera independiente y la probabilidad de que detecten al avión es de $0.92$.
¿Qué tan probable es que todos los radares detecten a un avión que acaba de pasar?
**Sol:**
Definamos los siguientes eventos: $R_{i}=$ el radar $i$ detecta al avión, con $i=1,2,3$. Sabemos que $P(R_{i})=0.92$ para $i=1,2,3$.
Como los radares trabajan de manera independiente, entonces tenemos que
$$
	P(R_{1}\cap R_{2}\cap R_{3})=P(R_{1})P(R_{2})P(R_{3})=(0.92)^{3}=0.77.
$$

¿Y si queremos la probabilidad de que al menos un radar lo detecte?
Para esto es más sencillo calcular el complemento, es decir la probabilidad de que ningún radar lo detecte. Es decir 
$$
	P(\text{al menos uno lo detecta})=1-P(\text{ninguno lo detecta})=1-P(R_{1}^{c}\cap R_{2}^{c}\cap R_{3}^{c})=1-(0.08)^{3}=0.99.
$$


#Probabilidad