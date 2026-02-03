# Práctica 1a: PLN con SpaCy

[Borja Navarro Colorado](https://cvnet.cpd.ua.es/curriculum-breve/es/navarro-colorado-francisco-de-borja/9307) y [Eduardo Grande Ruiz](https://cvnet.cpd.ua.es/curriculum-breve/es/grande-ruiz-eduardo/327690)

## Objeto

El objetivo de esta práctica es crear un *script* que procese un texto amplio con las aplicaciones comunes del PLN:

- lematización,
- *PoS_tagger*,
- *parser* de dependencias y
- detección de entidades nombradas.

Para ello, se utilizará el *pipeline* básico de la herramienta de PLN [SpaCy](https://spacy.io/).

## Herramientas

- Cuaderno en [Google Colab](https://colab.research.google.com) para crear el código (Utilizar la cuenta GCloud).
- Python: ya instalado en COLAB.
- [SpaCy](https://spacy.io/): Está ya instalado en COLAB, solo hay que importarlo.

## Corpus

Para darle algo de interés a la práctica, vamos a utilizar el tipo de texto más complejo que exite: el texto literario. En concreto debéis analizar una novela del corpus [ELTeC](https://github.com/COST-ELTeC).

ELTeC es un corpus multilingüe de novelas publicada en Europa durante los siglos XIX y XX. Cada novela está anotada a tres niveles: básico, estándar y avanzado. __Debéis seleccionar una novela del nivel estándar.__ A este nivel, cada novela está marcada en XML siguiendo el estándar [TEI](https://tei-c.org/). Podéis utilizar el idioma que queráis (siempre que se encuentre en SpaCy, ver [modelos disponibles](https://spacy.io/models)). Por ejemplo:

- novelas en español: [https://github.com/COST-ELTeC/ELTeC-spa/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-spa/tree/master/level1)
- novelas en inglés: [https://github.com/COST-ELTeC/ELTeC-eng/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-eng/tree/master/level1)
- novelas en francés: [https://github.com/COST-ELTeC/ELTeC-fra/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-fra/tree/master/level1)
- novelas en portugués: [https://github.com/COST-ELTeC/ELTeC-por/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-por/tree/master/level1)
- etc...

Dado que el corpus está en GitHub, se puede clonar el repo y abrir los ficheros directamente  directamente desde COLAB. O se puede acceder al fichero "raw" directamente.

## Documentación

- Documentación básica SpaCy. Aquí está explicado todo lo necesario sobre PLN para realizar esta páctica:
    [https://spacy.io/usage/spacy-101](https://spacy.io/usage/spacy-101)
- Más información sobre SpaCy:
  - Curso avanzado: [https://course.spacy.io/es/](https://course.spacy.io/es/)
  - Documentación oficial: [https://spacy.io/usage](https://spacy.io/usage)

### Por pasos

1. Crear un cuaderno vacío en Google Colab.
2. Importar SpaCy, descargar el módulo de idioma elegido e importar.
3. Clonar el corpus desde GitHub y abrir una única novela en la carpeta *level1*.
4. Procesar el XML y extraer los párrafos:
    - Los párrafos están marcados con la etiqueta "p".
    - Para procesar XML en python, se recomienda por su sencillez [Beautiful Soup](https://beautiful-soup-4.readthedocs.io/en/latest/#)
5. Analizar el texto con el *pipeline* básico de SpaCy y extraer un CSV con "palabra | lema | categoria_gramatical | tipo de dependencia sintáctica | palabra de quien depende ".
6. Extraer los 10 grupos nominales (de al menos dos palabras) más frecuentes y mostrarlos en un gráfico de barras (ordenados de mayor a menor ocurrencia).
7. Extraer las 10 entidades nombradas más frecuentes y mostrarlas en un gráfico de barras (ordenadas de mayor a menor ocurrencia).
8. Crear un gráfico donde se muestren la cantidad de nombres, adjetivos, verbos y adverbios.

## Amplicación 1 (obligatoria)

Realizar análisis de dependencias del corpus con SpaCy y extraer en formato CONLL. Desde SpaCy se puede utilizar STANZA y UD-Pipe.

Además, se debe:

- Mostrar por pantalla las palabras cuyo número sea plural.
- Mostrar por pantalla los verbos cuyo tiempo verbal sea pasado.

Documentación:

- [https://spacy.io/universe/project/spacy-conll](https://spacy.io/universe/project/spacy-conll)
- [https://github.com/BramVanroy/spacy_conll](https://github.com/BramVanroy/spacy_conll)

## Amplicación 2 - Análisis semántico con WordNet y NLTK (obligatoria)

<font color=red>__Esta ampliación se debe realizar DESPUÉS de estudiar el Tema 5 del Bloque 1 *Análisis semántico*__</font>

Dado un fragmento del corpus lematizado, realizar lo siguient:

- Extraer los cinco *synset* más frecuentes.
- Analizar los resultados obtenidos, discutiendo por qué son esos los más frecuentes y si sería correcta la clasificación obtenida.

Documentación:

- Acceso a Open Multilingual WordNet mediante NLTK: <https://www.nltk.org/howto/wordnet.html>
- (Opcional) Acceso a NLTK desde SpaCy: <https://spacy.io/universe/project/spacy-wordnet>

Truco: en WordNet, los sentidos de cada palabra están ordenados por frecuencia. Basta con extraer el primero para obtener el más frecuente.

## Entrega

Una vez realizada la práctica, deberás de enviar enlace del cuaderno de Google Colab al profesor mediante la aplicación [Evaluación](https://cvnet.cpd.ua.es/uaevalua) de UACloud. Además, adjuntar una copia del cuaderno (En Google Colab, Archivo > Descargar .ipynb).

*NOTA*: El cuaderno de Google Colab deberá de estar ejecutado, no borres las salidas de las celdas.
