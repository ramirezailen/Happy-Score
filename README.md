# Happy-Score
Utilizamos la biblioteca Pandas para cargar un archivo de datos CVS en la memoria, este archivo es el Informe Mundial sobre la felicidad correspondiente
al año 2015. 
Para el primer análisis, tomamos el campo felicidad (happyScore) y el campo ingresos promedio (avg_income)
para ver si hay una correlación entre crecimiento economico y aumento de la felicidad. 
De esta manera, visualizamos el gráfico de dispersión.

## Clasificación y filtrado
Luego ordenamos todos estos puntos de datos por el ingreso promedio.
También filtramos los países de la lista que tienen un ingreso superior a 15.000USD y el ingreso más bajo y el más alto en el conjunto de países ricos. 

## Estadisticas
Usando la funcionalidad NumPy en nuestro data frame, calculamos:
Cuál es la media en ese conjunto de países que son más ricos que 15.000USD.
Comparamos ese resultado con la media de todo el conjunto de datos. 
De esa forma, obtuvimos la media de todo el conjunto de datos y la media de las personas que tienen más de 15.000USD en ingresos medios.

## Etiquetado de puntos en el gráfico
En el Data frame "richest" que contiene todos los países que tienen un ingreso promedio de más de 15.000USD, usamos el ingreso promedio
y la puntuación feliz para colocar los puntos en el gráfico y usamos el nombre del país para que sea la etiqueta. 
Para esto, primero generamos la función plot con los valores x (richest[avg_income]) e y (richest[happy_Score]) 
que van a conformar el gráfico. 
Pero no muestra qué país es cuál punto. Por lo cual, generamos etiquetas de texto: para el ingreso promedio más rico y el más bajo.
Se puede ver que Luxemburgo, a pesar de que es el más rico de este conjunto de países, no tiene la puntuación feliz más alta. 

Luego, se presenta todos los nombres de los países en el gráfico iterando a través de las filas de el Data Frame. 
De esta forma, etiquetamos cada punto en el gráfico con la función "iterrows".


Entonces, lo que tenemos es el -ingreso- trazado en el eje x y la -puntuación feliz- trazada en el eje y. Retomando la pregunta de si los ingresos están conectados de alguna manera a la felicidad, podemos ver: que a medida que los ingresos aumentan de izquierda a derecha, la felicidad parece aumentar.
Pero también se puede ver en la parte superior izquierda del gráfico, hay varios países que tienen ingresos bajos pero parecen ser tan felices como los países con mayores ingresos. 

## Implementación K-Means
Replicamos la información que encontramos mirando el gráfico usando K-Means, de esta forma identificamos los puntos de una manera estadisticamente precisa. 
Para que podamos comparar nuestra interpretación visual de los datos con la interpretación de K-Means de los datos.

Elegimos 3 clústeres.
Con la función km_res.cluster_centers_ vimos dónde están los centros de clústeres. Y se encontró que hay un grupo de ingresos de 2.100USD con una calificación de felicidad baja, otro grupo con ingresos muy altos con alta felicidad y el último grupo que tiene ingresos bajos pero una puntuación de felicidad alta. 
Trazamos estos puntos en un gráfico. 
En color naranja están representados los 3 grupos: en la parte superior derecha, el ingreso alto y alta felicidad. Más abajo, el ingreso más bajo pero una buena puntuación de felicidad. Por último, el ingreso más bajo con una baja puntuación de felicidad.

Entonces, K-Means encontró el mismo conjunto de puntos de datos que notamos a simple vista. 

