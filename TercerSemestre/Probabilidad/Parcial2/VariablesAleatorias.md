#Probabilidad 

De manera burda, una variable aleatoria es una pregunta o medición que se hace a un sujeto o una población, cuya respuesta es un número real.
##### Ejemplos:
1. Número de infecciones de Dengue.
2. Temperatura máxima del día.
3. Número de ventas de un negocio.
4. Línea de crédito de una persona.

#### Definición
Sea $(\Omega,\mathcal{F},P)$ un [[Espacio_de_Probabilidad|espacio de probabilidad]] y sea $X:\Omega \to\mathbb{R}$ una función que relaciona el [[PrincipiosDeProbabilidad|espacio muestral]] con los reales, tal que 
$$
	\{ w\in \Omega:X(w)\leq x\}\in\mathcal{F},\forall x\in\mathbb{R}, 
$$
para $\mathcal{F}$ una [[SigmaAlgebra|sigma algebra]] (el conjunto es algo que se llama una condición de medibilidad). Entonces $X$ recibe el nombre de ***varialbe aleatoria***.

***Note:*** es decir que una variable aleatoria no es una variable, ni es aleatoria, si no que es una **función**. HDSPTM al que se le ocurrió el nombre.

##### Ejemplos
1.- Sea $\Omega=\{ \text{águila,sol} \}$ con $P(\text{águila})=P(\text{sol})=\frac{1}{2}$. Sea $X(w)=\begin{cases}1,\quad w=\text{águila} \\  0,\quad w=\text{sol}\end{cases}$.
Sea $x=7$, entonces $\{ w\in \Omega:X(w)\leq 7 \}=\{ \text{águila, sol} \}=\Omega\in\mathcal{F}$. Podemos repetir esto para cualquier número real, de forma que el conjunto siempre va a ser un elemento de nuestra sigma álgebra.
Notar que 
$$
	P(X=1)=P(\text{águila})=\frac{1}{2},
$$
$$
	P(X=0)=P(\text{sol})=\frac{1}{2},
$$
o también podemos calcular 
$$
	P(X\leq 2)=P(\{ \text{águila, sol} \})=1.
$$


2.- Suponga que se tiene una diana de tiro con centro en $(0,0)$ y radio 1. Entonces 
$$
	\Omega=\{ (x,y)\in R^{2}:x^{2}+y^{2}\leq 1 \}.
$$
Podemos definir las siguientes variables aleatorias:
a) $X(w)=x$ la coordenada $x$ del punto $w$. Entonces $X\in[-1,1]$.
b) $X(w)=x+y$ la suma de las coordenadas de $w$.
c) $X(w)=\sqrt{ x^{2}+y^{2} }$ la distancia al origen, de modo que $X\in[0,1]$.

En general, existen 2 tipos de variables aleatorias:
- Discretas: decimos que una variable aleatoria es discreta si tiene una probabilidad positiva sólo para un número finito o numberable de resultados.
- Continuas: son aquellas que toman valores en un subconjunto de $\mathbb{R}$.

#### Notación
Vamos a denotar a las variables aleatorias con letras mayúsculas $(X,Y,Z)$ y a los valores de las variables con letras minúsculas $(x,y,z)$.