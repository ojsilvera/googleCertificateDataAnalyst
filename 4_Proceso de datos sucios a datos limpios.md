# Proceso de datos sucios a datos limpios

## La importancia de la integridad

### Enfoque en la integridad

#### Introducción al enfoque en la integridad

¡Hola! Qué bueno volver a encontrarnos. Mi nombre es Sally y estoy aquí para enseñarte todo sobre el procesamiento de datos. Soy directora de analítica y mediciones en Google. Mi trabajo es ayudar a agencias publicitarias y empresas a medir el éxito y analizar sus datos, de modo que me reúno con muchas personas diferentes para mostrarles cómo el análisis de datos los ayuda en la publicidad. Hablando de análisis, hiciste un gran trabajo antes al aprender cómo recopilar y organizar los datos para análisis. Definitivamente es un paso importante en el proceso de análisis de datos, ¡bien hecho! Ahora hablemos sobre cómo asegurarnos de que tus datos organizados estén completos y sean precisos. Los datos limpios son la clave para asegurarte de la integridad de tus datos antes de analizarlos. Te mostraremos cómo asegurarte de que tus datos estén limpios y ordenados. Limpiar y procesar datos es una parte de todo proceso de análisis de datos. Como recordatorio rápido, ese proceso consiste en preguntar, preparar, procesar, analizar, compartir y actuar. Esto significa que es momento para que exploremos la fase de procesar y estoy aquí para guiarte en todo el camino. Conozco bien el lugar adonde estás ahora. Nunca había escuchado sobre análisis computacional de datos hasta que hice un programa similar a este. Una vez que comencé a avanzar, me di cuenta de cuanto disfrutaba el análisis computacional de datos y las puertas que podría abrir. ¡Y ahora estoy entusiasmada en ayudarte a abrir esas mismas puertas! Algo que comprendí mientras trabajaba para distintas empresas, es que los datos limpios son importantes en todas las industrias. Por ejemplo, al inicio de mi carrera, aprendí a estar atentar para identificar datos duplicados, un problema común con el que los analistas se encuentran al limpiar datos. Solía trabajar para una empresa que tenía distintos tipos de suscripciones. En nuestro conjunto de datos, cada usuario tendría una nueva fila para cada tipo de suscripción contratada, lo que significa que los usuarios aparecerían más de una vez en mis datos. De modo que si hubiera contado el número de usos en una tabla sin percatarme de los duplicados como este, habría contado a algunos usuarios dos veces en lugar de una. Como resultado, mi análisis habría resultado erróneo, lo que habría llevado a problemas en mis informes y para los interesados que confían en mis análisis. ¡Imagina si le contase al director general que tengo dos veces más clientes de los que realmente hay! Es por eso por lo que los datos limpios son tan importantes. De modo que el primer paso en el procesamiento de datos es aprender sobre la integridad de los datos. Descubrirás qué es la integridad de los datos y porqué es importante mantenerla durante todo el proceso de análisis de datos. Algunas veces puede que ni siquiera tengas los datos que necesitas, de modo que deberás crearlos. Esto te ayudará a aprender cómo el tamaño de la muestra y el muestreo aleatorio pueden ahorrarte tiempo y esfuerzo. Las pruebas de datos son otro paso importante al procesar datos. Compartiremos algunas pautas sobre cómo realizar pruebas de datos antes de que tus análisis comiencen oficialmente. Del mismo modo en que lavas tu ropa y tus platos en la vida diaria, los analistas limpian todos sus datos todo el tiempo, también. La importancia de los datos limpios será definitivamente el punto de atención aquí. Aprenderás técnicas de limpieza de datos para todos los escenarios, junto con algunas trampas para tener en cuenta durante el proceso. Explorarás la limpieza de datos en hojas de cálculo y bases de datos, a partir de lo que has aprendido sobre las hojas de cálculo. Hablaremos más sobre SQL y cómo puedes usarlo para limpiar datos y hacer otras cosas útiles, también. Cuando los analistas limpian sus datos, hacen mucho más que un control puntual para asegurarse de que la limpieza de datos está bien. Aprenderás formas de verificar e informar los resultados de tu tarea de limpieza. Esto incluye documentar tu proceso de limpieza, que tiene muchos beneficios que exploraremos. Es importante recordar que el procesamiento de datos es solo una de las tareas que completarás como analista de datos. Realmente, tus habilidades de limpieza de datos podrían ser algo que luego terminarás destacando en tu currículum cuando comiences a buscar trabajo. Hablando de tu currículum, podrás comenzar a pensar en cómo hacerlo desde la perspectiva de un analista de datos. Una vez que termines, tendrás una sólida apreciación de los datos limpios y de cuán importantes son en el proceso de análisis de datos. ¡Empecemos!

### Objetivos de la integridad de datos y del análisis de datos

#### Motivos por los cuales la integridad de datos es importante

