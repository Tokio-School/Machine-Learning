# Proyecto final
M06 - Ejercicio 1

## ¿Qué vamos a hacer?
- Preparar el proyecto final
- Enviarlo para revisión y evaluación
- Publicar el proyecto en nuestro perfil de Kaggle

## TODO






- Colgar en Kaggle


## Instrucciones generales
Como proyecto final vamos a entrenar un modelo de machine learning que resuelva un problema y un dataset que nosotros mismos escogeremos.

*INSTRUCCIONES*:
1. Busca y escoge un datset para un caso de uso de tu interés en [OpenML](https://www.openml.org).
1. Puedes resolver un dataset para aprendizaje supervisado, semi-supervisado o no supervisado, para regresión, clasificación, detección de anomalías, etc., escoge el que prefieras.
1. Como durante todo el curso, utiliza el entorno de desarrollo que prefieras: local, WSL, VM, Google Colab, cloud, etc.
1. Comienza creando un notebook de Jupyter que será parte de tus entregables finales.
1. Documenta todo el proceso en el notebook:
    1. Recuerda que el objetivo de un notebook no es mostrar el resultado final únicamente, sino que también puedes incluir celdas de cada prueba, iteración o hipótesis para documentar qué has probado y qué resultados ha dado
    1. Los nombres de variables para diferentes pruebas, como datasets preprocesados de forma diferente o diferentes modelos, pueden tener un nombre distinto para poder documentar tu trabajo y volver atrás para continuar refinando el modelo por otro camino 
    1. No es necesario que plantees unas variables o una celda nueva para cada paso que des, sólo para cada hipótesis principal, en especial para cada paso cuyos resultados luego quieras comparar con otras hipótesis o experimentos.
    1. Por tanto no es necesario una celda o variables nuevas cada vez que corrijas un problema o cambies el valor de un hiper-parámetro, pero sí p. ej. si quieres comparar un árbol de decisión frente a una regresión logística, o si quieres comparar tu modelo en un dataset base frente a varias versiones de un dataset más procesado.
1. Trabaja en base a hipótesis o experimentos:
    1. Los experimentos son diferentes pasos que proponemos, y en función de sus resultados, decidimos continuar avanzando por una vía u otra.
    1. Podemos experimentar con, entre otros, diferentes conjuntos de características, extracción o procesado de características, familias de modelos, modelos y sus hiper-parámetros, etc.
    1. Intenta siempre que puedas seguir el método científico, la ciencia de datos:
        1. Plantea y expón la situación original o actual.
        1. Plantea qué experimentos puedes proponer para avanzar y su justificación.
        1. Plantea los resultados de cada uno.
        1. Evalúa dichos resultados y justifica tu siguiente paso.
    1. Recuerda no probar simplemente todas las opciones disponibles, sino justificar el por qué y, especialmente, comprobar su idoneidad de antemano.
    1. Documenta en cada caso las métricas correspondientes antes y tras la hipótesis, resaltando la diferencia.
1. El objetivo es documentar tu trabajo para mostrar tu resultado y mostrar, en líneas generales, qué pasos has dado, qué has probado y qué resultados has obtenido, y por qué has continuado avanzando por una vía u otra.

## Definir caso de uso
1. Comienza por presentar tu caso de uso escogido. Cuéntanos un poco por qué te ha interesado.
1. Busca y referencia algunas citas de bibliografía, ejemplos o tutoriales que referencien dicho dataset u otros similares, y apóyate en dichos trabajos siempre que sea posible.

## Análisis del dataset
Presenta el dataset a utilizar y comienza por hacer un análisis de datos exploratorio del mismo:
- Origen del dataset, documentación, enlaces y referencias (si es posible).
- Tamaño.
- Características.
- Preprocesado ya realizado o "linaje del dato".
- Licencia del mismo.
- ¿Tendrás suficientes datos para tu caso de uso, según las características necesarias? ¿Qué nº de características te puedes permitir con ese nº de datos?
- Para explorarlo, puedes utilizar Numpy o Pandas, Matplotlib o Seaborn, etc.

## Definir requisitos técnicos
Un modelo de ML no es más que una aplicación, y un sistema basado en ML una solución de software, por lo que nuestro proceso debe comenzar por definir unos requisitos técnicos mínimos:
- Métricas de evaluación del modelo propuestas.
- Precisión final del modelo aceptable mínima.
- Precisión final del modelo deseable.
- Recursos (CPU y RAM) destinables.
- Tiempo máx. de entrenamiento.
- Documentar dependencias (librerías como Numpy, Pandas, Scikit-learn, etc.)

## Análisis de datos exploratorio
Necesitamos comprender en detalle los datos para entrenar nuestro modelo, ya que los datos serán su combustible.

Realiza un análisis de datos exploratorio para bucear en el mismo. Si has cursado el curso de Python e IA de Tokio School, puedes basarte en tus conocimientos de Python para la ciencia de datos:
1. Presenta el dataset/dataframe: forma, características, tipo de características, resumen del mismo.
1. Comprueba si existen valores incompletos, incorrectos, inválidos, nulos, no uniformes, etc.
1. Analiza las características:
    1. Numéricas: atributos como media, distribución típica, distribución y reprsentación como gráfica de puntos y boxplot.
    1. Categóricas: ordinal o nominal, moda, nº de categorías y representación como histograma.
1. Define tu variable objetivo.
1. Análisis de outliers.
1. Limpia los datos incorrectos, inválidos y valora eliminar o no los outliers y los incompletos.
1. Preprocesa las características:
    1. Numéricas: como tal, bucketizar o categorizar, polinomios, raíces y logaritmos, etc.
    1. Categóricas: ordinales, one-hot encoding, llevar a numéricas.
    1. Posibles cruces de características.
1. Si lo prefieres, rellena los datos incompletos con interpolaciones o medias.
1. Reordena los datos aleatoriamente.
1. Reescala o normaliza los datos de entrenamiento.
1. Resume las características y sus atributos y distribuciones tras el preprocesado.
1. Halla la correlación con la variable objetivo con una matriz de correlación representada gráficamente.
1. Divide tu dataset en subsets de entrenamiento, validación y test o haz K-fold.

## Funciones auxiliares
Define cuantas funciones de código auxiliares necesites para hacer tareas repetitivas, como p. ej. representar variables, distribuciones, validar modelos, presentar métricas, etc.

## Modelo base
Comienza tu trabajo definiendo un modelo base:
1. El modelo base debe ser medianamente adecuado, no simplemente el primero que planteemos, no en precisión sino en adecuación al caso previsto.
1. Evalúa el modelo:
    1. Representa sus métricas.
    1. Comprueba sus residuos.
    1. Comprueba si sufre desvianza o sobre-ajuste.
1. Para cada hipótesis o experimento, compara tus resultados entre sí y contra el modelo base, para comprobar su estás mejorando o no.

## Ingeniería de características
Parte de los datos base y realiza experimentos o hipótesis para mejorar tus características.

Cuando no sepas cómo avanzar con tu modelo, puedes volver al punto de partida y mejorar en su lugar las características utilizadas:
1. Evalúa la relevancia de las características tras entrenar tus modelos.
1. Plantea algunas mejoras, como proponer polinomios de distinto grado (no más de 4/5), logaritmos, cruces entre variables, etc.
1. Plantea PCA o reduce las características si la dimensionalidad/complejidad del modelo es muy alta.
1. Incorpora nuevas características

## Refinado del modelo
Comienza a plantear y refinar tus modelos:
- Prueba distintas familias de modelos relacionados con tu caso de uso: árboles de decisión, modelos lineales, SVM/SVRs, etc.
- Prueba distintos tipos de modelos dentro de las familias.
- Avanza planteando hipótesis o experimentos, evaluando y comentando los resultados.
- Continua mejorando tu modelo de una forma iterativa, planteando unas posibilidades, explorándolas, y avanzando sobre la más prometedora, ahondando en la misma.
- Evalúa cada modelo o experimento planteado:
    - Plantea cada modelo como una nueva versión, con un nombre descriptivo y versionado.
    - Métricas escogidas.
    - Tiempo de entrenamiento.
    - Sufre desviación o sobre-ajuste.
    - Comparación con otros modelos del mismo experimento y con el modelo base.
- Prueba métodos más avanzados si lo consideras necesario:
    - Volver al paso de extracción de características.
    - PCA y reducción de dimensionalidad.
    - Optimización de hiper-parámetros: ratio de entrenamiento, regularización, etc.
    - GridSearch, algoritmos genéticos
    - Ensamblajes

## Presentación del modelo
Presenta tu modelo final:
- Tipología
- Características utilizadas
- Hiper-parámetros
- Métricas y resultados
- Tiempo de entrenamiento y nº de iteraciones
- Nº de ejemplos de entrenamiento
- Variación o sobre-ajuste
- Comparación con modelo base
- Muestra sus pesos/coeficientes/parámetros (incluyendo bias)
- Justificación de su idoneidad y cumplimiento de los requisitos técnicos iniciales.

## Perfil en Kaggle
xxx

## Presentación del proyecto
Presenta tu proyecto para su evaluación.

Proceso:
1. Envía los entregables requeridos por la plataforma.
1. El instructor te dará su feedback, y si es positivo, procederá a plantearte 3 preguntas a responder.
1. Graba tu presentación del proyecto, caso de uso y resultados, y tus respuestas en un video corto de menos de 10 minutos, mostrándote tú y/o tu pantalla.
1. Tu nota final será la combinación del feedback del proyecto y tu presentación del mismo.

*ENTREGABLES:*
1. Notebook como "M6-1-Proyecto_final-nombre_del_alumno.ipynb".
