Un nuevo universo 🌌
===================================

Programa principal
------------------

En Visual Studio Code, crea un archivo con 
extensión `.py`, como se muestra en la imagen:



Ejecuta el código
------------------

En la parte superior de Visual Studio Code, haz clic 
en el botón `Ejecutar Archivo de Python` para 
ejecutar el código, como se muestra en la imagen:


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

    Creado usando Python y la biblioteca Arcade.
    """

    # Importar la librería "arcade" para crear videojuegos.
    

Librería Arcade
------------------

Antes de poder dibujar algo, necesitamos importar 
una :term:`librería` de código que contiene comandos para 
dibujar.

Si queremos usar la librería Arcade solo debemos 
agregar **import arcade** al inicio de nuestro programa.

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

La primera :term:`función` de Arcade que vamos a 
aprender es `arcade.open_window()`. 
Esta función abre una ventana con un tamaño y título 
específicos. La función **arcade.open_window** 
requiere al menos tres :term:`parámetros`:

- El *ancho* de la ventana en píxeles.
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


¡Funciona (pero, es muy rápido)!

Para mantener la ventana abierta, necesitamos hacer 
una pausa hasta que el usuario presione el botón de 
cerrar. 

Para hacer esto, usaremos la función 
**arcade.run()** de la librería Arcade. 
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

    # Iniciar el bucle principal del juego que mantiene la ventana abierta
    arcade.run()

Color de fondo y espacio de dibujo
------------------

En este momento tenemos el color blanco por defecto 
como el fondo de nuestra pantalla. 

¿Cómo podemos obtener un color diferente?

Para cambiar el color de fondo, usamos el comando 
**arcade.set_background_color( )**. Esta función
necesita el nombre de un color, 
por ejemplo: `arcade.color.BLUE_SAPPHIRE`.

Antes de poder ver el color, necesitamos dos comandos 
más. Estos comandos le dicen a la librería Arcade 
cuándo empiezas a dibujar (**arcade.start_render()**) y 
cuándo terminas de dibujar (**arcade.finish_render()**).

.. code-block:: python
    :emphasize-lines: 19,20,22,23,27,28

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
    arcade.set_background_color( arcade.color.BLUE_SAPPHIRE )

    # Inicio del dibujo
    arcade.start_render()

    # (Aquí irá el código para dibujar)

    # Fin del dibujo
    arcade.finish_render()

    # Iniciar el bucle principal del juego que mantiene la ventana abierta
    arcade.run()

.. note::

    Para especificar colores por nombre ( por 
    ejemplo `arcade.color.BLUE_SAPPHIRE`), puedes 
    consultar los nombres en la tabla de colores de 
    `ColorPicker <https://www.webfx.com/web-design/color-picker/color-chart/>`_.


.. glossary::

    librería
        Un conjunto de instrucciones especializadas que
        se pueden importar a un programa para realizar
        tareas específicas. También se conocen como módulos.

    función
        Un bloque de código que realiza una tarea específica
        y puede ser llamado desde cualquier parte del programa.
        Las funciones pueden tener parámetros y devolver valores.
    
    parámetros
        Valores que se pasan a una función para que los use
        al realizar su tarea. 