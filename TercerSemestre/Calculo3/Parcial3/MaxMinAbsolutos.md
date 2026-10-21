#Calculo 
#### Definición:
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ definida para $A\subset\mathbb{R}^{n}$. Si $x_{0}\in A$ y $f(x_{0})\geq f(x)\forall x\in A$, entonces decimos que en $x_{0}$ se alcanza un máximo absoluto.
Análogamente, si $f(x_{0})\leq f(x)\forall x\in A$, decimos que en $x_{0}$ se alcanza un mínimo absoluto. 
Otro nombre son mínimos y máximos globales.

#### Definiciones:
Sea $D\subset\mathbb{R}^{n}$, decimos que $D$ es ***cerrado*** si $D^{c}$ es abierto.
Sea $D\subset\mathbb{R}^{n}$, decimos que es ***acotado*** si existe $M>0$ tal que $\lvert \lvert x \rvert \rvert\leq M,\quad\forall x\in D$.
Sea $D\subset\mathbb{R}^{n}$ decimos que $x\in D$ es un ***punto límite*** o ***punto frontera*** si para cada $\varepsilon>0$, $B_{\varepsilon}(x)\cap D\neq \emptyset$ y $B_{\varepsilon}(x)\cap D^{c}\neq \emptyset$. Es decir que, cualquier bola centrada en $x$ contiene un punto dentro y un punto afuera del conjunto.

#### Teorema
Sea $f:\mathbb{R}^{n}\to\mathbb{R}$ una función continua en un conjunto cerrado y acotado $D$, entonces $f$ tiene un valor máximo absoluto y un valor mínimo absoluto.