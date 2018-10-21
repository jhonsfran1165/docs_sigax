.. Este documento posee todos los commandos importantes que se deben utilizar à la hora de documenta
.. Por favor mirarlos y añadir los que utilicen y sean importantes y que no esten aquí.

.. Título

Commandos Básicos
======================================

.. Listas

* This is a bulleted list.
* It has two items, the second
  item uses two lines.

1. This is a numbered list.
2. It has two items too.

#. This is a numbered list.
#. It has two items too.


.. Secciones principal

=================
Listas
=================


.. Listas anidadas

* this is
* a list

  * with a nested list
  * and some subitems

* and here the parent list continues


.. Bloques de textos

This is a normal text paragraph. The next paragraph is a code sample::

   It is not processed in any way, except
   that the indentation is removed.

   It can span multiple lines.

This is a normal text paragraph again.


=================
Notas
=================

.. Nota normal
.. note::

   Bienvenido a SIGAX. El Software para el crecimiento inmediato y masivo de empresas.

.. Nota warning
.. warning::

   Bienvenido a SIGAX. El Software para el crecimiento inmediato y masivo de empresas.

.. Bloque para referenciar documentación u otras cosas
.. seealso::

   Module :py:mod:`zipfile`
   Documentation of the :py:mod:`zipfile` standard module.
   `GNU tar manual, Basic Tar Format <http://link>`_
   Documentation for tar archive files, including GNU tar extensions.


.. Subtitulo
.. rubric:: 
   Ejemplo


.. Titulo centrado
.. centered:: LICENSE AGREEMENT


.. Hacer una Lista y dividirla en columnas.
.. hlist::
   :columns: 3

   * A list of
   * short items
   * that should be
   * displayed
   * horizontally

.. Escribir un bloque de código
.. code-block::
   python
   :linenos:

   Some more Ruby code.

.. Incluir un archivo completo en la documentación
.. literalinclude:: ../../manage.py



.. Incluir un archivo completo en la documentación
.. Y resaltar las lineas de código importantes
.. literalinclude:: ../../manage.py
   :language: python
   :emphasize-lines: 12,15-18
   :linenos:


.. Si no se quiere colocar todo el código se puede referenciar el archivo en el título y 
.. Escribir la línea de código importante
.. code-block:: python
   :caption: this.py 
   :name: this-py

   imprimir 'Explicito es mejor que implícito'



.. Secciones secundarias

Otros comandos
-------------------------

:emphasis: my arguments.
:code: asdasdasd
:literal: asdasdasd

.. Contanido de campos

:fieldname: Field content

.. Ejemplos

def my_function(my_arg, my_other_arg):
   :param my_arg: The first of my arguments.
   :param my_other_arg: The second of my arguments.
   :returns: A message (just for me, of course).

.. Hiperlinks

Para ver toda la documentación ingrese aquí `a link`_.

.. _a link: http://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html

.. imagenes

.. image:: images/prueba.png


