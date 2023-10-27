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

*El operador AND (“&”):*

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
