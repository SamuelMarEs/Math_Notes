#Calculo #Teorema 
#### Determinante Jacobiano
Sea ${}T:D^{*}\to \mathbb{R}^{2}{}$ una [[TransformacionesEnR2|transformación]] ${}C^{1}{}$ dada por ${}T(u,v)=(x(u,v),y(u,v)){}$. El determinante Jacobiano o únicamente Jacobiano, es el determinate de la matriz derivada:
$$
J(u,v)=\frac{\partial(x,y)}{\partial(u,v)}=\det \begin{bmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{bmatrix}.
$$
Si tomamos por ejemplo ${}T(r,\theta)=(r\cos \theta,r\sin \theta){}$, no es difícil de ver que ${}{}$

#### Teorema de cambio de variable
Si tenemos ${}T(u,v)=(x(u,v),y(u,v)){}$ con ${}(u,v)\in D^{*}\subseteq \mathbb{R}^{2}{}$. Si además tenemos ${}f:D\subseteq\mathbb{R}^{2}\to \mathbb{R}{}$ y ${}T(D^{*})=D{}$. Entonces 
$$
\iint_{D}f(x,y)dxdy=\iint_{D^{*}}f(x(u,v),y(u,v))\lvert J(u,v) \rvert dudv.
$$
(Aquí ${}f(x(u,v),y(u,v))=f(T(u,v)){}$ la composición de ${}f{}$ con ${}T{}$, y ${}J(u,v){}$ es el Jacobiano)
##### Demostración Barroca
Tomemos un rectángulo ${}D^{*}=[u_{0},u]\times[v_{0},v]{}$ con lados de tamaño ${}\Delta u=u-u_{0}{}$ y ${}\Delta v=v-v_{0}{}$, con área ${}A(D^{*})=\Delta u\Delta v{}$. (${}u,v{}$ no son fijos, son variables).
Sea ${}T:\mathbb{R}^{2}\to \mathbb{R}^{2}{}$ una transformación que mande ${}T(u_{0},v_{0})=(x_{0},y_{0}){}$, ${}T(D^{*})=D{}$,
y que además sea ${}C^{1}{}$.
Tomemos los lados del rectángulo ${}(u,v_{0}){}$ y ${}(u_{0},v){}$, cuyas imágenes van a dar a parar a las curvas que representan la “frontera” de ${}D{}$, es decir las curvas ${}\gamma(u)=T(u,v_{0}){}$, ${}\beta(v)=T(u_{0},v){}$. Estas curvas se pueden aproximar mediante los vectores tangente ${}\gamma’(u)=T_{u}(x_{u}(u,v_{0}),y_{u}(u,v_{0})){}$ y ${}\beta’(v)=T_{v}(x_{v}(u_{0},v),y_{v}(u_{0},v)){}$. 
Observemos que 
$$
T_{u}(u_{0},v_{0})=\lim_{ \Delta u \to 0 }  \frac{T(u_{0}+\Delta u,v_{0})-T(u_{0},v_{0})}{\Delta u},
$$
por lo que para ${}\Delta u{}$ chiquito, podemos aproximar 
$$
\Delta uT_{u}(u_{0},v_{0})\approx T(u_{0}+\Delta u,v_{0})-T(u_{0},v_{0}),
$$
y de forma análoga tenemos que para ${}\Delta v{}$ chiquito se llega a
$$
\Delta vT_{v}(u_{0},v_{0})\approx T(u_0,v_{0}+\Delta v)-T(u_{0},v_{0}).
$$
Tomemos el paralelogramo formado por estos dos vectores: ${}\mathcal{P}=\{ T(u_{0},v_{0})+t\gamma’(u)+s\beta’(v):0\leq t,s\leq 1 \}{}$. Entonces el área de ${}\mathcal{P}$ es una aproximación del área de ${}D{}$. En particular, los vectores que queremos son los vectores ${}\gamma’(u_{0}){}$ y ${}\beta’(v_{0}){}$.
El área de este paralelogramo se puede calcular de la forma $${}\Delta A\approx\lVert (\Delta u\gamma´(u_{0}),0)\times \Delta v(\beta’(v_{0}),0)\rVert=\lVert \Delta u(x_{u}(u_{0},v_{0}),y_{u}(u_{0},v_{0}),0)\times \Delta v(x_{v}(u_{0},v_{0}),y_{v}(u_{0},v_{0}),0) \rVert {}.$$
Esto, calculando el producto cruz, es lo mismo que 
$$
\begin{aligned}
\Delta A&\approx\Delta u\Delta v\lVert (0,0,x_{u}(u_{0},v_{0})y_{v}(u_{0},v_{0})-x_{v}(u_{0},v_{0})y_{u}(u_{0},v_{0})) \rVert \\
&=\Delta u\Delta v\lvert J(u_{0},v_{0}) \rvert .
\end{aligned} 
$$
Además, recordemos que la [[Integral_de_rectangulo|integral doble]] está definida como 
$$
\int_{D^{*}}f(x,y)dA=\lim_{ m,n \to \infty }\sum_{i=1}^{n}\sum_{j=1}^{m}f(c_{ij})\Delta A 
$$
y por lo tanto 
$$
\begin{aligned}
\iint_{D}f(x(u,v),y(u,v))\lvert J(u,v) \rvert dudv&=\lim_{ m,n \to \infty } \sum_{i=1}^{n}\sum_{j=1}^{m}f(x(u_{ij},v_{ij}),y(u_{ij},v_{ij}))\Delta u\Delta v\lvert J(u,v) \rvert \\
&=\int_{D^{*}}f(x,y)dA.
\end{aligned} 
$$


##### Ejemplos
1.- Sean ${}D=\{ (x,y):x^{2}+y^{2}\leq 1 \}{}$, ${}f(x,y)=1{}$ y ${}T(r,\theta)=(r\cos \theta,r\sin \theta){}$. Entonces 
$$
\iint_{D}f(x,y)dxdy=\iint_{D^{*}}f(x(r,\theta),y(r,\theta))\lvert J(r,\theta) \rvert d r d\theta=\iint_{D^{*}}r d r d\theta=\int_{0}^{2\pi}\int_{0}^{1}r d r d\theta
$$
lo cual nos da como resultado ${}\pi{}$, el área del círculo de radio 1 (${}D{}$).

2.- Sea ${}x=u^{2}-v^{2}{}$ y ${}y=2uv{}$, encontrar la imagen de ${}S=\{ (u,v)\in \mathbb{R}^{2} :0\leq u,v\leq 1\}{}$.
Tenemos que ${}T(S)=\{ (x,y)\in \mathbb{R}^{2}: -1\leq x\leq 1,0\leq y\leq2\}{}$.