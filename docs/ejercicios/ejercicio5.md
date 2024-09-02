# Ejercicio 5 - [nombre del ejercicio]

## Descripción

Su hermano menor está aprendiendo sobre la ley de la oferta y la demanda en la escuela. Como deber le pidieron que haga de cuenta que tiene un negocio y que le venda cosas a la familia. El problema que tiene que es distraido y no sabe cuánto cobrar por cada cosa. Usted tiene que ayudarlo, pero decide hacerle una maldad y le explica que la ley de la oferta y la demanda significa que cuanto más cosas tenga para vender, más caro puede venderlas.

Su hermano va a vender caramelos de distintos tipos y usted le dice que el precio de cada caramelo es igual a la cantidad de caramelos que tiene de ese tipo. Cada orden consiste en una cantidad de caramelos deseada, pero no se puede elegir cuántos caramelos de cada tipo se quieren. El objetivo es maximizar el precio total de la orden.

Aclaracion: Cada caramelo se vende de a uno, es decir que si tengo solo 3 chocolates y me piden una orden de 3 caramelos, la orden vale 6. Esto es porque el primero cuesta 3, el segundo 2 y el tercero 1.

## Entrada

La entrda se recibe en el siguiente formato:

- La primera línea contiene un entero `N`, que indica la cantidad de tipos de caramelos que hay.
- Las siguientes `N` líneas contienen un entero `C` que indica la cantidad de caramelos de ese tipo.
- La siguiente línea contiene un entero `M`, que indica la cantidad de órdenes que se van a hacer.
- Las siguientes `M` líneas contienen un entero `O` que indica la cantidad de caramelos de la orden.

## Salida

La salida debe contener M líneas, cada una con un entero que indica el precio total de la orden correspondiente.

## Restricciones

- $1 \leq N \leq 10^5$
- $1 \leq M \leq 10$

- $O(N\ logN)_{cp}$
- $O(N^2)_{pc}$

## Ejemplo

### Input

```plaintext
3
3
4
2
2
3
1
```

### Output

```plaintext
10
2
```

### Explicación

Cuento con 3 tipos distintos de caramelos. Digamos que tengo 3 chocolates, 4 de frutilla y 2 de menta.

A la primer orden le doy:

 1. 1 de frutilla por $4
    - Como tengo 1 menos de frutilla, ahora cuesta $3
 2. 1 de frutilla por $3
    - Como tengo 1 menos de frutilla, ahora cuesta $2
 3. 1 de chocolate por $3
    - Como tengo 1 menos de chocolate, ahora cuesta $2

Total: $10

A la segunda orden le doy:

 1. 1 de menta por $2
    - Como tengo 1 menos de menta, ahora cuesta $1
