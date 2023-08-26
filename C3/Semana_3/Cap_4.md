# Guía detallada Prácticas recomendadas en SQL

Estas prácticas recomendadas incluyen pautas para escribir consultas SQL y desarrollar documentación, así como ejemplos
de estas prácticas. Es un buen recurso para tener a mano cuando estés utilizando SQL por tu cuenta, así puedes dirigirte
a la sección que necesites para revisar esas prácticas. ¡Es como una guía práctica de SQL!

## Uso de mayúsculas y distinción entre mayúsculas y minúsculas

Con SQL, el uso de mayúsculas no suele importar. Puedes escribir SELECT, seleccionar o SeLeCT. ¡Todas las opciones funcionan!
Pero si utilizas mayúsculas como parte de un estilo coherente, tus consultas se verán más profesionales.

Para escribir consultas SQL como un profesional, siempre es bueno usar mayúsculas en los iniciadores de cláusulas (por
ejemplo, SELECT, FROM, WHERE, etcétera). Las funciones también deberían estar escritas con mayúsculas (por ejemplo, SUM()).

Los nombres de las columnas deberían estar escritos en minúscula (consulta la sección sobre snake_case que se encuentra
más adelante en esta guía).

Los nombres de las columnas deberían estar escritos en CamelCase (consulta la sección sobre CamelCase que se encuentra
más adelante en esta guía). Esto ayuda a que tus consultas sean coherentes y fáciles de leer, y no impactarán en los datos
que extraigas cuando las realices. En el único momento en que es importante el uso de mayúsculas es cuando se encuentran
dentro de citas (podrás leer más sobre citas más adelante).

Los proveedores de bases de datos SQL pueden utilizar variaciones ligeramente diferentes de SQL. Estas variaciones se
denominan dialectos SQL. Algunos dialectos SQL distinguen entre mayúsculas y minúsculas. BigQuery es uno de ellos. Vertica
es otro. Pero la mayoría, como MySQL, PostgreSQL y SQL Server no distinguen entre mayúsculas y minúsculas. Esto quiere decir
que si buscas country_code = ‘us’, te mostrará todas las entradas que contengan 'us', 'uS', 'Us' y 'US'. Esto no sucederá
con BigQuery. BigQuery distingue entre mayúsculas y minúsculas, de manera que esa misma búsqueda solo te mostrará entradas
en las que el country_code sea exactamente 'us'. Si el country_code es 'US', BigQuery no incluirá esas entradas en los
resultados.

Comillas simples o dobles: '' o " "

En la mayoría de los casos, tampoco es importante si utilizas comillas simples ' ' o comillas dobles " " cuando nos referimos
a las cadenas. Por ejemplo, SELECT es un iniciador de cláusula. Si escribes SELECT entre comillas, como 'SELECT' o "SELECT",
SQL lo tomará como una cadena de texto. Tu consulta será errónea porque necesita una cláusula SELECT.

Pero hay dos situaciones en las que sí importa qué tipo de comillas utilices:

Cuando quieres que las cadenas sean identificables en cualquier dialecto SQL

Cuando tu cadena contiene un apóstrofo o comillas

Dentro de cada dialecto SQL, hay reglas sobre lo que es aceptado y lo que no. Pero una regla general que comparten casi
todos los dialectos SQL es el uso de comillas simples para cadenas. Esto ayuda a evitar confusiones. Así que si queremos
referirnos a Estados Unidos en una cláusula WHERE (por ejemplo, country_code = 'US'), utiliza comillas simples para encerrar
la palabra 'US'.

La segunda situación es cuando tu cadena tiene comillas dentro. Imagina que tienes una columna de comidas favoritas en una
tabla denominada FavoriteFoods y otra columna que corresponde a cada amigo. Organizar y proteger tus datos
