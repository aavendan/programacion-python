Misión 01: Navegando por el espacio 🚀🌌🛸
===================================

.. code-block:: python

    player_list = arcade.SpriteList()

    # Título en (300, 200), de tamaño 32 pts.
    arcade.draw_text("Galaxia Indie", 300, 200, arcade.color.WHEAT, 32)

    # Crear sprite del astronauta
    astronaut = arcade.Sprite("astronautA_SE.png", 1.0)  # 1.0 is the scaling factor
    astronaut.center_x = 300  # Position X
    astronaut.center_y = 300  # Position Y
    player_list.append(astronaut)
    player_list.draw()