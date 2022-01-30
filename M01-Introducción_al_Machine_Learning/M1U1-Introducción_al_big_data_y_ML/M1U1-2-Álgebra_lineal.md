# Álgebra lineal
M1U1 - Ejercicio 2

## ¿Qué vamos a hacer?
- Resolver una serie de problemas de operaciones matemáticas de álgebra lineal

Recuerda seguir las instrucciones para las entregas de prácticas indicadas en [Instrucciones entregas](https://github.com/Tokio-School/Machine-Learning/blob/main/Instrucciones%20entregas.md).

## Instrucciones

Vamos a realizar una serie de operaciones matemáticas de álgebra lineal, para ayudar a que interioricemos estos conceptos plenamente.

Para este ejercicio se pide que resuelvas estos ejercicios de la forma que prefieras: usando un editor de texto con capacidad de incluir fórmulas matemáticas, LaTeX, un documento escaneado o incluso una fotografía de una hoja donde se aprecie claramente la solución.

Por favor, recuerda resolverlos paso a paso de forma manual. Eso sí, puedes usar cualquier calculadora para comprobar el resultado, pero queremos asentar las características de la operación para comprenderla bien.

Una vez completadas estas operaciones de forma manual, te asegurarás no tener ningún problema al realizarlas a través de código en implementaciones más complejas, como las que haremos durante el curso.

*Nota del profesor: Aunque pueda no sonar muy sexy hacer un ejercicio de matemáticas de bachillerato, preocuparte por poder resolverlo sin problema e interiorizar estos conceptos te va a ayudar a evitar muchos problemas durante el curso y en tu trabajo, en mi experiencia con ML :).*

### Matrices y vectores

$A_{3\times3} = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9 \\
\end{bmatrix}$

$B_{3\times3} = \begin{bmatrix}
10 & 20 & 30 \\
40 & 50 & 60 \\
70 & 80 & 90 \\
\end{bmatrix}$

$V_{3\times1} = \begin{bmatrix}
a \\
b \\
c \\
\end{bmatrix}$

$C_{3\times2} = \begin{bmatrix}
a & b \\
c & d \\
e & f \\
\end{bmatrix}$

$D_{2\times3} = \begin{bmatrix}
g & h & i \\
j & k & l
\end{bmatrix}$

$Y_{4\times1} = \begin{bmatrix}
y_1 \\
y_2 \\
y_3 \\
y_4
\end{bmatrix}$

$\Theta_{1\times3} = \begin{bmatrix}
\theta_1 & \theta_2 & \theta_3
\end{bmatrix}$

$X_{4\times3} = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9 \\
10 & 11 & 12
\end{bmatrix}$

### Ejercicios

1. Transpón la matriz *A*.
1. Halla la suma de la matriz *A* y *B*.
1. Multiplica la matriz *A* por el nº escalar 3.
1. Multiplica la matriz *A* por el vector *V*.
1. Multiplica la matriz *A* por la matriz *C*.
1. Multiplica la matriz *B* por la matriz *C*.
1. Multiplica la matriz *B* por la matriz *D*.
1. Sabiendo que, en una regresión lineal, *Y* es igual a la multiplicación del vector *Θ* y la matriz *X*, plantea la ecuación y resuélvela para cada elemento de *Y*, teniendo en cuenta:
    1. *Y* y *Theta* son vectores fila o columna, podemos transponerlos sin ningún problema.
    1. Podemos transponer *X* sólo si no queda otra opción.
    1. Podemos escoger el orden de la multiplicación que estimemos.

## Hemos aprendido que...

- La implementación del machine learning depende de cálculos del álgebra lineal.
- Debemos saber cómo multiplicar matrices paso a paso para saber cómo aprovechar estas operaciones a la hora de implementar los algoritmos de machine learning.
- No todas las operaciones son siempre posibles.
- Cuidado con las dimensiones de los vectores y matrices, *¡pero mucho cuidado!*.