¡Hola de nuevo! En este vídeo, vamos a hablar sobre la integridad de los datos y algunos riesgos que podrías correr al trabajar como analista de datos. Un análisis robusto depende de la integridad de los datos. Si los datos que estás usando están comprometidos de alguna manera, tu análisis no será tan sólido como debería. La integridad de los datos consiste en la exactitud, integridad, consistencia y confiabilidad de los datos a lo largo de su ciclo de vida. Esto puedo sonar como muchas cualidades para que los datos estén a la altura de las circunstancias. Pero créeme, vale la pena verificar todas estas cualidades por completo antes de proceder con tu análisis. De lo contrario, tu análisis podría ser erróneo. No porque hayas hecho algo mal, sino porque los datos con los cuales estabas trabajando eran erróneos desde el principio. Cuando la integridad de los datos es baja, puede causar cualquier inconveniente desde la pérdida de un píxel en una imagen hasta una decisión médica incorrecta. En algunos casos, una pieza faltante puede hacer que todos tus datos se tornen inservibles. La integridad de los datos puede estar comprometida de muchas formas diferentes. Existe la posibilidad de que los datos puedan estar comprometidos cada vez que se replican, transfieren o manipulan de cualquier forma. La replicación de datos es el proceso de almacenar datos en varios sitios. Si estás replicando datos en distintos momentos en distintos lugares, existe la posibilidad de que tus datos no estén sincronizados. Esos datos carecen de integridad porque distintas personas pueden no utilizar los mismos datos para sus conclusiones, lo cual puede causar inconsistencias. También está el tema de la transferencia de datos, que es el proceso de copiar datos desde un dispositivo de almacenamiento a la memoria o de una computadora a otra. Si tu transferencia de datos se interrumpe, podrías terminar con un conjunto de datos incompletos, lo cual podría no ser útil para tus necesidades. El proceso de manipulación de datos implica modificar los datos para que estén más organizados y sean más fáciles de leer. La manipulación de datos tiene como objetivo hacer que el proceso de análisis de datos sea más eficiente, pero un error durante el proceso puede comprometer la eficacia. Por último, los datos también pueden estar comprometidos por un error humano, virus, malware, piratería informática y fallas del sistema, que pueden llevar a más dolores de cabeza. Voy a parar aquí. Estas son suficientes potenciales malas noticias para digerir. Pasemos a algunas potenciales buenas noticias. En muchas empresas, el almacén de datos o el equipo de ingeniería de datos se encarga de garantizar la integridad de los datos. Próximamente, aprenderemos sobre cómo verificar la integridad de los datos como analista de datos. Pero quédate tranquilo, alguien más por lo general te cubrirá la espalda. Luego de averiguar con qué datos estás trabajando, es importante que compruebes dos veces que tus datos están completos y son válidos antes de analizarlos. Esto te ayudará a asegurar que tu análisis y conclusiones son precisas. Verificar la integridad de los datos es un paso crucial en el procesamiento de tus datos para tenerlos listos para el análisis, ya sea que tú u otra persona en la empresa lo hagan. Luego, aprenderás más sobre integridad de datos ¡Hasta pronto!

#### Más información sobre la integridad de datos y el cumplimiento normativo

![alt text](image-116.png)

#### Equilibrio entre los objetivos y la integridad de datos

Hola, recordemos comprobar la integridad de los datos. También es importante comprobar que los datos que uses estén alineados con el objetivo comercial. Esto agrega otra capa al mantenimiento de la integridad de tus datos porque los datos que estás usando podrían tener limitaciones con las que deberías lidiar. El proceso de hacer coincidir los datos con los objetivos comerciales puede ser bastante directo. Aquí te presentamos un ejemplo rápido. Digamos que eres un analista para una empresa que produce y vende autopartes.
Reproduce el video desde ::29 y sigue la transcripción0:29
Si necesitas responder una pregunta sobre la ganancia generada por la venta de una pieza determinada, entonces deberías utilizar la tabla de ganancias del conjunto de datos.
Reproduce el video desde ::37 y sigue la transcripción0:37
Si la pregunta es sobre opiniones de los clientes, deberías utilizar la tabla de opiniones para analizar los puntajes promedio. Pero antes de ahondar en cualquier análisis, debes considerar unas pocas limitaciones que pueden afectarlo. Si los datos no se limpiaron adecuadamente, no podrás usarlos. Deberás esperar hasta que se realice una limpieza exhaustiva. Ahora, digamos que estás intentando saber cuánto gasta el cliente promedio. Observas que los datos del mismo cliente aparecen en más de una línea. Eso se denomina dato duplicado. Para corregirlo, quizá debas cambiar el formato de los datos o quizá debas cambiar la forma en la que calculas el promedio. De lo contrario, parecerá que los datos corresponden a dos personas distintas y estarás atascado en cálculos engañosos. Puedes darte cuenta también de que no hay suficientes datos para completar un análisis preciso. Quizá tengas datos de ventas equivalentes a tan solo un par de meses. Existe una pequeña posibilidad de que podrías esperar a obtener más datos, pero es más probable que debas cambiar tu proceso o encontrar fuentes alternativas de datos mientras cumples con tu objetivo. Me gusta pensar en un conjunto de datos como en una fotografía. Toma esta fotografía. ¿Qué estás mirando?
Reproduce el video desde :1:48 y sigue la transcripción1:48
A menos que seas un viajero experto o conozcas el área, puede ser difícil elegir entre estas dos imágenes.
Reproduce el video desde :1:55 y sigue la transcripción1:55
Visualmente, es muy claro cuando no estamos viendo toda la imagen. Cuando obtienes el panorama completo, te das cuenta de que....¡estás en Londres!
Reproduce el video desde :2:4 y sigue la transcripción2:04
Con datos incompletos, es difícil ver el panorama completo para obtener un sentido real de qué sucede. A veces, confiamos en los datos porque si aparecen en filas y columnas, parecería que todo lo que necesitamos está ahí con solo realizar una consulta. Pero eso no es cierto. Recuerdo un momento cuando comprendí que no tenía suficientes datos y debía encontrar una solución.
Reproduce el video desde :2:26 y sigue la transcripción2:26
Estaba trabajando para una empresa minorista en línea y me pidieron que resolviera cómo acortar el plazo de entrega de las compras. Por lo general, una entrega más rápida hace que los clientes estén más felices. Cuando comprobé el conjunto de datos, encontré muy poca información sobre el seguimiento. Estábamos perdiendo algunos detalles importantes. De modo que, junto con los ingenieros de datos, creamos nuevos procesos para rastrear información adicional, como la cantidad de paradas en un viaje. Con esos datos, redujimos el tiempo que se tardaba desde la compra hasta la entrega y vimos una mejora en la satisfacción del cliente. ¡Eso se sintió genial! Aprender cómo resolver problemas con los datos mientras no pierdes de vista tu objetivo te ayudará a tener éxito en tu carrera como analista de datos. Y tu camino hacia el éxito continúa. Próximo paso: aprenderás más sobre cómo alinear los datos con los objetivos. Sigue así.

