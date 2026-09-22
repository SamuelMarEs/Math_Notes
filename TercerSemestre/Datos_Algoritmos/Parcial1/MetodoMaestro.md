#Algoritmos #Teorema
El método maestro es un teorema que podemos usar para calcular las cotas de complejidad de una [[Recursion|recursion]].
#### Teorema maestro
Sean $a\geq 1$, $b>1$ constantes y $f(n)\geq 0$. Consideremos 
$$
	T(n)=aT(n / b)+f(n),\quad T(1)=d>0,\quad p=\log_{b}a.
$$
- Si $f(n)\in O(n^{p-\varepsilon})$ para alguna constante $\varepsilon>0$, entonces $T(n)\in \Theta(n^{p})$.
- Si $f(n)\in \Theta(n^{p})$, entonces $T(n)\in \Theta(n^{p}\log n)$.
- Si $f(n)\in \Omega(n^{p+\varepsilon})$ para alguna constante $\varepsilon>0$, y además 
  $$
  	af(n / b)\leq \rho f(n)\quad\text{para alguna constante }0<\rho<1,
  $$
  para $n$ suficientemente grande, entonces $T(n)\in \Theta(f(n))$.

###### Ejemplo: caso 1
Sea $T(n)=4T(n / 2)+n$ y $T(1)=d>0$.
Parámetros: $a=4,b=2,f(n)=n$, y $p=\log_{2} 4=2$. Comparamos $f(n)$ con $n^{2}$. Entonces tenemos que $f(n)=n\in O(n^{2-1}))$, es decir que se cumple el primer caso del teorema para $\varepsilon=1$, y por lo tanto 
$$
	T(n)\in \Theta(n^{2}).
$$

###### Ejemplo: caso 2
Sea $T(n)=2T(n / 2)+n$, y $T(1)=d>0$.
Parámetos: $a=2,b=2,f(n)=n$, y $p=\log_{2} 2=1$. Comparamos $f(n)$ con $n$. Entonces tenemos que $f(n)=n\in \Theta n^{1}$, es decir que se satisface el caso dos del teorema. Por lo tanto 
$$
	T(n)\in \Theta(n\log n).
$$

###### Ejemplo: caso 3
Sea $T(n)=2T(n / 4)+cn^{2}$, y $T(1)=d>0$.
Parámetros: $a=2, b=4,f(n)=cn^{2}$ y $p=\log_{4} 2= \frac{1}{2}$. Comparamos $f(n)$ con $n^{1 / 2}$. Notemos que $f(n)\in \Omega(n^{1 / 2+3 / 2})$, es decir que $\varepsilon=3 / 2$.
Además, tenemos que $af(n / b)=2\left( c \frac{n^{2}}{16} \right)=\frac{1}{8}cn^{2}\leq \frac{1}{2}  cn^{2}$, es decir que se cumple la condición que necesitabamos con $\rho=\frac{1}{2}$.
Por lo tanto tenemos que 
$$
	T(n)\in \Theta(f(n))=\Theta(n^{2}).
$$

#### Límites del teorema
Algunas formas de recurrencias que no aplican al método maestro son:

| Recurrencia                  | Por que no aplica la versión presentada          |
| ---------------------------- | ------------------------------------------------ |
| $T(n)=T(n-1)+n$              | La reducción es aditiva, no por un factor de $n$ |
| $T(n)=2^{n}T(n / 2)+n$       | El coeficiente de llamda depende de $n$          |
| $T(n)=T(n / 3)+T(2n / 3)+cn$ | Los subproblemas tienen tamaños distintos.       |
