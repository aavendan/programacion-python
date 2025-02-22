Un nuevo universo 🌌
===================================

Comenta tu código
------------------

Antes de empezar a escribir programas largos, 
necesitamos aprender sobre los comentarios en el 
código. 

Cuando escribimos código, a veces queremos describir 
lo que hace, para nosotros mismos o para otros. 

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

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    

Librería Arcade
------------------

Antes de poder dibujar algo, necesitamos importar 
una :term:`librería` de código que contiene comandos para 
dibujar.

Si queremos usar la librería Arcade solo debemos 
agregar `import arcade` al inicio de nuestro programa.

.. code-block:: python
    :emphasize-lines: 14 

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


Ventana para dibujar
------------------

La primera :term:`función` de Arcade que vamos a aprender es `arcade.open_window()`. 
Esta función abre una ventana con un tamaño y título específicos.
La función `open_window`` requiere al menos tres parámetros:

- El *ancho de la ventana en píxeles.
- El *alto* de la ventana en píxeles.
- El *texto* que aparecerá en la barra de título.

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


¡Funciona (pero muy rápido)!

Para mantener la ventana abierta, necesitamos hacer 
una pausa hasta que el usuario presione el botón de 
cerrar. Para hacer esto, usaremos la función `run` 
de la librería Arcade. 

Esta función run no necesita parámetros, pero aún así 
requiere paréntesis.

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

    # Iniciar el bucle principal del juego que mantiene la ventana abierta
    arcade.run()

.. glossary::

    librería
        Un conjunto de instrucciones especializadas que
        se pueden importar a un programa para realizar
        tareas específicas. También se conocen como módulos.

    función
        Un bloque de código que realiza una tarea específica
        y puede ser llamado desde cualquier parte del programa.
        Las funciones pueden tener parámetros y devolver valores.