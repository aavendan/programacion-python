Taller 03
===================================

Reproduce la siguiente imagen mediante figuras primitivas de Arcade

.. figure:: ../img/talleres/final_program02.png
   :width: 450
   :figclass: align-center
   :alt: final_program02

Utiliza el siguente código como base para comenzar:

.. code-block:: python

      """
      Atardecer naranja de la ciudad

      Creado con Python y con Arcade.
      """

      # Importar la librería "arcade" para crear videojuegos.
      import arcade

      # Constantes
      ALTO = 600
      ANCHO = 600
      TITULO = "Atardecer naranja de la ciudad"

      # Crear una ventana de 600x600 píxeles con el título "Atardecer naranja de la ciudad"
      arcade.open_window(ANCHO, ALTO, TITULO)    

      # Establecer el color de fondo de la ventana
      arcade.set_background_color( arcade.csscolor.ORANGE_RED )

      # Inicio del dibujo
      arcade.start_render()

      # (Aquí irá el código para dibujar)

      # Fin del dibujo
      arcade.finish_render()

      # Inicia el bucle principal del juego que mantiene la ventana abierta
      arcade.run()

.. note::

    Puedes consultar los nombres en la 
    tabla de colores de 
    `arcade.csscolor <https://api.arcade.academy/en/latest/api_docs/arcade.csscolor.html>`_
    para especificar colores por nombre (por 
    ejemplo `arcade.csscolor.DARK_VIOLET`) o  `arcade.color <https://api.arcade.academy/en/latest/api_docs/arcade.color.html>`_
    para especificar colores por nombre (por 
    ejemplo `arcade.color.DARK_IMPERIAL_BLUE`)

.. rubric:: Formas básicas
  :heading-level: 2

Para las formas básicas puedes consultar la 
documentación de Arcade en el sitio oficial con más 
`formas básicas <https://api.arcade.academy/en/latest/example_code/drawing_primitives.html#drawing-primitives>`_ y el `índice de instrucciones de formas básicas <https://api.arcade.academy/en/latest/api_docs/quick_index.html#quick-index>`_.

.. rubric:: ChatGPT o Gemini
  :heading-level: 2

Puedes utilizar ChatGPT o Gemini para generar el código y para resolver tus dudas. Un prompt sugerido es:

.. code-block:: python
   
      """
      Utiliza Python y Arcade 3.0.2 para generar un pantalla como la que aparece en la imagen. No utilices funciones, ni main, ni bucle for, ni clases.
      """

Recuerda comprobar siempre el resultado de tu código en tu computadora.