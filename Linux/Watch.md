## ¿Que es watch y para que sirve?

Watch es un comando de Linux que sirve para ejecutar constantemente un programa y mostrar su salida de datos, de tal manera que esta se actualiza constantemente. Este comando tiene dos opciones: Difference y Interval.

La opción Difference sirve para destacar las diferencias de la salida de un programa al ser ejecutado y se ejecuta añadiendo un **-d** al final del comando.

La opción Interval sirve para gestionar el intervalo de actualización y viene configurado por defecto en 2 segundos, esta opción se ejecuta añadiendo un **-n** al final del comando. Un ejemplo de su uso sería escribir el comando así para que se actualice la salida de datos cada segundo:
> Watch -n 1 "nombre del programa"
