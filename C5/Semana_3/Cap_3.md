# Subconsultas

Una subconsulta es una consulta SQL que está anidada dentro de una consulta más grande.

Con las subconsultas puedes combinar distintas piezas de lógica entre sí. Dado que la lógica de tu consulta externa depende
de la consulta interna, puedes hacer más cosas con una sola consulta. Esto significa que toda la lógica está en un solo lugar,
lo que hace que sea más eficiente y fácil de leer.

La instrucción que contiene la subconsulta también puede llamarse *consulta externa o selección externa*. Esto convierte a
la subconsulta en la *consulta interna o selección interna*.

*La consulta interna se ejecuta primero para que los resultados puedan pasarse a la consulta externa para que los use.*

por ejemplo:

SELECT

    station_id.
    num_bikes_avaliable,
    --subquery
    (
        SELECT
            AVG(num_bikes_avaliable)
        FROM
            bigquery-public-data.new_york.citiebike_station
    ) AS avg_num_bikes_avaliable

FROM
    bigquey-public-data.new_york.citiebike_station

La subquieries pueden generarse en la clausulas FROM o WHERE, tambien, por ejemplo:

SELECT
    station_id,
    name,
    number_of_rides AS number_of_rides_starting_at_station
FROM
    (
        SELECT
            start_station_id,
            COUNT(*) AS number_of_rides
        FROM
            bigquery-public-data.new_york.citibike_trips
        GROUP BY
            start_station_id
    ) AS station_num_trips
JOIN
    bigquery-public-data.new_york.citibike_stations ON station_id = start_station_id
ORDER BY
    number_of_rides DESC

SELECT
    station_id,
    name
FROM
    bigquery-public-data.new_york.citibike_stations
WHERE
    station_id
IN
    (
        SELECT
            start_station_id
        FROM
            bigquery-public-data.new_york.citibike_trips
        WHERE
            'Subscriber'
    )

## Uso de subconsultas para agregar datos
