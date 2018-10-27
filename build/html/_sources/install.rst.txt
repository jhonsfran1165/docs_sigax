.. Título

Guía de Instalación de SIGAX
======================================

La Instalación de SIGAX implica ejecutar la aplicación en un ambiente definido en los requerimets. Además de esto es necesario preparar la base de datos
para que sea posible utilizar una configuracion multi esquema.


Todas estas tareas se programaron y sólo es necesario ejecutar una serie de archivos. Sin embargo se explicará cada archivo para que se tenga una
idea general de cómo funciona. Si desea profundizar debe ir al código.

SIGAX corre bajo python 3.6 por favor instale esta versión en especifíco para ejecutar el proyecto. 


====================
Clonar el proyecto
====================

Si tiene acceso al repositorio de SIGAX sólo debe clonar el repo a su computador. Si aún no tiene acceso debe solicitarlo. Ir a SIGAX en GitHub `a link`_.

.. _a link: https://github.com/jhonsfran1165/sigax


.. note::

    Recuerda que este repositorio es privado.


.. code-block::
   python
   :linenos:

   git clone https://github.com/jhonsfran1165/sigax.git


=================
Instalar Ambiente
=================


.. note::

   Inicialmente se utiliza un ambiente en virtualenv pero próximamente se manejará vía docker.


Virtualenv es una aplicación que permite encapsular parámetros globales en otras aplicaciones de forma local. Esto permite manejar las mismas versiones de 
los requerimientos que son necesarios para la ejecución del programa. Centralizar los parámetros evita el conflicto de versiones cuando se desarrolla
en grupos.


Como primer paso para instalar SIGAX, es necesario ejecutar el siguiente commando desde la consola.


.. code-block::
   python
   :linenos:

   virtualenv env_sigax
   source env_sigax/Scripts/activate


.. warning::

   Para ejecutar este commando debes tener instalado pip para python 3.6


   Si creas el virtualenv dentro del proyecto de SIGAX recuerda incluir el folder del ambiente en el .gitignore. Aconsejamos que lo crees afuera del repositorio.


Una vez creado y activado el ambiente se puede ingresar à la carpeta que se descargó al clonar el repositorio.



========================
Instalar Dependencias
========================


SIGAX trabaja con aplicaciones de terceros, en el sentido de que algunas funcionalidades se implementaron con ayuda de bibliotecas. Se deben instalar las versiones adecuadas para que el proyecto no tenga ningún error de dependencias.


.. code-block::
   sh
   :linenos:

	pip install -r requirements/requirements_development.txt


Una vez descagadas e instaladas las dependencias deberemos configurar la base de datos.




=========================================
Configurar Base de Datos & Migraciones
=========================================


Se debe crear una base de datos de forma local preferiblemente de nombre sigax. Se debe realizar una copia del local_settings.py.py ubicado en la carpeta sigax/sigax/


.. warning::

   Se debe agregar este archivo creado al .gitignore ya que representa la configuración usada para el proyecto en tu entorno local.


.. literalinclude:: ../../sigax/local_settings.py
   :language: python
   :linenos:
   :lines: 290 - 315	
   :emphasize-lines: 10-20


La parte subrayada de este archivo representa la configuración de la base de datos. Eres libre de configurar esta parte de acuerdo a tu conveniencia.


Cuando hayas validado que tu archivo de configuración es correcto. Por favor ejecuta el siguiente commando en la raiz del proyecto:

.. code-block::
   sh
   :linenos:

	sh install.sh


.. warning::

   Si tienes algún error al memento de ejecutar el script, debes solucionarlo, borrar la base de datos creada y volverla a crear. Luego de esto se ejecutar el Script nuevamente.


Ahora nuestro proyecto está casi listo, antes de iniciarlo debemos ejecutar las migraciones de las aplicaciones por medio de un bash automatizado.


Si no tuviste problemas puedes ingresar à la dirección localhost:port donde port es el puerto configurado. Si tu consola se cierra puedes iniciar de nuevo el proyecto con:

.. code-block::
   sh
   :linenos:

	python manage.py runserver localhost:port

