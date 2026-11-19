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
##### Ejemplos
1.- Sean ${}D=\{ (x,y):x^{2}+y^{2}\leq 1 \}{}$, ${}f(x,y)=1{}$ y ${}T(r,\theta)=(r\cos \theta,r\sin \theta){}$. Entonces 
$$
\iint_{D}f(x,y)dxdy=\iint_{D^{*}}f(x(r,\theta),y(r,\theta))\lvert J(r,\theta) \rvert d r d\theta=\iint_{D^{*}}r d r d\theta=\int_{0}^{2\pi}\int_{0}^{1}r d r d\theta
$$
lo cual nos da como resultado ${}\pi{}$, el área del círculo de radio 1 (${}D{}$).

2.- Sea ${}x=u^{2}-v^{2}{}$ y ${}y=2uv{}$, encontrar la imagen de ${}S=\{ (u,v)\in \mathbb{R}^{2} :0\leq u,v\leq 1\}{}$.
