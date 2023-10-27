# Explora la codificación en R

## Operaciones y cálculos

Los operadores, los definimos como un símbolo que designa el tipo de operación o cálculo a realizar en una fórmula.
Los operadores de asignación se usan para asignar valores a las variables y los vectores.

    sales_1 <- c(75.9, 96.55, 45.74, 65.23)

Los operadores aritméticos. Estos operadores se usan para completar cálculos matemáticos y podrían parecer familiares. Los
signos más(+) hacen sumas en las variables, y los signos menos(-) hacen restas. Usamos un asterisco(*) para hacer multiplica-
ciones y una barra inclinada(/) para hacer una división.

    x <- 1
    y <- 2
    z <- x + y
    [1] 3

## Operadores lógicos e instrucciones condicionales

Los operadores lógicos arrojan un tipo de dato lógico, cuyo valor de salida es TRUE o FALSE, con los cual entendemos que
solo tiene dos valores posibles, Existen tres tipos principales de operadores lógicos:

AND (algunas veces representado como & o && en R)

OR (algunas veces representado como | o || en R)

NOT (!)

### El operador AND (“&”)

El operador AND requiere de dos valores lógicos. El resultado es  TRUE si cada uno de los valores por separado es TRUE.
Esto significa que TRUE & TRUE dan como resultado  TRUE. Sin embargo, FALSE & TRUE, TRUE & FALSE y FALSE & FALSE arrojan
como resultado FALSE.

Si ejecutas el código correspondiente en R, obtienes los siguientes resultados

    > TRUE & TRUE
    [1] TRUE
    > TRUE & FALSE
    [1] FALSE
    > FALSE & TRUE
    [1] FALSE
    > FALSE & FALSE
    [1] FALSE

Es posible ilustrar esto mediante el uso de los resultados de nuestras comparaciones. Imagina que creas una variable x
que es igual a 10.

    x <- 10

Para revisar si x es mayor que 3 pero menor que 12, puedes utilizar

    x > 3 & x < 12

Cuando ejecutas la función, R arroja el resultado TRUE.

    [1] TRUE

TRUE La primera parte,  x > 3 dará como resultado  TRUE  ya que 10 es mayor que 3. La segunda parte, x < 12  también dará
como resultado TRUE a que 10 es menor que 12. Como ambos valores dan TRUE, el resultado de la expresión AND es TRUE. El
número 10 se ubica entre los números 3 y 12.

Sin embargo, si x es igual a 20, la expresión x > 3 & x < 12 arrojará un resultado diferente.

    x <- 20
    x > 3 & x < 12
    [1] FALSE

 Aunque x > 3 es TRUE (20 > 3), x < 12 es FALSE (20 < 12). entonces, toda la expresión dará como resultado FALSE (TRUE
 & FALSE = FALSE). De modo que el resultado de R será FALSE.

### Operador OR (“|”)

El operador OR (|) trabaja de un modo similar el operador AND (&). La diferencia principal consiste en que, al menos,
uno de los valores de la operación OR deber ser TRUE para que toda la operación OR dé como resultado TRUE. Sin embargo,
TRUE | TRUE, TRUE | FALSE, y FALSE | TRUE arrojan como resultado TRUE. Cuando ambos valores dan FALSE, el resultado es FALSE.

Si escribes el código, obtienes los siguientes resultados:

    > TRUE | TRUE
    [1] TRUE
    > TRUE | FALSE
    [1] TRUE
    > FALSE | TRUE
    [1] TRUE
    > FALSE | FALSE
    [1] FALSE

Por ejemplo, supón que creaste una variable y igual a 7. Para revisar si y es menor que 8 o mayor que 16, puedes utilizar
la siguiente expresión:

    y <- 7
    y < 8 | y > 16

El resultado comparativo es TRUE (7 es menor que 8) | FALSE (7 no es mayor que 16). Ya que un solo valor de una expresión
OR debe ser TRUE para que toda la expresión sea TRUE, R arroja como resultado TRUE.

    [1] TRUE

Ahora, imagina que y es 12. La expresión y < 8 | y > 16 ahora da FALSE (12 < 8) | FALSE (12 > 16). Ambas comparaciones
dan como resultado FALSE, de modo que es resultado es  FALSE.

    y <- 12
    y < 8 | y > 16
    [1] FALSE

### El operador NOT (“!”)

El operador NOT (!) simplemente niega el valor lógico al que se aplica. En otras palabras, !TRUE da FALSE y !FALSE da TRUE.

Cuando ejecutas el código, obtienes lo siguiente:

    > !TRUE
    [1] FALSE
    > !FALSE
    [1] TRUE

Igual que en el caso de los operadores OR y AND, puedes utilizar el operador NOT en combinación con los operadores lógicos.
Cero se considera FALSE y los números que no son cero se consideran TRUE. El operador NOT da como resultado el valor lógico
opuesto.

Imagina que tienes una variable x que es igual a 2:

    x <- 2

El operador NOT da como resultado FALSE porque toma el valor lógico opuesto de un número que no es cero (TRUE).

    > !x
    [1] FALSE

## Instrucciones condicionales

Una *instrucción condicional* es una declaración de que si una determinada condición se mantiene, entonces, debe producirse
un determinado evento. Por ejemplo, "Si la temperatura está por encima del punto de congelamiento, entonces, saldré a
caminar". Si la primera condición es verdadera (la temperatura está por encima del punto de congelamiento), entonces la
segunda condición sucederá (salir a caminar). Las instrucciones condicionales en código R tienen una lógica similar.

Veamos ahora cómo crear instrucciones condicionales en R utilizando tres instrucciones relacionadas:

### if()

La instrucción if establece una condición y si la condición arroja como resultado TRUE, el código R asociado a la ins-
trucción if se ejecuta.

    Sintaxis: if (condition) { expr si se cumple la condicion }

Por ejemplo, creemos una variable x igual a 4.

    x <- 4

Luego, creemos una instrucción condicional: si x es mayor que 0, entonces R imprimirá la cadena "x es un número positivo".

    if (x > 0) {

    print("x is a positive number")

    }

Dado que x=4, la condición es verdadera (4 > 0). Por lo tanto, cuando ejecutas el código, R imprime la cadena "x es un
número positivo".

    [1] "x is a positive number"

Pero si cambias x a un número negativo, como -4, entonces, el resultado de la condición será FALSE (-4 > 0). Si ejecutas
el código, R no ejecutará el código impreso. En su lugar, aparecerá una línea en blanco.

### else()

La instrucción else se utiliza en combinación con una instrucción if. Así se estructura el código en R:

    Sintaxis: if (condition) { expr1 si se cumple la condicion} else { expr2 si falla o no se cumple la codicion }

Por ejemplo. Primero creemos una variable x igual a 7.  

x <- 7

Ahora, establezcamos las siguientes condiciones: 

Si x es mayor que 0, R imprimirá "x es un número positivo".

Si x es menor que o igual a 0, R imprimirá "x es un número negativo o cero".

En nuestro código, la primera condición (x > 0) será parte de la instrucción if. La segunda condición de x menor que o igual a 0 queda implícita en la instrucción else. Si x > 0, R imprimirá "x es un número positivo". De otro modo, R imprimirá "x es un número negativo o cero". 

x <- 7

if (x > 0) {

 print ("x is a positive number")

} else {

 print ("x is either a negative number or zero")

}

### else if()
