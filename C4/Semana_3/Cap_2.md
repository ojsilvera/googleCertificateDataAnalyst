# Aprende sobre consultas básicas de SQL

## Consultas SQL más utilizadas

Consultar datos de una tablas

        SELECT -> las columnas de la tabla o tablas que buscas  Nombre_Tabla.nombre_columna
        FROM   -> nombre de la labla o tablas donde lo buscas, Nombre_BaseDedatos.Nombre_Tabla
        WHERE  -> que es lo que buscas

insertar datos en euna tabla

        INSERT INTO  Nombre_BaseDedatos.Nombre_Tabla
            (los campos a ingresar separados por comas)
        VALUES
            (los valores separados por comas, deben coincidir en orden y formato con los declarados en el into)

Actualizar un ragistro d ela base de datos, para hacer un update, debemos pasar el ID del campo a actualizar, que seria
una llave primaria que es unica e irrepetible

        UPDATE
            Nombre_BaseDedatos.Nombre_Tabla
        SET
            campo  = "valor del campo segun el tipo de datos"
        WHERE
            llave_primaria = valor

Crear una tabla

    CREATE TABLE IF NOT EXIST

Vaciar una tabla

    DROP TABLE IF EXIST

## Limpieza de cadenas de variables con SQL

### DISTINCT

Para limpiar IDs duplicados utilizamos DISTINCT en nuestra instrucción SELECT.

SELECT
    customer_ID
FROM
    customer_data.customer_address

La consulta anterior nos listara todos los id de clientes, aunque se encuentren duplicados para evitar esto utilizamos

SELECT
    DISTINCT customer_ID
FROM
    customer_data.customer_address

las cadenas de texto estan conformados por letras, numeros o ambos

Para trabajar con cadenas de texto en SQL utilizamos:

### Subcadena(SUBSTR())

Para obtener un numero de letras determinados de una dato, utilizamos SUBSTR() o substring, nos devolvera el numero de caracteres
que le indiquemos que sean iguales en nuestro conjunto de datos, ejemplo, si tenemos un codigo que corresponde a Estados Unidos
Escrito como US pero tambien como USA y no podemos actualizar la tabla para corregirlo, hacemos uso de SUBSTR() de la siguiente
manera, SUBSTR(columna_donde_buscar, caracter, caracter) = 'caracteres_que_busco':

SELECT
    customer_id
FROM
    customer_data.customer_address
WERE
    SUBSTR(country, 1, 2) = 'US' --nos devolvera solo los id de cliente cuyo pais es US o USA

SELECT
    customer_id,
    SUBSTR(country,1,3) as abr_country -> devuelve las 3 primeras letras de cada pais
FROM
    customer_data.customer_address
OREDER BY
    abr_country ASC -> ORDEN ASCENDENTE

### TRIM

Elimina espacios en blanco dentro de una cadena de texto, los espacios cuentan como un caracter, por lo tanto si usamos
la sentencia length, obtendremos aquellos que no cumplan con un criterio de largo preestablecido y asi sabremos cuales
tendrian espacios en blanco que no deberian estar, adicionalmente si llegaramos a tener registros duplicados, usariamos
la sentencia distinct.

SELECT
    DISTINCT(customer_id) --mostrara cada redistro una sola vez

FROM
    customer_data.customer_address

WHERE
    TRIM(states) = 'OH' --TRIM(la_columna_que_buscamos_limpiar) = 'el criterio de filtrado'

## informacion para transformacion de cadenas

### LENGTH(LEN)

trabaja con el largo que debe tener una cadena de texto para considerarse como valida, pro ejemplo para validar
codigos que deberian tener un largo fijo podriamos hacerlo d ela siguiente manera, que nos muestre solo aquellos codigos
que tengan mas de 2 digitos.

SELECT
    country
FROM
    customer_data.customer.address
WHERE
    LENGTH(country) > 2

en la consulta anterior nos devolvera solo aquellos paises id mayor a 2 digitos y asi identificamos anomalias en los codigos
por ejemplo.

### LIKE

Permite obtener coincidencias de auerdo a un patron determinado

columna LIKE 'Patron' -> el Patron puede ser parcial utilizando el caracter comodin %

por ejemplo para obtener todos los clientes cuyos paises inicien por la letra c, tendriamos la siguiente consulta:

SELECT
    customer_id, customer_name, country

FROM
    customer_data

WHERE

    country LIKE 'C%'
