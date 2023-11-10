# Crear visualizaciones de datos en R

Ejemplos de paquetes de visualizacion de datos para R

![Alt text](image-3.png)

La libreria mas utilizada en R para visualizacion de datos es ggplot2, que pertenece al paquete de tidyverse.

Algunos beneficios de ggplot2

![Alt text](image-2.png)

Los conceptos basicos en ggplot2 son:

Aesthetic

![Alt text](image.png)

Geoms

![Alt text](image-1.png)

Facets

![Alt text](image-4.png)

Labels and annotations

![Alt text](image-5.png)

Los puntos muestran la relación entre dos variables cuantitativas. Las barras muestran una variable cuantitativa que varía
entre diferentes categorías.

## Sintaxys ggplot2 basica

cargar el data ser + geoms a mostrar

    ggplot(data=penguins) + geom_point(mapping=aes(x=flipper_lenght_mm, y=body_mass_gg))

*"ggplot(data=penguins)" inicia el ggplot con el set de datos seleccionado a traves de data=nombre_set.*

*"+" agraga capas al ggplot, para formar el grafico y sus caracteristicas.*

*"geom_point(mapping=aes(x=flipper_lenght_mm, y=body_mass_gg))" establece la forma geometrica del grafico y cuales seran,*
                                                               *los campos que se mostraran y a que eje se le asignan.*

## Problemas mas comunes al visualizar en R
