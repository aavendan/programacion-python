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

Personajes
------------------

Nuestros juegos necesitan soporte para manejar objetos que colisionan. 
Pelotas que rebotan en paletas, rayos láser que golpean a extraterrestres 
o nuestro personaje favorito que recoge una moneda. Todos estos ejemplos 
requieren detección de colisiones.

La biblioteca Arcade tiene soporte para sprites. Un sprite es una imagen 
bidimensional que forma parte de una escena gráfica más grande. Por lo 
general, un sprite será algún tipo de objeto en la escena con el que se 
interactuará, como un automóvil, una rana o un pequeño fontanero.

  .. code-block:: python
    :emphasize-lines: 11-14

      ...

      # (Aquí irá el código para dibujar)
      planetas = arcade.SpriteList()

      planeta1 = arcade.Sprite("sprites/planet01.png", 0.08)
      planeta1.center_x = 150
      planeta1.center_y = 450
      planetas.append(planeta1)

      planeta2 = arcade.Sprite("sprites/planet02.png", 0.05)
      planeta2.center_x = 150
      planeta2.center_y = 450
      planetas.append(planeta2)

      planetas.draw()