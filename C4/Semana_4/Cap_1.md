# Limpiar datos manualmente

## Verificar e informar los resultados

La verificación es un proceso para confirmar que el esfuerzo de limpieza de datos se ejecutó correctamente y que los datos
resultantes son precisos y confiables. Implica volver a comprobar tu conjunto de datos limpio, realizar algunas limpiezas
manuales, de ser necesario, y tomarte un momento para relajarte y pensar realmente en el propósito original del proyecto.

De esa forma, puedes estar seguro de que los datos que recopilaste son confiables y apropiados para tus propósitos. Asegurarte
de que tus datos estén verificados correctamente es muy importante porque te permite verificar dos veces si el trabajo que
hiciste para limpiar tus datos fue exhaustivo y preciso.

Un registro de cambios es un archivo que contiene una lista ordenada cronológicamente de las modificaciones que se hicieron
a un proyecto. En general, está organizado por versión e incluye la fecha seguida de una lista de funciones agregadas, mejoradas
y eliminadas. Los registros de cambio son muy útiles para hacer un seguimiento de cómo evolucionó un conjunto de datos a lo
largo de un proyecto. También son otra gran forma de comunicar e informar sobre los datos a otros.

## La limpieza y tus expectativas de datos

La verificación es una parte crítica de cualquier proyecto de análisis. Sin ella, no tienes modo de saber si tu información
es confiable para tomar decisiones basada en datos. Piensa en la verificación como un sello de aprobación.

*la verificación* es un proceso para confirmar que un esfuerzo de limpieza de datos se ejecutó correctamente y que los datos
resultantes son precisos y confiables. También incluye la limpieza de datos manual para comparar tus expectativas con lo
que se nos presenta en realidad.

El primer paso en el proceso de verificación es regresar a tu conjunto de datos original sin depurar y compararlo con lo
que tienes ahora. Revisa los datos sucios y trata de identificar cualquier problema común.

Otra parte clave de la verificación incluye tener una visión general de tu proyecto. Esa es una oportunidad para confirmar
que te estás enfocando en el problema del negocio que necesitas resolver y en los objetivos generales del proyecto, y para
asegurarte de que los datos son realmente capaces de resolver ese problema y de alcanzar esos objetivos.

Obtener una visión general de tu proyecto implica hacer tres cosas:

- Primero, piensa en el problema del negocio que estás intentando resolver con los datos. Si has perdido de vista el pro-
  blema, no tienes forma de saber qué datos corresponden a tu análisis. Adoptar un enfoque del análisis que priorice el
  problema es esencial en todas las etapas de cualquier proyecto. Necesitas estar seguro de que tus datos realmente harán
  posible la resolución de tu problema comercial.

- Segundo, debes considerar el objetivo del proyecto. El objetivo  es hacer mejoras ya sea a productos, procesos u otras
  situaciones dentro de la organizacion.

- tercero, necesitas pensar si tus datos son capaces de resolver el problema y de cumplir con los objetivos del proyecto.
  Eso significa pensar de dónde vinieron los datos, y probar tu recopilación de datos y los procesos de limpieza. Este
  también es el momento de notar si algo te resulta sospechoso o potencialmente problemático en tus datos. pregúntate a ti
  mismo: ¿tienen sentido estos números?

Al final del día verificar tus datos te asegura que la información que puedas obtener del análisis es confiable. Es una
parte esencial de la limpieza de datos que ayuda a las empresas a evitar grandes errores. Ese es otro lugar en el que los
analistas de datos pueden salvar el día.

## El paso final en la limpieza de datos

El objetivo es asegurar que nuestro trabajo de limpieza de datos se haya realizado correctamente y que podemos confiar en
los resultados. Quieres verificar tus datos para saber que están 100 por ciento listos.

Recordando los pasos de verificacion tenemos:

- Primer paso en la verificación es regresar a tu conjunto de datos original sin limpiar y compararlo con lo que tienes ahora.
  Esa es una oportunidad para buscar problemas comunes. Luego, corriges los problemas de forma manual. para esto es posible
  utilizar herramientas automaticas o comandos en sql como trim por ejemplo que elimina espacios en blanco al inicio y final
  de cada campo de los registros, tambien tenemos, Una tabla dinámica la cual  es una herramienta de resumen de datos que
  se usa en el procesamiento de datos. La tabla dinámica selecciona, reorganiza, agrupa y cuenta los datos totales o pro-
  medios almacenados en una base de datos.

  Para un registro mal escrito o con que evidencie algun problema, podemos en la hoja de calculo utilizar la herramienta,
  "Buscar y reemplazar"(Find and Replace), la cual nos permite indicar la cadena de texto que requerimos encontrar e indicar
  por cual deseamos reemplazarla y la herramienta ejecutara el reemplazo para todas las coincidencias, sea 1 0 1000 por ejemplo,

  COUNTA en las hojas de calculo cuenta el nuemero total de valores que se encuentran en un rango, mientras que COUNT, cuenta
  el numero de valores de tipo numerico en un rango.

  En SQL una forma de abordar los errores de escritura es a traves de la sentencia CASE stament, la cual analiza una o mas
  condiciones  y retorna un valor en cuanto se cumplan una de las condiciones

  Su sintaxys seria, en caso de conocer el termino que se encuentra mal escrito:

          CASE
          WHEN compaHaEvaluar = 'dato_Incorrecto'  THEN 'Dato_Correcto'
          END AS Nombre_del_nuevo_campo

    SELECT
        customer_id,
        CASE
          WHEN first_name = 'Tnoy'  THEN 'Tony'
          END AS cleaned_name
    FROM
        customer_data

## Los problemas más comunes o qu ebuscar en la limpieza de datos

Asegúrate de haber identificado y corregido los problemas más comunes, que incluyen:

- Fuentes de errores: ¿Utilizaste las herramientas y las funciones correctas para encontrar la fuente de los errores en
  tu conjunto de datos?

- Datos nulos: ¿Buscaste DATOS NULOS utilizando el formato condicional y los filtros?

- Palabras mal escritas: ¿Localizaste todas las palabras mal escritas?

- Números mal escritos: ¿Revisaste dos veces que tus datos numéricos hayan sido ingresados correctamente?

- Espacios y caracteres extra: ¿Eliminaste los espacios y caracteres extra utilizando la función TRIM?

- Duplicados: ¿Eliminaste los duplicados en las hojas de cálculo utilizando la función Quitar duplicados o DISTINCT en SQL?

- Error de coincidencia de tipos de datos: ¿Revisaste que los datos numéricos, las fechas y las cadenas de datos tengan el tipo correcto?

- Cadenas desordenadas (incoherentes): ¿Te aseguraste de que todas tus cadenas sean coherentes y significativas?

- Formatos de fecha desordenados (incoherentes): ¿Diste formato a las fechas de forma uniforme en todo el conjunto de datos?

- Etiquetas engañosas de variables (columnas): ¿Asignaste nombres significativos a tus columnas?

- Datos truncados: ¿Comprobaste si había datos truncados o faltantes que debieran ser corregidos?

- Lógica de negocios: ¿Comprobaste si los datos tienen sentido dados tus conocimientos del negocio?

En sintesis a la hora de verificar el proceso de limpieza tenemos a rangos generales que estar pendientes de:

- *Confirmar el problema del negocio*

- *Confirmar el objetivo del proyecto*

- *Verificar que los datos pueden resolver el problema y que están alineados con el objetivo*
