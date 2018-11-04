## Como ejecutar comandos en segundo plano

Ejecutar comandos en segundo plano sirve para ejecutar un comando sin que la salida de datos no impida hacer uso de la terminal, para hacerlo hay dos maneras:

-Añadiendo un & al final del comando:
> htop &

-Ejecutando el comando en primer plano y pausándolo con ctrl+z para acto seguido ejecutar el comando bg, que sirve para ejecutar en segundo plano un comando etiquetado previamente por el terminal con un número:
> htop (ctrl +z)

>bg 1

Y para volver a usar el comando en primer plano se usa el comando fg (número de comando en segundo plano):
>fg 1
