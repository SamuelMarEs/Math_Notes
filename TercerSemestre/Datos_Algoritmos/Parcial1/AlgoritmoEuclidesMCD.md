##### Definición:
Sabemos que sean $a,b\in\mathbb{Z}$ con $b\neq 0$, decimos que $b|a$, $b$ divide a $a$ si y sólo si $\exists k\in\mathbb{Z}$ tal que $a=kb$.

##### Definición:
Para $a,b\in\mathbb{Z}$, no ambos cero, escribimos que $d$ es el ***máximo común divisor*** de $a$ y $b$, si $d$ satisface que
- $d\in\mathbb{Z}^{+}$.
- $d|a$ y $d|b$.
- Si $c|a$ y $c|b$, entonces $c\leq b$.
Y se denota como  $d=\text{mcd}(a,b)$.

##### Teorema: invarianza del MCD
Sean $a,b\in\mathbb{Z}$, con $b>0$. Si 
$$
	\exists q,r\in\mathbb{Z}:\quad a=qb+r\quad\text{y}\quad 0\leq r<b,
$$
entonces 
$$
	\text{mcd}(a,b)=\text{mcd}(b,r).
$$
Llamamos a $q$ el *cociente* y a $r$ el *residuo*.
##### Demostración:
Supongamos que $a=qb+r$ y $0\leq r<b$. Definimos el conjunto de divisores comunes entre dos números $x$ y $y$ como 
$$
	\mathcal{D}(x,y)=\{ d\in\mathbb{Z}^{+}:d|x\text{ y }d|y \}.
$$
Por la definición de MCD sabemos que 
$$
	\text{mcd}(x,y)=\text{max}\mathcal{D}(x,y).
$$
Por lo tanto, solo basta probar que $\mathcal{D}(a,b)=\mathcal{D}(b,r)$. Esto se puede probar demostrando la doble inclusión de ambos conjuntos:
$\mathcal{D}(a,b)\subset\mathcal{D}(b,r)$
Sea $c\in\mathcal{D}(a,b)$. Entonces $c|a$ y $c|b$. Es decir, existen enteros $m,n$ tales que $a=mc$ y $b=nc$. Además, por hipótesis $r=a-qb$, por lo tanto 
$$
	r=mc-qnc=c(m-qn),
$$
es decir que $c|r$, y por lo tanto $c\in\mathcal{D}(b,r)$.
$\mathcal{D}(b,r)\subset\mathcal{D}(a,b)$
Sea $c\in\mathcal{D}(b,r)$. Entonces $c|b$ y $c|r$. De forma análoga existen enteros $n,s$ tales que $b=nc$ y $r=sc$, y como por hipótesis $a=qb-r$, tenemos que 
$$
	a=qnc-sc=c(qn-s),
$$
es decir que $c|a$, y por lo tanto $c\in\mathcal{D}(a,b).\quad\square$

#### De la invarianza al algoritmo
El teorema anterior permite sustituir el problema por otro equivalente: 
$$
	\text{mcd}(a,b)=\text{mcd}(b,r),\quad a=qb+r,\quad 0\leq r<b.
$$
Esta idea se aplica de forma iterativa 
$$
	(a_{0},b_{0})\to(a_{1},b_{1})\to(a_2,b_{2})\to\dots
$$
donde en cada paso 
$$
	a_{i}=q_{i}b_{i}+r_{i},\quad (a_{i+1},b_{i+1})=(b_{i},r_{i}).
$$
Como $0\leq r_{i}<b_{i}$, el segundo componente disminuye hasta llegar a cero. Una vez que llegamos a cero, el último divisor no nulo es el MCD.

#### Pseudocódigo
```
Entrada: a,b enteros, no ambos cero
Inicializar a <- |a|, b <- |b|
Repetir mientras b != 0:
	Dividir a entre b: a = qb + r, 0 <= r < b
	Acutalizar a <- b
	Actualizar b <- r
Hasta que b = 0
Regresar d <- a
```


#Algoritmos