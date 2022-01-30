# Regresión lineal con hojas de cálculo
M1U1 - Ejercicio 1

## ¿Qué vamos a hacer?
- Resolver problemas de regresión lineal o ajuste de la recta por mínimos cuadrados
- Implementar las fórmulas de ajuste de la recta en una hoja de cálculo
- Representar gráficamente los datos iniciales y los resultados

Recuerda seguir las instrucciones para las entregas de prácticas indicadas en [Instrucciones entregas](https://github.com/Tokio-School/Machine-Learning/blob/main/Instrucciones%20entregas.md).

## Instrucciones

Vamos a simular un modelo matemático, con un conjunto de datos simulados, para comprender mejor cómo realizar una regresión lineal usando, en este caso, únicamente cualquier software de hojas de cálculo, como LibreOffice Calc, Microsoft Excel, Google Sheets, etc.:

- Usa cualquiera de estos software, con el que más cómodo te encuentres usando sus diferentes secciones. En especial, LibreOffice es un paquete de ofimática gratuito o Google Sheets es gratuito para todos los usuarios de Gmail.
- Como cada alumno puede utilizar un software diferente, no podemos explicar los pasos para ninguno de ellos, sino en general.
- Recuerda que si tienes cualquier problema, puedes buscar la solución rápidamente en cualquier buscador web, o estaremos encantados de ayudarte a través de los mensajes de la plataforma.
- En la misma carpeta del repositorio que este archivo, encontrarás varios archivos CSV con conjuntos de datos diferentes. Según las instrucciones, para cada tarea usaremos un conjunto de datos u otro.
- Puedes trabajar con varios documentos, uno por tarea, o mejor, con varias hojas en el mismo documento de cálculo
- Llama a cada hoja o documento "tarea-1", "tarea-2", etc.

Por favor, nombra los documentos, o las hojas dentro de un único documento, de forma descriptiva, aclarando qué tarea resuelve cada uno de ellos.

### Ejemplo: modelo y datos

En este ejemplo, vamos a simular un modelo de econometría: una curva de precio con el precio de un producto frente a su número de ventas.

Los modelos matemáticos/estadísticos/científicos se usan, habitualmente, para:
- Explicar la relación entre 2 o más variables: la variable dependiente del resto (la Y) y las variables independientes (la X), o modelizar su comportamiento.
- A partir de ese modelo, realizar predicciones en el futuro, sean interpolaciones o extrapolaciones.

Iremos discutiendo ambos objetivos durante la práctica.

### Modelo de regresión lineal por mínimos cuadrados

Vamos a realizar una regresión lineal por mínimos cuadrados sobre nuestros datos. Esta regresión lineal modelizará los datos, esto es, creará un modelo matemático a partir de los mismos.

El conjunto de datos, también llamado “dataset” en inglés, contendrá nuestros datos. Hemos comprobado cómo afecta el precio de venta de un producto con su número de ventas, a través de varios experimentos: diferentes variaciones del producto, descuentos y campañas promocionales, diferentes mercados, venta privada, etc.

El modelo matemático relacionará dos variables:
- La variable *Y* será el nº de ventas, la variable objetivo o dependiente.
- La variable *X* será el precio del producto, la variable independiente.

Hemos simplificado los nombres en *X* e *Y* para simplificar el ejercicio.

## Tarea 1
**Datos a usar:** M1U1-2-dataset_tarea1.csv

### Paso 1
Antes de entrenar ningún modelo, debemos siempre intentar visualizar los datos. En un modelo con un dataset mucho más completo y complejo, es habitualmente más complicado, pero en una regresión lineal simple, es muy simple.

Crea una gráfica de puntos (o “scatter plot”) y muestra en el eje horizontal o X la variable X, y en el eje vertical o Y, la variable Y.

En alguna celda del documento/hoja, indica “Pregunta 1” y responde a la pregunta:

*¿Qué forma crees que sigue la gráfica resultante? ¿Por qué crees que hablamos, en este caso, de regresión lineal?*

### Paso 2
Vamos a “modelizar los datos” (como diríamos en estadística) o “entrenar el modelo” (como diríamos en machine learning).

Para ello, calcula los valores de *m* y *b* según las siguientes fórmulas:

$$Y=m \times X + b$$

$$m=\frac{\sum xy-\frac{(\sum x)(\sum y)}{n}}{\sum x^2-\frac{(\sum x)^2}{n}}$$

$$b=\overline{y}-m\times\overline{x}$$

Notas:
- Las variables con una barra horizontal superior indica la media de la variable, y el símbolo *Σ* indica sumatorio, o sumar todos los valores de la variable.
- Indica las celdas que contendrán los valores de *m* y *b* de una forma descriptiva, de cara a evaluar la práctica.
- Puedes usar las funciones integradas de tu software de hojas de cálculo para hallar las medias y sumatorios o hacerlo de una forma manual.
- Te recomiendo usar otras celdas/columnas auxiliares para calcular valores intermedios cuando sea necesario.

Con estos coeficientes, hemos definido nuestro modelo. Estos coeficientes m y b son los que nos permiten explicar el comportamiento de las variables o hacer predicciones con el modelo.

### Paso 3
Vamos a evaluar el modelo usando el coeficiente de correlación.

Recuerda que lo puedes calcular con las fórmulas:

$$R^2 = \frac{\sigma_{xy}}{\sigma_x \cdot \sigma_y};$$

$$\sigma_{xy} = \overline{x \cdot y} - \bar{x} \times \bar{y};$$

$$\sigma_x = \sqrt{\frac{\sum x^2}{n} - \bar{x}^2};$$

$$\sigma_y = \sqrt{\frac{\sum y^2}{n} - \bar{y}^2}$$

Notas:
- Indica en una celda de forma clara el valor de *R<sup>2</sup>*.
- Para calcular *X · Y*, *X<sup>2</sup>* o *Y<sup>2</sup>*, puedes crear columnas auxiliares a partir de las columnas originales, multiplicando sus valores o elevándolos al cuadrado.
- Puedes comprobar tus cálculos con las funciones de desviación típica y covarianza de tu software de hojas de cálculo (cuidado: usa la función de la desviación típica para toda la población, no para una muestra, pueden ser funciones diferentes).

En alguna celda del documento/hoja, indica “Pregunta 2” y responde a la pregunta:

*¿Qué significa dicho valor de R<sup>2</sup>?*

### Paso 4
Vamos a calcular los valores de *Y* que el modelo predeciría para cada valor de *X*, según dichos valores de *m* y *b*.

Para ello, crea otra nueva columna llamada *y_pred* y calcula para ella dichos valores según la siguiente fórmula:

$$Y=m \times X + b$$

En alguna celda del documento/hoja, indica “Pregunta 3” y responde a la pregunta:

*¿Qué relación hay entre los resultados de dicha columna y el valor de R<sup>2</sup>?*

### Paso 5

**Este paso es opcional.**

En tu software de hoja de cálculo, vuelve a tu gráfica, añádele una línea de tendencia y calcula su *R<sup>2</sup>?* usando directamente las funcionalidades para ello del software, que habitualmente disponen de ellas en las gráficas de puntos.

## Tarea 2

**Datos a usar:** M1U1-2-dataset_tarea2.csv

Recukerda trabajar en una hoja o documento diferente para esta tarea, importando las columnas del dataset a utilizar en cada uno de los pasos

### Paso 1

Hasta ahora hemos usado unos datos simulados sin ningún error, con una correlación directa perfecta, lo cual no sucede habitualmente en la vida real.

Repite los pasos 1 al 4 de la tarea anterior (crear la gráfica, calcular *m* y *b*, calcular *R<sup>2</sup>* y calcular *y_pred*), excepto responder las preguntas, para los datos de las columnas *X_real* e *Y_real*.

Incorpora la columna *y_pred* como una nueva serie en la gráfica original de *X_real* e *Y_real*. Si es posible (no siempre lo es), incorpora esta serie como una gráfica de líneas en lugar de puntos, para que sea más fácil de visualizar la línea de tendencia.

### Paso 2

Ahora vamos a calcular los residuos. Los residuos son la diferencia entre la *Y* real y la *y_pred*. Calcúlalos para cada valor de *X* y luego crea una nueva gráfica donde representes los residuos en el eje vertical y X en el eje horizontal.

Verás que son valores pseudo-aleatorios que siguen una distribución normal que podemos denominar ruido. Esos residuos de nuestro dataset se corresponderían a errores en las medidas de las variables, diferencias aleatorias, variables ocultas que no tenemos en cuenta, etc.

### Paso 3

Por otro lado, vamos a utilizar este nuevo modelo para realizar predicciones sobre nuevos valores de 2 tipos:
- La interpolación es realizar predicciones sobre valores en el mismo rango que el dataset original, entre el valor máximo y mínimo.
- La extrapolación es realizar predicciones sobre valores fuera del rango del dataset original, con valores inferiores al mínimo o superiores al máximo.

Para ello, escoge 6 valores cualquiera, 3 de ellos el rango del dataset original y otros 3 fuera de dicho rango, y predice sus valores de *y_pred*.

## Tarea 3

**Datos a usar:** M1U1-2-dataset_tarea3.csv

### Paso 1

Vamos a repetir los pasos de la tarea anterior en un nuevo dataset, usando las columnas *X_error* e *Y_error*.

Para dichos datos, crea la gráfica, calcula *m* y *b*, calcula *R<sup>2</sup>*, *y_pred*, añade la línea de tendencia de *y_pred* a la gráfica y crea la gráfica de resíduos.

En este caso, analizando los resultados y las gráficas, no sólo *R<sup>2</sup>*, podemos ver que nuestro modelo es mucho más pobre que los anteriores.

*¿Serías capaz de averiguar por qué el modelo no funciona tan bien de antemano, sólo viendo la gráfica de puntos con X_error e Y_error?*


### Paso 2

Analiza la gráfica de *X_error* e *Y_error*:

*¿Qué relación dirías que tienen los datos originales? ¿Es una relación lineal, o de otro tipo?*


### Paso 3

*¿Se te ocurre alguna forma de transformar los datos originales para poder modelarlos usando regresión lineal simple?*

Pistas:
- Crea una nueva columna a partir de la *X* de los datos originales.
- Analiza en detalle la gráfica de puntos de *X* vs *Y*.
- Transforma los datos originales de alguna manera, p. ej. sumándoles un valor, multiplicándolos por un valor, elevándolos a un número, pasándolos por alguna función, etc.
- *La respuesta tiene 4 lados iguales* 8-).

