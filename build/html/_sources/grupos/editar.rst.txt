.. Este documento posee todos los commandos importantes que se deben utilizar à la hora de documenta
.. Por favor mirarlos y añadir los que utilicen y sean importantes y que no esten aquí.

.. Título

Edición de grupos
======================================

El sistema permite la Edición de grupos de usuarios, esto actualizará los grupos de usuarios creados anteriormente.

=================
Condiciones previas
=================

* Para usuarios que no son root, debe estar logeado con un grupo que tenga ya permisos para entrar en el modulo de grupos.
* Tener permisos ya establecidos en la base de datos.
* Tener grupos de usuarios ya establecidos en la base de datos.
* Ingresar al modulo de listado de grupos **/usuarios/listar_grupos/**

	* La petición GET retorna una pagina con todos los datos de permisos y grupos de usuarios ya establecidos en la base de datos:
	 Usando las clases dentro de "viwes.py" > "forms.py"
::

   ListarGroupView > CreateGroup

=================
Iniciar Edición
=================

1. Dentro del modulo listar grupos, en el modulo central se encuentra todos los grupos de usuarios creados con controles en la parte derecha de cada grupo, dar click donde está el botón **azul** con el icono **lapiz** para emprezar la edición del grupo y sus permisos.

.. image:: images/listado.png
    :align: center

.. image:: images/boton_editar.png
    :align: center

2. Se abre un modal con el formulario para la edición del grupo, los siguientes campos aparecen diligenciados con los datos del grupo seleccionado "No es obligatorio modificar todos los campos" :

	* El primer campo, es el nombre que se le pondrá al grupo.
	
	* El segundo campo, se encuentran los permisos, esta dividido en dos recuadros:
	
		* **Recuadro izquierdo:** Todos los permisos que existen y no se han seleccionado.
		* **Recuadro derecho:** Todos los permisos que existen y se han seleccionado para ser parte de este grupo.
		* Para mover de recuadro a recuadro los permisos, solo es dar click sobre el nombre del permiso que desea mover.
		
	* Existen dos botones en la parte inferior del modal: 
	
		* **Seleccionar todo:** Selecciona todos los permisos (pasa todo del recuadro izquierdo al recuadro derecho, dejando el recuadro izquierdo vacio).
		
		* **Deseleccionar todo:** Pasa todos los permisos del recuadro derecho al recuadro izquierdo, dejando el recuadro derecho vacío.

.. image:: images/modal_editar.png
    :align: center
		
3. Teniendo diligenciado el campo "nombre del grupo" y seleccionado como minimo 1 permiso en el segundo campo "permisos del grupo", el sistema permitirá actualizar el grupo, con el botón azul "Editar Grupo".

	* La petición POST se envia con los siguientes datos a la direccion **/usuarios/editar_group_tenants/** :
	
		* "name:" Nombre del grupo.
		* "permissions:" con los id de los permisos que se asigaran en ese grupo.
		
	* Se envía una petición GET a cuenta/login?next=/usuarios/crear_group_tenants/

.. image:: images/guardar_editar.png
    :align: center




