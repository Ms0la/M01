### Guia de fdisk

Para usar fdsik en linux (suponiendo que lo tengamos instalado) debemos ejecutarlo con permisos root, como es possible que lo abramos varias veces, lo mas recomendable es loggearte como root (**su - o sudo su**), ya que es mas rápido que escribir todo el rato **sudo fdisk**.

###### Crear una partición


Lo primero que haremos sera hacer un **fdisk -l** para ver las particiones que hay en el disco y saber de cuanto espacio disponemos, que nunca biene mal. Hecho esto, ejecutaremos **fdisk /dev/sda** para abrir el disco duro donde queremos ubicar la partición. 

Tras estos, se nos abrirá el disco y nos pedirá una orden, admeás nos dirá que ejecutemos la orden m si nescessitamos ayuda. En vez de eso, ejecutaremos la orden n para añadir una nueva partición. En caso de que la vayamos a crear con un disco MBR, nos dirá si queremos crear una primaria normal (p) o una partición primaria extendida (e), seleccionaremos la primaria normal. 

Nos pedirá el número de la partición y lo dejaremos en el número predeterminado, luego nos pedirá el primer y último cilindro y escribiremos allí el tamaño que queremos para la partición (Ej: 10K). Ahora volveremos al menú de fdisk y escribiremos w para guardar los cambios. Finalmente, escribiremos en la terminal **partprobe** para que se vuelva a leer la tabla de particiones y ejecutaremos **fdisk -l** para ver si la nueva partición està allí.
