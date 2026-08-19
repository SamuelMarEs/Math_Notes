[[TDA]] = Tipos de Datos Abstractos.
- Datos: valores que entran al programa y objetos que se crean.
- Control: orden de ejecución, decisiones y repeticiones.
- Estado: información que puede cambiar durante la ejecución.
- Resultado: valores devueltos, impresos.

Algunos tipos de datos en Python son:
~~~python
attempts = 3      # tipo int
student = "Ana"   # tipo str
values = [2, 4]   # tipo list
value = True      # tipo bool
price = 12.5      # tipo float
~~~

### Objetos inmutables y mutables
Un objeto inmutable es aquel que no cambia. Por ejemplo los valores tipo `int` no se pueden cambiar. El valor interno no cambia. Algunos ejemplos son `int`, `float`, `bool`, `str`. Las operaciones producen otro resultado.

Un objeto mutable, se puede modificar sobre la marcha. Se puede alterar. Por ejemplo, una lista `list`. El estado interno puede cambiar mediante operaciones que modifiquen al objeto. Ejemplos son `list`, `dict`.

### Colecciones integradas en Python
~~~python
lista = [2,4,6]             # por posicion
tupla = (2,4,6)             # por posicion
diccionario = {."na":8}     # por insercion
conjunto = {2,4,6}          # sin posicion
~~~

### Operadores lógicos
Los operadores lógicos en python son 
~~~python
and # ambas condiciones son verdaderas
or  # al menos una de las condiciones es verdadera
not # ninguna de las condiciones es verdadera
~~~
Python evalua primero `not`, después `and`, y por último `or`.

### Mutabilidad y aliasing
***Mutabilidad*** es una propiedad de un objeto: indica si su esado interno puede cambiar sin sustituirlo por otro objeto. Es lo que nos dice si el objeto es inmutable o mutable.
***Aliasing*** es una relación entre nombres: ocurre cuando dos o más nombres están asociados con el mismo objeto.
El resultado no implica mutabilidad y la mutabiidad no implica aliasing.



