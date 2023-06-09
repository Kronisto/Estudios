#PAR #TEMA_5 

Las máquinas sin unidades de almacenamiento conectadas a una red, no tienen la posibilidad de guardar su IP cuando se apagan. Cuando arrancan, deben usar la red para conectar con un servidor que les indique su *IP*. El protocolo utilizado es el RARP (similar a ARP) definido en el [[rfc 903.pdf|RFC 903]], adaptado del [[ARP|ARP]].

El host que quiere conocer su *IP* envía una **trama RARP de difusión**. Todas las máquinas reciben la trama que contiene el **paquete RARP**, pero sólo los **servidores RARP** contestan.

Debe tenerse en cuenta, que los hosts y el **servidor RARP** están obligados usar la misma red física, pues la única identificación del host es su *MAC*.