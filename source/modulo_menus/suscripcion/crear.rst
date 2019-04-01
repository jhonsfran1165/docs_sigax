.. Este documento posee todos los commandos importantes que se deben utilizar à la hora de documentar
.. Por favor mirarlos y añadir los que utilicen y sean importantes y que no esten aquí.

.. El sistema permite la creación de suscripciones, las cuales permiten agrupar un conjunto de menus disponibles para los Tenants.

Creación de Suscripciones
======================================

=====================
Condiciones previas
=====================

* Estar logeado como usuario root en el sistema (para la creación de las suscripciones).
* Tener permisos ya establecidos en la base de datos. ??
* Ingresar al modulo de listado de menus **/menus/listar_menus/**

.. image:: images/menu_lateral.jpg
    :align: center

=================
Iniciar Creación
=================

1. Dentro del modulo listar menus, en la parte superior derecha se encuentra el submodulo Gestionar Suscripciones,
donde está el botón verde para emprezar la creación de la suscripción.

.. image:: images/plus.png
    :align: center

2. Se abre un modal con el formulario para la creación del grupo:

	* El primer campo, es el nombre que se le pondrá a la suscripción.
	
	* El segundo campo, corresponde a la descripción que explica el contenido de la suscripción

	* Existen dos botones en la parte inferior del modal: 
	
		* **Cerrar:** Cierra el modal de creación.
		
		* **Crear suscripción:** Guarda la nueva suscripción en base de datos.

.. image:: images/modal_crear.jpg
    :align: center

3. Una vez diligenciado el formulario y al presionar el botón "Crear suscripción", deberá aparecer un cuadro de éxito:

.. image:: images/suscripcion_exitosa.png
	:align: center

4. Posteriormente, una vez creada la suscripción, se podrán asginar los menús desde el panel izquierdo.
Primero se selecciona la suscripción creada y luego se arrastran los menús al panel derecho:

.. image:: images/asignacion_menus.png
	:align: center