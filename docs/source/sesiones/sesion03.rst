Misión 03: Despegue 🚀
===================================

Programa principal: mision01.py
------------------

#. En Windows, crea la carpeta ``galaxia_indie``.

    .. figure:: ../img/sesion03/creacioncarpeta.png
        :figclass: align-center
        :alt: Crear la carpeta del proyecto

#. En Visual Studio Code, abre la carpeta ``galaxia_indie``. 

    .. figure:: ../img/sesion03/abrircarpeta.png
        :figclass: align-center
        :alt: Busca la carpeta del proyecto

    .. figure:: ../img/sesion03/abrirgalaxia_indie.png
        :figclass: align-center
        :alt: Abrir la carpeta del proyecto

#. Crea el archivo ``mision01.py`` dentro de la carpeta ``galaxia_indie``

    .. figure:: ../img/sesion03/crearmision01.png
        :figclass: align-center
        :alt: Crear el archivo mision01.py

#. Copia el siguiente código básico y pégalo en tu archivo ``mision01.py``:

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

        # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
        arcade.open_window(ANCHO, ALTO, TITULO)    

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

  .. figure:: ../img/sesion03/base.png
      :scale: 50%
      :figclass: align-center
      :alt: base

Sprite y SpriteList
------------------

.. rubric:: Imágenes de los planetas
  :heading-level: 2

#. Crea la carpeta `sprites` junto a tu archivo **mision01.py**.

    .. figure:: ../img/sesion03/crearsprites.png
        :figclass: align-center
        :alt: Crear el archivo sprites

#. Descarga las imágenes de :download:`planeta01 <../img/sesion03/planeta01.png>`, :download:`planeta02 <../img/sesion03/planeta02.png>` y :download:`planeta03 <../img/sesion03/planeta03.png>`
#. Coloca las imágenes en la carpeta `sprites`. 

    .. figure:: ../img/sesion03/imagenesplanetas.png
        :figclass: align-center
        :alt: Guardar imagenes de planetas

.. note::
    
    Puedes obtener más imágenes en `kenney.nl <https://kenney.nl/>`_.

.. rubric:: Planetas
  :heading-level: 2

Un :term:`sprite` es una imagen :term:`bidimensional` que forma 
parte de una escena gráfica más grande. Por lo general, un sprite 
será algún tipo de objeto en la escena con el que se interactuará, 
como un planeta, un extraterrestre o una nave.

Copia las siguientes instrucciones resaltadas y colócalas en las ubicaciones indicadas.

.. code-block:: python
    :emphasize-lines: 4-6, 8-11, 13-14, 22-23

    # Constantes
    ...

    # Variables 
    # Creamos una lista de sprites
    planetas = arcade.SpriteList()

    # Creamos un sprite y establecemos la posición
    planeta1 = arcade.Sprite("sprites/planeta01.png", 0.08)
    planeta1.center_x = 150
    planeta1.center_y = 450

    # Agregamos el sprite a la lista de sprites
    planetas.append(planeta1)

    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"

    ...

    # (Aquí irá el código para dibujar)

    # Dibujamos la lista de sprites
    planetas.draw()

    # Fin del dibujo
    ...

.. rubric:: Explicación
  :heading-level: 2
  :class: explanation

Antes de empezar, utilizaremos la variable ``planetas`` 
para almacenar nuestros sprites en una :term:`lista` 
(:py:func:`arcade.SpriteList()`).

.. code-block:: python

    ...
    # Creamos una lista de sprites
    planetas = arcade.SpriteList()


Luego, usamos la variable ``planeta1`` 
para almacenar un sprite :py:func:`arcade.Sprite()`, 
con la :term:`ruta` a la imagen y la :term:`escala`. 

Además, usamos la variable ``planeta1`` para 
colocar el sprite en la ventana cuyo centro es (``x``, ``y``), con 
``planeta1.center_x = 150`` y en ``planeta1.center_y = 450``.

.. code-block:: python

    ...
    # Creamos un sprite y establecemos la posición
    planeta1 = arcade.Sprite("sprites/planeta01.png", 0.08)
    planeta1.center_x = 150
    planeta1.center_y = 450

Luego, con :py:func:`planetas.append()` agregamos el sprite 
(``planeta1``) a la lista de sprites (``planetas``).

.. code-block:: python

    ...
    # Agregamos el sprite a la lista de sprites
    planetas.append(planeta1)

Finalmente, dibujamos la lista de sprites ``planetas`` en la ventana.

.. code-block:: python

    ...
    # Dibujamos la lista de sprites
    planetas.draw()


.. figure:: ../img/sesion03/planetaenventana.png
   :width: 300
   :figclass: align-center
   :alt: Planeta en la ventana


.. rubric:: Reto
  :heading-level: 2
  :class: mi-clase-css

#. Crea un sprite para la imagen ``sprites/planeta02.png``, con una escala de **0.02**. El centro se encuentra a **100 píxeles** menos del ancho de la ventana y a la **mitad vertical** de la ventana.
#. Crea un sprite para la imagen ``sprites/planeta03.png``, con una escala de **0.05**. El centro se encuentra a **100 píxeles** y a un **tercio de la vertical** de la ventana.
#. Agrega cada uno de los sprites a la lista de sprites.

Al ejecutar el código, deberías ver los tres planetas en la ventana como 
se muestra a continuación.

.. figure:: ../img/sesion03/tresplanetas.png
    :width: 300
    :figclass: align-center
    :alt: tresplanetas


.. admonition:: Haga click aquí para ver la solución
  :collapsible: closed

  .. code-block:: python
    :emphasize-lines: 4-8,10-14

    # Agregamos el sprite a la lista de sprites
    ...

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

    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"
    ...

.. rubric:: Reto
  :heading-level: 2
  :class: mi-clase-css

.. rubric:: Imagen
  :heading-level: 2

#. Descarga la imagen de la :download:`nave <../img/sesion03/nave01.png>`.
#. Guarda la imagen en la carpeta ``sprites``.

.. rubric:: Código
  :heading-level: 2

#. Crea una lista de sprites llamada ``naves``.
#. Crea un variable ``nave01`` para el sprite con la imagen ``sprites/nave01.png``, con una escala de **0.6**. El centro se encuentra a la **mitad horizontal** de la ventana  y a un **40 píxeles**.
#. Agrega cada el sprite de la nave a la lista de sprites ``naves``.
#. Dibuja la lista de sprites ``naves`` en la ventana.

Al ejecutar el código, deberías ver los tres planetas y la nave en la ventana como 
se muestra a continuación.

.. figure:: ../img/sesion03/tresplanetasynave.png
    :width: 300
    :figclass: align-center
    :alt: tresplanetasynave


.. admonition:: Haga click aquí para ver la solución
  :collapsible: closed

  .. code-block:: python
    :emphasize-lines: 4,10-14,20

    ...
    # Creamos una lista de sprites
    ...
    naves = arcade.SpriteList()
    ...

    # Sprite 3
    ...

    # Sprite 4
    nave01 = arcade.Sprite("sprites/nave01.png", 0.6)
    nave01.center_x = ANCHO / 2
    nave01.center_y = 40
    naves.append(nave01)

    # Crear una ventana de 600x600 píxeles con el título "Misión 01: Listos para el despegue"

    # (Aquí irá el código para dibujar)
    ...
    naves.draw()

.. rubric:: En resumen
  :heading-level: 2

Al finalizar esta sesión, tu código debería verse así:

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