#### Objetivos y datos alineados

<https://support.microsoft.com/en-us/office/datedif-function-25dba1a4-2812-480b-84dd-8b32a451b35c>

<https://support.microsoft.com/en-us/office/days360-function-b9a509fd-49ef-407e-94df-0cbda5718c2a>

<https://support.google.com/docs/answer/6055612?hl=en>

![alt text](image-117.png)

#### Cuestionario práctico: Pon a prueba tus conocimientos sobre integridad de datos y objetivos analíticos

![alt text](image-118.png)

### Supera los desafíos de datos insuficientes

#### Qué hacer en caso de datos insuficientes

Todos los analistas estuvieron en la situación en la que los datos son insuficientes para el objetivo comercial. Considerando la cantidad de datos que se generan diariamente, puede ser difícil de creer, pero es verdad. Entonces, veamos qué puedes hacer cuando tus datos no son suficientes. Veremos cómo establecer límites para el alcance de tu análisis y qué datos deberías incluir.
Reproduce el video desde ::21 y sigue la transcripción0:21
En un momento, fui analista de datos en un centro de soporte. Todos los días recibíamos preguntas de los clientes, que se registraban como tickets de soporte.
Reproduce el video desde ::29 y sigue la transcripción0:29
Me pidieron una proyección del número de tickets de soporte entrantes por mes para determinar cuántas personas adicionales necesitábamos contratar. Era muy importante tener una cantidad suficiente de datos que se remontasen como mínimo a un par de años atrás porque debía informar cambios interanuales y estacionales. Si solo hubiera tenido disponibles los datos del año en curso, no hubiera sabido que es normal un pico en enero y tiene que ver con las personas que piden reembolsos después de las fiestas. Como tenía una cantidad suficiente de datos, pude sugerir la contratación de más personal en enero para estar preparados. Es inevitable que aparezcan desafíos, pero las buenas noticias son que una vez que conoces tu objetivo comercial, podrás reconocer si tienes suficientes datos. Y si no los tienes, podrás resolverlo antes de comenzar tu análisis. Ahora, veamos algunas de esas limitaciones con las que puedes encontrarte y cómo puedes manejar distintos tipos de datos insuficientes.
Reproduce el video desde :1:22 y sigue la transcripción1:22
Digamos que estás trabajando en la industria del turismo y necesitas saber cuáles son los planes de viaje buscados con más frecuencia. Si solamente usas datos de un sitio de reservas, te estás limitando a los datos de una fuente únicamente. Otros sitios de reservas pueden mostrar distintas tendencias que quisieras considerar para tu análisis. Si una limitación como esta afecta tu análisis, puedes detenerte aquí y consultar nuevamente con los interesados para trazar un plan. Si tu conjunto de datos se sigue actualizando, significa que todavía hay ingreso de datos y pueden no estar completos. Por lo tanto, si hay una atracción turística nueva y estás analizando el interés y la concurrencia, probablemente no haya suficientes datos para que determines las tendencias. Por ejemplo, podrías querer esperar un mes para recolectar más datos. También puedes comprobar con los interesados y pedirles ajustar el objetivo. Por ejemplo, podrías analizar tendencias semana por semana en lugar de mes a mes. También podrías basar tu análisis en tendencias de los últimos tres meses y decir: "Así es como se vería la concurrencia a la atracción para el mes cuatro".
Reproduce el video desde :2:22 y sigue la transcripción2:22
Puedes no tener suficientes datos para saber si este número es demasiado alto o demasiado bajo. Pero le dirías a los interesados que es tu mejor cálculo basado en los datos que tienes actualmente. Por otra parte, tus datos podrían ser más antiguos y ya no ser pertinentes. Los datos desactualizados sobre la satisfacción al cliente no incluirán las respuestas más recientes. De modo que estarás confiando en las calificaciones para hoteles o alquileres de verano que podrían ya no ser precisos. En este caso, tu mejor opción sería encontrar un nuevo conjunto de datos para trabajar. Los datos limitados geográficamente también pueden ser poco confiables. Si tu empresa es global, no querrías usar datos limitados a viajes en solo un país. Querrías un conjunto de datos que incluyera a todos los países. De modo que esa es una de las limitaciones más comunes que encontrarás y algunas de las formas de resolverlas. Puedes identificar las tendencias con los datos disponibles o esperar más datos si el tiempo lo permite; también puedes hablar con los interesados y ajustar tu objetivo; o puedes buscar un conjunto de datos nuevo.
Reproduce el video desde :3:22 y sigue la transcripción3:22
La necesidad de tomar esas decisiones dependerá de tu rol en la empresa y posiblemente de las necesidades de la industria en general. Pero aprender cómo abordar los datos insuficientes siempre es una forma genial de prepararte para el éxito. Tus facultades como analista de datos están fortaleciéndose. Y justo a tiempo. Después de aprender más sobre limitaciones y soluciones, también aprenderás sobre poder estadístico, otra herramienta fantástica para que uses. ¡Hasta pronto!

