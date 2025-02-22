Sesión01: Un universo paralelo
===================================

Comenta tu código
------------------

Antes de empezar a escribir programas largos, 
necesitamos aprender sobre los comentarios en el 
código. Cuando escribimos código de computadora, 
a veces queremos poder escribir cosas para nuestro 
propio beneficio y para cualquier otra persona 
que lea el código. Como esto no será código de 
computadora, necesitamos decirle a la computadora 
que lo ignore.

A continuación se muestran dos formas de agregar 
comentarios al código en el lenguaje de programación 
Python:

.. code-block:: python

    """
    Este es un programa de ejemplo para mostrar 
    cómo dibujar usando Python y la biblioteca Arcade.

    Los comentarios de múltiples líneas están 
    rodeados por tres comillas dobles.

    Los comentarios de una sola línea comienzan con 
    un signo de numeral. #
    """

    # Este es un comentario de una sola línea

Librería Arcade
------------------

Antes de poder dibujar algo, necesitamos importar 
una "librería" de código que contiene comandos para 
dibujar.

Los lenguajes de computadora vienen con un conjunto 
de instrucciones básicas. La mayoría de los programas 
requerirán más instrucciones especializadas. 
A este conjunto de instrucciones especializadas se 
llaman **librerías** o **módulos**.

Si queremos usar la librería Arcade solo debemos 
agregar `import arcade` al inicio de nuestro programa.

.. code-block:: python

    """
    Space Wanderer

    Un juego indie minimalista de exploración espacial 
    donde navegas a través del vasto cosmos.
    Los jugadores controlan una solitaria nave espacial
    atravesando misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear juegos.
    import arcade
