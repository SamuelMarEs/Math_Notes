##### Definición:
La ***abstracción*** es un proceso mental que consiste en aislar propiedades o conceptos esencia les de un objeto, separándolo de sus detales particulares y del contexto. 
En ciencias de la computación, es el principio fundamental que consiste en ocultar detalles complejos y mostrar únicamente las características o funcionalidades esenciales de un objeto o sistema.
Se pueden abstraer *datos* y *procedimientos*.

##### Definición:
Un ***dato*** es una unidad de información que un programa puede representar, almacenar, transmitir o procesar.
El ***tipo de dato*** determina el conjunto de valores posibles y las operaciones que se pueden realizar.

Los datos  en Python pueden distinguirse por su origen en:
- Incorporados: ya forman parte de Python.
- Definidos por el usuario: los crea el programador para representar conceptos propios del problema. Por ejemplo una `class` específica es un ejemplo de un dato definido por el usuario.

##### Definición:
Una ***estructura de datos*** (ED) es una representación organizada de un conjunto de información.
Pueden ser
- Lineales: sus elementos forman una sola secuencia.
- No lineales: sus elementos no forman una única secuencia posicional; pueden organizar de diferentes formas.
Además, según si su estado puede cambiar pueden ser ser
- Mutables: permiten modificar el contenido del objeto.
- Inmutables: su estado no puede modificarse; una operación prodcue un objeto nuevo. 
Algunas operaciones freuentes son:
- Consulta: acceder, buscar o recorrer elementos.
- Transformación: insertar, eliminar o modificar elementos.

Algunos ejemplos en Python son `list`, `tuple`, `dict`, y `set`, que son a su vez estructuras de datos y tipos de datos incorporados al mismo tiempo.

##### Definición:
Un ***TDA*** (tipo de dato abstracto) especifica los estados válidos, las operaciones disponibles y las reglas que determinan su comportamiento, sin establecer cómo se representa o implementa.