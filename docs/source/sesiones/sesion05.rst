Misión 05: Navegando por el espacio 🚀🌌
===================================

En la misión anterior aprendimos a crear y a usar funciones propias. En esta sesión, aprenderemos a configurar panel de control de nuestra nave.

.. figure:: ../img/sesion05/panel_control.jpeg
    :scale: 120%
    :figclass: align-center
    :alt: panel de control

Para comenzar, abra **Visual Studio Code** y utiliza la carpeta ``galaxia_indie``. Verifica el archivo ``mision01.py`` tenga el siguiente código:

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

    # Constantes
    ALTO = 600
    ANCHO = 600
    TITULO = "Misión 01: Listos para el despegue"

    # Variables
    # Creamos una lista de sprites
    planetas = arcade.SpriteList()
    naves = arcade.SpriteList()

    # Creamos un sprite y establecemos la posición
    planeta1 = arcade.Sprite("sprites/planeta01.png", 0.08)
    planeta1.center_x = 150
    planeta1.center_y = 450

    # Agregamos el sprite a la lista de sprites
    planetas.append(planeta1)

    # Sprite 2
    planeta2 = arcade.Sprite("sprites/planeta02.png", 0.02)
    planeta2.center_x = ANCHO - 100
    planeta2.center_y = ALTO / 2
    planetas.append(planeta2)

    # Sprite 3
    planeta3 = arcade.Sprite("sprites/planeta03.png", 0.05)
    planeta3.center_x = 100
    planeta3.center_y = ALTO / 3
    planetas.append(planeta3)

    # Sprite 4
    nave01 = arcade.Sprite("sprites/nave01.png", 0.6)
    nave01.center_x = ANCHO / 2
    nave01.center_y = 40
    naves.append(nave01)

    #Funciones
    def abrir_ventana():
        """ Abre la ventana """
        
        # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
        arcade.open_window(ANCHO, ALTO, TITULO)

    def fondo_ventana():  
        """ Muestra el fondo de la ventana """
        
        # Establecer el color de fondo de la ventana
        arcade.set_background_color( arcade.color.DARK_IMPERIAL_BLUE )

    abrir_ventana()
    fondo_ventana()

    # Inicio del dibujo
    arcade.start_render()

    # (Aquí irá el código para dibujar)
    planetas.draw()
    naves.draw()

    # Fin del dibujo
    arcade.finish_render()

    # Inicia el bucle principal del juego que mantiene la ventana abierta
    arcade.run()

Control: Dibujar todos los sprites
------------------

El primer control a programar será **dibujar todos los sprites**. Para esto: 

#. Define la función :py:func:`dibujar_sprites()`,
#. Mueve las instrucciones para dibujar las listas de *sprites*. 
#. Llama a la función :py:func:`dibujar_sprites()` en el lugar donde se encontraban las instrucciones para dibujar las listas de *sprites*

.. code-block:: python
    :caption: Define la función dibujar_sprites
    :emphasize-lines: 5-12, 18-19

    ...
    def fondo_ventana():
        ...
   
    def dibujar_sprites():
        """ Limpia la pantalla y dibuja la lista de sprites """
        
        # Limpia la ventana antes de dibujar
        arcade.get_window().clear()
        
        planetas.draw()
        naves.draw()

    ...

    # (Aquí irá el código para dibujar)
    
    # El control on_draw sirve para indicar qué función se ejecutará cada vez que se necesite redibujar la ventana del juego
    arcade.get_window().on_draw = dibujar_sprites

Al ejecutar el código, deberías ver los tres planetas y la nave en la ventana como 
se muestra a continuación.

.. figure:: ../img/sesion05/tresplanetasynave.png
    :width: 300
    :figclass: align-center
    :alt: tresplanetasynave

El control :py:func:`arcade.get_window().on_draw` sirve para indicar qué función se ejecutará cada vez que se necesite redibujar la ventana del juego.

Control: Mover la nave
------------------

El segundo control a programar será **mover la nave**. Para esto: 

.. code-block:: python
    :caption: Define la función dibujar_sprites
    :emphasize-lines: 3, 9-13, 20-21

    # Constantes
    ...
    VELOCIDAD = 10

    ...
    def dibujar_sprites():
        ...

    def mover_sprites(tecla_principal, tecla_modificadora):
        """ Reacciona a la tecla presionada (tecla_principal) con el movimiento de la nave"""

        if tecla_principal == arcade.key.UP:
            nave01.center_y += VELOCIDAD
    
    ...

    # El control on_draw sirve para indicar qué función se ejecutará cada vez que se necesite redibujar la ventana del juego
    ...

    # El control on_key_press sirve para indicar qué función se ejecutará cuando se presione una tecla en el juego.
    arcade.get_window().on_key_press = mover_sprites


Al ejecutar el código, deberías ver los tres planetas y la nave en la ventana como 
se muestra a continuación.

.. figure:: ../img/sesion05/tresplanetasynavemoviendo.gif
    :width: 300
    :figclass: align-center
    :alt: tresplanetasynavemoviendo