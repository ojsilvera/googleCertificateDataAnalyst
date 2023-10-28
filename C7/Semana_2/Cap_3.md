# Aprende acerca de los paquetes R

## Paquetes R disponibles

CRAN web que almacena los paquetes y repositorios pertenecientes a R, es el mas usado [https://cran.r-project.org/], aunque
tambien github puede ser usado y cualquier otro sistema de control de versioens.

Los paquetes son unidades de código R reproducible y hacen que sea más fácil hacer un seguimiento del código. Fueron
creados por miembros de la comunidad R para hacer un seguimiento de las funciones R que ellos escriben y vuelven a usar.
Estos miembros de la comunidad podrían poner los paquetes a disposición de otros usuarios.

Los paquetes en R incluyen funciones en R reutilizables y documentación sobre las funciones, incluido cómo usarlas. También
contienen muestras de conjuntos de datos y pruebas para verificar tu código para asegurarte de que hace lo que quieres
que haga. Por defecto, R incluye un conjunto de paquetes denominados Base R que están disponibles para su uso en RStudio
cuando empiezas tu primera sesión de programación

## Ejemplos de paquetes y sus usos

[https://www.tidyverse.org/] -> La colección de tidyverse de paquetes de R está diseñada especialmente para trabajar con
datos. Es una biblioteca estándar para la mayoría de los analistas de datos, pero también puedes descargar los paquetes
en forma individual.

Tidyverse es, en realidad, una colección de paquetes en R con una filosofía de diseño común para la manipulación, explo-
ración y visualización de datos. Usar tidyverse puede ayudarte a trabajar a tu manera durante gran parte de todo el pro-
ceso de análisis de datos.

[https://support.rstudio.com/hc/en-us/articles/201057987-Quick-list-of-useful-R-packages] -> Esta es la lista de apoyo
de RStudio donde encontrarás paquetes útiles con instrucciones de instalación y la descripción de su funcionalidad.

[https://cran.r-project.org/web/views/] -> Este es un índice de los paquetes CRAN ordenados por tarea. Puedes buscar el
tipo de tarea que necesitas realizar y te traerá una página con paquetes relacionados con la tarea para que explores.

## tidyverse

El nucleo de paquetes de tidyverse son los siguientes: ggplot2, tidyr, readr, dplyr, tibble, purrr, stringr y forcats.

### tibble

    Tibble trabaja con marcos de datos.

### purrr

    Purrr trabaja con funciones y vectores que ayudan a que tu código sea más fácil de escribir y más expresivo.

### stringr

    Stringr incluye funciones que hacen que sea más fácil trabajar con cadenas.

### forcats

    Forcats proporciona herramientas que resuelven problemas comunes con factores.

*los factores almacenan datos categóricos en R donde los valores de datos están limitados y generalmente se basan en un*
*grupo finito como país o año.*

Pero, hay cuatro de estos paquetes que son una parte esencial del flujo de trabajo para los analistas de datos:

### ggplot2

    Ggplot2 se usa para visualización de datos, especialmente diagramas. Con ggplot2, puedes crear una variedad de vi-
    sualización de datos al aplicar propiedades visuales diferentes a las variables de datos.

### dplyr

    Dplyr ofrece un conjunto consistente de funciones que te ayudan a completar algunas tareas comunes de manipulación
    de datos. Por ejemplo, la función select, escoge variables según sus nombres, y la función filter encuentra casos
    donde determinadas condiciones son ciertas.

### tidyr

    Tidyr es un paquete que se usa para limpieza de datos para generar datos ordenados. Cubrimos datos ordenados o limpios
    anteriormente, pero, a modo de recordatorio, son datos donde cada parte de la tabla de datos o marco de datos es del
    tipo correcto en el lugar correcto. Tidyr funciona con datos en formato ancho y datos en formato largo para asegurarse
    de que esto funciona.

### readr

    readr, que se usa para importar datos. La función más común de readr es read_csv. Esto importará un archivo CSV en R.
    Un archivo CSV contiene datos separados por comas en un formato de tablas. Para leer correctamente un conjunto de datos
    con readr, combinas la función con una especificación de columna. La especificación de columna describe cómo debería
    cada columna convertirse en el tipo de datos más apropiado. Es bueno tener en cuenta que, en general, esto no es ne-
    cesario porque readr lo averiguaría por ti automáticamente.
