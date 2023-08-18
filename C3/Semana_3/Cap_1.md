# Trabajar con bases de datos

## Todo sobre las bases de datos

Una base de datos es un conjunto de datos almacenados en un sistema informático, pero el almacenamiento es solo el
comienzo. Las bases de datos posibilitan encontrar la información exacta que necesitas para tu análisis, ordenar los datos
para acercar aquellos que necesite,s para generar informes perspicaces, entre otros, un aspecto mas profundo de estas
caracteristicas son los metadatos, se puede decir que son “autoconsciente” (en inglés, “meta”). En general, están hablando
de cuando algo que se refiere a sí mismo o que está siendo consciente de sí mismo.

Ser autoconciente en el analisis de datos implica que el trabajo cuenta con una revisión de calidad, para asegurar de
que los métodos son justos, se ha prestado atención a cualquier sesgo que pueda afectar el resultado. La clave es tomar
distancia y preguntarnos a nosotros mismos si nuestros procesos tienen sentido.

Los metadatosson datos sobre los datos, indican de dónde vienen los datos, cuándo y cómo se crearon, y de qué se tratan.
cobran mayor importancia cuando trabajas con bases de datos. se asemejan a  una guía de referencia. Sin esa guía lo único
que tienes es un montón de datos sin un contexto que explique lo que significan.

Es posible tomar datos de una base de datos u otra fuente y agregarlos a una hoja de cálculo. Podrás hacer esto importando
datos directamente o utilizando SQL para generar la solicitud, esto es importante en la fase de preparacion del proceso
de analisis de datos, permite identificar cuales datos son utiles, correctos y que posibiliten la solucion de un problema
o dar respuesta a una pregunta en la organizacion.

Por lo tanto Las bases de datos permiten a los analistas manipular, almacenar y procesar datos.

## Características de las bases de datos

Las bases de datos son herramientas esenciales para los analistas de datos, estas  almacenan y organizan datos, lo que
facilita la gestión y el acceso a la información por parte de los analistas de datos.

### Beneficios del uso de bases de datos relacionales

Algunos beneficios de las bases de datos relacionales son:

    - Nos ayudan a obtener información de forma más rápida
    - Nos ayudan a tomar decisiones basadas en datos
    - Nos ayudan a resolver problemas,
    - simplifican muchos procesos de análisis
    - hacen que los datos sean más fáciles de encontrar y de usar

A continuacion un ejemplo grafico de como se veria en esquema una base de datos relacional:

![Alt text](2023-08-18-11-39-03.png)

Base de datos relacional, estan conformadas por tablas, estas a su vez estan conformadas por campos que son el detalle de
las caracteristicas de cada una de las tablas y por sus relaciones.

de acuerdo a lo anterior una base de datos relacional es una base de datos que contiene una serie de tablas relacionadas
que pueden conectarse mediante sus relaciones. Para que dos tablas tengan una relación, debe haber uno o más campos iguales
dentro de ambas tablas.

Por ejemplo el campo Branch ID, se encuentra en las tablas CarDealerShips y ProductDetails, este campo comun establece la
relacion entre ambas tablas o lo que es lo mismo establece una conexion entre ambas tablas.

Ahora bien el campo branchId es conocido como campo clave y se utiliza  para conectar ambas tablas, Hay dos tipos de claves.
el primero es *la clave primaria* que es un identificador que referencia a una columna en la que cada valor es único. Una
clave primaria, debe ser única, lo que quiere decir que no puede haber dos filas con la misma clave primaria. Tampoco
puede tener un valor nulo o en blanco.

Otra tipo de campo *clave son las claves externas o secundarias*, esto es un campo en una tabla que es una clave primaria
en otra tabla. En otras palabras, una clave externa es cómo una tabla puede conectarse con otra.

Como aclaracion se considera un campo como clave primaria, cuando dicho campo se encuentra en su tabla origen y se considera
clave secundario o externa, cuando el campo se encuentra en una tabla diferente a su origen y cuya funcion principal es
relacionar ambas tablas, las claves primarias son conosidas tambien como llaves primaria y las llaves secundarias son conocidas
como llaves foraneas.

![Alt text](image.png)

## clave primaria

Clave primaria se utiliza para asegurar que los datos de una columna específica son únicos y sus caracteristicas son:

    - Solamente identifica un registro en una tabla de base de datos relacional.
    - Solo se permite una clave primaria en una tabla
    - No puede contener valores nulos o en blanco.
    - Algunas tablas no requieren una clave primaria estando conformadas solo por claves secundarias

## Clave secundaria o foranea

Una clave externa es una columna o un grupo de columnas de una tabla de base de datos relacional que proporciona un
enlace entre los datos de las dos tablas.

    - Se refiere al campo de una tabla que es la clave primaria de otra tabla.
    - Puede haber más de una clave externa en una tabla.

## Clave compuesta

Una clave primaria también puede construirse a partir de varias columnas de una tabla. Este tipo de clave primaria se
denomina clave compuesta, este tipo de claves se forman de dos o mas claves primarias en campos diferentes y por lo tanto
la clave compuesta hereda el comportamiento de las claves primarias de ser unicas, no estar vacias o en blanco, ni con-
tener valores nulos.

## El lenguaje de consulta estructurado o SQL

Las bases de datos utilizan un lenguaje especial para comunicarse denominado lenguaje de consulta. El lenguaje de con-
sulta estructurado (SQL) es un tipo de lenguaje de consulta que permite a los analistas de datos comunicarse con la base
de datos. De este modo, un analista de datos usará SQL para crear una consulta con el fin de ver los datos específicos que
quiere visualizar en un conjunto más grande. En una base de datos relacional, los analistas de datos pueden escribir
consultas para obtener información de las tablas relacionadas.
