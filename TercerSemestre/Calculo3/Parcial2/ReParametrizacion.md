#Calculo #Geometria 
#### Definición:
Una función de $f:\mathbb{R}\to\mathbb{R}$ es ***suave*** si existen 
$$
	\frac{df}{dx}, \frac{d^{2}f}{x^{2}}, \frac{d^{3}f}{dx^{3}},\dots, \frac{d^{n}f}{dx^{n}},\dots
$$
es decir que existe la derivada $\frac{d^{n}f}{dx^{n}},\forall n\in\mathbb{N}$.
Entonces, decimos que una curva es suaves si existen 
$$
	\frac{d^{m}}{dt^{m}}x_{i}(t),\quad i=1,\dots,n,\quad\forall m\in\mathbb{N}.
$$
Es decir, si existen todas las derivadas para las funciones componentes.

#### Definición:
Una función $\gamma:(\alpha,\beta)\to\mathbb{R}^{n}$ es una ***reparametrización*** de la curva $c:(a,b)\to\mathbb{R}^{n}$ si existe una función biyectiva $\phi(\alpha,\beta)\to(a,b)$ tal que $\phi ^{-1}:(a,b)\to(\alpha,\beta)$ es suave, y $$\gamma(\tau)=c(\phi (\tau)),\quad\forall \tau\in(\alpha,\beta).$$
Observemos que para $t\in(a,b)$:
$$
	\gamma(\phi ^{-1}(t))=c(\phi(\phi ^{-1}(t)))=c(t).
$$
##### Ejemplo:
Sea $c(t)=(\cos t,\sin t)$ el círculo de radio 1. Sea $\phi(\tau)=\frac{\pi}{2}-\tau$, entonces tenemos que 
$$
	\begin{align}
	\gamma(\tau)=(\cos \phi \tau,\sin \phi \tau)&=\left(\cos \left( \frac{\pi}{2}-\tau \right),\sin\left( \frac{\pi}{2}-\tau \right)\right)  \\
	&=(\sin \tau,\cos \tau).
	\end{align}
$$
De modo que encontramos una reparametrización para nuestra curva.

#### Definición:
Si $c:\mathbb{R}\to\mathbb{R}^{n}$ es una curva, un punto $c(t_{0})$ se llama ***regular*** si $c'(t_{0})\neq 0$. Si todos los puntos $c(t)$ son regulares, entonces la curva es regular.

#### Proposición:
Si $\gamma$ es una reparametrización de una cruva regular $c(t)$, entonces la reparametrización es regular.
##### Demostración:
Por demostrar que $\gamma'(\tau)\neq 0$ para toda $\tau$.
Sean $t=\phi(\tau)$ y $\psi=\phi ^{-1}$, y por lo tanto $\tau=\psi(t)$. Entonces tenemos que $\phi(\tau)=\phi(\psi(\tau))=t$. La definición de reparametrización nos asegura que estas funciones sean suaves, y por lo tanto son derivables. Entonces, podemos derivar para obtener que 
$$
	\frac{d}{dt}\phi(\tau)= \frac{d\phi}{d\tau} \frac{d\psi}{dt}
$$
y además sabemos que $\frac{d}{dt}\phi(\tau)=\frac{d}{dt}t=1$, es decir que 
$$
	\frac{d\phi}{d\tau}\neq 0\quad\text{y}\quad \frac{d\psi}{dt}\neq 0.
$$
Entonces, como $\gamma$ es una reparametrización, tenemos que $\gamma(\tau)=c(\phi(t))$ , entonces
$$
	\frac{d}{d\tau}\gamma(\tau)=\frac{dc}{dt} \frac{d\phi}{d\tau}
$$
donde ambas derivadas de la derecha son distintas de cero, y por lo tanto 
$$
	\frac{d}{d\tau}\gamma(\tau)\neq 0\quad\forall \tau.
$$

#### Proposición:
Si $c(t)$ es una curva regular, entonces 
$$
	s(t)=\int_{\alpha}^{t}\lvert \lvert c'(\tau) \rvert  \rvert d\tau 
