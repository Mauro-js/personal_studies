#        3. Determinantes

   El determinante de una matriz cuadrada <mark>**es un único número** que se asocia a dicha matriz</mark>; es por tanto una **función del conjunto de las matrices cuadradas** en el conjunto numérico al que pertenecen los elementos de las matrices. En nuestro caso estos números <mark>Serán los reales o los complejos</mark>, pero se puede dar sobre conjuntos "numéricos" más generales.

  El uso del determinante surgió de las fórmulas que dan las soluciones de sistemas de n ecuaciones con n incógnitas, luego fue identificado (en el caso 3 por 3) como área de paralelogramo o volumen de un paralelepípedo, hasta extenderse a definiciones más generales que la que nosotros daremos en este curso (función multilineal alternada).

  Más adelante se verá que podemos hablar del determinante de una tranformación lineal entre espacios vectoriales, a la que se puede asociar matrices de una manera sencilla. <mark>**En particular las matrices invertibles son las únicas que tienen determinantes distintos de cero**</mark>. Así, una propiedad tan definitoria de una matriz (su invertibilidad) estará caracterizada por la no nulidad de su determinante (o sea por el valor de un único número).


## 3.1 Definición

  La definición de determinante de una matriz cuadrada será dada de manera inductiva en el número de filas (o de columnas). O sea, daremos la definición de determinate de una matriz n x n a partir del conocimiento de los determinantes de matrices (n - 1) x (n - 1). El determinante de una matriz A se representa con el símbolo |A|; tratándose de una matriz dada por sus coeficientes, en general no escribiremos los paréntesis con los que en general encerramos el "cuadrado" de los números.

**DEFINICIÓN** <code>3.1</code> Sea A = ((a<sub>ij</sub>)) una matriz *n x n*, se definie la **matriz adjunta del elemento** a<sub>ij</sub> como la submatriz A<sub>ij</sub> de la matriz A que se obtiene eliminando la fila *i* y la columna *j* de A

**OBSERVACIÓN** <code>3.1</code>. Si la matriz cuadrada A es de tamaño *n*, las matrices adjuntas A<sub>ij</sub> son de tamaño (*n*-1) x (*n*-1).

**DEFINICIÓN** <code>3.2</code> **(Inductiva en el tamaño de la matriz)** El determinante de una mantriz 1 X 1 <mark>es el propio número</mark>. El determinante de la matriz 2 X 2,  A = (a b, c d) es el número |A|<sup>def</sup>= ad - bc

El determinante de una matriz A *n* X *n* se define como el número


|A|<sup>def</sup>= (-1)<sup>1+1</sup> a<sub>11</sub> |A<sub>11</sub>| + ... + (-1)<sup>*i*+1</sup> a<sub>*i*1</sub> |A*i*1| + ... + (-1)<sup>*n*+1</sup> a<sub>*n*1</sub> |A*n*1|

<details>
  <summary><b><mark>Material extra en videos</mark></b></summary>

##Videos de la definicion de Determinante

  <details>
  <summary> Video Definición Determinante Teórico 2019 </summary>
   
https://github.com/user-attachments/assets/dfdc7e26-a71b-4549-b7c6-f03727addb36

