Estrellas✨ y Planetas🌑
===================================

Sistema de coordenadas
------------------

Hemos aprendido a especificar el color de lo que queremos dibujar, lo 
siguiente que necesitamos aprender es cómo ubicarlos. En tus clases 
de matemáticas, probablemente has aprendido sobre el sistema de 
coordenadas cartesiano, que se ve así:

.. figure:: ../img/cartesian_coordinate_system.svg
   :width: 400
   :figclass: align-center
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
    :emphasize-lines: 4-8, 10-13

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

.. figure:: ../img/sesion02/estrella.png
   :width: 300
   :figclass: align-center
   :alt: Estrella
  

.. rubric:: Reto
  :heading-level: 2
  :class: mi-clase-css

Crea tu propia estrella dentro de la ventana, tomando como centro el 
punto (100,100). Decide y escoge el tamaño, el grosor y el color de 
las líneas de la estrella.

.. admonition:: Haga click aquí para ver la solución
  :collapsible: closed

  .. code-block:: python
    :emphasize-lines: 8-12, 14-16

    ...
    # (Aquí irá el código para dibujar)
    ...

    # Arriba a la izquierda (425, 475) hacia abajo la derecha (475, 425)
    ...

    # Estrella en  (100,100)
    # Línea horizontal
    arcade.draw_line(75, 100, 125, 100, arcade.color.HELIOTROPE, 1)
    # Línea vertical
    arcade.draw_line(100, 75, 100, 125, arcade.color.HELIOTROPE, 1)

    # Líneas diagonales
    arcade.draw_line(85, 85, 115, 115, arcade.color.HELIOTROPE, 3)
    arcade.draw_line(85, 115, 115, 85, arcade.color.HELIOTROPE, 3)

    # Fin del dibujo
    ...

De círculos a planetas
------------------

Para dibujar un círculo, se utiliza con la función 
:py:func:`arcade.draw_circle_filled()` con los siguientes parámetros:

1. La coordenada del centro (posición en X, posición en Y), 
2. El radio del círculo,
3. El color de la línea. 

En nuestra imagen de ejemplo, usaremos un círculo para dibujar un planeta:

.. code-block:: python
    :emphasize-lines: 9-10

    ...

    # (Aquí irá el código para dibujar)
    ...

    # Líneas diagonales
    ...

    # Planeta	
    arcade.draw_circle_filled(100, 350, 30, arcade.csscolor.DARK_VIOLET)

    # Fin del dibujo
    ...

.. note::

    Puedes consultar los nombres en la 
    tabla de colores de 
    `arcade.csscolor <https://api.arcade.academy/en/latest/api_docs/arcade.csscolor.html>`_.
    para especificar colores por nombre (por 
    ejemplo `arcade.csscolor.DARK_VIOLET`), 

De círculos a cráteres
------------------

En nuestra imagen de ejemplo, usaremos varios círculos para dibujar los 
cráteres en el planeta al sobreponer círculos de diferentes formas y colores:

.. code-block:: python
    :emphasize-lines: 12-15

    ...

    # (Aquí irá el código para dibujar)
    ...

    # Líneas diagonales
    ...

    # Planeta	
    arcade.draw_circle_filled(100, 350, 30, arcade.csscolor.DARK_VIOLET)

    # Cráteres del planeta
    arcade.draw_circle_filled(90, 360, 5, arcade.csscolor.DARK_SLATE_GRAY)
    arcade.draw_circle_filled(110, 355, 4, arcade.csscolor.DARK_SLATE_GRAY)
    arcade.draw_circle_filled(95, 340, 3, arcade.csscolor.DARK_SLATE_GRAY)

    # Fin del dibujo
    ...

.. figure:: ../img/sesion02/crateres.png
   :width: 300
   :figclass: align-center
   :alt: Cráteres

.. rubric:: Reto
  :heading-level: 2
  :class: mi-clase-css

Crea tu propio planeta dentro de la ventana, tomando como centro el
punto (200,200), con radio 15 y color `arcade.csscolor.GRAY`. 
Agrega los cráteres con las siguientes características:

1. Con el centro (190, 205), radio 3 y color `arcade.csscolor.DARK_GRAY`
2. Con el centro (210, 195), radio 3 y color `arcade.csscolor.DARK_GRAY`
3. Con el centro (205, 210), radio 2 y color `arcade.csscolor.DARK_GRAY`

.. admonition:: Haga click aquí para ver la solución
  :collapsible: closed

  .. code-block:: python
    :emphasize-lines: 7-9, 11-14

    # (Aquí irá el código para dibujar)
    ...

    # Cráteres del planeta
    ...

    # Planeta en (200,200)
    # Planeta Gris
    arcade.draw_circle_filled(200, 200, 15, arcade.csscolor.GRAY)
    
    # Cráteres del planeta
    arcade.draw_circle_filled(190, 205, 3, arcade.csscolor.DARK_GRAY)
    arcade.draw_circle_filled(210, 195, 3, arcade.csscolor.DARK_GRAY)
    arcade.draw_circle_filled(205, 210, 2, arcade.csscolor.DARK_GRAY)

    # Fin del dibujo
    ...

Texto
------------------

Para dibujar texto, se utiliza con la función :py:func:`arcade.Text()` 
con los siguientes parámetros:

1. El texto a dibujar,
2. La coordenada del punto inicial (posición en X, posición en Y),
3. El color del texto,
4. El tamaño del texto.

.. code-block:: python
    :emphasize-lines: 9-10

    ...

    # (Aquí irá el código para dibujar)
    ...

    # Cráteres del planeta
    ...

    # Título en (300, 200), de tamaño 32 pts.
    arcade.Text("Galaxia Indie", 300, 200, arcade.color.WHEAT, 32).draw()

    # Fin del dibujo
    ...