## Tarea 4

**Datos a usar:** M1U1-2-dataset_tarea4.csv

En esta ocasión, carga los datos *X_rand* e *Y_rand* y represéntalos en una gráfica.

En alguna celda del documento/hoja, indica “Pregunta 4” y responde a la pregunta:

*¿Crees que podemos entrenar un modelo que encuentre algún tipo de relación lineal entre ambas variables, incluso transformando los datos? ¿Por qué?*

## Tarea 5

En esta tarea no vamos a usar ningún dataset, sino que vas a crear tú uno propio.

Vamos a simular datos sintéticos que sigan una determinada relación, para poder generar datasets de prueba y comprobar nuestros algoritmos e implementaciones de machine learning.

Para ello, crea una nueva hoja o documento donde vas a crear varias parejas de columnas, según las siguientes instrucciones:

### Paso 1

Vamos a generar un dataset similar al que hemos usado en la primera tarea. Para ello, sigue los siguientes pasos:
1. Crea una columna *X_paso1*, con valores en el rango *\[0, 10, 20, …, 100\]*.
1. Crea 2 celdas para tus valores de *m* y *b* y dales 2 valores cualesquiera.
1. Genera otra columna calculada *Y_paso1* con tus valores de *m*, *b* y *X_paso1*.

### Paso 2

