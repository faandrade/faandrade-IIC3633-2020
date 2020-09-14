# Comentario: Context-Aware Recommender Systems. AI Magazine.

## Contexto:

Los *Context-aware recommender systems(CARS)* son sistemas que generan recomendaciones más relevantes para el usuario ya que se adaptan al contexto de su caso de uso en particular. Este artículo explora cómo la información del contexto puede ser usada para crear sistemas de recomendación útiles e inteligentes. Da una mirada a las distintas facetas que tiene la noción de "contexto" y  se discuten distintas formas de incorporar la información contextual al proceso de recomendación, además se muestra el uso de esta en distintas áreas de aplicación en donde se explotan diferentes contextos y se concluye con una discusión sobre los desafíos y futuras líneas de investigación para este tipo de sistemas.

---
## Aspectos interesantes:

Es interesante notar que el comportamiento humano efectivamente está condicionado por un contexto específico, el cual es dinámico y , según lo afirmado en el artículo, muy difícil de capturar en un modelo de recomendación ya que dependen directamente de la calidad de las heurísticas utilizadas, las cuales son específicas para cada caso de uso, por ejemplo, ir al cine con la familia y con el novio/a son dos contextos totalmente diferentes para consumir un mismo item (peliculas en este caso), y es de esperar que las caracteríisticas de cada item consumido sea diferentes en cada caso.  Es por esto que, incluir información del contexto al modelo hace que, en mi opinion, la modelación sea mucho mas robusta y que represente de mejor forma la realidad, lo cuál se ha traducido en mejoras significativas en algoritmos de recomendación, como por ejemplo, al incorporar estos factores en una tecnica de *machine learning* llamada *Support Vector Machines* en el articulo se expone lo siguiente:

~~~
Oku et al.(2006) empirically show that context-aware SVM significantly outperforms noncontextual SVMbased recommendation algorithm in terms of predictive accuracy and user’s satisfaction with recommendations
~~~

Lo cual muestra que, a pesar de que este tipo de sistemas son relativamente nuevos, su potencial es gigantesco y podrían impactar profundamente en la forma en que son abordados los problemas de recomendación, mejorando tanto a nivel de precision, como de satisfacción del usuario.

---
## Críticas

Si bien el artículo expone cada tema de forma clara y muy completa, en la sección *Proactive and Distributed Approaches*  se afirma lo siguiente:
~~~
If the surrounding environment can use sensors to recognize us and our activities, then novel proactive and distributed services will be possible (“ubiquitous computing”).
~~~

pero en ningún momento se mencionan los problemas éticos que podrían generar, por ejemplo, el usuario debería estar al tanto de que información suya esta siendo recolectada, de qué forma y con qué fin. Por otro lado, llevandolo a un extremo en donde estos sistemas son capaces de capturar el contexto a tal forma que predicen exactamente el comportamiento de cada individuo, podría tener un impacto más profundo que solo mostrar items potenciales que al usuario le gustaría consumir, sino que pasarían a influir directamente en el comportamiento de este, lo que podría rayar incluso en restringir de cierta forma la libertad de cada individuo. A pesar de que aún falta mucho para que este tipo de sistemas tengan tal poder, su desarrollo debiese ser siempre teniendo en cuenta el alcance y las consecuencias que estos podrían generar. Por otro lado, un problema más actual de los sistemas recomendadores es el *filter bubble*, donde la diversidad de información mostrada a cada usuario se ve sesgada por su comportamiento en el pasado, quizas este tipo de sistema podría resolver en parte este problema, por ejemplo, capturando un contexto en donde el usuario está investigando un tema nuevo para él y se le presenta información variada con distintos puntos de vista sobre dicho tema, más que tratar de predecir cuales son los puntos de vista que más le van a gustar en base a su comportamiento anterior.  

---

## Conclusión

Los *Context-aware recommender systems(CARS)* son un tipo de sistemas que, al incorporar información sobre el contexto, tienen un impacto considerable en las recomendaciones, tanto a nivel de precisión del algoritmo como de satisfacción del usuario, esto se puede deber principalmente a que, efectivamente el contexto juega un rol fundamental a la hora de predecir el comportamiento de un individuo, por lo que la incorporación de estos factores hacen que el modelo represente de forma mas precisa la realidad, sin embargo, a pesar de que estos tienen un potencial enorme para mejorar los sistemas de recomendación, se debe tener en cuenta la privacidad del usuario a la hora de recolectar datos, sobre todo en sistemas propuestos como *Proactive and Distributed Approaches* y así poder cumplir el objetivo de una buena calidad de recomendaciones, sin caer en ningun conflicto con la ética ni privacidad de los individuos. 


---