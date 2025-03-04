Misión 01: Listos para el despegue 🚀
===================================

Programa principal: mision01.py
------------------

En Visual Studio Code, crea el archivo ``mision01.py`` con el siguiente 
código básico:

.. code-block:: python

    """
    Galaxia Indie

    Un juego indie minimalista de exploración espacial 
    donde viajarás a través del cosmos.
    Navega a través de misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado con Python y con Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    import arcade

    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
    arcade.open_window(600, 600, "Misión 01: Listos para el despegue")    

    # Establecer el color de fondo de la ventana
    arcade.set_background_color( arcade.color.DARK_IMPERIAL_BLUE )

    # Inicio del dibujo
    arcade.start_render()

    # (Aquí irá el código para dibujar)

    # Fin del dibujo
    arcade.finish_render()

    # Inicia el bucle principal del juego que mantiene la ventana abierta
    arcade.run()

Ejecuta el código y verás una ventana con el color de fondo azul oscuro, como 
se muestra en la siguente imagen. 

.. imagen

Hasta ahora, hemos aprendido cómo importar **Arcade** y cómo llamar a ciertas 
funciones para dibujar figuras geométricas. El siguiente paso es hacer nuestro 
código más flexible.

Constantes
------------------

Una :term:`constante` es un valor que no cambia durante la ejecución del 
programa, por ejemplo el título, el ancho y el alto de la ventana.

.. code-block:: python
    :emphasize-lines: 3,6

    ...

    ANCHO = 600

    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
    arcade.open_window( ANCHO, 600, "Misión 01: Listos para el despegue")    

    ...

El código anterior, se asigna el valor de 600 la constante ``ANCHO``. 
Luego, en la función :py:func:`arcade.open_window()` reemplace el valor de 600 
por el nombre de la constante ``ANCHO``.

.. warning::
    
    1. Los nombres deben ser descriptivos, 
    2. Todas las letras en **mayúscula**, 
    3. Si tienes varias palabras, sepáralas con un guión bajo, y 
    4. Los nombres no pueden  comenzar con un número ni tener un 
    espacio ni ningún símbolo que no sea un guión bajo. 

.. rubric:: Reto
  :heading-level: 2
  :class: mi-clase-css

Crea las constantes ``ALTO`` y ``TITULO``. Asigna a cada constan el valor 
correspondiente. Luego, en la función :py:func:`arcade.open_window()` reemplace 
los valores por la constante correspondiente.

.. admonition:: Clic aquí para ver una pista
  :collapsible: closed

  A continuación, la solución al reto anterior.

  .. code-block:: python
    :emphasize-lines: 4,5,8

    ...

    ANCHO = 600
    ALTO = 600
    TITULO = "Misión 01: Listos para el despegue"
    
    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
    arcade.open_window( ANCHO, ALTO, TITULO )    

    ...

Variables
------------------

Una :term:`variable` es un valor que la computadora almacena en la memoria y 
que puede cambiar (variar) en otra parte del programa. 

A continuación, realiza el siguiente cambio en el código anterior:

  .. code-block:: python

    ...

    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
    arcade.open_window( ANCHO, ALTO, TITULO ) 


Para identificar las variables y las constantes, hay nombres que debes usar, 
nombres que no debes usar y nombres que no puedes usar.

.. warning::
    
    1. Los nombres deben ser descriptivos, 
    2. Todas las letras en **minúscula**, 
    3. Si tienes varias palabras, sepáralas con un guión bajo, y 
    4. Los nombres no pueden  comenzar con un número ni tener un 
    espacio ni ningún símbolo que no sea un guión bajo. 

Personajes
------------------

.. code-block:: python

    player_list = arcade.SpriteList()

    # Crear sprite del astronauta
    astronaut = arcade.Sprite("astronautA_SE.png", 1.0)  # 1.0 is the scaling factor
    astronaut.center_x = 300  # Position X
    astronaut.center_y = 300  # Position Y
    player_list.append(astronaut)
    player_list.draw()