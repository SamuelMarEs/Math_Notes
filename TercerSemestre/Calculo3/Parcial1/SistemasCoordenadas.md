### Coordenadas rectangulares
Para $R^{2}$ tenemos la tipicas $(x,y)$, mientras que si estamos trabajando en $R^{3}$ tenemos $(x,y,z)$. Estas coordenadas son respecto a los ejes coordenados y no tienen nada de nuevo.

### Coordenadas polares ($R^{2}$)
Las coordenadas polares $(r,\theta)$ se relacionan con las rectangulares de la forma 
$$
	x=r\cos \theta,\quad y=r\sin\theta.
$$

![[CoordenadasPolares]]

De forma inversa, dadas las coordenadas polares $(r,\theta)$, podemos volver a las rectangulares mediante 
$$
	r=\sqrt{ x^{2}+y^{2} },\quad \theta=\arctan\left( \frac{y}{x} \right).
$$

### Coordenadas cilindricas ($R^{3}$)
Se relacionan con $(x,y,z)$ de forma casi identica a las coordenadas polares, pero considerando una tercera coordenada, la altura.
Dadas las coordenadas rectangulares, tenemos 
$$
	x=r\cos \theta,\quad y=r\sin \theta,\quad z=h.
$$
Por otro lado, dadas las coordenadas cilindricas $(r,\theta,h)$, podemos pasar a rectangulares mediante 
$$
	r=\sqrt{ x^{2}+y^{2} },\quad \theta=\arctan\left( \frac{y}{x} \right),\quad \theta=z.
$$

### Coordenadas esféricas ($R^{3}$)
Así como las coordenadas polares se pueden ver como una transformación de $R^{2}$ en círculos, las coordenadas esféricas lo expanden a $R^{3}$, relacionando las coordenadas con puntos en una esfera.
Dadas las coordenadas rectangulares $(x,y,z)$, pasamos a las esféricas mediante 
$$
	\rho=\sqrt{ x^{2}+y^{2}+z^{2} },\quad \theta= \arctan\left( \frac{y}{x} \right),\quad\phi=\arctan\left( \frac{r}{z} \right),\quad r=\sqrt{ x^{2}+y^{2} }.
$$
Las coordenadas esféricas son la terna $(\rho,\theta,\phi)$.
![[CoordenadasEsfericas]]
De forma inversa, podemos obtener las coordenadas rectangulares mediante 
$$
	r=\rho \sin \phi,\quad x=\rho \sin \phi \cos \theta,\quad y=\rho \sin \phi \sin \theta,\quad z=\rho \cos \phi.
$$


#Calculo #Geometria
