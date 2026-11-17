#AlgebraLineal 
Recordemos de secciones anteriores que, sea ${}V=W_{1}\oplus W_{2}{}$, entonces un operador lineal ${}T{}$ sobre ${}V{}$ es la **proyección** de ${}W_{1}{}$ **a lo largo de** ${}W_{2}{}$ si, para ${}x=x_{1}+x_{2}{}$ donde ${}x_{1}\in W_{1}{}$ y ${}v_{2}\in W_{2}{}$, se tiene que ${}T(x)=x_{1}{}$.  Se tiene a partir de esto que ${}R(T)=W_{1}{}$ y ${}N(T)=W_{2}{}$, de modo que tenemos que ${}V=R(T)\oplus N(T){}$. Además, se puede demostrar que ${}T{}$ es una proyección si y sólo si ${}T=T^{2}{}$. Como ${}V=W_{1}\oplus W_{2}=W_{1}\oplus W_{3}{}$ no implica que ${}W_{2}=W_{3}{}$, podemos ver que ${}W_{1}{}$ no describe de forma única a ${}T{}$. Sin embargo, si ${}T{}$ es una ***proyección ortogonal***, entonces esta determinada únicamente por su rango:
#### Definición:
Sea ${}V{}$ un espacio de producto interno, y sea ${}T:V\to V{}$ una proyección. Decimos que ${}T{}$ es una ***proyección ortogonal*** si ${}R(T)^{\perp}=N(T){}$ y ${}N(T)^{\perp}=R(T){}$.
Si ${}V{}$ es de dimensión finita, entonces basta con una sola de las condiciones. 

Sea ${}W{}$ un subespacio de dimensión finita de ${}V{}$, previamente habíamos definido la proyección ortogonal de un vector ${}y{}$ sobre ${}W{}$ como ${}T(y)=u{}$, para ${}y=u+z{}$ donde ${}z\in W^{\perp}{}$, y no es dificil mostrar que esta transformación ${}T{}$ es una proyección ortogonal bajo esta nueva definición. Además, se puede mostrar que la proyección ortogonal de ${}V{}$ sobre ${}W{}$ es única.

#### Teorema 6.24
Sea ${}V{}$ un espacio de producto interno, y sea ${}T{}$ un operador lineal sobre ${}V{}$. Entonces ${}T{}$ es una proyección ortogonal si y sólo si ${}T{}$ tiene un [[OperadorAdjunto|adjunto]] ${}T^{*}{}$ y ${}T^{2}=T=T^{*}{}$.

Me da hueva escribir la demostración, y dudo que sea muy útil, entonces así se queda.