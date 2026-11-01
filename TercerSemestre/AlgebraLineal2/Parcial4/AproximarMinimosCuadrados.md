#AlgebraLineal 
Supongamos que se colectan datos ${}y_{1},\dots,y_{m}{}$ en los tiempos ${}t_{1},\dots,t_{m}{}$ respectivamente. Si tenemos las parejas ${}(t_{i},y_{i}){}$, ${}1\leq i\leq m{}$, y suponemos una relación lineal entre ${}y{}$ y ${}t{}$, es decir ${}y=ct+d{}$, lo que queremos hacer es encontrar las constantes ${}c{}$ y ${}d{}$ de modo que la recta aproxime de la mejor forma posible a los datos recabados.
Una forma de estimar que tan buena es una aproximación dados ${}c{}$ y ${}t{}$, es tomar el error como la suma de los cuadrados de las distancias verticales entre los puntos de los datos recabados y la recta aproximada, es decir 
$$
E=\sum_{i=1}^{m}(y_{i}-ct_{i}-d)^{2}.
$$
De este modo, lo que queremos encontrar son ${}c{}$ y ${}d{}$ que minimicen ${}E{}$.