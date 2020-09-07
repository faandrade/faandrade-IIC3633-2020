# Comentario: Document clustering based on non-negative matrix factorization

## Contexto:

En este paper se propone un nuevo método  para hacer *Clustering* de documentos, específicamente uno del tipo *document partitioning* o *flat clustering*, a través de la *factorizacion no-negativa* de la matriz *term-document* del cuerpo de dicho documento. Luego este método es comparado con otros que buscan cumplir la misma tarea, tales como clustering de documentos basado en *descomposicion de valores singulares* (SVD) y basado en *vectores propios* o *eigen-vectors*, resultando tener una mejor explicabilidad de los *Clusters* obtenidos, es decir, es más facil explicar el por qué un documento fue agrupado en un *Cluster* específico, y además resultó tener una mejor precisión en comparación a los métodos mencionados anteriormente 


---
## Aspectos interesantes:

Es interesante destacar la forma en la que los autores presentan su método  y las suposiciones que utilizaron, apelando a la "naturalidad" de estas, por ejemplo, en el primer parrafo de la sección 3, *The proposed method* se plantea lo siguiente:

> *it is more __natural__ to consider __each document as an additive rather than subtractive mixture of the underlying topics__, the linear combination coefficients __should all take non-negative values__. Furthermore, it is also quite common that the topics comprising a document corpus are not completely independent of each other, and there are some overlaps among them. In such a case, the axes of the semantic space that capture __each of the topics are  not necessarily orthogonal__*

Derivando así de forma "natural" el cómo se modeló el problema, y es precisamente este modelamiento en donde un documento no pertenece sólo a un tema en específico, como es en el caso de los otros métodos, sino a una combinación de varios posibles lo que, a mi parecer, le lleva a obtener finalmente los buenos resultados en los experimentos.

---
## Críticas

Con respecto a la cantidad de factores latentes utilizados para representar un documento, en el paper no se explicita de que forma afectan al rendimiento del algoritmo, sería interesante hacer experimentos y análisis de sensibilidad sobre este parámetro. Suponiendo que para este trabajo seleccionaron ese *k* mediante *cross validation*, valdría la pena investigar sobre alguna forma de al menos estimar este parámetro, ya que la complejidad de la resolución del problema no es trivial y podría eventualmente generar problemas de escalabilidad. 

---

## Conclusión

La forma en que los investigadores modelan el problema descrito, dando origen al método propuesto basado en *factorización no-negativa* supone una mejora significativa en esta área de investigación, no solo por los resultados experimentales y la precisión alcanzada, sino principalmente porque además los resultados del algoritmo son fáciles de explicar y de comprender, lo que ciertamente es muy atractivo ya que es una característica que generalmente no se da en otros algoritmos de *clustering*, como por ejemplo en *K-means*.

---