#### Qué hacer cuando encuentras un problema en tus datos

![alt text](image-119.png)

#### La importancia del tamaño de la muestra

Bien, antes hablamos de tener el tipo correcto de datos para cumplir con tus objetivos comerciales y la importancia de tener la cantidad correcta de datos para asegurarte de que tu análisis sea lo más preciso posible. Quizás recuerdes que para los analistas de datos, una población representa a todos los valores de datos posibles de un conjunto de datos determinado. Si puedes usar el 100% de una población en tu análisis, ¡es genial! Pero a veces recabar información sobre una población entera no es posible. Consume mucho tiempo o es muy caro. Por ejemplo, digamos que una organización internacional quiere saber más sobre dueños de mascotas que tienen gatos. Tu tarea es determinar qué tipo de juguetes prefieren los dueños de gatos en Canadá. Pero hay millones de dueños de gatos en Canadá, de manera que obtener datos de todos ellos sería un desafío enorme. Pues bien, ¡no temas! Permíteme presentarte..... ¡al tamaño de la muestra! Cuando utilizas un tamaño de muestra o una muestra, usas una parte de una población que es representativa de la población. El objetivo es obtener suficiente información de un grupo pequeño dentro de una población para formular predicciones o conclusiones sobre la población total. El tamaño de la muestra ayuda a asegurar el grado respecto del cual puedes estar confiado en que tus conclusiones representan con precisión a la población. Para los datos sobre dueños de gatos, un tamaño de la muestra podría incluir datos sobre cientos o miles de personas en lugar de millones. Usar una muestra para análisis es más rentable y lleva menos tiempo. Si se hace con cuidado y a conciencia, puedes obtener los mismos resultados usando un tamaño de muestra en lugar de intentar encontrar a cada uno de los dueños de los gatos para averiguar cuáles son sus juguetes favoritos. Sin embargo, existe una desventaja potencial. Cuando utilizas únicamente una muestra pequeña de una población, puede llevar a la incertidumbre. No puedes estar el 100% seguro de que tus estadísticas son una representación precisa y completa de la población. Esto lleva a un sesgo del muestreo, que se trató anteriormente en el programa. El sesgo del muestreo ocurre cuando una muestra no es representativa de la población en su conjunto. Esto significa que algunos miembros de la población están siendo sobre o subrepresentados. Por ejemplo, si la encuesta usada para recoger datos de los dueños de gatos solamente incluyó a personas con teléfonos inteligentes; entonces, los dueños de gatos que no tienen un teléfono inteligente no estarían representados en los datos. Utilizar un muestreo aleatorio puede ayudar a resolver algunos de esos problemas relacionados con el sesgo del muestreo. El muestreo aleatorio es una forma de seleccionar una muestra de una población de manera que cada tipo posible de la muestra tenga una posibilidad igual de ser elegido. Volviendo a los dueños de gatos, usar una muestra aleatoria de dueños de gatos significa que los dueños de gatos de cada tipo tienen una posibilidad igual de ser elegidos. Los dueños de gatos que viven en departamentos en Ontario tendrían la misma posibilidad de ser representados que aquellos que viven en casas en Alberta. Como analista de datos, encontrarás que crear tamaños de muestras usualmente se hace aún antes de recibir los datos. Pero aun así es bueno que sepas que los datos que vas a analizar son representativos de una población y sirven para tu objetivo. También es bueno saber con qué te encontrarás a continuación en tu recorrido por los datos. En el próximo vídeo, tendrás la opción de sentirte aún más cómodo con los tamaños de las muestras. ¡Nos vemos!

