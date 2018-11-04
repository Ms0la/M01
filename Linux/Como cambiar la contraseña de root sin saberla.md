Para cambiar la contraseña de root sin saberla en tu Linux, nescessitaras que tu usuario pueda usar comandos como sudo y saberte obviamente la contraseña de tu usuario. Si cumplimos con estos dos fáciles requisitos (ya que el usuario configurado después de la instalación posee permisos para usar sudo por defecto) escribiremos el siguiente comando:
>sudo su

Nos pedirá nuestra contraseña y una vez la hayamos metido, habremos entrado como usuario root. Hecho esto solo hará falta ejecutar el siguiente comando y elegir la nueva contraseña:
>passwd root
