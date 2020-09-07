# Comentario: Content-based recommendation systems. In The adaptive web (chapter 10)

## Contexto:
 En este capítulo se discuten los *sistemas de recomendación basados en contenido*, es decir, los sistemas que basan sus recomendaciones en las características de cada item, acompañado de un perfil de las preferencias de cada usuario.  En primer lugar se presentan distintas alternativas para representar los items a recomendar, luego se discuten distintos algoritmos que podrían ser adecuados de utilizar en base a la representación escogida para el item, y finalmente el capitulo concluye con una discusión sobre los distintos enfoques que pueden tener estos sistemas, sus fortalezas y debilidades, junto con las futuras líneas de investigación y desarrollo en el área. 


---
## Aspectos interesantes:

Llama la atención la forma simple y explicativa en la que está escrito el capítulo, si bien cada tema no se aborda en un nivel de detalle lo suficientemente profundo como para implementar cada uno de estos sistemas sólo en base a lo desarrollado, cada uno de ellos se explica de forma clara y simple, permitiendo que el lector tenga un alto nivel de comprensión (al menos conceptual) sin desgastarse de forma excesiva en la lectura, esto tambien incluye la explicaciones de ecuaciones utilizadas por algunos modelos que no son triviales y de algunos resultados desconcertantes, de los cuales destaco la explicación de la formula de de *descenso de gradiente* en la seccion 10.7 *Linear Classifiers*
> *The equation shows how the weight vector w can be derived incrementally. The inner product of instance xi and weight vector wi is the algorithm’s numeric prediction for instance xi. The prediction error is determined by subtracting the instance’s known score, yi, from the predicted score. The resulting error is then multiplied by the original instance vector xi and the learning rate η to form a vector that, when subtracted from the weight vector w, moves w towards the correct prediction for instance xi. The learning rate η controls the degree to which every additional instance affects the previous weight vector*

y la afirmación presenatda en la sección 10.8 *Probabilistic Methods and Naïve Bayes* donde se indica que el modelo funciona a pesar de que se violan algunos supuestos

>*Even though the naïve Bayes assumption of class-conditional attribute independence is clearly violated in the context of text classification, naïve Bayes per-forms very well. Domingos and Pazzani [12] offer a possible explanation for this paradox by showing that class-conditional feature independence is not a necessary condition for the optimality of naïve Bayes. The naïve Bayes classifier has been used in several content-based recommendation systems including Syskill & Webert [29].*

---
## Críticas

A pesar de que cada tema no se desarrolla en mayor profunidad, creo que vale la pena al menos mencionar los problemas de escalabilidad que supondrían algunos modelos propuestos, como por ejemplo en la seccion 10.5 *Nearest Neighbor Methods*, donde eventualmente si no se precomputan algunos datos, los recursos necesarios para ejecutar el algoritmo van a ser excesivos y el sistema va a dejar de funcionar correctamente, lo cual en ningun momento se menciona. Por otro lado, la mayoría de los temas fueron ejemplificados para el caso de *text classification*, lo cual si bien puede dar una línea para que el lector pueda comparar de mejor manera los distintos algoritmos y técnicas propuestas, también se pierde la visión de la amplitud y variedad de situaciones en las que estos modelos son aplicables, las cuales ciertamente son muchísimas, sobre todo en la sociedad sobrecargada de información en la que vivimos hoy en día.

---

## Conclusión

El capítulo ofrece una explicación simple y concisa sobre los *sistemas de recomendación basados en contenido*, los algoritmos más relevantes y algunas de sus fortalezas y debilidades. A pesar de que no se desarrollan en excesiva profundidad, el lector es capaz de asimilar los conceptos sin un mayor esfuerzo, lo que hace que la lectura sea muy llevadera y hace de este capítulo una buena herramienta para todo aquel interesado en el tema y que quiera aprender o reforzar las características escenciales de este tipo de sistemas.

---