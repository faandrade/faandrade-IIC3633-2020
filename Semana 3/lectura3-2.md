# Comentario:  Evaluating recommendation systems

## Contexto:

*Evaluating recommendation systems* es el octavo capitulo del libro *Recommender systems handbook* escrito por *Francesco Ricci*, *Lior Rokach* y *Bracha Shapira*.
En él se discute sobre cómo comparar sistemas recomendadores basados en un set de propiedades (*accuracy*, *robustness*, *scalability*, etc) que son relevantes para cada aplicación. Se describen los ajustes o *settings* experimentales que se deben seguir para poder tomar decisiones sobre que algoritmo usar y se revisan tres tipos de experimentos:
- *offline setting*, donde no hay interacción con el usuario
- *user studies*, donde un grupo pequeño de usuarios reporta feedback
- *large scale online experiments*, que representa el caso de uso real que tendría el sistema

También se sugieren protocolos para la experimentación, se discute sobre cómo sacar conclusiones confiables en base a los experimentos realizados y se finaliza con una revisión de una gran cantidad de propiedades de estos sistemas, explicando cómo evaluarlos en base a estas.


---

## Aspectos interesantes:

Lo que más destaco sobre el capítulo, además de la completitud con la que los autores desarrollan cada tema, es la forma instructiva y didáctica con la que lo hacen, lo que se puede ver por ejemplo en la seccion 8.2, donde se desarrollan cada uno de los tres tipos de experimentos mencionados anteriormente, mostrando ventajas y desventajas de cada uno además de discutir sobre cómo debiesen ser llevados a cabo, disminuyendo así el esfuerzo y tiempo que necesita ser empleado por el lector para lograr una comprensión más profunda, lo cuál es muy valioso teniendo en cuenta la complejidad de cada tema abordado no es trivial, y puede tener un impacto profundo a la hora de modelar y desarrollar un sistema recomendador, cuya utilidad hoy en dia en un mundo sobrecargado de información es gigantesca.

---
## Críticas

Con respecto al desarrollo de los experimentos offline, se menciona que muchas veces hay registro del tiempo en que la interacción con el usuario fue llevada a cabo, también llamado *timestamp*, sin embargo, en ningun momento se desarrolla un modelo que los utilice, como podría ser por ejemplo, una red neuronal o algún algoritmo de aprendizaje profundo.

---

## Conclusión

Podemos concluir que el capítulo provee una ayuda fundamental para aquellos que busquen desarrollar o implementar algún sistema recomendador, dando herramientas sobre cómo discernir que algoritmo seleccionar en base a los posibles candidatos (de acuerdo al caso de uso particular), además de abordar temas importantes como por ejemplo, qué consideraciones tener al desarrollar experimentos y las métricas asociadas que deben ser tomadas en cuenta. Todo esto presentado y desarrollado de forma didáctica e instructiva para el lector.

---