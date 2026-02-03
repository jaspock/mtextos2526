
P3. Modelos generativos
====================================

```{admonition} Nota
:class: note
Lee con atención la práctica 3 del bloque 3. Realiza los ejercicios y entrega la correspondiente prácica que se anunciará en la introducción de la asignatura y a través del uaCloud.

Tiempo de dedicación: 3 horas (asíncrona) + 3 horas trabajo independiente
```

## **Clase práctica.**

### Modelos generativos: Caso de estudio de Clasificación de noticias

<!-- **Autores:**

- [Yoan Gutiérrez Vázquez][yoan]
- [Eduardo Grande] Ruiz[grande] 
- [Juan Pablo Consuegra Ayala] [consuegra]
-->

### Descripción

En esta clase práctica estudiaremos cómo diseñar distintos sistemas de clasificación textual utilizando modelos generativos.
Se orientarán ejercicios a resolver en los que el estudiante deberá proponer y diseñar sistemas teniendo en cuenta lo estudiado en esta práctica.

Las entregas de ejercicios se han de hacer a través del UAcloud>Evaluación>[Nombre de la práctica].

### Ejemplos demostrativos

- **[News-InstructionTuning]**


### Ejercicios

#### Ejercicio 1

Basándose en los ejemplos anteriores haga uso del siguiente dataset y diseñe su propio sistema para el análisis de sentimientos. Se disponibilizan unas funciones python para la limpieza y carga de dataset.

- sample_data/ejercicio_bbc_train.csv
- sample_data/ejercicio_bbc_test.csv

#### Ejercicio 2

Basándose en los ejemplos anteriores haga uso del siguiente dataset y diseñe su propio sistema para el análisis de sentimientos. Se disponibilizan unas funciones python para la limpieza y carga de dataset..

- sample_data/ejercicio_tripadvisor.csv
- tripadvisor_Utils.py

#### Ejercicios adicionales

Elige alguno de los siguientes datasets y conforma tu propio sistema de sentiment analysis.

- [SA Kaggle todos][kaggle]
- [Product review][product] (recomendado)
- [SA huggingface][huggingface]

### Criterios a tener en cuenta para la práctica:

- El cuaderno a entregar no debe tener errores de ejecución.
- Cada modificación de autor incorporada en cuaderno debe ser señalada con comentario. Por ejemplo ####Codigo NOMBRE_DEL_AUTOR ....#####.
- Se deben comentar y describir los aportes realizados por el autor, y explicar los motivos
- Se deben evaluar varias opciones de experimentación (i.e. preprocesamiento, configuraciones, tecnologías, modelos) y explicarlas.
- Se deben describir discusiones y conclusiones del estudio.


[huggingface]: https://huggingface.co/datasets?search=sentiment
[product]: https://www.kaggle.com/arbazkhan971/product-sentiment-analysis
[kaggle]: https://www.kaggle.com/search?q=sentiment+analysis+in%3Adatasets

[News-PromptTuning]: https://github.com/TeachingTextMining/TextClassification/blob/main/07-SA-Gen/promptTuning.ipynb
[News-InstructionTuning]: https://github.com/TeachingTextMining/TextClassification/blob/main/07-SA-Gen/instructionTuning.ipynb



[yoan]: https://orcid.org/0000-0002-4052-7427
[grande]: https://cvnet.cpd.ua.es/curriculum-breve/es/grande-ruiz-eduardo/327690
[consuegra]: https://orcid.org/0000-0003-2009-393X