[Video Original](https://open.fing.edu.uy/courses/gal119/1/)

</details>
<details>
   <summary> Video Introducción Determinante Teórico 2013 </summary>


https://github.com/user-attachments/assets/a28239c4-cac6-4093-bfa3-cd72f0b86c82


[Video Original](https://open.fing.edu.uy/courses/gal1/9/)
   
</details>
</details>

## 3.2 Propiedades de los determinantes

### Linealidad (respecto a una fila)

#### a) Aditividad (respectoo a una fila)

$$
C=
\begin{bmatrix}
a_{11} & a_{12} & ... & a_{1n} \cr
: & : & ... & :  \cr
a_{i1} + b_{i1} & a_{i2} + b_{i2} & ... & a_{in} + b_{in}  \cr
: & : & ... & :  \cr
a_{n1} & a_{n2} & ... & a_{nn} 
\end{bmatrix}
\=
\begin{bmatrix}
a_{11} & a_{12} & ... & a_{1n} \cr
: & : & ... & : \cr
a_{i1} & a_{i2} & ... & a_{in} \cr
: & : & ... & : \cr
a_{n1} & a_{n2} & ... & a_{nn} 
\end{bmatrix}
+
\begin{bmatrix}
a_{11} & a_{12} & ... & a_{1n} \cr
: & : & ... & : \cr
b_{i1} & b_{i2} & ... & b_{in} \cr
: & : & ... & : \cr
a_{n1} & a_{n2} & ... & a_{nn} 
\end{bmatrix}
\=
|A| + |B|
$$

**DEMOSTRACIÓN.** Por inducción completa

Para *n* = 2. Por un lado 

$$
C=
\begin{bmatrix}
a_{11} & a_{12} \cr
a_{21} + b_{21} & a_{22} + b_{22} \cr
\end{bmatrix}
\=
a_{11}a_{22} + a_{11}b_{22} - a_{12}a_{21} - a_{12}b_{21}
$$

y por otro

$$
|A| + |B| = 
\begin{bmatrix}
a_{11} & a_{12} \cr
a_{21} & a_{22} \cr
\end{bmatrix}
+
\begin{bmatrix}
a_{11} & a_{12} \cr
b_{21} & b_{22} \cr
\end{bmatrix}
\=
(a_{11}a_{22} - a_{12}a_{21}) + (a_{11}b_{22} - a_{12}b_{21})
$$

Con lo cual |C| = |A| + |B|.

Hipótesis inductiva: La propiedad es válida para matrices de orden menor que n 

Tesis inductiva: La propiedad es válida para matrices de orden n.

En efecto

<code>(3.18)</code>  |C| <sup>def</sup>= (-1)<sup>1+1</sup>*a*<sub>11</sub> |C<sub>11</sub>| + ... + (-1)<sup>*i*+1</sup>(a<sub>*i*1</sub> + b<sub>*i*1</sub>) |C<sub>*i*1</sub>| + ... + (-1)<sup>*n*+1</sup> a<sub>*n*1</sub> |C<sub>*n*1</sub>|

Observemos que si $k\neq i$, como la matriz C<sub>k1</sub> es de orden $n - 1$, por la hipótesis inductiva se tiene que 

$$
|C_{k1}| = 
\begin{bmatrix}
a_{12}          & ... & a_{1n}          \cr
   :            & ... &     :           \cr
a_{k-12}        & ... & a_{k-1n}        \cr
a_{k+12}        & ... & a_{k+1n}        \cr
   :            & ... &     :           \cr
a_{i2} + b_{i2} & ... & a_{in} + b_{in} \cr
   :            & ... &     :           \cr
\end{bmatrix}
\=
\begin{bmatrix}
a_{12}          & ... & a_{1n}          \cr
   :            & ... &     :           \cr
a_{k-12}        & ... & a_{k-1n}        \cr
a_{k+12}        & ... & a_{k+1n}        \cr
   :            & ... &     :           \cr
a_{i2}          & ... & a_{in}          \cr
   :            & ... &     :           \cr
\end{bmatrix}
\=
\begin{bmatrix}
a_{12}          & ... & a_{1n}          \cr
   :            & ... &     :           \cr
a_{k-12}        & ... & a_{k-1n}        \cr
a_{k+12}        & ... & a_{k+1n}        \cr
   :            & ... &     :           \cr
b_{i2}          & ... & b_{in}          \cr
   :            & ... &     :           \cr
\end{bmatrix}
\=
|A_{k1}| + |B_k1|;
$$

luego si sustituimos en <code>(3.18)</code> se tiene que 

|C| = (-1)<sup>1+1</sup> a<sub>11</sub> [|A<sub>11</sub>| + |B<sub>11</sub>|] + ... + (-1)<sup>i+1</sup> (a<sub>i1</sub> + b<sub>i1</sub>) |C<sub>i1</sub>| + ... + (-1)<sup>n+1</sup>  a<sub>n1</sub> [|A<sub>n1</sub>| + |B<sub>n1</sub>|] =

(-1)<sup>1+1</sup> a<sub>11</sub>  |A<sub>11</sub>| + ... + (-1)<sup>i+1</sup> a<sub>i1</sub> |C<sub>i1</sub>| + ... + (-1)<sup>n+1</sup> a<sub>n1</sub> |A<sup>n1</sup>| + (-1)<sup>1+1</sup> a<sub>11</sub>  |B<sub>11</sub>| + ... + (-1)<sup>i+1</sup> b<sub>i1</sub> |C<sub>i1</sub>| + ... + (-1)<sup>n+1</sup> a<sub>n1</sub> |B<sub>n1</sub>|

Pero como 

$$
|C_{i1}| =
\begin{bmatrix}
a_{12}          & ... & a_{1n}          \cr
   :            & ... &     :           \cr
a_{i-12}        & ... & a_{i-1n}        \cr
a_{i+12}        & ... & a_{i+1n}        \cr
   :            & ... &     :           \cr
a_{n2}          & ... & a_{nn}          \cr
\end{bmatrix}
= |A_{i1}| = |B_{i1}|
$$

resulta que

|C| = (-1)<sup>1+1</sup> a<sub>11</sub> |A<sub>11</sub>| + ... + (-1)<sup>i+1</sup> a<sub>i1</sub> |A<sub>i1</sub>| + ... + (-1)<sup>n+1</sup> a<sub>n1</sub> |A<sub>n1</sub>| + (-1)<sup>1+1</sup> a<sub>11</sub> |B<sub>11</sub>| + ... + (-1)<sup>i+1</sup>  b<sub>i1</sub> |B<sub>i1</sub>| + ... + (-1)<sup>n+1</sup> a<sub>n1</sub> |B<sub>n1</sub>|

= |A| + |B|


**OBSERVACIÓN** <code>3.2</code> No es cierto que |A + B| = |A| + |B|


#### b) Homogeneidad (respecto a una fila)

Si B es una matriz que se obtiene de A multiplicando una de sus filas por un número $\alpha$ entonces

$$
|B| =
\begin{bmatrix}
a_{11}        &  a_{12}         & ... & a_{1n}             \cr
   :          &    :            & ... &     :              \cr
\alpha a_{i1} &  \alpha a_{i2}  & ... &  \alpha a_{i-1n}   \cr
   :          &    :            & ... &     :              \cr
a_{n1}        &  a_{n2}         & ... & a_{nn}             \cr
\end{bmatrix}
\= 
\alpha
\begin{bmatrix}
a_{11}        &  a_{12}         & ... & a_{1n}             \cr
   :          &    :            & ... &     :              \cr
a_{i1}        &  a_{i2}         & ... & a_{i-1n}           \cr
   :          &    :            & ... &     :              \cr
a_{n1}        &  a_{n2}         & ... & a_{nn}             \cr
\end{bmatrix}
\=
\alpha |A|
$$




















