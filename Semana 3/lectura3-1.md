# Comentario:  Performance of recommender algorithms on top-n recommendation tasks

## Contexto:

El paper explora y analiza el desempeño de distintos sistemas recomendadores en la tarea de recomendar *top-N* items a un usuario. Se discute acerca de las métricas que deberían utilizarse para medir este desempeño (*error metircs* vs *accuracy metrics*) y se comparan distintos tipos de algoritmos:
- *Not personalized* (Most Popular, Average Rating)
- *Neighborhood-based* (itemKNN)
- *Latent factor models*

Además lo anterior, se propone un nuevo algoritmo para esta tarea llamado *PureSVD*, el cual resulta tener un mejor desempeño a la hora de recomendar.

Para medir el rendiminto de cada algoritmo se utilizaron las metricas *recall* y *precision* sobre dos datasets de ratings de películas, *Netflix* y *Movielens*. 


---
## Aspectos interesantes:

Es interesante destacar que los algoritmos fueron puestos a prueba con dos versiones del mismo dataset. Una contemplando todos los datos, y otra sólo usando lo que los autores denominan como "*long tail*", que es la data extrayendole los items más populares e.g con mayor cantidad de ratings. Donde en la primera versión el método *Most Popular* tuvo un mejor rendimiento que otros algoritmos más sofisticados, lo que es inesperado, sin embargo, en la segunda versión su desempeño empeoró significativamente obteniendo los resultados esperados.

También cabe destacar la utilización de un set de validación o *probe set* para ajustar los hiperparametros del model, preveniniendo o disminuyendo un posible sobreajuste.



---
## Críticas

La metodología utilizada consiste en usar los items donde el usuario dio un rating de 5 estrellas, junto con una muestra aleatoria de otros 1000 items que son considerados no relevantes para el usuario e.g que el usuario no ha rateado. Luego el resultado del algoritmo es un set de N items recomendados para dicho usuario y si el item al que le dió 5 estrellas está dentro del set entonces se considera como un acierto o *hit* y en caso contrario como una falla o *miss*

Vale la pena cuestionarse que tan buena es la suposición de que estos 1000 items no son relevantes, quizás se podría seleccionar una muestra disinta con algún tipo de heurística y hacer un analisis de sensibilidad en cuanto al numero de items seleccionados.

Por último, los analisis fueron realizados en base a dos datasets del mismo dominio  y con una distribución muy similar, por lo que el resultado de esta investigación no es extrapolable a otros tipos de dominio ya que no se muestra que tanto afecta la distribución de los datos en los resultados entregados por el algoritmo.

---

## Conclusión

El análisis efectuado y el algoritmo propuesto tienen un gran impacto a la hora de abordar el problema de recomendar un set de *top-N* items a un usuario, dada su fácil implementación y buenos resultados (al menos para este dominio). Pero es necesario hacer un análisis sobre otros factores que podrían afectar el desempeño del algoritmo, como por ejemplo la distribución de los datos, para tener un resultado concluyente sobre el potencial y efectividad real que tiene, la cual es muy prometedora.

---