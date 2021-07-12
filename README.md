# Happy-Score
Utilizamos la biblioteca Pandas para cargar un archivo de datos CVS en la memoria, este archivo es el Informe Mundial sobre la felicidad correspondiente
al año 2015. 
Para el primer análisis, tomamos el campo felicidad (happyScore) y el campo ingresos promedio (avg_income)
para responder a la pregunta ¿el crecimiento economico aumenta la felicidad?
De esta manera, visualizamos el gráfico de dispersión.

Clasificación y filtrado
Luego ordenamos todos estos puntos de datos por el ingreso promedio.
También filtramos los países de la lista que tienen un ingreso superior a 15.000USD y el ingreso más bajo y el más alto en el conjunto de países ricos. 

Estadisticas
Usando la funcionalidad NumPy en nuestro data frame, calculamos:
Cuál es la media en ese conjunto de países que son más ricos que 15.000USD.
Comparamos ese resultado con la media de todo el conjunto de datos. 
De esa forma, obtuvimos la media de todo el conjunto de datos y la media de las personas que tienen más de 15.000USD en ingresos medios

