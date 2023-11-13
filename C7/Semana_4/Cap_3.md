# Anota y guarda visualizaciones

## Capa de anotaciones

Anotar significa agregar notas a un documento o diagrama, para explicar o comentar o resaltar un punto de este, el proposito
del diagrama.

Es de gran utilidad agregar etiquetas informativas a un diagrama, como titulos, subtitulos o leyemdas

Para agregar un titulo en un diagrama o grafico en r, colocamos labs() que es una fucnion creqada con dicho objetivos de
la siguiente manera:

    ggplot(data=data_set_name)+
        geaom_(graphic_tipe)()+
            labs(titele="title")

notece que usamos el sigono "+" para agregar una nueva capa al grafico que seria la funcion labs con su titulo entre comillas
ya que requiere un argumento tipo texto.

![Alt text](image-25.png)

la salida:

![Alt text](image-26.png)

Para agregar un titulo y subtitulo en un diagrama o grafico en r, colocamos labs() que es una fucnion creqada con dicho
objetivos de la siguiente manera:

    ggplot(data=data_set_name)+
        geaom_(graphic_tipe)()+
            labs(titele="title_text", subtitle="subtitle_text")

Para agregar un titulo, subtitulo y leyenda en un diagrama o grafico en r, colocamos labs() que es una fucnion creqada con
dicho objetivos de la siguiente manera:

    ggplot(data=data_set_name)+
        geaom_(graphic_tipe)()+
            labs(titele="title_text", subtitle="subtitle_text", caption="caption_text")

Para agregar un anotacion en un diagrama o grafico en r, colocamos annotate() que es una fucnion creqada con
dicho objetivos de la siguiente manera:

![Alt text](image-27.png)

Notece que requiere un texteo que sera el tipo de anotacion(geom), las coordenadas donde se ubicacra la anotacion X/Y que
es un dato de tipo numerico y un texto que sera el cuerpo de la anotacion.

es posible cmabiar las cracteristicas de la anotacion tales como, color, tipo de letra, tamaño, tambien la alineacion a traves
del grado de inclinacion del texto, etc.

## guardado de diagramas ggplot

El guardado puede ser por exportacion, ya sea en multiples formatos de imagen o pdf y tambien con la funcion ggsave.

Ggsave es una función útil para guardar un diagrama. De manera predeterminada, guarda el último diagrama que mostraste y
usa el tamaño del dispositivo gráfico actual.

    ggsave("file_name.extension")

la extension, es un formato de imagen o pdf
