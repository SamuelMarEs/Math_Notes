Una clase nos permite definir nuestro propio [[TDA]].
- `class` es una plantilla que nos permite definir atributos y métodos de nuestro tipo de dato abstracto.
- `object` es una instancia concreta de una clase en específico.
- El *estado* es información interna en un momento dado. El estado actual de los atributos.

Al trabajar con nuestras propias clases, a menudo es importante tener en cuenta las *pre-condiciones* y *post-condiciones*. 
Las pre-condiciones son aquellas que se deben de cumplir para que un método específico pueda ejecutarse.
Por otro lado, las post-condiciones son aquellas que se deben cumplir después de ejecutar una operación, siempre y cuando las pre-condiciones fueran válidas.

#### Interfaz pública vs. representación interna
La *interfaz pública* es lo que el usuario debe usar. Los métodos, que son accesibles para el usuario.
Por otro lado la *representación interna* son los elementos que la clase utiliza para funcionar correctamente. Los atributos, detalles de almacenamiento y decisiones de implementación.

#### Encapsulamiento:
Encapsular significa ocultar los detalles internos de una implementación y exponer solo una interfaz clara.
En `Python`, se suele usar un guión bajo para indicar que un atributo es interno. Sin embargo, esto no prohíbe el acceso y es sólo una convención.

#### Acoplamiento:
El acoplamiento mide cuánto depende un componente de las decisiones de otro componente.
*Alto acoplamiento* es cuando se accede directamente a la representación interna.
Por otro lado, un *bajo acoplamiento* es cuando un método únicamente depende de la interfaz pública, sin necesidad de acceder al estado interno del objeto.
Por ejemplo, consideremos un TDA que represente un punto en el plano, ya sea de forma cartesiana
```Python
self._x = x
self._y = y

def disance_to_origin(self):
	return (self._x**2 + self._y**2)**0.5
```
o de forma polar
```Python
self._r = hypot(x, y)
self._theta = atan2(y, x)

def distance_to_origin(self):
	return self._r
```

Un ejemplo de código que muestre la distancia al origen de un punto es el siguiente:
***Alto acoplamiento***
```Python
def show_distance(p):
	d = (p._x**2 + p._y**2)**0.5
	print(d)
```
***Bajo acoplamiento***
```Python
def show_distance(p):
	print(p.distance_to_origin())
```

#### Cohesión
La cohesión mide que tan enfocada está una clase o módulo en una responsabilidad clara.
Una *alta cohesión* implica que la clase se encarga de una función en específico.
Una *baja cohesión* indicaría que la clase puede hacer muchas otras cosas o tiene muchas funciones no esenciales para su funcionamiento.
Se recomienda que el diseño de código tenga una **alta cohesión**.
###### Principio:
Cada componente del código debe tener una responsabilidad principal y bien delimitada.


#Algoritmos 