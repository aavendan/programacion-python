Misión 01: Un nuevo universo 🌌
===================================

Programa principal: intro.py
------------------

#. En Visual Studio Code, crea un nuevo archivo

    .. figure:: ../img/sesion01/creacionarchivo.png
        :figclass: align-center
        :alt: Creación de archivo

#. Selecciona el tipo de archivo Python

    .. figure:: ../img/sesion01/pythonextension.png
        :figclass: align-center
        :alt: Extension Python

#. Selecciona una carpeta para guardar el archivo con el nombre ``intro.py``

    .. figure:: ../img/sesion01/intropy.png
        :figclass: align-center
        :alt: Intro.py

#. Ahora estamos listos para comenzar a programar

    .. figure:: ../img/sesion01/intropyready.png
        :figclass: align-center
        :alt: Intro.py ready   

Ejecuta el código
------------------

En la parte superior de Visual Studio Code, haz clic en la opción ``Run``, 
en la subopción ``Run Without Debugging``, como se muestra en la image:

.. figure:: ../img/sesion01/runwithoutdebugging.png
    :figclass: align-center
    :alt: Ejecutar sin depurar 

En la parte inferior de Visual Studio Code, aparecerá el :term:`terminal`, 
o :term:`línea de comandos`, con el que se ejecutará tu programa.

.. figure:: ../img/sesion01/outputterminal.png
    :figclass: align-center
    :alt: Terminal



Comenta tu código
------------------

Antes de empezar a escribir programas largos, 
necesitamos aprender sobre los comentarios en el 
código. 

Los comentarios sirven para describir 
lo que hace el código. Lo cual, es útil para nosotros 
mismos o para otros. 

A continuación se muestran dos formas de agregar 
comentarios al código escrito en Python.

.. code-block:: python
    :emphasize-lines: 1-11,13

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
    

Librería Arcade
------------------

Antes de poder dibujar algo, necesitamos importar 
una :term:`librería` de código que contiene comandos para 
dibujar.

Si queremos usar la librería Arcade solo debemos 
agregar :py:data:`import arcade` al inicio de nuestro programa.

.. code-block:: python
    :emphasize-lines: 14 

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


Ventana para dibujar
------------------

La primera :term:`función` de Arcade que vamos a 
aprender es :py:func:`arcade.open_window()`. 
Esta función abre una ventana con un tamaño y título 
específicos y requiere al menos tres :term:`parámetros`:

- El **ancho** de la ventana en píxeles.
- El **alto** de la ventana en píxeles.
- El **texto** que aparecerá en la barra de título.

.. code-block:: python
    :emphasize-lines: 16,17

    """
    Galaxia Indie

    Un juego indie minimalista de exploración espacial 
    donde viajarás a través del cosmos.
    Navega a través de misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    import arcade

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window(600, 600, "Galaxia Indie")    


¡Funciona (pero, es muy rápido)!

Para mantener la ventana abierta, necesitamos hacer 
una pausa hasta que el usuario presione el botón de 
cerrar. 

Para hacer esto, usaremos la función 
:py:func:`arcade.run()` de la librería Arcade. 
Esta función run no necesita parámetros, pero aún 
así requiere paréntesis.

.. code-block:: python
    :emphasize-lines: 19,20

    """
    Galaxia Indie

    Un juego indie minimalista de exploración espacial 
    donde viajarás a través del cosmos.
    Navega a través de misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    import arcade

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window(600, 600, "Galaxia Indie")   

    # Inicia el bucle principal del juego que mantiene la ventana abierta
    arcade.run()

Color de fondo y espacio de dibujo
------------------

En este momento tenemos el color blanco por defecto 
como el fondo de nuestra pantalla. 

¿Cómo podemos obtener un color diferente?

Para cambiar el color de fondo, usamos el comando 
:py:func:`arcade.set_background_color()`. Esta función
necesita un parámetro: el color. En este caso, el nombre de un color, 
por ejemplo: `arcade.color.DARK_IMPERIAL_BLUE`.

Antes de poder ver el color, necesitamos dos comandos 
más. Estos comandos le dicen a la librería Arcade 
cuándo empiezas a dibujar (:py:func:`arcade.start_render()`) y 
cuándo terminas de dibujar (:py:func:`arcade.finish_render()`).

.. code-block:: python
    :emphasize-lines: 19-20,22-23,25,27-28

    """
    Galaxia Indie

    Un juego indie minimalista de exploración espacial 
    donde viajarás a través del cosmos.
    Navega a través de misteriosos sistemas estelares,
    descubriendo antiguos artefactos y desentrañando los 
    misterios de una civilización olvidada.

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear juegos.
    import arcade

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window(600, 600, "Galaxia Indie")

    # Establecer el color de fondo de la ventana
    arcade.set_background_color( arcade.color.DARK_IMPERIAL_BLUE )

    # Inicio del dibujo
    arcade.start_render()

    # (Aquí irá el código para dibujar)

    # Fin del dibujo
    arcade.finish_render()

    # Iniciar el bucle principal del juego que mantiene la ventana abierta
    arcade.run()

.. note::

    Puedes consultar los nombres en la 
    tabla de colores en 
    `arcade.color <https://api.arcade.academy/en/latest/api_docs/arcade.color.html>`_.
    para especificar colores por nombre (por 
    ejemplo `arcade.color.DARK_IMPERIAL_BLUE`)


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

    # Crear una ventana de 600x600 píxeles con el título "Galaxia Indie"
    arcade.open_window(600, 600, "Galaxia Indie")

    # Establecer el color de fondo de la ventana
    arcade.set_background_color( arcade.color.DARK_IMPERIAL_BLUE )

    # Inicio del dibujo
    arcade.start_render()

    # (Aquí irá el código para dibujar)

    # Fin del dibujo
    arcade.finish_render()

    # Inicia el bucle principal del juego que mantiene la ventana abierta
    arcade.run()
