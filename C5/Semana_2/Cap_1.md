# Convertir y formatear datos

## De un tipo a otro

La forma de formatear tipos de datos en hojas de cálculo; Convertir datos. Eso significa cambiar ciertas cifras para que
tengan el formato de fecha, cadena de texto, porcentaje o, incluso, moneda.

El primer paso inclusive antes de la limpieza, es la estandarizacion de los formatos del conjuntos de datos, segun el
campo en el que se encuentren, ya sea, textos, tiempo, monedas, distancia, etc, esto ayudara a que una vez en el proceso
de limpieza y posterior el de analisis evitemos errores que nos retracen o invaliden las conclusiones que sacamaos del
conjunto.

En las hojas de caluclo, tenemos la barra de herramientas en la parte superior de la hoja, verás un menú que te puede
ayudar a convertir estos números en tipos de datos específicos. En el menú desplegable tienes muchas opciones, como cifra,
moneda, fecha, porcentaje... Si haces clic y abres todo el menú, tienes aún más opciones, incluida una para formato per-
sonalizado de cifras. Seleccionamos la columna y hacer clic en el atajo de moneda.

Con la funcion CONVERT podemos convertir una unidad de medida a otra, por ejemplo la sintaxis para fraengeith a celcius
seria:

    = convert(Celda_origen,"F","C")

Donde Celda_origen es donde tenemos el dat a convertir, luego la unidad en la que se encuentra el dato y por ultimo la
unidad en la que se requiere el dato realmente.
