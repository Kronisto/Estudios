#PAR #TEMA_5 

Un host A desea comunicarse con un host B del que conoce su IP pero no su MAC, envía a la red un paquete ARP con dirección de difusión, en el que pide al nodo con la IP del host B que responda con su MAC. Todos los nodos de la red reciben esta trama y la aceptan, pero sólo el host B responde con su MAC.

Un host quiere comunicarse con otro, antes de enviar el **paquete ARP**, busca en una tabla dinamica (*contiene las IP’s con sus correspondientes **MAC***) para ver si tiene su **MAC**.

Cuando un **paquete ARP** viaja por la red de una máquina a otra, lo hace encapsulado en una trama de lvl de enlace. En la siguiente figura podemos ver un **paquete ARP** encapsulado en una **trama Ethernet**:
| Preámbulo | Destino | Origen | Tipo | Paquete ARP tratado como datos | CRC |
| --------- | ------- | ------ | ---- | ------------------------------ | --- |