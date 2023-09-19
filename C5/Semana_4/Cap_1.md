# realizar calculos ocn datos

## Calculos de datos - Fórmulas de cálculos comunes

= SUM(Rango), suma los valores numericos de un rango de celdas.

- controlador de relleno, se encuentra en la esquina inferior izquierda de la celda y permite entre otros: seleccionar muchas
  celdas para una fórmula o para continuar un patrón a lo largo de muchas celdas.

- Crecimiento bruto, restas el año actual menos el año anterior,

        = CeldaAñosActual - CeldaAñoAnterior

- Tasa de crecimiento, dividir el creciemiento bruto entre los dos años y el toal del año anterior, luego ocnvertir en
  porcentaje

        = Creciemientobruto / CeldaAñoAnterior
        - ver como porcentaje

- Peromedio: calcula el promedio de un rango de celdas

        = AVERAGE(rango)

- Promedio minimo y maximo

        = MIN(Rango)
        = Max(Rango)

El formato condicional es una herramienta de la hoja de cálculo que cambia la forma en que aparecen las celdas cuando los
valores cumplen ciertas condiciones.

Tabla de resumen simple, es una tabla que se utiliza para resumir información estadística sobre los datos.

- Contar Sí -> cuenta el numero de veces que aparece un valor en un rango determinado

        = COUNTIF(RANGO, "criterio(>x, =X,  >=x, etc)")

- Contar Sí S -> cunta en mas de un rango las coincidencias

        COUNTIFS(RANGO_BUSCAR1, "CRTERIO1", RANGO_BUSCAR2, CRITERIO2,..., RABGO_BUSCARN, CRITERION )

- Suma sí -> SUMIF es una función que suma datos numéricos basados en una condición.
  
        = SUMIF(Rango_evaluar, "criterio_condicion", Rango_sumar)

        = SUMIF(B3:B50, "=1", C3:C50)

- Suma Sí S -> sumar si con multiples condiciones

        = SUMIFS(RANGO_SUMAR, Rango_buscar1, "Criterio1", Rango_buscar2, "Criterio2"..., Rango_buscarN, "CriterioN")

- AVERAGEIF promediará los valores en una matriz basada en criterios determinados.

        = AVERAGEIF(Rango_Buscar, "Criterio_condicion", Ramgo_calcular_promedio)

- MAXIFS -> calcula el maximo de un rango de acuerdo a un criterio/condicion determinado

        = MAXIFS(Rango_calcular, rango_bucar, "Criterio")

        = MAXIFS(Rango_calcular, rango_bucar1, "Criterio1", rango_bucar2, "Criterio2",.., rango_bucarN, "CriterioN" )

## Funciones compuestas

*SUMPRODUCT* es una función que multiplica las matrices y muestra el resultado de la suma de esos productos.

        = SUMPROPRODUCT(RangoColumna1, ArngoColumna2, ...,  ArngoColumnaN)

Esta funcion primero multiplica el item en la primera posicion de ambas columbas, luego el segun y asi hasta la ultima
posicion, posterior a eso sumara todos los resultados, dando una gran suma al final de la operacion.

*El margen de beneficio* es un porcentaje que indica cuántos centavos de beneficio se generaron por cada dólar de venta.
