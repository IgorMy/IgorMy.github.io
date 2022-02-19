---
layout: post
title:  "Todo empieza con un perceptrón"
date:   2022-02-17 09:00:00 +0200
categories: Red Neuronal
---

<img class='img-half-width-right' src="{{ '/assets/posts/01/neuronal-network.png' | absolute_url }}"/>

Siempre que escuchamos el término **Red Neuronal** nos imaginamos una especie de sistema complejo en forma de grafo de nodos interconectados. 

Pero, nunca nos preguntamos que son esos nodos, o porque están conectados, o como están conectados, etc. 

Este post es el primero de una serié de posts de redes neuronales en los cuales trataré de responder a todas estas preguntas. También, me gustaría puntualizar que para entender correctamente su contenido, es necesario que el lector tenga nociones básicas en `Python` y `Matemáticas`.

<hr>

Antes de lanzarnos a explorar diferentes redes, su funcionamiento y sus características. Primero, debemos de entender su composición. En este primer post de redes neuronales me centraré en explicar la unidad mínima de una red neuronal, el  **perceptrón**.

Para poder explicarlo de una forma más sencilla y rápida, usaré un perceptrón *simple*, especializado en la *clasificación* de datos y utilizado comúnmente en aprendizaje *supervisado*. 
Estos conceptos, que os puedan sonar extraños, los entenderéis a medida que vayáis leyendo esta serie.

Y como bien dice el dicho, una imagen vale más que mil palabras.

<img class='img-23half-width-center' src="{{ '/assets/posts/01/perceptron.svg' | absolute_url }}" alt='Imágen de perceptrón'>  

Y aquí estamos, yo enseñando diagramas que, para los ojos inexpertos, puede llegar a resultar muy confusos. Pero, no os preocupéis, ahora iremos repasando cada uno de los conceptos que se ven en el diagrama.

<hr>
##### Datos de entrada
<img class='img-half-width-left' src="{{ '/assets/posts/01/perceptron-entrada.svg' | absolute_url }}" alt='Imágen de perceptrón'> Como cualquier función en la programación o en matemáticas, necesitamos alimentarla con datos para que nos devuelva un resultado. En este caso, representamos los datos de entrada del perceptrón con los valores (X1, ..., Xn). Estos datos siempre son numéricos, ya que un ordenador no entiende de palabras.

En el caso de que nuestro *dataset* solo estuviese compuesto por palabras, a cada palabra se le asignaría un número dentro del dominio de la clase, para facilitar su procesamiento.

##### Pesos sinápticos
<img class='img-half-width-left' src="{{ '/assets/posts/01/perceptron-pesos.svg' | absolute_url }}" alt='Imágen de perceptrón'> Una vez que los datos entran en el perceptrón, son preprocesados por el mismo aplicándoles un peso sinápticos. En concreto, el peso sináptico es un número en coma flotante que multiplica al dato de entrada. En función de como se definan estos pesos sinápticos, el perceptrón realizará correctamente su función o no.

Para ello, durante el entrenamiento de la red neuronal, los pesos van cambiando para ir ajustando su funcionamiento.

##### Umbral
<img class='img-half-width-left' src="{{ '/assets/posts/01/perceptron-umbral.svg' | absolute_url }}" alt='Imágen de perceptrón'> Si, para aquellos que pensaron que me faltaba algo por destacar en los diagramas anteriores, los diagramas anteriores están bien. La parte que "faltaba" destacar y está destacado en este diagrama comprende el umbral de funcionamiento.

Este, está compuesto por un valor de entrada X0 que siempre es **-1** y un peso sináptico W0, siendo W0 el umbral. Este umbral se utiliza principalmente para eliminar posible ruido a procesar.

##### Sumatório
<img class='img-half-width-left' src="{{ '/assets/posts/01/perceptron-suma.svg' | absolute_url }}" alt='Imágen de perceptrón'> 
<br>
<br>
<br>
Una vez que los datos sean preprocesados, se les aplica una función de sumatorio. En esta, se suman todos los datos preprocesados y, al estar entre ellos el umbral, se aplica este. Eliminando posibles ruidos o datos que no sean de interés.
<br>
<br>
<br>

##### Función de activación
<img class='img-half-width-left' src="{{ '/assets/posts/01/perceptron-funcion-activacion.svg' | absolute_url }}" alt='Imágen de perceptrón'>
Y aquí estamos, con otro de los componentes más importantes de un perceptrón, la función de activación. Como su nombre indica e igual que en la biología, es la función que determina si el dato que se obtiene del sumatorio activa o no al perceptron.

Es muy importante elegir correctamente la función de activación, ya que de ella depende lo que nos devuelve el perceptrón. Por ejemplo:
<br>
<br>

* Si queremos clasificar nuestros datos de entrada entre dos posibles clases, lo correcto es elegir una función de activación signo o bipolar.
* Si queremos que el perceptrón se active superando un cierto umbral, usaremos la función umbral. 

Repasaremos las funciones más usadas en post posteriores. Pero, si sois impacientes, os dejo los nombres de las funciones más usadas:

* Función de activación signo o bipolar.
* Función de activación umbral.
* Función de activación escalón.
* Función de activación ReLu.

##### Datos de salida
<img class='img-half-width-left' src="{{ '/assets/posts/01/perceptron-salida.svg' | absolute_url }}" alt='Imágen de perceptrón'>
<br>
<br>
<br>
El último componente de este diagrama es el resultado del procesado del perceptrón. Este dato depende directamente de la función de activación como se definió en el apartado anterior.
<br>
<br>
<br>
<hr>
Llegados a este punto, ya hemos repasado completamente que es y como está compuesto un perceptrón. Pero no he dado ningún ejemplo sólido de su funcionamiento ni ninguna fórmula para mejorar su entendimiento. Viendo que este post se está empezando a alargar mucho, dejaremos estas partes tan interesantes para la siguiente entrega de esta serié de posts. Pero antes, para no dejaros con la miel en la boca, al menos os dejaré la función matemática que representa el perceptrón.

<img class='img-half-width-center' src="{{ '/assets/posts/01/perceptron-math.svg' | absolute_url }}" alt='Imágen de perceptrón' >
<hr>
<p class="links">
    <a href="{{ site.linkedin }}" target="_blank">
        <img class="link-button" src="{{ site.baseurl }}/assets/icons/linkedin.png">
    </a>
    <a href="mailto:{{ site.email }}" target="_blank">
        <img class="link-button" src="{{ site.baseurl }}/assets/icons/email.png">
    </a>
    <a href="{{ site.github }}" target="_blank">
        <img class="link-button" src="{{ site.baseurl }}/assets/icons/github.png">
    </a>
</p>