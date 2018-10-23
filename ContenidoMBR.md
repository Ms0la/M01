## Contenido MBR
El sistema de particiones MBR contiene:

**-Tabla de particiones:** 

*Contiene información sobre la partición/disco*: 

El formato, el tamaño, el sector de inicio, si es arrancable o no y en caso del disco, sobre las particiones

**-Master Boot Code:**

*Cuyas funciones son*:

-Escanear la tabla de particiones para hallar la partición activa

-Encontrar el sector inicial de la partición activa

-Cargar una copia del sector de arranque (donde se contiene el gestor de arranque) en la memoria RAM

-Transferir el control al sector de arranque que acaba de copiar en la memoria RAM

**-Firma de disco:**

*Cuya función es marcar el disco para poder distingirlo de otros instalados*

**Así que se puede afirmar que la firma de disco y la tabla de particiones contienen información y el master boot code se encarga de usar esa información para arrancar el sistema operativo**
