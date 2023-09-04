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
