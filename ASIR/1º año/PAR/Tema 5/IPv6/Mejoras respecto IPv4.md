#PAR #TEMA_5 
Campo de direcciones ampliado a 128 bits frente a 32 bits del **IPv4**.

Extensión del tamaño máx. de paquete. Para redes con una [[PALABREJAS#MTU|MTU]] grande, existe la posibilidad de transmitir paquetes de más de 64 kB hasta 4 GB ([[PALABREJAS#Jumbogram|Jumbograms]]).

* **Multidifusión**: No tiene difusión global, pero puede difusión enviando un paquete al grupo de multidifusión “*todos los hosts*” del enlace local.

* **SLAAC** (***S**tate**L**ess **A**ddress **A**uto**C**onfiguration*). Los nodos *IPv6* pueden configurarse a sí mismos automáticamente cuando son conectados a una red ruteada en *IPv6* usando los mensajes de descubrimiento de **routers** de [[ICMP|ICMPv6]].

	* La 1º vez que son conectados a una red, el *nodo* envía una **RS** (***R**outer **S**olicitation*) de enlace-local usando multicast pidiendo los parámetros de configuración; y si los **routers** están configurados para esto, responderán con un **RA** (***R**outer **A**dvertisement*), contiene los parámetros de configuración de capa de red. También puede utilizarse [[¿Qué es el DHCP?|DHCPv6]] o asignación manual para establecer la configuración de red.

* **Mayor flexibilidad en el direccionamiento**: No se tiene la rigidez de las "clases de redes". Los bits de red no están limitados a unos pocos valores, ya no existe **[[Subnetting (VLSM)|VLSM]]** o **[[Supernetting (CIDR)|CIDR]]**.

* **Mejoras de rendimiento en el procesado de paquetes**. Los paquetes *IPv6* simplifican las *cabeceras*, con menos campos, más simples, un tamaño fijo de *cabecera*, y ocupando menos espacio a pesar de que las direcciones son 4 veces más grandes. Un **enrutador** ya no puede fragmentar 1 paquete, sólo se puede fragmentar paquetes desde origen. No se realiza suma de comprobación de las *cabeceras*, se delega todo el control de errores a capas superiores. Todo ello aumenta el rendimiento general del protocolo y reduce el consumo de procesamiento para enrutar paquetes.

* **Seguridad y confidencialidad**. **IPsec** (***I**nternet **P**rotocol **S**ecurity*), pasa a formar parte esencial de *IPv6* proporcionando cifrado y autentificación. En *IPv4* era opcional.