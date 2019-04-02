Base de datos
===============

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

