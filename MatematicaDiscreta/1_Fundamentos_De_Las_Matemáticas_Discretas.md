# 1 Principios fundamentales del conteo

La enumeración, o conteo, puede parecer un proceso obvio que un estudiante aprende al estudiar aritmética por primera vez. Pero luego, según parece, se presta poca atención en lo que se refiere a un desarrollo más amplio del conteo conforme el estudiante pasa a áreas "más difíciles" de la matemáticas, como el álgebra, la geometría, la trigonometría y el cálculo. En consecuencia, este primer capítulo deberá servir como advertencia acerca de la seriedad y dificultad del "mero" conteo.
  La enumeración no termina con la aritmética. También tiene aplicaciones en áreas como la teoría de códigos, la prababilidad y estadística (en matemáticas), y el análisis de algoritmos (en ciencias de la computación). Los capitulos posteriores mostrarán algunos ejemplos específicos de estas aplicaciones.
  A medida que vayamos entrando en este fascinante campo de las matemáticas, nos encontraremos con muchos problemas que se pueden enunciar en forma sencilla pero que son "duros" de resolver. Así, asegúrese de aprender y comprender las fórmulas básicas, pero no confíe demasiado en ellas, ya que, sin el análisis de cada problema, el mero conocimiento de las fórmulas es casi inútil. En vez de ello, acepte el reto de resolver problemas poco usuales o diferentes de los problemas que ha visto en el pasado. Busque soluciones con base en su propio análisis sin importar si es exactamente la que proporciona el autor. Con frecuencia existen varias vías para resolver un problema dado.

## 1.1 Reglas de la suma y del producto

Nuestro estudio de las matemáticas discreta y combinatoria comienza con dos principios básicos del conteo: las reglas de la suma y del producto. Los enunciados y aplicaciones iniciales de estas reglas parecen sencillos. Al analizar problemas más complejos, a menudo podemos descomponerlos en partes que puenedn resolverse mediante estos principios básico. Queremos desarrolar la capacidad de "descomponer" dichos problemas y acomodar nuestras soluciones parciales para llegar a la respuesta final. Una buena forma de hacerlo consiste en analizar y resolver muchos problemas distintos de enumeración, tomando nota, todo el tiempo, de los principios utilizados en la solución. Éste es el método que seguiremos.
  Nuestro primer principio del conteo puede expresarse de la forma siguiente:

*Regla de la suma:* Si una primera tarea puede realizarse de m formas, mientras que una segunda tarea puede realizarse de n formas, y no es posible realizar ambas tareas de manera simultánea, entonces, para llevar a cabo cualquiera de ellas pueden utilizarse cualquiera de m + n formas.

Observe que cuando decimos que una ocurrencia particular, como una primera tarea, puede realizarse de m formas, se supone que estas m formas son distintas, a menos que se indique lo contrario. Esto será así a lo largo de todo el texto.

### Ejemplo 1.1 
  La biblioteca de la universidad tiene 40 libros de texto de sociología y 50 de antropología. Por la regla de la suma, un estudiante de esta universidad puede elegir entre 40 + 50 = 90 libros de texto para aprender acerca de alguno de estos dos temas.

### Ejemplo 1.2 
  La regla puede ampliarse a más de dos tareas, siempre que ninguna pareja de tareas pueda ocurrir en forma simultánea. Por ejemplo, un instructor de ciencias de la computación que tiene, digamos, cinco libros de nivel introductorio acerca de APL, BASIC, FORTRAN y Pascal puede recomendar cualquiera de estos 20 libros a un estudiante interesado on aprender un primer lenguaje de programación.

### Ejemplo 1.3
El instructor de ciencias de la computación del ejemplo 1.2 tiene dos colegas. Uno de ellos tiene tres libros de texto acerca del análisis de algoritmos y el otro cuenta con cinco libros. Si n denota el número máximo de libros diferentes sobre el tema que el instructor puede pedirles prestados, entonces $ 5 \le n \le 8 $ , ya que ambos profesores podrían tener copias del mismo libro (o libros).