Ahora vamos a generar un dataset con ruido aleatorio.

Para ello, sigue los pasos del punto anterior para generar un par de columnas *X_paso2* e *Y_paso2*, y además:
1. Vamos a añadir un término de ruido a la columna *Y_paso2*.
1. Crea una nueva celda auxiliar *e* que representará la escala del error. Puede estar en unidades, decenas, centenas, decimales, incluso números negativos.
1. Crea una nueva columna *Y_paso2_error* con la fórmula $Y_paso2_error = Y_paso2 + Y_paso2 * N * e$.
1. *N* es un número aleatorio en el rango \[-1, 1\] que podemos generar usando la función de generación de números aleatorios (de distribución normal o no) de tu software de hoja de cálculo siguiendo la fórmula: `(RANDN - 0,5) * 2`
1. Representa en una gráfica de puntos los valores de las columnas *X_paso2*, *Y_paso2* e *Y_paso2_error*.
1. Juega variando el valor de *e*, viendo cómo afecta a los valores de *Y_paso2_error*, hasta que quede un error más o menos normal.

### Paso 3

En este paso, vamos a generar un dataset con datos polinómicos.

Para ello, sigue los pasos del paso 1 para generar un par de columnas *X_paso3* e *Y_paso3*, y además:
1. Si lo prefieres, puedes usar una nueva hoja o documento.
1. Crea una nueva columna *X_paso3_cuadrado* con los valores de *X_paso3* elevados al cuadrado.
1. Cambia la columna *Y_paso3* para que use los pasos de la columna *X_paso3_cuadrado* en lugar de la columna *X_paso3*.
1. Representa ambas columnas *X_paso3_cuadrado* e *Y_paso3* en una gráfica de puntos.