#### Cómo calcular el tamaño de la muestra

<https://www.investopedia.com/terms/c/central_limit_theorem.asp>

<https://www.statisticssolutions.com/dissertation-resources/sample-size-calculation-and-sample-size-justification/sample-size-formula/>

<https://www.coursera.org/learn/process-data/lecture/mSj5A/determine-the-best-sample-size>

<https://www.coursera.org/learn/process-data/supplement/ZqcDw/sample-size-calculator>

![alt text](image-120.png)

#### Cuestionario práctico: Autorreflexión: ¿Por qué son importantes las actividades previas a la limpieza?

![alt text](image-121.png)

#### Cuestionario práctico: Pon a prueba tus conocimientos sobre datos insuficientes

![alt text](image-122.png)

### Cómo usar el poder estadístico

#### Cómo usar el poder de la estadística

0:01
¡Hola! Probablemente todos hemos soñado con tener un superpoder al menos una vez en nuestras vidas. Yo sé cuál. Me encantaría poder volar. Pero hay otro superpoder del cual quizá no hayas oído hablar: el poder estadístico.
Reproduce el video desde ::14 y sigue la transcripción0:14
El poder estadístico es la probabilidad de obtener resultados significativos de una prueba. Creo que este no es un superpoder con el cual hayan soñado. Aun así, es un poder bastante genial. Para los analistas de datos, tus proyectos pueden comenzar con la prueba o el estudio. La prueba de hipótesis es una forma de ver si una encuesta o experimento tiene resultados significativos. Aquí hay un ejemplo: Digamos que trabajas en una cadena de restaurantes que está planificando una campaña de marketing para sus nuevos batidos. Debes realizar una prueba de publicidad en un grupo de clientes antes de realizarla a nivel nacional.
Reproduce el video desde ::50 y sigue la transcripción0:50
En la prueba, quieres verificar si a los clientes les gusta o no la campaña. También quieres descartar cualquier factor externo a la publicidad que pueda llevarlos a indicar que no les gusta ese aviso.
Reproduce el video desde :1:1 y sigue la transcripción1:01
Utilizar a todos tus clientes llevaría mucho tiempo y sería muy caro. Por lo tanto, necesitas saber cuántos clientes necesitarás para demostrar que la publicidad es efectiva. Cincuenta probablemente no serían suficientes. Incluso si eligieras 50 clientes al azar, podrías terminar con clientes a quienes no les gustan para nada los batidos. Y si eso sucede, no podrás medir la efectividad de tu publicidad para obtener más pedidos de batidos dado que ninguno de los que están en el tamaño de la muestra los pediría. Es por eso por lo que necesitas un tamaño mayor de muestra: para que puedas asegurarte de obtener un buen número de todos los tipos de personas para tu prueba. Usualmente, cuanto más grande es el tamaño de la muestra, mayor será la posibilidad de obtener resultados estadísticamente significativos con tu prueba. Y ese es el poder estadístico.
Reproduce el video desde :1:46 y sigue la transcripción1:46
En este caso, usar tantos clientes como sea posible mostrará las diferencias reales entre los grupos a quienes les gusta o no versus las personas cuya decisión no estaba basada en absoluto en la publicidad.
Reproduce el video desde :1:58 y sigue la transcripción1:58
Existen formas de calcular con precisión el poder estadístico, pero no vamos a verlas ahora. Puede que necesites hacer ese cálculo por ti mismo como analista de datos.
Reproduce el video desde :2:8 y sigue la transcripción2:08
Por ahora, debes saber que el poder estadístico generalmente se muestra como un valor de uno. De manera que si tu poder estadístico es 0.6; es lo mismo que decir 60%. En la prueba de la publicidad del batido, si calculaste un poder estadístico de 60%, eso significa que existe un 60% de posibilidades de que obtengas un resultado estadísticamente significativo en la eficacia de la publicidad.
Reproduce el video desde :2:32 y sigue la transcripción2:32
"Estadísticamente significativo" es un término utilizado en estadísticas. Si quieres aprender más sobre el significado técnico, puedes buscar en línea. Pero en términos básicos, si una prueba es estadísticamente significativa, eso significa que los resultados de la prueba son reales y no un error causado por factores aleatorios.
Reproduce el video desde :2:52 y sigue la transcripción2:52
De manera que hay 60% de chances de que los resultados de la prueba de publicidad del batido sean confiables y reales y un 40% de chances de que el resultado de la prueba sea incorrecto.
Reproduce el video desde :3:2 y sigue la transcripción3:02
Usualmente, se necesita un poder estadístico de al menos 0.8 u 80% para considerar que tus resultados son estadísticamente significativos.
Reproduce el video desde :3:11 y sigue la transcripción3:11
Consideremos un escenario más. Quedémonos con los batidos porque, bueno, porque me gustan los batidos. Imagina que trabajas en una cadena de restaurantes que quiere lanzar un nuevo batido con sabor a torta de cumpleaños con sabor a batido.
Reproduce el video desde :3:24 y sigue la transcripción3:24
El costo de producción de este batido será más caro que el de tus otros batidos. Tu empresa espera que el entusiasmo por el nuevo sabor atraiga a más clientes y dinero para compensar el costo. Quieren probarlo primero en algunos restaurantes. Entonces, pensemos cuántos locales deberías usar para que tus resultados sean confiables.
Reproduce el video desde :3:44 y sigue la transcripción3:44
Primero, deberías pensar qué es lo que evita que consigas resultados estadísticamente significativos. ¿Hay otros restaurantes que estén ofreciendo otras promociones que puedan atraer a nuevos clientes? ¿Algunos de esos restaurantes tienen clientes que siempre compran el producto más nuevo, sin importar qué es? ¿Algunos de esos restaurantes comenzaron algunas construcciones que evitarían que los clientes fueran al restaurante?
Reproduce el video desde :4:7 y sigue la transcripción4:07
Para lograr un poder estadístico más alto, deberías considerar todos estos factores antes de decidir cuántos locales incluir en el tamaño de la muestra para tu estudio.
Reproduce el video desde :4:16 y sigue la transcripción4:16
Quieres asegurarte de que cualquier efecto se deba, más probablemente, al nuevo sabor del batido, no a otros factores.
Reproduce el video desde :4:23 y sigue la transcripción4:23
Los efectos mensurables serían un incremento en las ventas o el número de clientes en los locales en el tamaño de tu muestra. Muy bien, eso es todo por ahora. Próximamente, vamos a explorar los tamaños de las muestras en detalle, para obtener una mejor idea de cómo impactan en tus pruebas y estudios.
Reproduce el video desde :4:39 y sigue la transcripción4:39
Mientras tanto, has aprendido un poco más sobre los batidos y los superpoderes. Y, por supuesto, sobre el poder estadístico. Lamentablemente, solo el poder estadístico puede ser realmente útil para los analistas de datos. Sin embargo, ponerme mi capa y volar a comprar un batido justo ahora suena bastante bien.

