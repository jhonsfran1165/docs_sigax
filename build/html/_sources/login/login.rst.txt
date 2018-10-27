.. Este documento posee todos los commandos importantes que se deben utilizar à la hora de documenta
.. Por favor mirarlos y añadir los que utilicen y sean importantes y que no esten aquí.

.. El sistema permite la creación de grupos de usuarios, esto hará que los usuarios con dichos grupos tengan permisos a distintas funciones o modulos dentro de la aplicación.

Login
======================================

A continuación se explicará cómo funciona el Login del proyecto y cuales son las condiciones previas para que funcione.

=================
Condiciones previas
=================

* El Usuario debe estar creado en la aplicación
* El Usuario debe estar activo
* El Usuario debe tener fechas de ingreso a la aplicación activas. Ver tabla Perfil de Usuarios en la BD

=================
Iniciar Sesión
=================

El ingredar à la url de inicio de sesión del proyecto **/cuenta/login** se despliega una interfaz como la siguiente:

.. image:: images/login.png
    :align: center



El sistema le pedirá el usuario y la contraseña, y además deberá completar el captcha para poder ingresar.