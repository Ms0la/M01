##Instalación básica de Openbox 

En esta guia vamos a instalar Openbox haciendo uso de los paquetes del repositorio, de tal manera que no se considerará aquí la possibilidad de que no esté añadido en tu repositorio. Para ello ejecutaremos el siguiente comando:
>Sudo apt-get install openbox tint2 obconf (aquí detras podemos escribir los paquetes extra que queremos instalados, en mi caso **tint2** (el panel) y **obconf** (para configurar los temas de las ventanas)

Una vez finalizada la instalación, cerramos la sessión (de tal manera que abra el gestor de login) y buscamos el botón de elección del entorno de escritorio. Lo pulsamos y seleccionamos el Openbox (en caso de que no este allí, prueba a reiniciar el equipo). Tras esto se nos abrirá el openbox sin el panel.

Para configurar el panel deberemos editar el archivo autostart ubicado en **/etc/xdg/openbox/autostart**, para editarlo requeriremos de permisos root, así que deberemos abrirlo desde la terminal o como usuario root en caso de que nos hayamos loggeado como tal en el gestor de login. Yo hice uso de nano para abrirlo, de tal manera que el comando que usé fue el siguiente:
>**sudo nano /etc/xdg/openbox/autostart**

Una vez lo tenemos abierto, es tan fácil como escribir al final del archivo y sin almoadilla (#) lo siguiente:
>**tint2&**

Hecho esto, guardamos el archivo y reiniciamos el Openbox para poder visualizar el panel al fondo de todo. Ahora ya solo queda el paso opcional de añadirle un fondo de pantalla, para ello, buscamos la imagen que queramos y la descargamos. Hecho esto, ejecutamos los siguientes comandos (desde Openbox):
>**sudo apt-get install nitrogen**

>**mkdir /home/(nombre de usuario)/wallpaper**

>**cp /home/(nombre de usuario)/Descargas/(nombre de imagen + extensión) ~/.home/(nombre de usuario)/wallpaper**

>**nitrogen ~/wallpaper**

Y lo configuramos como queremos, para que se abra automáticamente al abrir el Openbox, haremos lo siguiente:
>**nano ~/.config/openbox/autostart.sh**

Así abriremos el archivo, y ya solo restará pegarle al final de este:
>**nitrogen --restore &**

Y ya tendremos el Openbox configurado de forma básica.

<img src="https://drive.google.com/file/d/1Zkata-JwUkwVzIrB5gnoNS0OQ81wNkvr/view?usp=sharing">



