# Programar con RStudio

## Comprender los conceptos básicos de programación

En programación, una estructura de datos es un formato para organizar y almacenar datos. Es importante que conozcas las
estructuras de datos porque las usarás con frecuencia cuando utilices R para el análisis de datos. Las estructuras de
datos más comunes en el lenguaje de programación R incluyen:

### Vectores

Un vector es un grupo de elementos de datos del mismo tipo almacenado en una secuencia en R. No puedes tener un vector
que contenga valores lógicos y numéricos.

*Tipos de vectores:*

Existen dos tipos de vectores: vectores atómicos y listas. Luego, aprenderás sobre las propiedades básicas de los vectores
atómicos y las listas, y cómo utilizar el código R para crearlos.

Vectores atómicos

Primero, repasaremos los diferentes tipos de vectores atómicos. Luego, aprenderás cómo utilizar el código R para crear,
identificar y nombrar a los vectores.

Existen seis tipos primarios de vectores atómicos: lógicos, enteros, dobles, carácter (que contiene cadenas), complejos y
sin formato. Los dos últimos, complejo y sin formato, no son comunes en el análisis de datos, de modo que nos vamos a
concentrar en los primeros cuatro. Juntos, los vectores entero y doble son conocidos como vectores numéricos porque ambos
contienen números. Esta tabla resume los cuatro tipos primarios:

![Alt text](image.png)

Este diagrama ilustra la jerarquía de relaciones entre estos cuatro tipos principales de vectores:

![Alt text](image-1.png)

*Crear vectores:*

Una forma de crear un vector es utilizar la función c() (llamada función "combinar"). La función c() en R combina valores
múltiples en un vector. En R, esta función es solo la letra "c" seguida de los valores que deseas colocar en tu vector,
entre paréntesis, separados por una coma: c(x, y, z, …).

Por ejemplo, puedes utilizar la función c() para almacenar datos numéricos en un vector.

    v_1 <- c(2.5, 48.5, 101.5)

Para crear un vector de números enteros utilizando la función c(), debes colocar una "L" directamente después de cada número.

    v_2 <- c(1L, 5L, 15L)

También puedes crear un vector que contenga caracteres o valores lógicos.

    v_3 <- c(“Sara” , “Lisa” , “Anna”)

    v_4 <- c(TRUE, FALSE, TRUE)

Marcos de datos

Matrices

Rangos
