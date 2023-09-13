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

### CAST

Convierte un tipo de dato en otro, lo cual se concoce como conversion de tipos.

SELECT
    CAST(purchase_price AS FLOAT64) AS float_price --convierte el formato tipo string de la columna purchase_price a float
FROM
    cars.cars_info

ORDER BY
    float_price ASC --ordenar la nueva colummna de manera ascendente

Convertir DATETIME a DATE-> en el ejemplo obtenemos las ventas realizadas por una tienda entre 1 y 31 de diciembre

SELECT
    purchase_date,
    customer_name,
    purchase_price
FROM
    forniture_flowers.purchase_flowers

WHERE
    purchase_date BETWEEN '2023-12-01' AND '2023-12-31' --retorna valores de compra entre las fechas iundicadas, pero
                                                        --en formato datetime y lo requerimos en date

Ajustando formato

SELECT
    CAST(purchase_date AS date) AS purchase_date,
    customer_name,
    purchase_price
FROM
    forniture_flowers.purchase_flowers

WHERE
    purchase_date BETWEEN '2023-12-01' AND '2023-12-31' --retorna valores de compra entre las fechas iundicadas, pero
                                                        --en formato datetime y lo requerimos en date

### CONCAT

Suma cadenas de texto para crear nuevas cadenas de texto que es posible usar como llaves unicas, por ejemplo cuando hay
que establecer una diferencia entre dos productos, tendriamos en la tienda de flores la necesidad de encontrar si los clientes
prefieren rosas rojas o rosas blancas, pero los datos reflejan el codigo de las rosas de manera general y los colores en otro
campo, por lo cual podriamos concatenar el codigo de la rosa y su color y obtener una llave unica que nos permita distinguir
cuan de los dos colores es el preferido de los clientes:

SELECT
    flower_id,
    flower_color,
    customer_name,
    flower_price,
    flower_name
    purchase_date

FROM
    forniture_flowers.purchase_flowers

La consulta anterior arrojara los datos generales de compra, a continuacion concatenamos el id y el color, distinguiendo
cada grupo de manera mas sencilla

SELECT
    CONCAT(flower_id, flower_color) AS new_id_color,

FROM
    forniture_flowers.purchase_flowers

WHERE
    flower_name = 'Rose'

Esto retornara todas las rosas, con el campos new id_color, permitiendo distinguir entre rosas blancas o amarillas y permitirnos
tener un punto de partida para el analisis de cual prefieren mas los clientes

### COALESCE

Muestra valores que no son nulos en el conjunto. al tener un campo no obligatorio es probable que este campo sea nulo en
el conjunto la mayor parte del tiempo, por ejemplo teniendo un campo primer_nombre, segundo_nombre, apellido, identificacion
y grado, siendo segundo_nombre un campo opcional, en una tabla de estudiantes, tendriamos algunos campos nulos ya que en
algunos casos se puede tener un solo nombre y el que se encuentre cuenta como el primer nombre, por lo tanto tendriamos

SELECT
    CONCAT(primer_nombre, segundo_nombre) AS nombre,
    apellido,
    identificacion,
    grupo

FROM
    institucion_la_nube.estudientes

WHERE
    grado = '11'

esta consulta arriojara un listado de estudiantes de grado 11 y colocara el primer nombre o segundo nombre de acuerdo a lo que
encuentre, apellido, identificacion y el grupo al que pertenece el estudiante

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

### Count y Filtro multiple

Se nos solicita que determinemos el numero de cuentas para un pais determinado en este caso alemania, cuyo monto total
es mayor a 5 dolares.

La clausula count nos permite determinar el numero de registor que retorna la base de datos, sgun el filtro aplicado
en este caso limitado por le pais y el monto total.

SELECT
    count(*) AS Total_bills
FROM
    invoices
WHERE
    BillingCountry = "Germany" AND Total > 5
