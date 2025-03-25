Misión 04: Satélite espacial 🛰️
===================================

.. figure:: ../img/sesion04/satelite.jpeg
    :scale: 40%
    :figclass: align-center
    :alt: ordenes

En la misión anterior aprendimos a usar instrucciones, crear variables, a crear en expresiones matemáticas y a usar sprites. 

En esta misión, aprenderemos a crear nuestras propias :term:`funciones` para dar un instrucciones a la computadora.

Ya hemos usado funciones, por ejemplo, la función :py:func:`arcade.draw_line()`, la función :py:func:`arcade.Text()` o la función :py:func:`arcade.Sprite()`. Ahora vamos a aprender a crear nuestras propias funciones.

De la sesión anterior, abre la crea la carpeta ``galaxia_indie`` que contiene el archivo llamado ``mision01.py``. :

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

  # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
  arcade.open_window(ANCHO, ALTO, TITULO)

  # Establecer el color de fondo de la ventana
  arcade.set_background_color( arcade.color.DARK_IMPERIAL_BLUE )

  # Inicio del dibujo
  arcade.start_render()

  # (Aquí irá el código para dibujar)
  planetas.draw()
  naves.draw()

  # Fin del dibujo
  arcade.finish_render()

  # Inicia el bucle principal del juego que mantiene la ventana abierta
  arcade.run()

Función: Crear ventana
------------------

.. rubric:: 1. Selecciona y copia las instrucciones
  :heading-level: 2

**Selecciona y copia** las siguientes instrucciones y comentarios:

.. code-block:: python
   :caption: Selecciona y copia las instrucciones
   :emphasize-lines: 5

    # Sprite 4
    ...

    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
    arcade.open_window(ANCHO, ALTO, TITULO)

    # Establecer el color de fondo de la ventana
    arcade.set_background_color( arcade.color.DARK_IMPERIAL_BLUE )

    # Inicio del dibujo
    ...

.. rubric:: 2. Escribe la función y coloca el código
  :heading-level: 2

#. Ve al inicio del programa, después de crear todas las variables y define la función :py:func:`crear_ventana()`. 
#. Pega las instrucciones y los comentarios que copiaste anteriormente.
#. Selecciona las instrucciones y los comentarios pegados recientemente, y presiona una (1) vez la tecla TAB.

.. code-block:: python
   :caption: Función titulo_juego
   :emphasize-lines: 4-9

    #Variables
    ....

    #Funciones
    def crear_ventana():
      """ Esta función muestra la ventana. """

      # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
      arcade.open_window(ANCHO, ALTO, TITULO)

      # Establecer el color de fondo de la ventana
      arcade.set_background_color( arcade.color.DARK_IMPERIAL_BLUE )

    # Inicio del dibujo
    ...

.. rubric:: 3. Llama a la función
  :heading-level: 2

Coloca el nombre de la función seguido a un par de paréntesis ``()`` en lugar de se encontraban las instrucciones previamente.

.. code-block:: python
   :caption: Llamada a la función titulo_juego
   :emphasize-lines: 4
  
   ...

   #Funciones
   ...
   
   crear_ventana()

   # Inicio del dibujo
   ...