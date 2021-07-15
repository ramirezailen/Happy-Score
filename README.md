# Happy-Score
Utilizamos la biblioteca Pandas para cargar un archivo de datos CVS en la memoria, este archivo es el Informe Mundial sobre la felicidad correspondiente
al año 2015. 
Para el primer análisis, tomamos el campo felicidad (happyScore) y el campo ingresos promedio (avg_income)
para responder a la pregunta ¿el crecimiento economico aumenta la felicidad?
De esta manera, visualizamos el gráfico de dispersión.

## Clasificación y filtrado
Luego ordenamos todos estos puntos de datos por el ingreso promedio.
También filtramos los países de la lista que tienen un ingreso superior a 15.000USD y el ingreso más bajo y el más alto en el conjunto de países ricos. 

## Estadisticas
Usando la funcionalidad NumPy en nuestro data frame, calculamos:
Cuál es la media en ese conjunto de países que son más ricos que 15.000USD.
Comparamos ese resultado con la media de todo el conjunto de datos. 
De esa forma, obtuvimos la media de todo el conjunto de datos y la media de las personas que tienen más de 15.000USD en ingresos medios

## Etiquetado de puntos en el gráfico
En el dataframe "richest" que contiene todos los países que tienen un ingreso promedio de más de 15.000USD, usamos el ingreso promedio
y la puntuación feliz para colocal los puntos en el gráfico y usamos el nombre del país para que sea la etiqueta. 
Para esto, primero generamos la función plot con los valores x (richest[avg_income]) e y (richest[happy_Score]) 
y los muestra en el gráfico. 
Pero no muestra qué país es cuál punto. Por lo cual, generamos etiquetas de texto: para el ingreso promedio más rico y el más bajo.
Se puede ver que Luxemburgo, a pesar de que es el más rico de este conjunto de países, no tiene la puntuación feliz más alta. 

Luego, se presenta todos los nombres de países en el gráfico iterando a través de las filas de el Data Frame. 
De esta forma, etiquetamos cada punto en el gráfico con la función "iterrows"


Entonces, lo que tenemos es el -ingreso- trazado en el eje x y la -puntuación feliz- trazada en el eje y. Retomando la pregunta ¿Los ingresos están conectados de alguna manera a la felicidad?
Y podemos ver: a medida que los ingresos aumentan de izquierda a derecha la felicidad parece aumentar.
Pero también se puede ver en la parte superior izquierda del gráfico, hay varios países que tienen ingresos bajos pero parecen ser tan felices como los países con mayores ingresos. 