El siguiente ejemplo presenta nuestro segundo principio de conteo.

### Ejemplo 1.4
Al tratar de tomar una decisión acerca de la ampliación de una planta, un administrador organiza a 12 de sus empleados en dos comités. El comité A esta formado por 5 miembros y está encargado de investigar los resultados favorables posibles de dicha ampliación. Los otros siete empleados, del comité B, revisarán todas las posibles repercusiones desfavorables. Si el administrador decide hablar sólo con un comité antes de tomar su decisión, entonces, por la regla de la suma, existirán 12 empleados a los que puede llamar. Sin embargo para tener menor sesgo, antes de tomar una decisión, decide hablar con un miembro del comité A el lunes y el matres con un miembro del comité B. Mediante el siguinte prencipio, vemos que puede elegir a esos dos empleados de 5 X 7 = 35 formas.

---
*Regla del producto:* Si un procedimiento se puede descomponer en las etapas primera y segunda, y si existen m resultados posibles de la primera etapa y si, para cada uno de estos resultados, existen n resultados posibles para la segunda etapa, entonces el procedimiento total se puede realizar, en el orden dado, de mn formas.
---

Esta regla se conoce también como el principio de elección


### Ejemplo 1.5
El club de teatro de la Universidad Central realiza ensayos para una obra que se montará en primavera. Si seis hombres y ocho mujeres ensayan para los papeles principales (masculino y femenino), por laregla del producto, el director puede elegir a la pareja principal de 6 X 8 = 48 formas.

### Ejemplo 1.6 
Ahora ejemplificaremos varias extensiones de la regla, examinando la fabricación de placas de automóvil que constan de dos letras seguidas por cuatro dígitos.

- a) Si ninguna letra o dígito se puede repetir, habrá 26 X 25 X 10 X 9 X 8 X 7 = 3,276,000 placas posibles diferentes.
- b) Si se permite repetir las letras y los dígitos, será posible tener 26 X 26 X 10 X 10 X 10 X 10 = 6,760,000 placas diferentes.
- c) Si se permiten las repeticiones, como en la parte (b), ¿cuántas placas tendrán solamente vocales (A, E, I, O, U) y dígitos pares? (0 es un entero par.)

### Ejemplo 1.7
En la memeria principal de un computador, la información se almacena en celdas de memoria. Para identificar las celdas de memeria principal del computador,, cada celda tiene asignado un nombre único conocido como su **dirección**. En algunos computadores, una dirección se representa mediante una lista ordenada de ocho símbolos, en la que cada símbolo es uno de los **bits** (de binary digits, dígitos binarios) 0 o 1. Esta lista de ocho bits se denomina byte. Mediante la regla del producto, vemos que existen 2 X 2 X 2 X 2 X 2 X 2 X 2 = 2<sup>8</sup> = 256 de esos bytes. Por lo tanto, tenemos 256 direcciones para las celdas de memoria en las cuales es posible almacenar información.

  Algunas máquinas (incluyendo la familia de la PDP 11 utilizan direcciones de dos bytes. Tal dirección se forma con dos bytes consecutivos, o 16 bits consecutivos, de modo que es posible almacenar hasta 256 X 256 = 2<sup>8</sup> X 2<sup>8</sup> = 2<sup>16</sup> = 65,536 piezas de información.
Otros computadores (incluyendo el IBM PC/RT) utilizan sistemas de direccionamiento de cuatro bytes. En este caso,, se dispone de hasta 2<sup>8</sup> X 2<sup>8</sup> X 2<sup>8</sup> X 2<sup>8</sup> = 2<sup>32</sup> = 4,294,967,296 direcciones para almacenar información en las celdas de memoria de la máquina.

### Ejemplo 1.8
A veces es necesario combinar varios tipos diferentes de principios de conteo en la solución de un problema. Aquí veremos que necesitamos ambas reglas, la de la suma y la del producto, para obtener el resultado.
  En algunas de las primeras versiones del lenguaje