#### Qué hacer cuando no hay datos

<https://towardsdatascience.com/is-there-a-difference-between-open-data-and-public-data-6261cd7b5389>
<https://www.kaggle.com/>
<https://www.kaggle.com/sakshigoyal7/credit-card-customers>
<https://www.kaggle.com/datasnaek/youtube-new>
<https://www.kaggle.com/rtatman/188-million-us-wildfires>
<https://www.kaggle.com/bigquery/google-analytics-sample>
<https://www.kaggle.com/docs/datasets>
<https://www.kaggle.com/datasets>

![alt text](image-123.png)

#### Cómo determinar el mejor tamaño de la muestra

¡Qué bueno volver a verte! En este vídeo, vamos a ver en más detalle los tamaños de las muestras y la integridad de los datos. Si alguna vez estuviste en una tienda donde entregan muestras, sabes que ese es uno de los pequeños placeres de la vida. ¡Al menos para mí! Esas pequeñas muestras también son una forma muy inteligente de parte de las empresas para conocer más sobre sus productos a través de los clientes sin tener que entregar a todos una muestra gratis. Muchas empresas usan el tamaño de las muestras de manera similar. Toman una parte de algo más grande. En este caso, una muestra de una población. Algunas veces, realizarán pruebas complejas en sus datos para ver si cumplen con sus objetivos comerciales. Nosotros no profundizaremos en todos los cálculos que se necesitan para hacer todas estas pruebas de manera efectiva. En cambio, nos enfocaremos en la "idea general": ver el proceso y qué comprende. A modo de recordatorio, el tamaño de la muestra es una parte de una población que es representativa de toda la población. Para las empresas, es una herramienta muy importante. Puede resultar caro y llevar mucho tiempo analizar una población entera de datos. Utilizar un tamaño de muestra generalmente es lo más lógico e, incluso, puede derivar en conclusiones válidas y útiles. Existen calculadoras disponibles en línea que pueden ayudarte a calcular el tamaño de la muestra. Debes ingresar el nivel de confianza, el tamaño de la población y el margen de error. Ya hemos hablado antes sobre el tamaño de la población. Para avanzar, aprenderemos sobre el nivel de confianza y el margen de error. Conocer estos conceptos te ayudará a entender por qué los necesitas para calcular el tamaño de la muestra. El nivel de confianza es la probabilidad de que tu muestra refleje de manera precisa la mayor parte de la población. Puedes considerarlo como si se tratase de la confianza en cualquier otra cosa. Es la intensidad que sientes y te permite saber si puedes confiar en algo o en alguien. Tener el 99% de confianza es lo ideal. Pero la mayoría de las industrias esperan como mínimo tener un 90 o 95% de nivel de confianza. Las industrias como la farmacéutica generalmente quieren un nivel de confianza que sea lo más alto posible cuando utilizan un tamaño de muestra. Esto tiene sentido porque se realizan pruebas en medicamentos y es necesario tener certeza de que funcionan y son seguros para el uso masivo. Para otros estudios, las organizaciones quizá solo deben saber que los resultados de las pruebas o las encuestas los están llevando por la dirección correcta. Por ejemplo, si una empresa de pintura está realizando pruebas en colores nuevos, está bien un nivel de confianza menor. También debes considerar el margen de error de tu estudio. Aprenderás más acerca de este tema pronto, pero básicamente indica si los resultados del tamaño de tu muestra se aproximan o no a lo que serían tus resultados si usaras toda la población que está representada en el tamaño de tu muestra. Piénsalo de esta manera. Digamos que el director de una escuela secundaria te pide un estudio sobre las preferencias de dulces de los estudiantes. Necesitan conocer un tamaño de muestra apropiado y lo necesitan ahora. La escuela tiene una población de 500 estudiantes, y están pidiendo un nivel de confianza del 95% y un margen de error del 5%. Incluimos una calculadora en la hoja de cálculo, pero también puedes encontrar fácilmente este tipo de calculadora buscando "calculadora de tamaño de muestras" en Internet. Del mismo modo que en esas calculadoras, nuestra hoja de cálculo no muestra ningún tipo de cálculos más complejos para determinar el tamaño de la muestra. Todo lo que debemos hacer es ingresar los números de nuestra población, el nivel de confianza y el margen de error. Y cuando escribimos 500 para el tamaño de la población, 95 para nuestro porcentaje de nivel de confianza, 5 para nuestro porcentaje de margen de error el resultado es aproximadamente 218. Para este estudio, eso significa que un tamaño apropiado de muestra sería 218. Si encuestáramos a 218 estudiantes y encontráramos que el 55% de ellos prefiere el chocolate, entonces podríamos estar bastante seguros de que esto sería verdad para los 500 estudiantes. 218 es el número mínimo de personas que necesitamos encuestar con base en nuestro criterio de 95% como nivel de confianza y 5% como margen de error. En caso de que te preguntes, el nivel de confianza y el margen de error no deben sumar 100%. Son independientes uno de otro. Entonces, digamos que cambiamos nuestro margen de error de 5% a 3%. Por lo tanto, nuestro tamaño de muestra debería ser más grande, aproximadamente 341 en lugar de 218, para hacer que los resultados del estudio sean más representativos de la población. Practica libremente con la calculadora en línea. Conocer el tamaño de muestra y cómo calcularlo te ayudará cuando trabajes con datos. Tenemos más conocimientos útiles para ofrecerte, incluso sobre el margen de error. ¡Hasta pronto!

