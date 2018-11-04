## Contenido MBR
El sistema de particiones MBR contiene:

**-Tabla de particiones (64 bytes):** 

*Contiene información sobre el disco*: 

El contiene información sobre las particiones de la unidad de memoria, sobre su formato, ubicación en el disco, el tipo de partición que es y sobre su tamaño.

**-Gestor de arranque (446 bytes):**

*Es una parte del gestor de arranque instalada en MBR que se encarga de copiar el resto del gestor de arranque en la memoria RAM y de cederle el control a dicha copia*:

**-Firma de disco(2 bytes):**

*Se encarga de identificar la unidad para diferenciarla de otras*

**Así que se puede afirmar que la firma de disco y la tabla de particiones son archivos con información y el gestor de arranque es un software que se sirve de dichos para arrancar el sistema operativo**
