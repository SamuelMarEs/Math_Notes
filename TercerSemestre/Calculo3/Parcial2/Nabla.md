#Calculo 
#### Operador Nabla
Hasta ahora, hemos usado el símbolo "nabla" $\nabla$ para denotar al gradiente de una función.
El operador nabla $\nabla$ se define como 
$$
	\nabla=\left( \frac{\partial}{\partial x_{1}},\dots, \frac{\partial}{\partial x_{n}} \right),
$$
de modo que, si por ejemplo tenemos $f:\mathbb{R}^{3}\to\mathbb{R}$, entonces al aplicar el operador nabla a $f$ obtenemos el [[Gradiente|gradiente]] de nuestra función: 
$$
	\nabla f=\left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z} \right).
$$

#### Divergencia
Si $F:\mathbb{R}^{n}\to\mathbb{R}^{n}$ es un [[CamposVectoriales|campo vectorial]] dado por $F=(F_{1},F_{2},\dots,F_{n})$, dónde $F_{i}:\mathbb{R}^{n}\to\mathbb{R}$ para $i=1,2,3$. Dado el operador nabla $\nabla=\left( \frac{\partial}{\partial x_{1}},\dots, \frac{\partial}{\partial x_{n}} \right)$, entonces la divergencia se define como 
$$
	\nabla \cdot F=	\frac{\partial F_{1}}{\partial x_{1}}+\dots+ \frac{\partial F_{n}}{\partial x_{n}}.
$$
***Note:*** En un sentido estricto, no se está realizando un producto punto, y la notación es más como una nemotecnia para recordar como es.

#### Rotacional
Definimos el rotacional de un campo vectorial $F$ como 
$$
	\nabla \times F,
$$
para $F:\mathbb{R}^{3}\to\mathbb{R}^{3}$ dada por $F=(F_{1},F_{2},F_{3})$. Esto es lo mismo que 
$$
	\nabla \times F=\left( \frac{\partial F_{3}}{\partial y}- \frac{\partial F_{2}}{\partial z}, \frac{\partial F_{1}}{\partial z}- \frac{\partial F_{3}}{\partial x}, \frac{\partial F_{2}}{\partial x}- \frac{\partial F_{1}}{\partial y}\right).
$$
***Note:*** Nuevamente, no es un producto cruz en el sentido estricto, si no más bien una forma de expresarlo, ya que técnicamente no estamos multiplicando la parcial por la función, si no realizando la operación.