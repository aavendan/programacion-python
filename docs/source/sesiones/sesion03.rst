Misión 01: Listos para el despegue 🚀
===================================

Programa principal: mision01.py
------------------

En Visual Studio Code, crea el archivo ``mision01.py``, con el siguiente 
código básico:

Personajes
------------------

Constantes
------------------

Variables
------------------

.. code-block:: python

    player_list = arcade.SpriteList()

    # Crear sprite del astronauta
    astronaut = arcade.Sprite("astronautA_SE.png", 1.0)  # 1.0 is the scaling factor
    astronaut.center_x = 300  # Position X
    astronaut.center_y = 300  # Position Y
    player_list.append(astronaut)
    player_list.draw()