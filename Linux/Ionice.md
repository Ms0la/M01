## ¿Que es el Ionice y para que sirve?

Ionice es un comando de Linux que sirve para gestionar la prioridad de acceso a los recursos de entrada y salida de un programa, condicionando su acceso al disco duro dependiendo de la condición del ordenador. Con este comando se puede assignar niveles de prioridad (dentro de la classe de prioridad assignada) del 0 al 7, siendo el 0 el mas alto y el 7 el mas bajo con el comando **ionice -n0**; también se puede assignar 3 clases al programa, siendo la classe 1 la mas baja (solo le otorgará acceso a los recursos cuando no haya otros programas que los estén usando) y 3 la mas alta (se le otorgará acceso a los recursos tan pronto como los pida), esta función se usa con el comando **ionice -c3**. La classe que viene predeterminada es la 2.

De acuerdo a lo anterior, si usamos el comando **ionice -c3 -n0** el programa que ejecutamos tendrá la máxima prioridad en los recursos del disco.
