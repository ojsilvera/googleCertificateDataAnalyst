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
supera al resultado previsto. Está incluido en el paquete de diseño Sim.

sintaxys

    bias(resultado_obtenido, resultado_previsto)

ejemplo

    actual_temp <- c(68.3, 79, 72.4, 71, 67, 70)
    predictive_temp <- c(67, 69, 71.5, 70, 67, 69)
    
    bias(actual_temp, predictive_temp)

el resultado obtenido debe encontrase muy cercano a cero, sindo cero el resultado ideal, esto es tanto para reultados
positivos ocmo negativos

## Trabajar con datos sesgados

Todo analista de datos encontrará un elemento de sesgo en algún momento del proceso de análisis de datos. Por eso es tan
importante saber cómo identificar y gestionar los datos sesgados siempre que sea posible. Tal vez recuerdes que exploramos
el sesgo en detalle en el curso 3 de este programa. En esta lectura, leerás un ejemplo de la vida real de un analista que
descubrió un sesgo en sus datos, y aprenderás cómo utilizó R para solucionarlo.

### Cómo abordar los datos sesgados con R

Este escenario fue compartido por un analista cuantitativo que recopila datos de personas de todo el mundo. Explica cómo
descubrieron el sesgo en los datos y cómo usaron R para solucionarlo:

"Trabajo en un equipo que recopila datos tipo encuesta. Una de las tareas que realiza mi equipo se llama comparación por
pares. Por ejemplo, podemos mostrar a los usuarios dos anuncios uno al lado del otro al mismo tiempo. En nuestra encuesta,
preguntamos cuál de los dos anuncios prefieren. En un caso, tras muchas iteraciones, observamos un sesgo constante a favor
del primer elemento. También hubo una disminución apreciable de la preferencia por un elemento si cambiamos su posición a
la segunda.

Así que decidimos añadir aleatoriedad a la posición de los anuncios usando R. Queríamos asegurarnos de que los artículos
aparecieran en la primera y segunda posición con frecuencias similares. Utilizamos sample() para inyectar un elemento de
aleatoriedad en nuestra programación en R. En R, la función sample() permite tomar una muestra aleatoria de elementos de
un conjunto de datos. Al agregar este fragmento de código se barajan las filas de nuestro conjunto de datos de forma aleatoria.

Así, cuando presentamos los anuncios a los usuarios, las posiciones de los anuncios eran ahora aleatorias y se controlaba
el sesgo. Esto hizo que la encuesta fuera más eficaz y los datos más fiables".