#### Calculadora de tamaño de muestra

<https://www.surveymonkey.com/mp/sample-size-calculator/>
<http://www.raosoft.com/samplesize.html>

![alt text](image-124.png)

#### Cuestionario práctico: Pon a prueba tus conocimientos sobre cómo probar tus datos

![alt text](image-125.png)

### Considerar el margen de error

#### Evaluar la confiabilidad de tus datos

0:01
¡Hola! Anteriormente hablamos sobre el margen de error sin explicarlo del todo. Bien, vamos a ver qué está bien o mal en este vídeo, ya que explicaremos mejor qué es el margen de error. Incluso incluiremos un ejemplo de cómo calcularlo.
Reproduce el video desde ::14 y sigue la transcripción0:14
Como analista de datos, es importante que calcules el tamaño de las muestras y las variables como el nivel de confianza y el margen de error antes de comenzar a realizar cualquier tipo de pruebas o encuestas. Es la mejor forma de asegurar la objetividad de tus resultados y te brinda una mayor posibilidad de obtener resultados estadísticamente importantes. Pero si ya conoces el tamaño de la muestra, como, por ejemplo, cuando recibes resultados de encuestas para analizar; entonces, puedes calcular el margen de error tú mismo. De ese modo tendrás una mejor idea de cuál es la diferencia entre tu muestra y tu población. Empezaremos por el principio con una definición más completa. El margen de error es el máximo que se espera que difieran los resultados de la muestra de los de la población real.
Reproduce el video desde :1: y sigue la transcripción1:00
Pensemos en un ejemplo de margen de error.
Reproduce el video desde :1:3 y sigue la transcripción1:03
Sería genial encuestar o realizar una prueba sobre una población entera, pero generalmente es imposible o poco práctico. Entonces, en cambio, se toma una muestra de la población más grande.
Reproduce el video desde :1:15 y sigue la transcripción1:15
Basado en el tamaño de la muestra, el margen de error resultante nos mostrará lo distinto que pueden ser los resultados comparados con los resultados si hubiéramos encuestado a toda la población.
Reproduce el video desde :1:27 y sigue la transcripción1:27
El margen de error te ayuda a entender lo confiable que son los datos de la prueba de tu hipótesis.
Reproduce el video desde :1:33 y sigue la transcripción1:33
Cuanto más cerca a cero esté el margen de error, más cerca los resultados de tu muestra coincidirán con los resultados de la población total.
Reproduce el video desde :1:43 y sigue la transcripción1:43
Por ejemplo, digamos que realizaste una encuesta nacional utilizando una muestra de la población. Le preguntaste a personas que trabajan cinco días a la semana si les gustaría la idea de trabajar cuatro días a la semana. De modo que tu encuesta dice que el 60% prefiere una semana de cuatro días. El margen de error fue del 10%, lo cual indica que entre el 50 y 70% de las personas les gustó la idea. De esta manera, si tuviéramos que encuestar a todos los trabajadores de cinco días en toda la nación, entre el 50 y el 70% estaría de acuerdo con nuestros resultados.
Reproduce el video desde :2:18 y sigue la transcripción2:18
Ten en cuenta que nuestro rango es entre el 50 y el 70%. Esto es así porque el margen de error se cuenta en ambas direcciones de los resultados de la encuesta de 60%. Si estableces un nivel de confianza de 95% para tu encuesta, habrá una posibilidad del 95% de que las respuestas de toda la población estén entre el 50 y el 70% que dirán que sí, que quieren una semana laboral de cuatro días.
Reproduce el video desde :2:46 y sigue la transcripción2:46
Dado que tu margen de error se superpone con la marca de 50%, no puedes asegurar que al público le agrada la idea de una semana laboral de cuatro días. En ese caso, tendrás que decir que tu encuesta fue no concluyente.
Reproduce el video desde :3: y sigue la transcripción3:00
Ahora, si querías un margen de error más bajo, por ejemplo, 5% con un rango entre 55 y 65%, podrías incrementar el tamaño de la muestra. Pero si te indicaron el tamaño de la muestra, puedes calcular el margen de error tú mismo.
Reproduce el video desde :3:18 y sigue la transcripción3:18
De ese modo, puedes decidir por ti mismo el nivel de probabilidad de que tus resultados sean estadísticamente significativos con base en tu margen de error. En general, a mayor cantidad de personas que incluyas en tu encuesta, será más probable que tu muestra sea representativa de toda la población.
Reproduce el video desde :3:34 y sigue la transcripción3:34
Disminuir el nivel de confianza también tendría el mismo efecto, pero eso haría menos probable que tu encuesta sea precisa.
Reproduce el video desde :3:43 y sigue la transcripción3:43
Es decir que, para calcular el margen de error, necesitas tres cosas: el tamaño de la población, el tamaño de la muestra, y el nivel de confianza.
Reproduce el video desde :3:52 y sigue la transcripción3:52
Y del mismo modo que con el tamaño de la muestra, puedes encontrar muchas calculadoras en línea si buscas "calculadora de margen de error".
Reproduce el video desde :3:59 y sigue la transcripción3:59
Pero vamos a mostrarte en una hoja de cálculo del mismo modo que cuando calculamos el tamaño de la muestra.
Reproduce el video desde :4:5 y sigue la transcripción4:05
Digamos que estás realizando un estudio sobre la eficacia de un medicamento nuevo. Tienes un tamaño de muestra de 500 participantes cuya enfermedad afecta al 1% de la población mundial. Es decir, aproximadamente 80 millones de personas, que es la población para tu estudio.
Reproduce el video desde :4:23 y sigue la transcripción4:23
Dado que es un estudio sobre medicamentos, necesitas tener un nivel de confianza del 99%. También necesitas tener un margen de error bajo. Vamos a calcularlo. Vamos a escribir los números para la población, el nivel de confianza y el tamaño de la muestra, en las celdas correspondientes de la hoja de cálculo. Y nuestro resultado es un margen de error cercano a 6%, más o menos. Cuando el estudio del medicamento esté completo, aplicarás el margen de error a tus resultados para determinar su nivel de confiabilidad.
Reproduce el video desde :5:4 y sigue la transcripción5:04
Las calculadoras como esta en las hojas de cálculo son una de las muchas herramientas que puedes utilizar para asegurar la integridad de tus datos.
Reproduce el video desde :5:11 y sigue la transcripción5:11
Y también es bueno recordar que verificar la integridad de los datos y alinearlos con tus objetivos te pondrá en buena forma para completar tus análisis.
Reproduce el video desde :5:21 y sigue la transcripción5:21
Tener conocimientos sobre tamaño de muestras, poder estadístico, margen de error y otros temas que hemos tratado ayudará a que tus análisis se realicen sin problemas. Son muchos conceptos nuevos para asimilar. Si te gustaría revisarlos en cualquier momento, puedes encontrarlos todos en el glosario, ¡o puedes ver nuevamente el vídeo! Pronto explorarás los pros y los contras de los datos limpios. ¡La aventura de los datos continúa! ¡Y me alegra que avances con ellos! ¡Tú puedes!

#### Todo sobre el margen de error

<https://goodcalculators.com/margin-of-error-calculator/>
<https://www.checkmarket.com/sample-size-calculator/#sample-size-margin-of-error-calculator>

![alt text](image-126.png)

#### Cuestionario práctico: Pon a prueba tus conocimientos sobre el margen de error

![alt text](image-127.png)

### Desafío semanal 1 curso 4

![alt text](image-128.png)

## Datos impecables

### Limpiar los datos es imprescindible

### Empezar a limpiar datos

### Limpieza de datos en hojas de cálculo

### Desafío semanal 2 curso 4

## Limpieza de datos con SQL

## Verificar e informar los resultados de tu limpieza de datos

## Opcional: Agregar datos a tu currículum

## Desafío del curso
