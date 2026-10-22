# Propuesta proyecto final
Samuel Márquez Estrada y Emiliano Panuncio Almaraz Gonzalez.

---
#### Propuesta e interés
***Limit Order Book:*** 
Un libro de órdenes limitadas (LOB por sus siglas en inglés) en un registro que lleva una bolsa de valores para organizar las acciones (compras (bids) y ventas (offers)) de una determinada acción, y sus transacciones.
El libro da prioridad a la oferta de compra más alta, y la oferta de compra más baja.
Los componentes del libro son:
- Lados: lista de compras y lista de ventas.
- Spread (diferencial): diferencia entre la oferta de compra más alta (best bid) y la oferta de compra más baja (best ask).
- Motor de emparejamiento: empareja de forma automática las ofertas entrantes con las que ya están en el libro por prioridad precio-tiempo

---
#### Funcionamiento previsto
Se esperarían $N$ entradas de la siguiente forma:

| Campo           | Significado                                                           | Ejemplo             |
| --------------- | --------------------------------------------------------------------- | ------------------- |
| id (str)        | Identificador de la oferta                                            | "C1", "V1", "V2"    |
| lado (str)      | Tipo de oferta (compra o venta)                                       | "compra", "venta"   |
| precio (float)  | Precio ofertado de compra o venta                                     | 101.1, 200.1, 67.67 |
| cantidad (int)  | Numero de acciones que se quiere comprar o vender                     | 67, 100, 200, 25    |
| timestamp (int) | Orden de llegada de las ofertas (para diferenciar cual llega primero) | 1, 2, 3, ...        |
Posteriormente, el programa regresaría una lista de transacciones, así como el estado actual del libro.
Ejemplo de funcionamiento
```Entrada
3
V1 venta 101.0 200 1
V2 venta 100.5 100 2
C1 compra 101.0 250 3
```
La salida de transacciones tendría un formato en forma: `comprador, vendedor, precio, cantidad`
```Salida
Transacciones:
C1 V2 100.5 100
C1 V1 101.0 150
Estado del libro:
best_bid = None        # no quedan ofertas de compra
best_ask = 101.0       # mejor precio de venta disponible
asks = [101.0, 50]     # quedan 50 acciones de V1 en el libro
```

---
#### Contenido del curso
- Heaps: un max-heap de precios de compra y un min-heap de precios de venta.
- Colas: ordenada por orden de llegada, usando el principio FIFO.
- Diccionario (hash map)

---
#### Declaración de IA
Usamos IA (Deepseek y Claude) para generar una lluvia de ideas de proyecto que se alinearan con nuestro interés. Posteriormente, usamos nuevamente Claude para organizar la idea de forma más ordenada (ejemplos de entrada y salida, así como una idea de los contenidos del curso que podríamos usar).

