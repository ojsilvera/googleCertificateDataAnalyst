# Preparar datos para la exploración

Es momento de aprender cómo preparar los datos. Aprenderás a identificar cómo se generan y se recolectan los datos y
explorarás diferentes formatos, tipos y estructuras de datos.

*Entender los tipos y las estructuras de datos*:

Todos generamos muchos datos en nuestra vida cotidiana. En esta parte del curso, comprobarás cómo generamos datos y cómo
los analistas deciden qué datos recoger para su análisis. También aprenderás sobre los datos estructurados y no estructurados,
los tipos de datos y los formatos de datos mientras empiezas a pensar en cómo preparar tus datos para la exploración.

Entender el sesgo, la credibilidad, la privacidad, la ética y el acceso: Cuando los analistas de datos trabajan con datos,
siempre verifican que los datos sean imparciales y creíbles. En esta parte del curso, aprenderás cómo identificar distintos
tipos de sesgos en los datos y cómo garantizar la credibilidad de tus datos. También explorarás los datos abiertos y la
relación que existe entre la importancia de la ética de datos y la privacidad de datos.

*Bases de datos*: Donde viven los datos: Cuando analices datos, accederás a gran parte de los datos de una base de datos.
Es donde viven los datos. En esta parte del curso, aprenderás todo sobre las bases de datos, incluso la forma de acceder
a ellas y de extraer, filtrar y ordenar los datos que contienen. También le echarás un vistazo a los metadatos para descubrir
los diferentes tipos y cómo los usan los analistas.

*Organizar y proteger tus datos*: Tener un buen nivel de organización es una parte importante de la mayoría de los trabajos,
y el análisis computacional de datos no es diferente. En esta parte del curso, aprenderás las prácticas recomendadas para
organizar los datos y mantenerlos seguros. También aprenderás cómo los analistas usan las convenciones de nomenclatura de
archivos para poder mantener su trabajo organizado.

*Participar en la comunidad de datos (opcional)*: Tener una fuerte presencia en línea puede ser de gran ayuda para los
solicitantes de empleo de todo tipo. En esta parte del curso, explorarás cómo gestionar tu presencia en línea. También
descubrirás los beneficios de la creación de redes con otros profesionales del análisis computacional de datos.

*Completar el Desafío del curso*: Al final de este curso, podrás poner en práctica todo lo que has aprendido con el Desafío
del curso. El Desafío del curso te hará preguntas sobre los conceptos clave y luego te dará la oportunidad de ponerlos
en práctica a través de dos escenarios.

Lo que aprenderás:

    - Cómo se generan los datos
    - Características de diferentes tipos, campos y valores de datos
    - Estructuras de las bases de datos
    - La función de los metadatos en el análisis computacional de datos
    - Funciones del Lenguaje de consulta estructurado (SQL)

Conjuntos de habilidades que desarrollarás:

    - Garantizar el uso de prácticas éticas en el análisis de datos
    - Abordar los problemas de sesgo y credibilidad
    - Acceso a bases de datos e importación de datos
    - Escribir consultas sencillas
    - Organización y protección de los datos
    - Conectarse con la comunidad de datos (opcional)

## Recopilar datos

Hablaremos sobre las formas en que los datos pueden generarse y cómo las industrias recopilan datos por su propia cuenta.
Cada pieza de información es un dato. Todos los datos se generan usualmente como resultado de nuestra actividad en el mundo,
Con las redes sociales y los dispositivos móviles millones y millones de personas están agregando enormes cantidades de
datos todos y cada uno de los días.

Se pueden generar datos al recolectar información. Esta generación de datos y su recolección traen aparejadas algunas
cosas más en que pensar. Necesita ser realizado teniendo en cuenta la ética, de modo de mantener los derechos y la priva-
cidad de las personas.

Ejemplo del mundo real:

*La Oficina del Censo de los Estados Unidos* utiliza formularios para recolectar datos acerca de la población del país.
Estos datos son utilizados por distintas razones, como financiar escuelas, hospitales y cuarteles de bomberos. La Ofici-
na también recolecta información sobre otras cosas como las empresas estadounidenses, y crean sus propios datos en el pro-
ceso. Lo mejor acerca de esto es que otros pueden utilizar los datos para sus propias necesidades, incluyendo el análisis.

