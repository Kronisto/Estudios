#PAR #Arquitectura_redes #Modelo_TCP-IP 

* la arquitectura no distingue con claridad los conceptos de servicio, interfaz, y protocolo. 

* No es general en absoluto, y no resulta apropiado para describir cualquier pila de protocolos distinta de [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo TCP-IP/Concepto|TCP/IP]]. _Ejemplo_ --> tratar de describir SNA mediante el [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo TCP-IP/Concepto|modelo TCP/IP]] sería casi imposible. 

* [[4 - Host a red|La capa host a red]] en realidad no es una capa en el sentido normal en que se usa el término en el contexto de los protocolos de capas. Es una interfaz (_entre la red y las capas de enlace de datos_). La distinción entre interfaz y capa es crucial y hay que ser muy minuciosos al respecto. 

* Por último, aunque los protocolos IP y TCP se pensaron y se implementaron con cuidado, muchos otros protocolos se fueron creando conforme surgía la necesidad.

![[Pasted image 20221027083922.png]]