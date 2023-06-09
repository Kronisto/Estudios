#PAR #TEMA_5 

Algunas **IP** se reservan para usos específicos y no pueden ser asignadas a un **host** en **Internet**. Sirven para poder asignar libremente **IP** en una **LAN** que no serán propagadas a **Internet**. 

* 0.0.0.0 es usada por los hosts al arrancar, pero no se utiliza después. 

* La IP con todos los bits a 1 permite la difusión sobre LAN (broadcast)  Las IP que incluyan un identificador de red y los bits del host a 1, permiten enviar paquetes de difusión a redes remotas.

* 127.xx.yy.zz están reservadas para pruebas de realimentación, los paquetes enviados a esa IP se procesan localmente como si fueran de entrada. 

* La [[rfc 1918.pdf|rfc 1918]] establece que las IP comprendidas entre los siguientes valores son IP privadas:
	* *10.0.0.0 - 10.255.255.255*
	* *172.16.0.0 - 172.31.255.255*
	* *192.168.0.0 - 192.168.255.255*
