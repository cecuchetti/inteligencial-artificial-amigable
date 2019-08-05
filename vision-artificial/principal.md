## ¿Qué es un histograma?

Un histograma es una herramienta gráfica que representa las frecuencias relativas de los niveles de gris de una imagen.

  


## ¿Para qué se usa un histograma?

Se usa para el cálculo de coeficientes estadísticos tales como: el valor medio, la desviación estándar y la entropía. El histograma resulta muy útil para determinar si el contraste o la exposición de una imagen digital son los adecuados. Y se puede utilizar para aplicar un procedimiento de mejoramiento de imágenes denominado ecualización o igualación de histograma.

  


## ¿Cómo se interpreta el gráfico?

![](https://lh6.googleusercontent.com/vBoJUR2-oYYAVXbrdszlxAxeXS76Xb5XoAdLObhmfYcFiUSYohh9dJ1UOdMY9GEI1pnuocwU79yr0pl_Gi4G5TFAPLllMX1BGSZzB2dNNfL0qarmwRKGHWeWUGmACawlOXvCebaL)

Los números que aparecen el eje horizontal representan los niveles de gris (g) que pueden aparecer en la imagen: a la izquierda está el valor más oscuro (negro) y en el extremo derecho el más claro (blanco). El resto de niveles se distribuyen uniformemente. Se ha puesto una escala con los tonos de gris correspondientes para facilitar la comprensión. En un histograma real habitualmente no encontrará numerado el eje vertical, ni la escala de tonos para el eje horizontal.

La altura de cada barra representa el número de píxeles de la imagen que presentan ese nivel de gris concreto. Se puede deducir entonces que la imagen tiene 15 píxeles completamente negros (con nivel 0), 11 de tono gris oscuro (nivel 1) y 38 píxeles completamente blancos (nivel 3). No hay ningún píxel en la imagen con un nivel de gris 2.

  


## ¿Qué podría deducir mirando el histograma?

Con sólo mirar el histograma podemos deducir algunas cosas interesantes sobre la imagen, lo que demuestra su utilidad:

-   La mayor parte de los píxeles son blancos, así que probablemente se aprecie un fondo blanco uniforme.
-   Hay un número significativo de píxeles totalmente blancos y totalmente negros, por lo que presentará un aspecto bien contrastado.

  


## Explicar ecualización de histogramas.

-   Este proceso se basa en una transformación g -> g’ de manera de lograr un reacomodamiento de las líneas del histograma en nuevos intervalos Δg.
-   Es una transformación que pretende obtener para una imagen un histograma con una distribución uniforme. Es decir, que exista el mismo número de pixeles para cada nivel de gris del histograma de una imagen monocroma.
-   En la transformación, todos los pixels de un mismo nivel de gris se transformarán a otro nivel de gris, y el histograma se distribuirá en todo el rango disponible separando en lo posible las ocupaciones de cada nivel.
-   El resultado de la ecualizaciónmaximiza el contraste de una imagen sin perder información de tipo estructural, esto es, conservando su entropía
-   Basándonos en:h(g)Δg=cte.Así, cuanto más alto sea h(g) mayor será la separación entre las barras.
-   Para el cálculo del nuevo valor de g usaremos la siguiente fórmula: gnuevo = gprevio + k h(g)

  


## ¿Hay un histograma ideal?

Cada imagen tiene su propio histograma. Pero como regla general se considera que una imagen tiene un buen contraste si su histograma se extiende ocupando casi todo el rango de tonos.

  


## ¿Qué son los filtros de imagen?

-   Es el conjunto de técnicas depreprocesamiento de imágenes basado en operadores cuyo objetivo fundamental es obtener, a partir de una imagen origen, otra final cuyo resultado sea más adecuado para una aplicación específica mejorando ciertas características que posibilite efectuar operaciones del procesado sobre ella.
-   Esta herramienta calcula un pixel para la imagen transformada, en función de la vecindad local en la imagen original.
-   Se consideran los filtros como operaciones que se aplican a los píxeles de una imagen digital para optimizarla, enfatizar cierta información o conseguir un efecto especial en ella.

  


## ¿Qué tipo de filtros conoce?

Filtro paso bajo (suavizamiento): utilizados para eliminar ruidoo detalles pequeños de poco interés puesto que sólo afecta a zonas con muchos cambios. Se emplean diversas técnicas:

-   **Media**: reemplaza cada píxel por el valor medio de sus contiguos.
-   **Mediana**: sustituye por el valor de la mediana de los píxeles vecinos (normalmente se comporta mejor que el de promedio).
-   Gaussiano: aproximación a la distribución gaussiana.

El filtro de la**mediana** consiste en tomar una ventana de 1x5, reemplazar el valor central por el valor de la mediana de los números que la componen. (La mediana se calcula ordenando los elementos y tomando el valor que queda en el centro). El filtro de la**media** es similar pero se reemplaza el valor del medio por el promedio del conjunto.

  


## ¿Qué es la convolución de imágenes digitales?

-   En matemáticas, la convolución es un operador que transforma dos funciones f y g en una tercera función que en cierto sentido representa la magnitud en la que se superponen f y una versión trasladada e invertida de g.
-   En imágenes digitales, es el tratamiento de una matriz por otra llamada máscara. El filtro matriz de convolución usa una primera matriz que es la imagen que será tratada. La máscara deseada (otra matriz) depende del efecto deseado. Matrices comunes son de 5x5 o 3x3
-   Elmétodo puede hacer resaltar o disminuir la presencia de ciertos valores en una región deseada mediante el uso de máscaras.
-   Un filtro de convolución discreta, para una imagen digital, en el espacio real (X,Y), puede representarse como una matriz cuadrada o rectangular (matriz de convolución), de dimensiones (M,N) mucho más pequeñas que la de la imagen.
-   La matriz de convolución se desplaza sobre la imagen de tal forma que el elemento central de la matriz de convolución coincida con cada uno de los píxeles de la imagen.
-   En cada posición, se multiplica el valor de cada píxel de la imagen, que coincide en posición con un elemento de la matriz de convolución, por el valor de éste.
-   El píxel de la imagen, que coincide con el elemento central de la matriz de convolución, es substituido por la suma de los productos.

PrewitSobelPrewitSobel

![](https://lh6.googleusercontent.com/8AgC2fNHhIrKQowaXNR5NB4FGCmHo1QIATxuo4zfl-QMLbGUlYHUZ4lpP7Z-dEFbweOXMWqeZPVDLbJRCLNDwVKjC_DyVkdQTpCsHf7qYHwbATs0SMIG3gdTVAS8Fi2bXtgbaGz0)![](https://lh6.googleusercontent.com/rKBlvUIkxHvvLoqgNHbrMRgCG0wRZ_TWGrzWN5tsjSVtHBi8pIYLZ7W90FK2LmeO4gF8RTAky3NVumskpgptswgDmOBG87y5GwMO9qfD1m2_aasPMbY4_nO7cIi5zisA0B2QX3el) Bordes Verticales![](https://lh3.googleusercontent.com/vAzRC4TvM1o82a0vI1nxB8jYBtZwTM1OpnoTEq6ZXCFBXMB-GPf5AnedlJZmBBgqdX694kOOp8ojmJ95h075epo-ETjI7-maznOQ7Xn-vVZoAU5iTq-C0GWROeTZUkG_2_KVtD6S)![](https://lh5.googleusercontent.com/nQeGgyUl8dpdvRnJ9dnFwpdAxVaW3AoiZCWuCYf4STd33se_SNytsRkWzNkPsnNO-TudG8tdeRCKuuvROZF2Dah4NIG2HkwIEOtKb8zMkz9vHr4IoRi6nsUFkLk7groGTmD4NNs9)Bordes Horizontales

  




Transformada de Hough como técnica de segmentación

  


La segmentación es el proceso que divide una imagen en regiones u objetos cuyos píxeles poseen atributos similares. Cada región segmentada suele tener un significado físico dentro de la imagen. Es uno de los procesos más importantes de un sistema automatizado de visión ya que permite extraer los objetos de la imagen para su posterior descripción y reconocimiento.

Las técnicas de segmentación pueden encuadrarse en 3 grupos fundamentales: técnicas basadas en la detección de fronteras, técnicas de umbralización y técnicas basadas en el agrupamiento de píxeles.

En las técnicas basadas en la frontera, la segmentación de una imagen puede llevarse a cabo mediante la detección de los límites de cada región, es decir, detectando los bordes de la imagen.

Las otras dos técnicas umbralización y técnicas basadas en el agrupamiento de píxeles) enfocan la segmentación como un problema de clasificación de píxeles en un grupo de píxeles, donde píxeles de una región suelen ser similares y pixeles de regiones distintas deben ser no similares. Las regiones resultantes deben tener cierto significado para el procesamiento posterior.

La transformada de Hough es una técnica de segmentación basada en la frontera. Esta transformada es una herramienta que permite detectar curvas en una imagen. Es una técnica muy robusta frente al ruido y a la existencia de huecos en las fronteras del objeto. A la hora de aplicar la transformada a una imagen, es necesario primero obtener una imagen binaria de los píxeles que forman parte de la frontera del objeto.

A continuación explicamos de forma muy simplificada la transformada de Hough para detectar rectas. El objetivo es encontrar puntos alineados que puedan existir en la imagen, es decir puntos en la imagen que satisfagan la ecuación de la recta para distintos valores de ϱ y ϑ.

Ecuación de la recta en forma polar

Por lo tanto hay que realizar una transformación entre el plano imagen (coordenadas XY) el plano espacio de parámetros ( ϱ, ϑ).

Para aplicar la transformada es necesario discretizar el espacio de parámetros en una serie de celdas denominadas celdas de acumulación. Esta discretización se realiza sobre los intervalos (ϱ min, ϱ max) y (ϑ min, ϑ max).

El siguiente paso es evaluar la ecuación de la recta para cada punto de la imagen (xy) si se cumple esta ecuación se incrementa en 1 el número de votos en la célula.

Un número de votos elevados indica que el punto pertenece a la recta. En primer lugar usaremos la transformada de Hough para detectar rectas. La transformada considera las relaciones globales entre píxeles de bordes permitiendo encontrar ciertos patrones en la imagen como líneas o círculos.

Supongamos que para n puntos de la imagen se desean encontrar aquellos subconjuntos de puntos que caen en líneas rectas. Una posible solución podría ser encontrar en primer lugar todas las líneas determinadas por cada par de puntos y entonces encontrar todos los subconjuntos de puntos que estén cerca de cada recta en particular.

## Neocognitrón

-   No es backpropagation, ya que estas se usan para propósitos más generales.
-   Fueron creados con una arquitectura de propósito concreto: reconocimiento de caracteres escritos a mano.
-   Es un modelo del cerebro que emula la arquitectura funcional de la corteza visual.
-   Presenta una estructura jerárquica por capas donde se extraen características
-   Se usaron resultados de estudios neurobiológicos para crear una arquitectura de red.
-   Las capas pueden ser S, C, V.
-   Las capas S imitan a la retina
-   La ventaja principal es que no solo reconocen patrones aprendidos, sino también aquellos que fueron producidos por alteraciones en esos patrones al: desplazarlos, rotarlos u otras distorsiones.
-   1 capa es un conjunto de células planas. Esas células dependen del número de características a extraer
-   Las capas V tienen una sola célula plana
