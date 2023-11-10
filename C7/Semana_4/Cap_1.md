# Crear visualizaciones de datos en R

Ejemplos de paquetes de visualizacion de datos para R

![Alt text](image-3.png)

La libreria mas utilizada en R para visualizacion de datos es ggplot2, que pertenece al paquete de tidyverse.

Algunos beneficios de ggplot2

![Alt text](image-2.png)

Los conceptos basicos en ggplot2 son:

Aesthetic

![Alt text](image.png)

Mapping

![Alt text](image-6.png)

Geoms o formas geometricas, incluyen, puntos, barras, lineas, etc

![Alt text](image-1.png)

Facets

![Alt text](image-4.png)

Labels and annotations

![Alt text](image-5.png)

Los puntos muestran la relación entre dos variables cuantitativas. Las barras muestran una variable cuantitativa que varía
entre diferentes categorías.

## Sintaxys ggplot2 basica

Una secuencia basica para la creacion de una visualizacion en ggplot2 seria algo como:

![Alt text](image-8.png)

cargar el data ser + geoms a mostrar

    ggplot(data=penguins) + geom_point(mapping=aes(x=flipper_lenght_mm, y=body_mass_gg))

*"ggplot(data=penguins)" inicia el ggplot con el set de datos seleccionado a traves de data=nombre_set.*

*"+" agraga capas al ggplot, para formar el grafico y sus caracteristicas.*

*"geom_point()" establece la forma geometrica del grafico, dentro del parentecis se colocara la estetica del grafico.*

*"mapping=aes(x=flipper_lenght_mm, y=body_mass_gg)" cuales seran, los campos que se mostraran y a que eje se le asignan,*
                                                  *hace parte de la estetica de ggplot*

### plantillas para visualizacion en ggplot

Para evitar la repeticion de codigo es posible reemplazr por variables ciertas porciones del codigo, apar ello utilizamos:

    <Aqui_La_Variables>

la sintaxys anterior le indica a R que es posible realizar el cambio de ese trozo de codigo por la variable previamente
dedinida, por ejemplo:

    ggplot(data=<data_set>) + <geom_function>(mapping=aes(x=<axes_x>, y=<axes_y>))

donde

    data_set = dataset_name
    geom_function = geoms_form
    axes_x = campo del sata set para el eje x
    axes_y = campo del sata set para el eje y

por ejemplo

    data_set = penguins
    geom_function = geom_point
    axes_x = flipper_lenght_mm
    axes_y = body_mass_gg

    ggplot(data=<data_set>) + <geom_function>(mapping=aes(x=<axes_x>, y=<axes_y>))

## Problemas mas comunes al visualizar en R

    Es case sensituve, distingue mayuculas y minusculas

    Los parentecis de cierre y apertura deben coincidir

    las parablas reservadas del lenguajes deben escribirse tal cual

    El signo mas ("+") debe agregarse para crear la capa de visualizacion y siempre al final de la lina de codigo, dispara
    error en cualquier otra posicion

    Los pipes (canalizacion) no funcionan como objetos de cracion de capas debe ser el signo + ("+")

Para obtener ayuda sobre un afuncion escribir, basta con escribir el signo de interrogacion "?", seguido del nombre de la
funcion que buscamos:

    ?El_nombre_de_la_funcion
