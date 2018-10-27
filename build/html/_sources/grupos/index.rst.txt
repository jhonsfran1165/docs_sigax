.. Este documento posee todos los commandos importantes que se deben utilizar à la hora de documenta
.. Por favor mirarlos y añadir los que utilicen y sean importantes y que no esten aquí.

.. El sistema permite la creación de grupos de usuarios, esto hará que los usuarios con dichos grupos tengan permisos a distintas funciones o modulos dentro de la aplicación.

Grupos de usuarios (Grupo de permisos para usuarios)
======================================


=================
Creación
=================

El sistema permite la creación de grupos de usuarios, esto permitirá agregar grupos de usuarios con permisos a distintas funciones o modulos dentro de la aplicación. `Ver <crear.html>`_ .

=================
Edición
=================

El sistema permite la Edición de grupos de usuarios, esto actualizará los grupos de usuarios creados anteriormente. `Ver <editar.html>`_ .

=================
Eliminación
=================

El sistema permite la eliminación de grupos de usuarios, si y solo si, no esta asignado ya a usuarios del sistema, esto eliminará un grupo de usuario creado anteriormente. `Ver <eliminar.html>`_ .


Base de datos
======================================

Las Tablas en la base de datos que son afectadas por este modulo son

* **auth_group** ::
	
    * id	
		* tipo: int
		* Largo: --
		* Nulo: No
		* PK: Si

    * name	
		* tipo: character varying
		* Largo: 80
		* Nulo: No
		* PK: No
		

* **auth_permission** ::
	
    * id	
		* tipo: int
		* Largo: --
		* Nulo: No
		* PK: Si

    * name	
		* tipo: character varying
		* Largo: 255
		* Nulo: No
		* PK: No

    * content_type_id	
		* tipo: int
		* Largo: --
		* Nulo: No
		* PK: No

    * codename	
		* tipo: character varying
		* Largo: 100
		* Nulo: No
		* PK: No

* **auth_group_permissions** ::
	
    * id	
		* tipo: int
		* Largo: --
		* Nulo: No
		* PK: Si

    * group_id	
		* tipo: int
		* Largo: --
		* Nulo: No
		* PK: No
		* Refiere a: "id" - auth_group

    * permission_id	
		* tipo: int
		* Largo: --
		* Nulo: No
		* PK: No
		* Refiere a: "id" - auth_permission

