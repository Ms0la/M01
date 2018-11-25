### ¿Que es Partprobe y para que sirve?
Partprobe es un comando de Linux cuya función es volver a leer la tabla de particiones del dispositivo de almacenamiento seleccionado. Esto es útil en el contexto de que hayamos añadido una partición a un disco que ya contenia particiones, en cuyo caso se nos avisará de que el disco está ocupado (busy). 

##### ¿Como se usa el comando?

La sintaxis del comando vendría siendo la siguiente:

**sudo partprobe /dev/sda**

Donde sda es el nombre del dispositivo del cual quieres efectuar la relectura de la tabla de particiones

También se puede usar la opción -s para que te muestre en el output la cantidad de particiones por orden:

**sudo partprobe -s /dev/sda**
>/dev/sda: gpt partitions 1 2 3 4 7 5 6

