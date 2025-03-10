Misión 03: Galaxias 🌌
===================================

En la misión anterior aprendimos a usar funciones, crear variables y a usar las variables en expresiones. 

Ahora, vamos a aprovechar este conocimiento para crear funciones. Una :term:`función` es un grupo de comandos que le damos a la computadora. 

.. figure:: ../img/sesion03/ordenes.jpeg
    :scale: 50%
    :figclass: align-center
    :alt: ordenes

Ya hemos usado funciones, por ejemplo, la función :py:func:`arcade.draw_line()` o la función :py:func:`arcade.Text()`. Ahora vamos a aprender a crear nuestras propias funciones.

Función basica
------------------

.. code-block:: python
   :caption: Ejemplo de función

    def dibujar_estrella():
        """ Esta función dibuja una estrella en la pantalla. """

        # Rayos de luz
        # Horizontal, de izquierda (400, 450) a derecha (500, 450)
        arcade.draw_line(400, 450, 500, 450, arcade.color.HELIOTROPE, 1)

Para escribir una función:

#. Comienza con la palabra clave def, que es la abreviatura de “define”.
#. A continuación, dale un nombre a la función. 

    .. warning::
        Los nombres de funciones siguen las mismas reglas que los nombres de variables. Deben:

            1. Comenzar con una letra minúscula. (O en casos especiales, un guión bajo).
            2. Después de la primera letra, solo usa letras, números y guiones bajos.
            3. No se permiten espacios. Usa guiones bajos en su lugar.
            4. Si bien se pueden usar letras mayúsculas, los nombres de las funciones normalmente son todos en minúsculas.

#. Después de eso, tenemos un par de paréntesis. Dentro de los paréntesis irán los parámetros. Los explicaremos en breve.
#. A continuación, dos puntos.
#. 

