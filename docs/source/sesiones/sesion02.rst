Estrellas ✨ y Planetas 🪐
===================================

Sistema de coordenadas
------------------

Hemos aprendido a especificar el color de lo que queremos dibujar, lo 
siguiente que necesitamos aprender es cómo ubicarlos. En tus clases 
de matemáticas, probablemente has aprendido sobre el sistema de 
coordenadas cartesiano, que se ve así:

.. image:: ../img/cartesian_coordinate_system.svg
  :width: 400
  :alt: Sistema de coordenadas

Fuente: `Wikipedia: Cartesian coordinate system <https://commons.wikimedia.org/wiki/File:Cartesian_coordinate_system_(comma).svg>`_

Nuestros gráficos se dibujarán usando este mismo sistema. Pero 
debemos tener en cuenta:

1. Solo dibujaremos en el cuadrante superior derecho (Cuadrante I). 
Por lo tanto, el punto 0,0 estará en la esquina inferior izquierda 
de la pantalla, y todas las coordenadas negativas estarán fuera de 
la pantalla.

2. Cada punto es un :term:`píxel`. Así que tu ventana tiene 600 
píxeles de ancho. 

.. warning::

  Recuerda que los píxeles se cuentan desde el cero (0). El cero es uno 
  de los píxeles, por lo que van desde el 0 hasta el 599 (600) píxeles.

De líneas a estrellas
------------------

Para dibujar una línea, se utiliza con la función :py:func:`arcade.draw_line()` 
con los siguientes parámetros:

1. La coordenada del punto inicial (posición en X, posición en Y), 
2. La coordenada del punto final (posición en X, posición en Y),
3. El color de la línea, y
4. El ancho de la línea. 

En nuestra imagen de ejemplo, usaremos varias líneas para dibujar 
rayos de una estrella:

.. code-block:: python
    :emphasize-lines: 8-12, 14-17

    ...

    # Inicio del dibujo
    ...

    # (Aquí irá el código para dibujar)

    # Rayos de luz
    # Horizontal, de izquierda (400, 450) a derecha (500, 450)
    arcade.draw_line(400, 450, 500, 450, arcade.color.HELIOTROPE, 1)
    # Vertical, de arriba (450, 500) a abajo (450, 400)
    arcade.draw_line(450, 500, 450, 400, arcade.color.HELIOTROPE, 1)

    # Abajo a la izquierda (425, 425) hacia arriba la derecha (475, 475)
    arcade.draw_line(425, 425, 475, 475, arcade.color.HELIOTROPE, 3)
    # Arriba a la izquierda (425, 475) hacia abajo la derecha (475, 425)
    arcade.draw_line(425, 475, 475, 425, arcade.color.HELIOTROPE, 3)

    # Fin del dibujo
    ...

.. rubric:: Reto
  :heading-level: 2

Ahora, crea tu propia estrella dentro de la ventana, tomando como centro 
el punto (100,100).

.. important::
  
  Recuerda escoger el tamaño, el grosor y el color de las líneas 
  en la estrella.


De círculos a planetas
------------------

Para dibujar un círculo, se utiliza con la función 
:py:func:`arcade.draw_circle_filled()` con los siguientes parámetros:

1. La coordenada del centro (posición en X, posición en Y), 
2. El radio del círculo,
3. El color de la línea. 

En nuestra imagen de ejemplo, usaremos un círculo para dibujar un planeta:

.. code-block:: python
    :emphasize-lines: 6,7

    ...

    # Inicio del dibujo
    ...

    # Planeta	
    arcade.draw_circle_filled(100, 350, 30, arcade.color.arcade.csscolor.DARK_VIOLET))

    # Fin del dibujo
    ...

.. note::

    Puedes consultar los nombres en la 
    tabla de colores de 
    `arcade.csscolor package <https://api.arcade.academy/en/latest/api_docs/arcade.csscolor.html>`_.
    para especificar colores por nombre (por 
    ejemplo `arcade.csscolor.PURPLE_MOUNTAIN_MAJESTY`), 

De círculos a cráteres
------------------

En nuestra imagen de ejemplo, usaremos varios círculos para dibujar los 
cráteres en el planeta al sobreponer círculos de diferentes formas y colores:

.. code-block:: python
    :emphasize-lines: 9-12

    ...

    # Inicio del dibujo
    ...

    # Planeta	
    arcade.draw_circle_filled(100, 350, 30, arcade.csscolor.DARK_VIOLET)

    # Cráteres del planeta
    arcade.draw_circle_filled(90, 360, 5, arcade.csscolor.DARK_SLATE_GRAY)
    arcade.draw_circle_filled(110, 355, 4, arcade.csscolor.DARK_SLATE_GRAY)
    arcade.draw_circle_filled(95, 340, 3, arcade.csscolor.DARK_SLATE_GRAY)

    # Fin del dibujo
    ...

.. rubric:: Reto
  :heading-level: 2

Ahora, crea tu propio planeta dentro de la ventana, tomando como centro 
el punto (150,30).

.. important::
  
  Recuerda escoger colocar varios crácteres en el planeta.

Otras formas
------------------