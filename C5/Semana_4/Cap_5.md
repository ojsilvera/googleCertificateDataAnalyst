# Cómo utilizar SQL con tablas temporales

Una tabla temporal es una tabla de una base de datos que se crea y existe de manera temporal en el servidor de la base de
datos. Las tablas temporales, como las llamamos, almacenan subconjuntos de datos de tablas de datos estándar durante un
período determinado. Luego, se eliminan automáticamente cuando finalizas la sesión de la base de datos en SQL. Dado que
las tablas temporales no están almacenadas de manera permanente, son útiles solo cuando necesitas una tabla por poco tiempo
para completar tareas de análisis, como los cálculos.

Usar una tabla temporal te permitirá ejecutar varias consultas sobre estos datos sin tener que seguir filtrándolos. Hay
distintas formas de crear tablas temporales en SQL, lo que dependerá de la base de datos relacional que estés utilizando.

*La cláusula WITH* es un tipo de cláusula temporal que puedes consultar varias veces. La cláusula WITH se aproxima a una
tabla temporal. Básicamente, significa que crea algo que hace lo mismo que una tabla temporal. Incluso si no agrega una
tabla a la base de datos en la cual estás trabajando para que otros la vean, aún puedes ver los resultados y cualquiera
que necesite revisar tu trabajo puede ver el código que lleva a tus resultados.

    WITH
        nombre_tabla_temporal
    AS
        --aqui el subquery que formara la tabla temporal
        (
            SELECT
                CAMPOS
            FROM
                ORIGEN_DATOS
        )

    -- AQUI LA CONSULTA PROPIAMENTE DICHA
    SELECT
        --campos de la tabla temporal
    FROM
        --aca el nombre de la tabla temporal como origen
        nombre_tabla_temporal

ejemplo:

OBJECTIVE: To return the average number of orders, or sales made, by EmployeeID for ShipperID -> 2 and ShipperID -> 3.

--1st CTE
WITH cte_sales
AS
(SELECT
    EmployeeID,
    COUNT(OrderID) as Orders,
    ShipperID
FROM Orders
GROUP BY EmployeeID, ShipperID),

--2nd CTE (nested)
shipper_cte
AS
(SELECT *
FROM cte_sales
WHERE ShipperID=2 or ShipperID=3)

--Query using CTE
SELECT
    ShipperID, AVG(Orders) average_order_per_employee
FROM
shipper_cte
GROUP BY ShipperID

consultar jemplos desarrollados

    [https://learnsql.com/blog/sql-with-clause/]

*SELECT INTO* es un buen ejemplo de cómo hacer una tabla temporal. Esta instrucción copia datos de una tabla en una tabla
nueva, pero no agrega la tabla nueva a la base de datos. Es útil si quieres hacer una copia de una tabla con una condición
específica, como una consulta con una cláusula WHERE.
