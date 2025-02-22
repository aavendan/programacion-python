Un nuevo universo 🌌
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

Los lenguajes de programación vienen con un conjunto 
de instrucciones básicas. La mayoría de los programas 
requerirán más instrucciones especializadas. 
A este conjunto de instrucciones especializadas se 
llaman **librerías** o **módulos**.

Si queremos usar la librería Arcade solo debemos 
agregar `import arcade` al inicio de nuestro programa.

.. code-block:: python

    """
    Galaxia Indie

    Un juego indie minimalista de exploración espacial 
    donde viajarás a través del cosmos.
    Navega a través de misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    import arcade


Ventana para dibujar
------------------

La primera **función** de Arcade que vamos a aprender es `arcade.open_window()`. 
Esta función abre una ventana con un tamaño y título específicos.
La función `open_window`` requiere al menos tres parámetros:

- El *ancho de la ventana en píxeles.
- El *alto* de la ventana en píxeles.
- El *texto* que aparecerá en la barra de título.

.. code-block:: python

    """
    Galaxia Indie

    Un juego indie minimalista de exploración espacial 
    donde viajarás a través del cosmos.
    Navega a través de misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    import arcade

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window(600, 600, "Galaxia Indie")    


¡Funciona (pero muy rápido)!

Para mantener la ventana abierta, necesitamos hacer 
una pausa hasta que el usuario presione el botón de 
cerrar. Para hacer esto, usaremos la función `run` 
de la librería Arcade. 

Esta función run no necesita parámetros, pero aún así 
requiere paréntesis.

.. code-block:: python

    """
    Galaxia Indie

    Un juego indie minimalista de exploración espacial 
    donde viajarás a través del cosmos.
    Navega a través de misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    import arcade

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window(600, 600, "Galaxia Indie")   

    # Iniciar el bucle principal del juego que mantiene la ventana abierta
    arcade.run()