
(label_tecnicas)=
Técnicas para la minería de textos
==================================

En este bloque se aborda el estudio de algunos modelos neuronales utilizados para procesar textos. El profesor de este bloque es Juan Antonio Pérez Ortiz. 


El bloque comienza con un repaso del funcionamiento del regresor logístico, que nos servirá para asentar los conocimientos necesarios para entender posteriores modelos. A continuación se estudia con cierto nivel de detalle *skip-grams*, uno de los algoritmos para la obtención de *embeddings* incontextuales de palabras. Después se repasa el funcionamiento de las arquitecturas neuronales *feedforward* y se estudia su aplicación a modelos de lengua. El objetivo último es abordar el estudio de la arquitectura más importante de los sistemas actuales de procesamiento de textos: el transformer. Una vez estudiadas estas arquitecturas, finalizaremos con un análisis del funcionamiento de los modelos preentrenados (modelos fundacionales), en general, y de los modelos de lengua, en particular.

Los materiales de clase complementan la lectura de algunos capítulos de un libro de texto ("Speech and Language Processing" de Dan Jurafsky y James H. Martin, borrador de la tercera edición, disponible online) con anotaciones realizadas por el profesor.

## Prácticas a entregar para este bloque

Durante las sesiones de este bloque, estudiaremos diferentes implementaciones en PyTorch de modelos neuronales para procesar textos. Para cada cuaderno de código se planteará uno o más ejercicios que tendrás que resolver y entregar en forma de un informe final. **Importante:** solo has de realizar los ejercicios que se indican en esta página de la asignatura y no los que pudieran aparecer al final del cuaderno. La longitud máxima de la respuesta de cada ejercicio es de 800 palabras, excluyendo los fragmentos de código. En cualquier caso, mantén estos fragmentos de código al mínimo y no copies todo el código de los cuadernos, sino solo aquellas líneas más relevantes para complementar tu respuesta. Si incluyes fragmentos de código en tu informe, asegúrate de que los incluyes como texto (con los estilos adecuados) y no como imagen; y, mucho menos, como imagen con fondo oscuro, que dificulta la lectura y derrocha tinta en caso de impresión. Entrega un único PDF final a través de una tutoría de UACloud. El **plazo de entrega acaba el 14 de mayo de 2026** a las 23.59 horas. Las prácticas, excepto casos puntuales, se han de hacer en parejas. Recuerda que hay un examen final de la asignatura, por lo que es muy recomendable que ambos miembros del equipo se impliquen de igual manera.

A la hora de corregir los informes de prácticas, no se penalizará el uso de asistentes generativos de texto. El uso de ciertas herramientas de inteligencia artificial puede aumentar tus capacidades profesionales. Sin embargo, el abuso de su uso hasta el punto de despersonalizar tus entregas, desproveerlas de tu estilo personal, de tus propios razonamientos o de contenido relevante sí afectará negativamente a tu nota. Todo esto suele ser bastante fácil de detectar, pero para casos dudosos el profesor podrá realizar una pequeña prueba con el estudiante en la que no se permita el uso de asistentes generativos de texto para comprobar la consistencia entre lo entregado y lo que el estudiante es capaz de producir por sí mismo.

## Primera sesión (15/04/2026)

**<span style="font-size: 1.15em">Contenidos a preparar antes de la sesión del 15/04/2026</span>**

Las actividades a realizar antes de esta clase son:

- Lectura y estudio de los contenidos de [esta página](https://www.dlsi.ua.es/~japerez/materials/transformers/regresor) sobre regresión logística. Como verás, la página te indica qué contenidos has de leer del libro. Tras una primera lectura, lee las anotaciones del profesor, cuyo propósito es ayudarte a entender los conceptos clave del capítulo. Después, realiza una segunda lectura del capítulo del libro. En total, esta parte debería llevarte unas 3 horas 🕒️ de trabajo.
- Visionado y estudio de los tutoriales en vídeo de esta [playlist oficial de PyTorch](https://www.youtube.com/playlist?list=PL_lsbAsL_o2CTlGHgMxNrKhzP97BaG9ZN).  Estudia al menos los 4 primeros vídeos (“Introduction to PyTorch”, “Introduction to PyTorch Tensors”, “The Fundamentals of Autograd” y “Building Models with PyTorch”). En total, esta parte debería llevarte unas 2 horas 🕒️ de trabajo.
- Lectura y estudio de [esta página](https://www.dlsi.ua.es/~japerez/materials/transformers/embeddings) sobre la obtención de embeddings incontextuales. Como verás, la página te indica qué contenidos has de leer del libro. Tras una primera lectura, lee las anotaciones del profesor, cuyo objetivo es ayudarte a entender los conceptos clave del capítulo. Después, realiza una segunda lectura del capítulo. En total, esta parte debería llevarte unas 3 horas 🕒️ de trabajo.
- Tras acabar con todo lo anterior, realiza este [test de evaluación](https://forms.gle/E1xzZHw6hzMWJaNr7) de estos contenidos. Son pocas preguntas y te llevará unos minutos.


**<span style="font-size: 1.15em">Contenidos para la sesión presencial del 15/04/2026</span>**

En la clase presencial (4 horas 🕒️ de duración), repasaremos los contenidos preparados con anterioridad a la clase y veremos cómo se implementa un regresor logístico en PyTorch siguiendo la implementación de un regresor logístico binario y de uno multinomial que se comentan en [este apartado](https://www.dlsi.ua.es/~japerez/materials/transformers/implementacion/#codigo-para-un-regresor-logistico-y-uno-multinomial). También veremos la implementación del algoritmo [skip-grams](https://www.dlsi.ua.es/~japerez/materials/transformers/implementacion/#codigo-para-skip-grams).

**Ejercicios**: para este bloque, haz los siguientes ejercicios. Repasa las normas que se indican más arriba sobre cómo entregar los ejercicios.

1. **Regresor logístico binario**: modifica el código para que el conjunto de entrenamiento se divida en en entrenamiento, validación y test. Usa el conjunto de evaluación para determinar cuándo detener el entrenamiento. Añade un gráfico que muestre la evolución de la función de pérdida en el conjunto de entrenamiento y en el de validación. 

2. **Regresor logístico multinomial**: estudia las probabilidades emitidas por el modelo ya entrenado para cada clase tanto con las frases del cuaderno como con algunas frases nuevas que tú propongas. Juega con frases que estén a medio camino entre diferentes temáticas.



## Segunda sesión (23/04/2026)

**<span style="font-size: 1.15em">Contenidos a preparar antes de la sesión del 23/04/2026</span>**

Las actividades a realizar antes de esta clase son:

- Lectura y estudio de [esta página](https://www.dlsi.ua.es/~japerez/materials/transformers/ffw) sobre las redes neuronales hacia delante. En total, esta parte debería llevarte unas 2 horas 🕒️ de trabajo.
- Estudio de [esta página](https://www.dlsi.ua.es/~japerez/materials/transformers/attention) sobre el modelo transformer y el capítulo correspondiente del libro. Consulta también las anotaciones del profesor que hay en la página web. En total, esta parte debería llevarte unas 4 horas 🕒️ de trabajo.

<!--
- Primeros pasos en el estudio del modelo transformer. Volveremos a dedicar más horas a esta arquitectura para la próxima sesión de forma que la abordaremos en dos fases. Por ahora, lee con detenimiento la introducción a mecanismos de atención de ["Visualizing A Neural Machine Translation Model"](https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/), así como la introducción visual a los transformers de ["The Illustrated Transformer"](http://jalammar.github.io/illustrated-transformer/) y la más elaborada de ["The Illustrated GPT-2"](https://jalammar.github.io/illustrated-gpt2/). El objetivo es que entiendas conceptualmente el mecanismo de atención de los transformers, pero no es necesario que en este momento comprendas todos los detalles técnicos (especialmente las ecuaciones del modelo), ya que volverás a dedicarle tiempo a este capítulo más adelante. En total, esta parte debería llevarte ahora unas 3 horas 🕒️ de trabajo.
-->
- Realización del [test de evaluación](https://forms.gle/Eb3ZwwGxbQp88t4FA) de estos contenidos. Son pocas preguntas y te llevará unos minutos.

<!-- A continuación, lee el apartado 9.7 (solo este apartado) del capítulo ["Deep learning architectures for sequence processing"](https://web.archive.org/web/20221216193204/https://web.stanford.edu/~jurafsky/slp3/9.pdf); -->


**<span style="font-size: 1.15em">Contenidos para la sesión presencial del 23/04/2026</span>**

En la clase presencial (4 horas 🕒️ de duración), repasaremos los contenidos de estudio previo y veremos la implementación en PyTorch de un modelo de lengua basado en [redes feedforward](https://www.dlsi.ua.es/~japerez/materials/transformers/implementacion/#codigo-para-un-modelo-de-lengua-con-redes-feedforward). También comenzaremos a ver cómo se [implementa el modelo transformer en PyTorch](https://www.dlsi.ua.es/~japerez/materials/transformers/implementacion/#codigo-para-el-transformer).


**Ejercicios**: para este bloque, haz los siguientes ejercicios sobre el código de skip-grams estudiado en clase en la sesión anterior. Repasa las normas que se indican más arriba sobre cómo entregar los ejercicios. Aunque ambos ejercicios se basan en el cuaderno del algoritmo skip-grams, ten en cuenta que el cuaderno de las redes feedforward también te será muy útil para preparar el examen.

1. **Skip-grams**: modifica el código para que se pueda seleccionar el tamaño de la ventana L y realiza un pequeño estudio sobre cómo esto afecta a los embeddings obtenidos.
2. **Skip-grams**: sustituye la parte del código que usa la notación de Einstein por una multiplicación convencional de matrices seguida de una operación que se quede con los valores que nos interesan. Compara los tiempos de ejecución de ambas implementaciones.

<div style="border: 2px solid #333; padding: 40px; margin: 20px 0; border-radius: 8px; display: flex; align-items: center; gap: 20px;">
  <span style="font-size: 2rem;">⚠️</span>
  <p style="margin: 0; line-height: 1.5;">
    Los contenidos a partir de este punto no son definitivos y podrían sufrir ligeras variaciones.
  </p>
</div>

## Tercera sesión (30/04/2026)

**<span style="font-size: 1.15em">Contenidos a preparar antes de la sesión del 30/04/2026</span>**

Las actividades a realizar antes de esta clase son:

- Ampliar el estudio del transformer con la arquitectura codificador-descodificador completa, así como con la basada solo en codificador siguiendo para ello las secciones de [esta página](https://www.dlsi.ua.es/~japerez/materials/transformers/attention2/). En total, esta parte debería llevarte unas 3 horas 🕒️ de trabajo.
- Ahondar en la operativa de los grandes modelos de lengua 

- Realiza el [test de evaluación](https://forms.gle/qJMmKi6KGhtKDJtYA) de estos contenidos. Son pocas preguntas y te llevará unos minutos.
- Realiza el [test de evaluación](https://forms.gle/yHuUBZrqxDrnARkM8) de estos contenidos. Son pocas preguntas y te llevará unos minutos.


**<span style="font-size: 1.15em">Contenidos para la sesión del 30/04/2026</span>**

En la clase presencial (4 horas 🕒️ de duración), terminaremos de explorar cómo se [implementa el modelo transformer en PyTorch](https://www.dlsi.ua.es/~japerez/materials/transformers/implementacion/#codigo-para-el-transformer).


**Ejercicios**: para este bloque, haz los siguientes ejercicios. Repasa las normas que se indican más arriba sobre cómo entregar los ejercicios.

1. **Modelos de lengua basados en transformers**: léete este tutorial [sencillo](https://pub.towardsai.net/multi-query-attention-explained-844dfc4935bf) y este otro más [avanzado](https://fireworks.ai/blog/multi-query-attention-is-all-you-need) sobre el concepto de multi-query attention y, a continuación, modifica el código del modelo de lengua basado en transformers para que use multi-query attention sin implementar todavía una caché KV. Realiza un pequeño estudio sobre cómo afecta esto a la calidad del modelo; para esto puedes medir qué probabilidad da el modelo a algunas frases similares a las del conjunto de entrenamiento. Adicionalmente, estudia cómo afecta a la calidad del modelo el uso de una caché KV que tendrás que implementar. Aunque sería deseable poder medir el impacto de ambas cosas en los tiempos de ejecución, no es necesario que lo hagas, ya que probablemente no puedas medirlo con precisión suficiente salvo que incrementes el tamaño de los datos de entrenamiento y el número de parámetros del modelo. Explica en tu respuesta las ideas básicas tanto de multi-query attention como de la caché KV. *Nota:* este ejercicio es más complejo que los anteriores por lo que requerirá un mayor esfuerzo por tu parte; la nota final de tu informe se basará un 35% en los ejercicios de la sesión 1, un 35% en los de la sesión 2 y un 30% en los de esta sesión, por lo que se puede considerar que es un ejercicio *para nota*. Puedes usar, además, el doble de espacio para responder a este ejercicio.
