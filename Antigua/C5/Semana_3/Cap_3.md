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

HAVING básicamente te permite agregar un filtro a tu consulta en vez de a la tabla subyacente cuando trabajas con funciones
de agregado. De esa manera, solo devuelve registros que cumplen tus condiciones específicas. Asimismo, CASE devuelve registros
dentro de tus condiciones permitiéndote incluir instrucciones IF/THEN en tu consulta.

SELECT
    Warehouse.warehouse_id,
    CONCAT(Warehouse.state, ': ', Warehouse.warehouse_alias) AS warehouse_name,
    COUNT(Orders.order_id) AS number_of_orders,
    (
        SELECT
            COUNT(*)
        FROM
            warehouse_orders.Orders AS Orders
    ) AS total_orders,
    CASE
        WHEN
            COUNT(Orders.order_id)/(SELECT COUNT(*) FROM warehouse_orders.Orders AS Orders) <= 0.20
        THEN
            "fullfilled 0-20% of orders"
        WHEN
            COUNT(Orders.order_id)/(SELECT COUNT(*) FROM warehouse_orders.Orders AS Orders) > 0.20  AND
            COUNT(Orders.order_id)/(SELECT COUNT(*) FROM warehouse_orders.Orders AS Orders) <= 0.60
        THEN
            "Fulfilled 21-60% of orders"
        ELSE
            "Fulfilled more than 60% of orders"
        END AS fulfillment_summary
FROM
    warehouse_orders.Warehouse AS Warehouse
LEFT JOIN
    warehouse_orders.Orders AS Orders
ON
    Orders.warehouse_ID = Warehouse.warehouse_id
GROUP BY
    Warehouse.warehouse_id,
    warehouse_name
HAVING
    COUNT(Orders.order_id) > 0

## Rglas que deben seguir las subconsultas

- Las subconsultas tienen que estar dentro de paréntesis

- Una subconsulta puede tener una sola columna especificada en la cláusula SELECT. Si quieres que una subconsulta compare
  varias columnas, esas columnas deben haberse seleccionado en la consulta principal.

- Las subconsultas que devuelven más de una fila solo pueden usarse con múltiples operadores de valor, tales como el operador
  IN que permite especificar múltiples valores en una cláusula WHERE.

- Una subconsulta no puede estar anidada en un comando SET. El comando SET se usa con UPDATE para especificar qué columnas
  (y valores) se deben actualizar en una tabla.