*La encuesta anual de empresas* se utiliza para conocer las necesidades de las empresas y cómo brindarles los recursos
necesarios para ayudarlas a tener éxito.

*Los científicos* también generan datos. Utilizan muchas observaciones en su trabajo. Por ejemplo, pueden recolectar datos
al estudiar el comportamiento animal u observando bacterias bajo el microscopio.

Mi informacion recolectada de una empresa a la cual aplicare para un puesto de analista, al presentarme a la entrevista
la empresa reparte encuestas y formularios, al inicio y al final, esto con fines de muizas mejorar el proceso o medir la
acertividad del proceso a la hora de contrartar es un camino de doble via.

## Determinar qué datos recoger

No importa qué tipo de datos utilices, deben ser controlados respecto de la precisión y confiabilidad, Estos datos pueden
provenir de un amplio número de fuentes diferentes antes de que los investigues. Pueden no ser tan confiables, pero no
quiere decir que no puedan ser útiles. Quieres asegurarte de controlar su su precisión, sesgo y credibilidad.

Solo recuerda que los datos que elijas deben aplicarse a tus necesidades y deben estar aprobados para su uso.

### Sugerencias en la recopilacion de datos

Algunas consideraciones sobre la recopilación de datos que hay que tener en cuenta para el análisis:

*Cómo se recogerán los datos:*

Decide si vas a recopilar los datos con tus propios recursos o si los vas a recibir (y posiblemente comprar) de otra
parte. Los datos que tú mismo recoges se denominan datos de primera fuente.

*Fuentes de datos:*

Si no recoges los datos con tus propios recursos, puedes obtenerlos de proveedores de datos de segunda mano o de terceros.
Los datos de segunda fuente son recogidos directamente por otro grupo y luego vendidos. Los datos de terceros son vendidos
por un proveedor que no ha recogido los datos por sí mismo. Los datos de terceros pueden proceder de distintas fuentes.

    *Datos de primera fuente:* Estos datos son recolectados por una persona o por un grupo por medio de sus propios
    recursos, Recopilar datos de primera fuente es típicamente el método de preferencia porque sabes exactamente de
    dónde provienen.

    *Datos de segunda fuente:* son datos recolectados por un grupo directamente de su público y que, luego, se venden.

Cuando recopiles los datos, también querrás asegurarte de elegir el *tipo correcto de datos*, pueden ser fechas, numericos
texto, boleanos, etc.

*Resolver el problema empresarial:*

Los conjuntos de datos pueden mostrar mucha información interesante. Pero asegúrate de elegir datos que realmente puedan
ayudar a resolver tu problema. Por ejemplo, si estás analizando tendencias a lo largo del tiempo, asegúrate de utilizar
datos de series temporales, es decir, datos que incluyan fechas.

*Cuántos datos hay que recoger:*

En el análisis computacional de datos, *una población* se refiere a todos los valores de datos posibles en un cierto con-
junto de datos, a veces tomar una poblacion es una tarea ardua, por lo tanto usamos *una muestra*la cual es una parte de la
población que es representativa de la población.

Si estás recogiendo tus propios datos, toma decisiones razonables sobre el tamaño de la muestra. Una muestra aleatoria
de los datos existentes puede estar bien para algunos proyectos. Otros proyectos pueden necesitar una recogida de datos
más estratégica para centrarse en determinados criterios. Cada proyecto tiene sus propias necesidades.

*Marco temporal:*

Para la recopilación de datos. si es requerida una respuesta inmediata, debes utilizar los datos históricos, es decir da-
tos preexistentes, sino seran datos en tiempo real, pero es un proceso mas lento y dispendioso.

Si estás recopilando tus propios datos, decide cuánto tiempo necesitarás para recopilarlos, especialmente si estás haciendo
un seguimiento de las tendencias durante un largo periodo de tiempo. Si necesitas una respuesta inmediata, puede que no
tengas tiempo para recoger datos nuevos. En este caso, tendrás que utilizar los datos históricos que ya existen.
