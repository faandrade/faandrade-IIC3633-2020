# Comentario: Multi-Armed Recommender System Bandit Ensembles

## Contexto:

Los ensambles en sistemas recomendadores han mostrado tener una efectividad mayor que sus componentes por separado, sin embargo, la mayoría de las investigaciones en el área se ha centrado en escenarios simplistas donde los algoritmos son testeados y comparados luego de solo una ejecución (1 run), y donde no hay interacción con el usuario.

Este paper  considera un escenario mas realista, tomando en cuenta la naturaleza iterativa de la tarea de recomendación, donde gran parte de las entradas del sistema son recolectadas a partir de las reacciones que tiene el usuario luego de que sus recomendaciones son entregadas, dandole la oportunidad al sistema para que aprenda de esto y progresivamente vaya mejorando la efectividad de las recomendaciones, mejorando la configuración de algoritmos que forman el ensamble en forma progresiva.

Los investigadores buscan lograr esto a través de la adaptación de un *multi-armed bandit*  para abordar el problema, donde los sistemas combinados son *arms* (brazos) y el ensamble corresponde al *bandit*, que en cada iteración se escoge un *arm* para hacer las recomendaciones.

---
## Aspectos interesantes

Es interesante destacar la visión que tuvieron los investigadores al abordar el problema, ya que se dieron cuenta de que la mayoría del trabajo en el área solo contemplaba pruebas y comparaciones entre algoritmos en un contexto estático y sin interacciones con el usuario, lo cual es poco realista considerando la forma en que estos sistemas serían implementados en un caso de uso real, es por esto, que los resultados de los experimentos que llevaron a cabo son una aproximación mucho mas valiosa para alguien que quisiera implementar este tipo de recomendadores. Por otro lado, el enfoque propuesto en esta investigación de la adaptación de un *multi-armed bandit* logró mejores resultados empíricos que las alternativas de ensamble y que los algorítmos de forma individual, y todo esto con un bajo costo computacional, lo cual es importante destacar ya que un requisito hoy en día para cualquier recomendador que busque ser usado en algun caso real, dada la cantidad de información presente en la actualidad, es la escalabilidad.

---
## Críticas

Con respecto a las métricas usadas para calcular el desempeño del algoritmo, solo se mide en cuanto a *cumulative recall*, lo cual si bien es importante, no abarca la totalidad de dimensiones por la que un recomendador podría ser medido, por lo que sería interesante analizar otras métricas como *nDCG*, *novelity*, *serendipity*, etc. Para tener una idea más completa del desempeño general de este ensamble. Por otro lado, el ensamble se limita a los algoritmos *kNN*, *Matrix Factorization* and *Nonpersonalized Most-popular*, que si bien son una buena base para experimentar sobre la eficiencia de su propuesta de ensamble, sería interesante ampliar esa lista, con el fin de ver si el número de algoritmos afecta el rendimiento del ensamble (y de qué forma) y si la calidad de recomendaciones es consistente a medida que crece el ensamble, y que se agregan otro tipo de algoritmos de recomendación como *BPR*, por ejemplo.


---
## Conclusión

Para concluir, podemos decir que el enfoque de los experimentos realizados en este trabajo, donde hay una interacción con el usuario y la respuesta de este es utilizada para que el sistema afine su configuración y mejore las predicciones, es muy valiosa ya que deja atrás los escenarios simplistas y poco realistas, que habían sido estudiados en el área en forma predominante, además se muestra en el paper que su sistema a partir de un *multi-armed bandit* logra buenos resultados y a un bajo costo computacional, haciendolo escalable, lo que hace de este sistema un candidato potencial para todo aquel que quiera implementar un recomendador en un caso de uso real.

---