# Fundamentos de paneles en tableau

elementos de mosaico son paneles fijos que acompañan el eje central de explicaion de los datos a los interesados
los elementos flotaten se superponen a los demas elementos y permiten enfatizar ciertos aspectos que son cambiantes en
la narrativa de la historia que plantean los datos.

los dashboards o paneles, le otorgan el control de la historia a los interesados, ya no es el analista contando una historia,
sino los interesados ordenando los elementos para llegar a una conclusion, mientras qu elos informas son esaticos y presentan
de una manera fija las conclusiones entregadas por los analistas.

## Paneles e información estática

Los paneles y la información estática permiten al cliente o al usuario tener el control de su narrativa. Con los paneles,
cualquiera puede utilizar los datos y tomar sus propias decisiones. Un panel puede construirse sobre información o datos
estáticos, es decir, datos que no cambian una vez que fueron registrados. Esto permite controlar de forma estricta la narrativa
y la forma en que los datos se presentan visualmente, ya sea a través de gráficos, tablas, etc.

Identificar si los datos son activos o estáticos depende de ciertos factores:

        ¿Qué antigüedad tienen los datos?

        ¿Cuánto tiempo falta para que los datos sean obsoletos o dejen de ser válidos para tomar decisiones?

        ¿Es necesario actualizar regularmente estos datos o análisis para que sigan siendo valiosos?

Los datos *estáticos* implican proporcionar capturas de pantalla o instantáneas en las presentaciones o construir paneles
utilizando instantáneas de datos. Los datos estáticos tienen pros y contras.

    PROS

        Pueden controlar de forma estricta una narrativa puntual de los datos y la información

        Permiten explicar en profundidad análisis complejos a un público más amplio

    CONTRAS

        La información empieza a perder valor inmediatamente y continúa haciéndolo cuanto más tiempo permanecen los datos
        en un estado estático

        Las instantáneas no pueden seguir el ritmo de los cambios en los datos

Los datos *activos* significan que se pueden crear paneles, informes y vistas conectadas a los datos actualizados
automáticamente.

    PROS

        Se pueden crear paneles más dinámicos y escalables

        Proporcionan los datos más actualizados a las personas que los necesitan en el momento en que los necesitan

        Permiten obtener vistas actualizadas de los datos con la capacidad de construir una “única fuente de verdad” es-
        calable para diversos casos de uso

        Permiten tomar medidas inmediatas sobre los datos que cambian con frecuencia

        Alivian el tiempo y los recursos dedicados a los procesos de cada análisis

    CONTRAS

        Pueden requerir recursos de ingeniería para mantener las canalizaciones activas y escalables, lo que puede estar
        fuera del alcance de la asignación de recursos de datos de algunas empresas

        Sin la capacidad de interpretar los datos, se puede perder el control de la narrativa, lo que puede provocar un
        caos de datos (es decir, que los equipos lleguen a conclusiones contradictorias basadas en los mismos datos)

        Pueden causar potencialmente una falta de confianza si los datos no se manejan adecuadamente

## Filtros

las siguientes tareas se pueden utilizar filtros en Tableau, limitar la información, personalizarla o resaltar un punto
de datos.
