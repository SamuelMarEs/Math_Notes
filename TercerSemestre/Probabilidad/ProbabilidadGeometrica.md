Supongamos que el espacio muestral de un fenómeno aleatorio se puede representar como un subconjunto de $\mathbb{R}^{2}$.
La probabilidad geométrica de un evento $A$ definido sobre un [[PrincipiosDeProbabilidad|espacio muestral]] $\Omega$ se calcula 
$$
	P(A)=\frac{\text{área }A}{\text{área }\Omega}.
$$
Siempre que el espacio sea equiprobable.

Esta es una forma de cierto modo una generalización de la [[ProbabilidadClasica|probabilidad clásica]] pero para conjuntos que quizás no necesariamente son discretos, si no más bien continuos.

##### Ejemplo:
Supongamos que tengamos una diana de tiro con arco de los números 10 al 6. Supongamos que el radio del círculo del 10 es 5 unidades, y de los demás círculos suman 10 unidades.
Sea $A=$ obtener un 9. Entonces tenemos que 
$$
	P(A)=\frac{\pi 15^{2}-\pi 5^{2}}{\pi 45^{2}}=\frac{(10)(20)}{45^{2}}=\frac{8}{81}=0.09.
$$

##### Ejercicio:
Se elige un número $a$ al azar en el intervalo $(-1,1)$. ¿Cuál es la probabilidad de que la ecuación $ax^{2}+x+1=0$ tenga dos raices reales?
##### Solución:
Nuestro polinomio tiene raíces reales si y sólo si el discriminante satisface 
$$
	1-4a> 0 \implies a< \frac{1}{4},
$$
es decir que $a\in (-1, \frac{1}{4})$. 
Entonces nuestro espacio muestral $\Omega=(-1,1)$, y nuestro evento $A=\text{ haya dos raíces reales }\implies a\in\left( -1, \frac{1}{4} \right)$. Entonces tenemos que 
$$
	P(A)=\frac{\text{longitud }A}{\text{longitud }\Omega}=\frac{\frac{1}{4}+1}{1+1}=\frac{5 / 4}{2}=\frac{5}{8}=0.625.
$$


Este ejemplo nos indica que la probabilidad geométrica no está limitada a áreas, si no que puede trabajarse en otras dimensiones. Es decir, puede generalizarse al volumen, o "áreas" de más dimensiones.

#Probabilidad #Geometria
