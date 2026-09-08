### Suma directa
##### Definición:
Sea $V$ un [[EspaciosVectoriales|espacio vectorial]], y sean $W_{1},W_{2}$ subespacios vectoriales de $V$. Decimos que $V$ es ***suma directa*** de $W_{1}$ y $W_{2}$ si 
$$
	V=W_{1}+W_{2}\quad\text{y}\quad W_{1}\cap W_{2}=\{ 0 \},
$$
y se denota como 
$$
	V=W_{1}\oplus W_{2}.
$$
Recordemos que $V=W_{1}+W_{2}$ si podemos escribir cualquier $v\in V$ de la forma 
$$
	v=w_{1}+w_{2};\quad\text{para}\quad w_{1}\in W_{1},w_{2}\in W_{2}.
$$

##### Ejemplo:
Sea $V=R^{2}$. Sean $W_{1}=$ eje $x$ y $W_{2}=$ eje $y$, tenemos que $V=W_{1}\oplus W_{2}$, pues la los dos ejes se intersectan únicamente en el origen, y cualquier $v\in R^{2}$ se puede escribir como 
$$
	(x,y)=(x,0)+(0,y)\quad\text{donde}\quad(x,0)\in W_{1},(0,y)\in W_{2}.
$$


### Proyección
##### Definición:
Sea $V$ un espacio vectorial y $W_{1},W_{2}$ subespacios de $V$ tales que $V=W_{1}\oplus W_{2}$. La función $T:V\to V$ definida por $T(x)=x_{1}+x_{2}$ donde $x=x_{1}+x_{2}$ con $x_{1}\in W_{1}$ y $x_{2}\in W_{2}$, se llama la ***proyección*** de $V$ sobre $W_{1}$, o la proyección de $W_{1}$ a lo largo de $W_{2}$.
De forma análoga podemos definir la proyección de $V$ sobre $W_{2}$, o la proyección de $W_{2}$ a lo largo de $W_{1}$.

##### [[Tarea1_AlgebraLineal2|Ejercicio]]:
25.- Sea $T:R^{2}\to R^{2}$. Incluya figuras para cada una de las siguientes:
- Encuentre una fórmula para $T(a,b)$, donde $T$ repersenta la proyección sobre el eje $y$ a lo largo del eje $x$.
  **Sol:** Sea $(a,b)\in R^{2}$, podemos reescribir nuestro vector de la forma $(a,0)+(0,b)$ dónde $(a,0)\in$ eje $x$, y $(0,b)\in$ eje $y$.
  Entonces, podemos dar la siguiente forma para la transformación lineal: 
  $$
	T(a,b)=(0,b).
  $$
  Geométricamente, esta transformación se puede ver como "comprimir" el espacio $R^{2}$ sobre el eje $y$.
  ![[ProyeccionSobreYdeX]]
- Encuentre una fórmula para $T(a,b)$, donde $T$ representa la proyección sobre el eje $y$ a lo largo de la recta $L=\{ (s,s):s\in R \}$.
  **Sol:** Sea $(a,b)\in R^{2}$, podemos reescribir el vector como $(a,b)=(a,a)+(0,b-a)$ donde $(a,a)\in L$ y $(0,b-a)\in$ eje $y$. Entonce, podemos dar la fórmula para la transformación lineal de la siguiente forma: 
  $$
	T(a,b)=(0,b-a).
  $$
  Geométricamente, está es la proyección de la recta identidad sobre el eje $y$.


#AlgebraLineal