.. figure:: ../img/sesion02/texto.png
   :width: 300
   :figclass: align-center
   :alt: Texto

Hasta ahora, hemos aprendido cómo importar **Arcade** y cómo llamar a ciertas 
funciones para dibujar figuras geométricas. El siguiente paso es hacer nuestro 
código más flexible.

Constantes
------------------

Una :term:`constante` es un valor que no cambia durante la ejecución del 
programa, por ejemplo el ancho de la ventana.

.. code-block:: python
    :emphasize-lines: 4-5,7-8

    # Importar la librería "arcade" para crear videojuegos.
    ...

    # Constantes
    ANCHO = 600

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window( ANCHO, 600, "Galaxia Indie")    

    ...

El código anterior, se asigna el valor de 600 la constante ``ANCHO``. 
Luego, en la función :py:func:`arcade.open_window()` reemplace el valor de 600 
por el nombre de la constante ``ANCHO``.

.. warning::
    
    1. Los nombres deben ser descriptivos, 
    2. Todas las letras en **mayúscula**, 
    3. Si tienes varias palabras, sepáralas con un guión bajo, y 
    4. Los nombres no pueden  comenzar con un número ni tener un espacio ni ningún símbolo que no sea un guión bajo. 

.. rubric:: Reto
  :heading-level: 2
  :class: mi-clase-css

Crea las constantes ``ALTO`` y ``TITULO``. Asigna a cada constante el valor 
correspondiente. Luego, en la función :py:func:`arcade.open_window()` reemplace 
los valores por la constante correspondiente.

.. admonition:: Haga click aquí para ver la solución
  :collapsible: closed

  .. code-block:: python
    :emphasize-lines: 4-5,7-8

    ...
    # Constantes
    ANCHO = 600
    ALTO = 600
    TITULO = "Galaxia Indie"
    
    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window( ANCHO, ALTO, TITULO )    

    ...

Variables
------------------

Una :term:`variable` es un valor que la computadora almacena en la memoria y 
que puede cambiar (variar) en otra parte del programa. 

A continuación, modifica las siguientes instrucciones al código anterior:

  .. code-block:: python
    :emphasize-lines: 4-7,14,17-18,20

    # Constantes
    ...
    
    # Variables
    planeta_centro_x = 200
    planeta_centro_y = 200
    radio = 15

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    ...

    # Planeta en (200,200)
    # Planeta Gris
    arcade.draw_circle_filled( planeta_centro_x, planeta_centro_y, radio, arcade.csscolor.GRAY)
    
    # Cráteres del planeta
    crater1_centro_x = planeta_centro_x - 10
    crater1_centro_y = planeta_centro_y + 5

    arcade.draw_circle_filled(crater1_centro_x, crater1_centro_y, 3, arcade.csscolor.DARK_GRAY)
    arcade.draw_circle_filled(210, 195, 3, arcade.csscolor.DARK_GRAY)
    arcade.draw_circle_filled(205, 210, 2, arcade.csscolor.DARK_GRAY)
    

    ...

El código anterior, se asignan el valor de 200 para cada una de 
las variables ``planeta_centro_x`` y ``planeta_centro_y``. 
Luego, en la función :py:func:`arcade.draw_circle_filled()` 
reemplace los valores por los nombres de las variables ``planeta_centro_x`` 
y ``planeta_centro_y``. 

Calculamos el valor ``crater1_centro_x`` restando 10 a la variable 
``planeta_centro_x``. Además, calculamos el valor ``crater1_centro_y`` sumando 5
a la variable ``planeta_centro_y``.
Finalmente, en :py:func:`arcade.draw_circle_filled()` reemplazamos el valor 
de 190 por la variable ``crater1_centro_x`` y reemplazamos el valor de 205 por 
la variable ``crater1_centro_y``.

.. warning::
    
    1. Los nombres deben ser descriptivos, 
    2. Todas las letras en **minúscula**, 
    3. Si tienes varias palabras, sepáralas con un guión bajo, y 
    4. Los nombres no pueden  comenzar con un número ni tener un espacio ni ningún símbolo que no sea un guión bajo. 

.. rubric:: Reto
  :heading-level: 2
  :class: mi-clase-css

Crea las variables ``crater2_centro_x``, ``crater2_centro_y``, 
``crater3_centro_x`` y ``crater3_centro_y`` y asigna el valor calculado 
correspondiente considerando las coordenadas centro del 
planeta (``planeta_centro_x`` y ``planeta_centro_y``).
Luego, reemplaza las variables correspondientes en las funciones 
:py:func:`arcade.draw_circle_filled()`.

.. admonition:: Haga click aquí para ver la solución
  :collapsible: closed

  .. code-block:: python
    :emphasize-lines: 6-9,12-13

    ...

    # Cráteres del planeta
    crater1_centro_x = planeta_centro_x - 10
    crater1_centro_y = planeta_centro_y + 5
    crater2_centro_x = planeta_centro_x + 10
    crater2_centro_y = planeta_centro_y - 5
    crater3_centro_x = planeta_centro_x + 5
    crater3_centro_y = planeta_centro_y + 10

    arcade.draw_circle_filled(crater1_centro_x, crater1_centro_y, 3, arcade.csscolor.DARK_GRAY)
    arcade.draw_circle_filled(crater2_centro_x, crater2_centro_y, 3, arcade.csscolor.DARK_GRAY)
    arcade.draw_circle_filled(crater3_centro_x, crater3_centro_y, 2, arcade.csscolor.DARK_GRAY)

    ...