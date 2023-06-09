El IEEE ha definido un protocolo que puede operar por encima de todos los protocolos de LAN y MAN de la familia 802. 

Esconde las diferencias entre los distintos tipos de redes 802, proporcionando un formato único y una interfaz con la
[[3 - Red|capa de red]]. Este formato, interfaz y protocolo están basados estrechamente en [[ASIR/1º año/PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|OSI]].

El **LLC** forma la mitad superior de la [[2 - Enlace de datos|capa de enlace de datos]], con la [[2.1 - Control de Acceso al Medio (MAC)|subcapa de MAC]] por debajo de él.

==Uso típico== --> la [[3 - Red|capa de red]] de la máquina transmisora pasa un paquete al **LLC** usando las primitivas de acceso del **LLC**. La subcapa **LLC** entonces agrega una cabecera **LLC** que contiene los nº de secuencia y acuse. La estructura resultante se introduce entonces en el campo de carga útil de un marco 802.x y se transmite. En el receptor ocurre el proceso inverso.

El **LLC** proporciona 3 servicios diferentes:

1. Servicio no confiable de datagramas.
2. Servicio reconocido de datagramas.
3. Servicio confiable orientado a conexión.

![[Pasted image 20221107093827.png]]