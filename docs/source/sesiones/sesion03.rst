Misión 03: Galaxias 🌌
===================================

En la misión anterior aprendimos a usar funciones, crear variables y a usar las variables en expresiones. 

Ahora, vamos a aprovechar este conocimiento para crear funciones y así agrupar varias instrucciones relacionadas entre sí.  Una :term:`función` es un grupo de comandos que le damos a la computadora.

.. figure:: ../img/sesion03/istockphoto-1845480259-612x612.jpg
    :scale: 40%
    :figclass: align-center
    :alt: ordenes

Ya hemos usado funciones, por ejemplo, la función :py:func:`arcade.draw_line()` o la función :py:func:`arcade.Text()`. Ahora vamos a aprender a crear nuestras propias funciones.

Función: Título del juego
------------------

.. code-block:: python
   :caption: Función titulo_juego

    def titulo_juego():
        """ Esta función muestra el título del juego. """

        # Título en (300, 200), de tamaño 32 pts.
        arcade.Text("Galaxia Indie", 300, 200, arcade.color.WHEAT, 32).draw()
        
Para escribir una función:

#. Comienza con la palabra clave ``def``, que es la abreviatura de *define*.
#. A continuación, escribe el nombre de la función. 

    .. warning::
        Los nombres de funciones siguen las mismas reglas que los nombres de variables. Deben:

            1. Comenzar con una letra minúscula.
            2. Después de la primera letra, solo usa letras, números y guiones bajos.
            3. No se permiten espacios. Usa guiones bajos en su lugar.
            4. Si bien se pueden usar letras mayúsculas, los nombres de las funciones normalmente son todos en minúsculas.

#. Después de eso, tenemos un par de paréntesis. Dentro de los paréntesis irán los parámetros (Los veremos después).
#. A continuación, dos puntos.
#. Por lo general, comenzamos una función con un comentario de varias líneas que explica lo que hace la función.
#. Todo el código que va en la función estará en las siguientes líneas. Ese código debe tener una :term:`sangría` o :term:`indentación`. 

.. rubric:: Crea la función
  :heading-level: 2

Para escribir la función en tu programa, define la función :py:func:`titulo_juego()` al inicio de tu programa. Copia y pega el código de la función en tu programa.

.. code-block:: python
   :caption: Función titulo_juego
   :emphasize-lines: 4-9

    #Variables
    ....

    #Funciones
    def titulo_juego():
        """ Esta función muestra el título del juego. """

        # Título en (300, 200), de tamaño 32 pts.
        arcade.Text("Galaxia Indie", 300, 200, arcade.color.WHEAT, 32).draw()

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    ...

.. rubric:: Llama a la función
  :heading-level: 2

Reemplaza o comenta el código por la llamada a la función:

.. code-block:: python
   :caption: Llamada a la función titulo_juego
   :emphasize-lines: 4-5

   ...
   
   # Título en (300, 200), de tamaño 32 pts.
   # arcade.Text("Galaxia Indie", 300, 200, arcade.color.WHEAT, 32).draw()
   titulo_juego()

   # Fin del dibujo
   ...


Función: Dibujar una estrella
------------------

.. admonition:: Haga click aquí para ver la solución
  :collapsible: closed
  
  .. code-block:: python
    :caption: Función dibujar_estrella

    # Variables
    ...
    
    def dibujar_estrella():
    
        """ Esta función dibuja una estrella en la pantalla. """

        # Rayos de luz
        # Horizontal, de izquierda (400, 450) a derecha (500, 450)
        arcade.draw_line(400, 450, 500, 450, arcade.color.HELIOTROPE, 1)
        # Vertical, de arriba (450, 500) a abajo (450, 400)
        arcade.draw_line(450, 500, 450, 400, arcade.color.HELIOTROPE, 1)

        # Abajo a la izquierda (425, 425) hacia arriba la derecha (475, 475)
        arcade.draw_line(425, 425, 475, 475, arcade.color.HELIOTROPE, 3)
        # Arriba a la izquierda (425, 475) hacia abajo la derecha (475, 425)
        arcade.draw_line(425, 475, 475, 425, arcade.color.HELIOTROPE, 3)