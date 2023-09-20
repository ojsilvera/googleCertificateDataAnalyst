# El proceso de validación de datos

La validación de datos, una función de la hoja de cálculo que agrega listas desplegables a las celdas. Usar la validación
de datos te permite controlar lo que se puede o no ingresar en tu hoja de cálculo. Uno de sus usos es proteger datos y
fórmulas estructurados en las hojas de cálculo.

La validación de datos ademas implica comprobar y volver a comprobar la calidad de tus datos para que sean completos,
precisos, seguros y coherentes. Aunque el proceso de validación de datos es una forma de limpieza de datos deberías usarlo
a lo largo de tu análisis.

## Tipos de validación de datos

La siguiente tabla describe el propósito, los ejemplos y las limitaciones de los seis tipos de validación de datos. Los
primeros cinco son tipos de validación asociados con los datos (tipo, rango, limitación, coherencia y estructura) y el
sexto tipo se centra en la validación del código de aplicación que se utiliza para aceptar los datos a partir del aporte
del usuario.

Como analista de datos junior, es posible que no tengas que realizar todas estas validaciones. Pero podrías consultar si
los datos se validaron y de qué manera antes de comenzar a trabajar con un conjunto de datos. La validación de datos ayuda
a garantizar la integridad de los datos. Además, te proporciona confianza en cuanto a que los datos que estás utilizando
están limpios. La siguiente lista describe los seis tipos de validación de datos y el propósito de cada uno e incluye
ejemplos y limitaciones.

1- Tipo de datos

Propósito: Comprobar que los datos coincidan con el tipo de datos definido para un campo.

Ejemplo: Los valores de los datos para los grados escolares de 1 a 12 deben ser del tipo de datos numéricos.

Limitaciones: El valor de datos 13 pasaría la validación del tipo de datos pero sería un valor inaceptable. En este caso,
la validación del rango de datos también es necesaria.

2- Rango de datos

Propósito: Comprobar que los datos se ubiquen dentro de un rango de valores aceptable definido por el campo.

Ejemplo: Los valores de datos para los grados escolares deben ser valores entre 1 y 12.

Limitaciones: El valor de datos 11.5 estaría dentro del rango de datos y también sería aceptable como un tipo de dato
numérico. Sin embargo, no sería aceptable porque no existen medios grados. En este caso, la validación de la limitación
de datos también es necesaria.

3- Limitaciones de datos

Propósito: Comprobar que los datos cumplan con ciertas condiciones o criterios para un campo. Esto incluye el tipo de datos
ingresados además de otros atributos del campo como, por ejemplo, el número de caracteres.

Ejemplo: Restricción del contenido: Los valores de los datos para los grados escolares de 1 a 12 deben ser números enteros.

Limitaciones: El valor de datos 13 es un número entero y pasaría la validación de restricción de contenido. Sin embargo,
no sería aceptable dado que 13 no es un grado escolar reconocido. En este caso, la validación del rango de datos también
es necesaria.

4- Coherencia de los datos

Propósito: Comprobar que los datos tienen sentido en el contexto de otros datos relacionados.

Ejemplo: Los valores de los datos para las fechas de envío del producto no pueden ser anteriores a las fechas de producción
del producto.

Limitaciones: Los datos podrían ser coherentes pero son incorrectos o poco precisos. Una fecha de envío podría ser posterior
a una fecha de producción y aun así ser incorrecta.

5- Estructura de los datos

Propósito: Comprobar que los datos siguen o se ajustan a una estructura establecida.

Ejemplo: Las páginas web deben seguir una estructura prescrita para que se muestren adecuadamente.

Limitaciones: Una estructura de datos podría ser correcta siendo los datos incorrectos o poco precisos. El contenido de
una página web podría mostrarse adecuadamente y aun así contener información incorrecta.

6- Validación del código

Propósito: Comprobar que el código de aplicación realice sistemáticamente cualquiera de las validaciones antes mencionadas
durante el ingreso de datos del usuario.

Ejemplo: Los siguientes son problemas comunes que se descubren durante la validación del código: más de un tipo de datos
permitido, comprobación del rango de datos no realizada o finalización de cadenas de texto que no están bien definidas.

Limitaciones: La validación del código podría no validar todas las posibles variaciones con el ingreso de datos.
