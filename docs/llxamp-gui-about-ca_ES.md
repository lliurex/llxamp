# Acerca de este programa...

## ¿Que es LLXAMP?

LLxamp es una instancia de Linux+Apache+PHP+MariaDB que puede ser utilizada para ejecutar prácticas estudiantiles con el lenguaje de programación PHP, aprender a configurar un servidor web como Apache o bien aprender a utilizar sistemas de gestión de bases de datos MySQL/MariaDB.

## ¿Porque necesito LLXAMP?

El software contenido en Llxamp también puede ser obtenido desde la paquetería del sistema operativo, pero en algunos casos puede presentar problemas si ya se está utilizando dicho software para otras tareas en el sistema y no se desea utilizar la instalación existente para realizar prácticas que puedan dejar sin servicio dicha configuración.

Además una instalación del sistema puede no ser suficiente si se desea que múltiples usuarios accedan a estas prácticas en la misma máquina dado que la instalación en el sistema es única y requiere permisos de administración para la modificación de los ficheros de configuración.

## Características de LLXAMP

 - Permite instalar el software para que funcione en modo usuario teniendo toda la instalación en el directorio de usuario donde pueden ser modificados los ficheros por parte del estudiante.
 - Permite el uso de "hosts virtuales" (limitado a dominios .local) sin necesidad de permisos de superusuario.
 - Es eficiente en el uso de disco, parte de la instalación es compartida por todos los usuarios de la máquina.
 - Dispone de una interfaz gráfica para el arranque/parada/estado de los servidores y modificación de ficheros importantes, así como un visor para los registros que van generando.
 - Permite accesos con SSL

## ¿Como comenzar a utilizarlo?

Este programa aunque dispone de múltiples comandos de línea de ordenes está pensado para ser utilizado desde la interfaz gráfica *"llxamp-gui"* que puede ser lanzada desde consola o bien desde el menú de aplicaciones del sistema gráfico del entorno.

La primera vez que es utilizado por el usuario aún no se dispone del software instalado en su carpeta privada de usuario *"$HOME"*, será necesario preparar la instalación para cada usuario desde el único botón activo que presenta la interfaz gráfica, posteriormente cuando acabe el proceso de instalación ya es posible utilizar todos los servicios y se habilitaran todas las opciones en la interfaz.

La instalación será realizada en la ruta *"$HOME/llxamp"* donde el usuario puede observar y modificar todos los ficheros de la instalación, no hay peligro de romper nada del sistema dado que podria volver a regenerarse este directorio forzando otra reinstalación desde la interfaz gráfica.

Si se desean modificar los ficheros de configuración, no es necesario utilizar otra herramienta diferente a la interfaz gráfica Llxamp, desde los menús superiores pueden editarse los ficheros de configuración en uso por los servicios.

En la parte derecha de la interfaz se disponen botones que permiten realizar las acciones mas habituales como son:

- Arrancar los servicios Apache y MariaDB.
- Parar los servicios activos.
- Abrir el navegador para comprobar la página que sirve Apache por defecto.
- Abrir el navegador para comprobar la página que sirve Apache utilizando SSL.
- Abrir el navegador con el portal de administración PhpMyAdmin para administrar del SGBD MariaDB.
- Mostrar los puertos TCP utilizados en el sistema.
- Mostrar los puertos TCP disponibles en el sistema.
- Realizar una copia de seguridad de los datos que el usuario ha modificado en su instalación desde que fué instalada.
- Mostrar un resumen compacto de la configuración utilizada en el servidor web Apache.
- Mostrar un resumen compacto de la configuración utilizada por PHP.

## ¿Cual es la contraseña inicial para poder entrar a PhpMyAdmin?

La instalación inicial utiliza el usuario "root" y contraseña "root"

## ¿Como puedo comodamente empezar a servir paginas web utilizando la instalación PHP?

## ¿Como puedo utilizar VirtualHosts?

