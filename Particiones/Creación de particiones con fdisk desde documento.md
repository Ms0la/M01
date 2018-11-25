### Creación del disco duro virtual y montage de este

Para crear el archivo a particionar usaremos el comando:
> sudo ionice -n4 dd if=/dev/zero of=~/image.sda bs=1024K count=500

Donde **ionice** junto con su opción **-n4** se encargarán de establecer la prioridad de uso de los recursos de entrada y salida, **dd** se encargará de crear el disco junto con sus opciones: **if=/dev/zero** para establecer el contenido del disco, **of=~/image.sda** para elegir la ubicación y el nombre del arachivo, **bs=1024K** para elegir el tamaño de los bloques y **count=500** para elegir la cantidad de bloques.

Y ahora para que el ordenador nos reconozca la imagen creada como un dispositivo de almacenamiento, usaremos:
> **sudo losetup /dev/loop0 ~/image.sda**

Donde losetup configura la lectura del disco y, de las opciones **/dev/loop0** se encargará de establecer el punto donde se montará el disco y su nombre; y **~/image.sda** se encargará de seleccionar la ubicación del archivo y de identificarlo.

### Particiones del disco con fdisk

Ahora abriremos el disco virtual con fdisk:
>fdisk /dev/loop0

Y procederemos a particionarlo según nuestras nescesidades, para ello haremos uso de las opciones de fdisk que podremos ver con **m**. Por ejemplo, yo quiero particionar el archivo de tal manera que haya una primaria activa de 100K, una primaria NTFS de 70M y una extended de 205M dentro de la cual habrán dos particiones ext4 de 100M y una swap de 5M. Para ello seguiré el siguiente patrón:

> :n
 :p
 :1
 :
 :+100M


