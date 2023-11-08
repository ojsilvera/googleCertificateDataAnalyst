# Observar los datos con mas detalle

## mismos datos diferentes resultados

El cuarteto de Anscombe. El cuarteto de Anscombe tiene cuatro conjuntos de datos con estadísticas de resumen casi idén-
ticas. Pero esas estadísticas de resumen podrían ser engañosas. Las visualizaciones de datos, especialmente para conjuntos
de datos como estos, son muy importantes. Ayudan a descubrir detalles en nuestros datos que de otra forma permanecerían
ocultos. Además, descubrirás algunas de las formas en que R puede crear visualizaciones maravillosas.

datasauRus paquete de visualizacion para cuartetos de datos que parecen similares en las ltablas pero diferieren entre
ellos realmente

## Función de sesgo

En R, en realidad podemos cuantificar el sesgo comparando el resultado real de nuestros datos con el resultado previsto.
Hay una explicación estadística bastante compleja detrás de esto. Sin embargo, con la *función bias* en R, no tienes que
hacer este cálculo en forma manual. Básicamente, *la función bias* calcula el monto promedio en que el resultado real
supera al resultado previsto.

sintaxys

    bias(resultado_obtenido, resultadoprevisto)

ejemplo

    actual_temp <- c(68.3, 79, 72.4, 71, 67, 70)
    predictive_temp <- c(67, 69, 71.5, 70, 67, 69)
    
    bias(actual_temp, predictive_temp)

el resultado obtenido debe encontrase muy cercano a cero, sindo cero el resultado ideal, esto es tanto para reultados
positivos ocmo negativos

## Trabajar con datos sesgados
