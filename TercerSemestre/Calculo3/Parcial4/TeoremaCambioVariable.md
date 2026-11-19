#Calculo #Teorema 
#### Determinante del Jacobiano
Sea ${}T:D^{*}\to \mathbb{R}^{2}{}$ una transformación ${}C^{1}{}$ dada por ${}T(u,v)=(x(u,v),y(u,v)){}$. El determinante del Jacobiano es 
$$
\det J(u,v)=\frac{\partial(x,y)}{\partial(u,v)}=\det \begin{bmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{bmatrix}.
$$

#### Teorema de cambio de variable
Si tenemos ${}T(u,v)=(x(u,v),y(u,v)){}$ con ${}(u,v)\in D^{*}\subseteq \mathbb{R}^{2}{}$. Si además tenemos ${}f:D\subseteq\mathbb{R}^{2}\to \mathbb{R}{}$ y ${}T(D^{*})=D{}$.

##### Ejemplo
Sean ${}D=\{ (x,y):x^{2}+y^{2}\leq 1 \}{}$, ${}f(x,y)=1{}$ y ${}T(r,\theta)=(r\cos \theta,r\sin \theta){}$. Entonces 
$$
\iint_{D}f(x,y)dxdy=\iint_{D^{*}}f(x(r,\theta),y(r,\theta))d
$$