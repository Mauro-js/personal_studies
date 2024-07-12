        <h1>3. Determinantes</h1>

  El determinante de una matriz cuadrada es un único número que se 
asocia a dicha matriz; es por tanto una función del conjunto de las matrices
cuadradas en el conjunto numérico al que pertenecen los elementos de
las matrices. En nuestro caso estos números serán los reales o los
complejos, pero se puede dar sobre conjuntos "numéricos" más generales.

  El uso del determinante surgió de las fórmulas que dan las soluciones
de sistemas de n ecuaciones con n incógnitas, luego fue identificado
(en el caso 3 por 3) como área de paralelogramo o volumen de un
paralelepípedo, hasta extenderse a definiciones más generales que la que
nosotros daremos en este curso (función multilineal alternada).

  Más adelante se verá que podemos hablar del determinante de una
tranformación lineal entre espacios vectoriales, a la que se puede asociar
matrices de una manera sencilla. En particular las matrices invertibles son
las únicas que tienen determinantes distintos de cero. Así, una propiedad
tan definitoria de una matriz (su invertibilidad) estará caracterizada por
la no nulidad de su determinante (o sea por el valor de un único número).


      3.1 Definición

  La definición de determinante de una matriz cuadrada será dada de manera
inductiva en el número de filas (o de columnas). O sea, daremos la definición
de determinate de una matriz n x n a partir del conocimiento de los
determinantes de matrices (n - 1) x (n - 1). El determinante de una matriz
A se representa con el símbolo |A|; tratándose de una matriz dada por sus
coeficientes, en general no escribiremos los paréntesis con los que en
general encerramos el "cuadrado" de los números.

DEFINICIÓN 3.1 Sea A = ((a<sub>ij</sub>)) una matriz
