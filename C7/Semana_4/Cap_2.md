# Explora la estética en el análisis

## Mejoras a visualizaciones en R

La estética, puedes destacar puntos claves de tus datos y comunicarte con mayor claridad y efectividad con tus interesados.

*Estética* es una propiedad visual de un objeto en tu diagrama. Por ejemplo, en un diagrama de dispersión la estética incluye
el tamaño, la forma y el color de tus puntos de datos. Puedes mostrar un punto de diferentes maneras modificando su es-
tética o su apariencia.

Podemos modificar, forma, color, tamaño, etc de nuestro diagramas de dos maneras, una utilizando las variables asociadas
a la funcion aes de la mapping, separadno con una como y agragando el atributo a modificar por ejemplo, lo siguiente
cambiara el color del grafico para distinguir la especies y la forma:

    ggplot(data=penguins) + geom_point(mapping=aes(x=flipper_lenght_mm, y=body_mass_gg, color=species, shape=species))

el resultado

![Alt text](image-10.png)

con el atributo alpha aclaramos unos puntos y asentuamos otros para mejorar la viasualizacion para personas con limitaciones
visuales.

esto trabaja con los colores por defecto, si se quiere dar un colo en particular al grafico podriamos hacerlo, colocando
el atributo a modificar fuera del parentecis de la sigueinet forma:

    ggplot(data=penguins) + geom_point(mapping=aes(x=flipper_lenght_mm, y=body_mass_gg), color="purple")

El resultado

![Alt text](image-11.png)

### Atributos estéticos

En esta lectura, aprenderás acerca de tres atributos estéticos básicos a tener en cuenta al crear visualizaciones ggplot2
en R: color, tamaño y forma. Estos atributos son herramientas esenciales para crear visualizaciones de datos con ggplot2
y se incorporan directamente a su código.

![Alt text](image-12.png)

*Estética en ggplot2:*

Ggplot2 es un paquete de R que te permite crear diferentes tipos de visualizaciones de datos directamente en tu lugar de
trabajo R. En ggplot2, una estética se define como una propiedad visual de un objeto de tu diagrama.

Existen tres atributos estéticos en ggplot2:

    Color: te permite modificar el color de todos los puntos de tu diagrama o el color de cada grupo de datos

    Tamaño: te permite modificar el tamaño de los puntos de tu diagrama por grupo de datos

    Forma: te permite modificar la forma de los puntos de tu diagrama por grupo de datos

Este es un ejemplo de cómo se muestran los atributos estéticos en R:

    ggplot(data, aes(x=distance, y= dep_delay, color=carrier, size=air_time, shape = carrier)) +

      geom_point()

Al aplicar estos atributos estéticos a tu trabajo con ggplot2, puedes crear visualizaciones de datos en R que comunican
tendencias con claridad en tus datos.
