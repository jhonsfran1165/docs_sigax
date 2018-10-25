.. Este documento posee todos los commandos importantes que se deben utilizar à la hora de documenta
.. Por favor mirarlos y añadir los que utilicen y sean importantes y que no esten aquí.

.. Título

Eliminar de grupos
======================================

El sistema permite la eliminación de grupos de usuarios, si y solo si, no esta asignado ya a usuarios del sistema, esto eliminará un grupo de usuario creado anteriormente.

=================
Condiciones previas
=================

* Para usuarios que no son root, debe estar logeado con un grupo que tenga ya permisos para entrar en el modulo de grupos.
* Tener grupos de usuarios ya establecidos en la base de datos.
* Ingresar al modulo de listado de grupos **/usuarios/listar_grupos/**

	* La petición GET retorna una pagina con todos los datos de permisos y grupos de usuarios ya establecidos en la base de datos:
	 Usando las clases dentro de "viwes.py" > "forms.py"
::

   ListarGroupView > CreateGroup

=================
Iniciar Eliminación
=================

1. Dentro del modulo listar grupos, en el modulo central se encuentra todos los grupos de usuarios creados con controles en la parte derecha de cada grupo, dar click donde está el botón **COLOR** con el signo **SIGNO** para emprezar la eliminación del grupo y sus permisos.

.. image:: images/plus.png

2. Se abre una verificación para confirmar si se está seguro de realizar la eliminación.

.. image:: images/plus.png
		
3. Al aceptar, se procede a la eliminación del grupo:

	* La petición POST se envia con los siguientes datos a la direccion **/usuarios/eliminar_group_tenants/** :
	
		* "grupo:" id del grupo a eliminar.
		
	* Se envía una petición GET a cuenta/login?next=/usuarios/crear_group_tenants/



