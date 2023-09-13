# Ordenar datos en hojas de cálculo

## Ordenación de conjuntos de datos

En las hojas de cálculo, puedes ordenar datos en orden ascendente o descendente mediante número o letras. Si las celdas
están etiquetadas con color, puedes ordenarlas también por color. Cuando ordenes datos en una hoja de cálculo, puedes elegir
"Ordenar hoja" u "Ordenar rango".
Si usas "Ordenar hoja", todos los datos de la hoja de cálculo se ordenarán por las condiciones de una única columna, pero
la información relacionada en otras filas, permanece junta.

En cambio, "Ordenar rango" no mantiene junta la información de las distintas filas. Cuando ordenas un rango, seleccionas
un conjunto específico de celdas o el rango al que quieres que se limite la ordenación. No se reorganizará ningún otro
dato de las hojas de cálculo, solo las celdas especificadas. Hay dos métodos para ordenar datos en hojas de cálculo:

uno involucra el uso del menú; el otro implica escribir la función de ordenar.

### ordenación con el menú

En la ordenación con el menú, seleccionamos toda la columna que se desea ordenar, vamos a la pestaña datos, tienes dos
opciones: ordenar una hoja o un rango de datos. Sí el contenidosseleccionado tiene relacion con las demas celdas, ose,
que la seleccion y las celdas contiguas horizontalmente permanezcan juntas, debemos ordenar por hoja, esto mantendra
los datos juntos por fila. sin importar cómo los ordenes. Según el orden que desees que tengan las fechas, puedes ordenar
de la A a la Z, lo cual también clasificará las fechas en forma numérica. O puedes ordenar de la Z a la A, que ordenará
los datos en sentido contrario, por lo tanto elejiremos ordenar hoja por.. y nos aparecera el nombre de la columna que
hemos seleccionado al inicio.

Si nuestra seleccion es independiente del resto del conjunto de datos y queremos que este no sea moficicado por el
ordenamiento, elejimos, ordenar rango por columna, este ordenara solo la columan seleccionad, por lo que el conjuto se
notara un poco desordenado con respecto al inicio y esto solo es para columnas de datos independientes con el resto del
conjunto.

### ordenacion con la funcion SORT

Recordar que cuando usas la función SORT, en realidad estás cambiando el conjunto de datos existente

Sintasis:

    = SORT(Rango_i:Rango_f, columna_numero, Ordenamiento)

El rango_i hace referencia a la celda mas a la izquierda o donde inician nuestros datos y Rango_f es la celda mas a la derecha
o donde termina nuestro conjunto de datos.

columna_nemro, es el numero de la columna a ordenar.

para true ordenamiento ascendete, false ordenamiento descendente

El criterio de ordenación personalizada es aquel que ordena los datos en una hoja de cálculo usando múltiples condiciones.
Esto significa que la ordenación se basará en el orden de las condiciones que selecciones, para esto se selecciona el rango,
luego en el menu se selecciona oredenar rango, si el conjuto tiene una cabecera, esto se selecciona para evitar que se
mezclen con el resto d elos datos, elejimos ordenamiento alfabetico, aplicado a la columan que deseamos oredena y
agregamos tantos creterios de ordenamiento como sea requerido, señalando la columna ha ordena,.

### Diferencias entre ordenar con funcion y menu

La ordenación desde la pestaña Datos de una hoja de cálculo puede excluir de la ordenación una fila de encabezado en el
rango de datos, mientras que el rango de datos para una función SORT escrita nunca debe contener una fila de encabezado.

La ordenación desde la pestaña Datos de una hoja de cálculo sobrescribe las celdas que contienen los datos sin ordenar
con los datos ordenados, mientras que la función SORT escrita inserta los datos ordenados en un rango de celdas diferente.
