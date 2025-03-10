Misión 03: Galaxias 🌌
===================================

En la misión anterior aprendimos a usar funciones, crear variables y a usar las variables en expresiones. 

Ahora, vamos a aprovechar este conocimiento para crear funciones. Una :term:`función` es un grupo de comandos que le damos a la computadora. 

.. figure:: ../img/sesion03/ordenes.jpeg
    :scale: 50%
    :figclass: align-center
    :alt: ordenes

Ya hemos usado funciones, por ejemplo, la función :py:func:`arcade.draw_line()` o la función :py:func:`arcade.Text()`. Ahora vamos a aprender a crear nuestras propias funciones.

Función básica
------------------

.. code-block:: python
   :caption: Ejemplo de una función básica 

    def dibujar_estrella():
        """ Esta función dibuja una estrella en la pantalla. """

        
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