$$
la función [[LongitudDeArco|longitud de arco]] es suave para $\alpha\in(a,b)$.
##### Demostración:
Sabemos por el Teorema Fundamental del Cálculo, 
$$
	\begin{align}
	\frac{d}{dt}s(t)=\lvert \lvert c'(t) \rvert  \rvert =\sqrt{ (x_{1}'(t))^{2}+\dots+(x_{n}'(t))^{2} },
	\end{align}
$$
por lo tanto la primera derivada existe.
Sabemos que $f(x)=\sqrt{ x }$ es suave en $(0,\infty)$. Se puede demostrar por inducción que 
$$
	\frac{d^{n}f}{dx^{n}}=(-1)^{n-1} \frac{1\cdot 3\cdot\dots \cdot(2n-3)}{2^{n}}x^{-\frac{2n-1}{2}}
$$
para $n\geq 2$.
Entonces tenemos que 
$$
	\frac{d}{dt}s(t)= f(x_{1}'(t)^{2}+\dots+s
	x_{n}'(t)^{2})
$$
es la composición de dos funciones diferenciables, y ambas son suaves, la $n$-ésima derivada existe para ambos casos. Por lo tanto la función longitud de arco es suave.

#### Proposición:
Una curva tiene una parametrización por longitud de arco si y sólo si es regular.
##### Demostración:
$\Rightarrow)$ Si $c(t)$ tiene una parametrización por longitud de arco $\gamma$, entonces existe $\phi$ tal que $t=\phi(\tau)$,  es decir que $c(t)=c(\phi(\tau))=\gamma(\tau)$. 
Por regla de la cadena, tenemos que 
$$
	\frac{d\gamma}{d\tau}=\frac{dc}{dt} \frac{dt}{d\tau},
$$
y si tomamos la norma, tenemos que 
$$
	\lvert \lvert \frac{d\gamma}{d\tau} \rvert  \rvert =\lvert \lvert \frac{dc}{dt} \rvert  \rvert \lvert \lvert  \frac{dt}{d\tau} \rvert  \rvert .
$$
Como por hipótesis $\lvert \lvert \gamma' \rvert \rvert=1$ (por ser una parametrización por longitud de arco), entonces tenemos que $\lvert \lvert c'(t) \rvert \rvert \neq 0$, por lo tanto $c'(t)\neq 0$, es decir que es regular.

($\Leftarrow$ Si $c(t)$ es regular, sabemos que la función longitud de arco $s(t)$ es suave, y que 
$$
	\frac{ds}{dt}=\lvert \lvert c'(t) \rvert  \rvert >0.
$$
Como $c(t)$ es regular, o $c(t)$ es estrictamente creciente, o estrictamente decreciente, y por lo tanto $s(t)$ es estrictamente creciente y continua, por lo tanto es inyectiva.
Por lo tanto, sea $s:(a,b)\to\mathbb{R}$, tomemos $(\alpha,\beta)=s(a,b)$, de modo que podemos definir la inversa $s ^{-1}:(\alpha,\beta)\to(a,b)$. Llamemos a la inversa $\phi=s ^{-1}$, correspondiente a la reparametrización $\gamma$.
Entonces tenemos que 
$$
	\gamma(s)=c(t)\Rightarrow \frac{d\gamma}{ds} \frac{ds}{dt}= \frac{dc}{dt}.
$$
Entonces si tomamos la norma, tenemos que 
$$
	\left\lvert  \left\lvert  \frac{d\gamma}{ds}  \right\rvert   \right\rvert \frac{ds}{dt}=\left\lvert  \left\lvert  \frac{dc}{dt}  \right\rvert   \right\rvert ,
$$
pero como $s(t)$ es la longitud de arco, tenemos que $s'(t)=\lvert \lvert c'(t) \rvert \rvert$, y por lo tanto tenemos que 
$$
	\left\lvert  \left\lvert  \frac{d\gamma}{ds}  \right\rvert   \right\rvert =1,
$$
es decir que $\gamma$ es una parametrización por longitud de arco. $\quad\square$
