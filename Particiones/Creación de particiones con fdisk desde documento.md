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

Y procederemos a particionarlo según nuestras nescesidades, para ello haremos uso de las opciones de fdisk que podremos ver con **m**. Por ejemplo, yo quiero particionar el archivo con las reglas de MBR y de tal manera que haya una primaria activa de 100Kib, una primaria NTFS de 70Mib y una extended de 205Mib dentro de la cual habrán dos particiones ext4 de 100Mib y una swap de 5Mib. Para ello seguiré el siguiente patrón:

Para la creación de la tabla de MBR:
> :o :w sudo partprobe /dev/loop0 sudo fdisk /dev/loop0

Para la creación de la primaria activa:
> :n :p :1 : :+100K :a

Para la creación de la primaria de 70Mib:
> :n :p :2 : :+70M

Para la creación de la primaria extended:
> :n :e :3 : :+205M

Para la creación de las lógicas:
> :n :l :5 : :+100M

> :n :l :6 : :+100M

Y para la creación de la swap:
> :n :l :7 : : :t :7 :82




