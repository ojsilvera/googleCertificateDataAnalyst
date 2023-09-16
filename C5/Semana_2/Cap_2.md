# Combinar distintos conjuntos de datos

## Unión y distintas fuentes

Para un conjunto de datos que contiene datos en dos campos separados del tipo string o texto, utilizamos la funcion
CONCAT(), la cual nos permitira concatenar dos o mas cadenas de texto si le especificamos el campo de la tabla en el
cual se enccuentran ubicados, su sintaxis seria:

    CONCAT(campo1, campo2) o CONCAT(campo1, " texto separador ", campo2)

ejemplo de consulta que obtiene la ruta de un pasajero concatenando el inicio del recorrido y su destino, el umero de viajes
realizados ,ordenando por tipo de usuario, inicio ruta, final ruta y ordenado por numero de viajes de manera descendente

SELECT
    usertype,
    CONCAT(start_sations_name, " to ", "end_sations_name") AS Route,
    COUNT(*) AS num_trips,
    ROUND(AVG(cast(tripduration as int64/60,2))) AS Duration

FROM
    ´basedatos.tabla´

GROUP BY
    start_sations_name, end_sations_name, usertype

ORDER BY
    num_trips DESC

## Cadenas de texto en hojas de cálculo

Las funciones LEN, LEFT, RIGHT y FIND.

LEN ->  entre la longitud de una cadena de texto, = LEN(celda).
LEFT->  Toma un numero de caracteres entre una posicion inicial y final, = LEFT(celda, inicio, fin).
RIGHT-> Toma un numero de caracteres entre una posicion inicial y final, = RIGHT(celda, inicio, fin).
FIND->  Encuentra un caracter dentro de una ubicacion, = FIND(""caracter, ubicacion).