### Paso 4

Por último, vamos a crear datos con relaciones con relaciones diferentes a una relación lineal o polinómica:
1. Si lo prefieres, puedes usar una nueva hoja o documento.
1. Crea una columna *X_paso4*, con valores en el rango \[0, 10, 20, …, 100\].
1. Crea otra columna *Y_paso4* y calcula sus valores en función de la fórmula `Y_paso4 = 3 * log(X_paso4 + 2)` 
1. Representa ambas columnas en una gráfica de puntos.

## Tara 6

¡Vamos a conocernos! Y ver cómo podemos contactar por la plataforma.

Para esta tarea, envíame (instructor Marcos Manuel Ortega) un mensaje por la plataforma con la siguiente información:
1. Busca información sobre la siguiente frase y analízala. Explícame por qué crees que es interesante recordarla siempre cuando analizamos datos. La frase es: *“La correlación no implica causalidad”*.
1. Busca algunos artículos, blog o similares donde expongan ejemplos de análisis de datos estadístico donde la correlación no implicó causalidad y envíamelos.
1. Busca algún meme, chiste o frase graciosa relacionada con dicha frase o similares y compártelo. *¡Hay muchos :D!*
1. Busca la famosa tira cómica de XKCD sobre dicha frase, analízala y envíamela junto a una explicación del chiste.

## Hemos aprendido que...

- Hasta ahora, no hemos hecho machine learning de verdad. Nos hemos limitado a crear modelos estadísticos, analizarlos y evaluarlos.
- Hemos visto, por ahora, cómo el machine learning no es más que realizar modelos estadísticos. Durante el curso veremos que la diferencia está en la implementación y en usar algoritmos más avanzados.
- Hemos visto la necesidad de analizar los datos antes de pretender entrenar ningún modelo.
- Hemos descubierto el concepto de residuos.
- Hemos visto cómo muchas veces debemos transformar los datos antes de entrenar un modelo sobre ellos.
- Hemos aprendido a crear nuestros propios datasets sintéticos para hacer pruebas de modelos y sus implementaciones.

