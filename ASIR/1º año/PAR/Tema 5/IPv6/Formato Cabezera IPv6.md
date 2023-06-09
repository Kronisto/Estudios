#PAR #TEMA_5 

La cabecera del IPv6 pasa a tener 40 B. También se simplifica con menos campos y con un tamaño fijo.

![[Cabezera IPv6.png]]

* **Versión** (*4*). Versión 6.

* **Clase de tráfico** (*8*): Indica la prioridad del tráfico y se divide en 2 rangos: Control de congestión en origen o sin el.

* **Etiqueta de Flujo** (*20*): Ideado para la gestión de calidad de servicio (QoS) en comunicaciones con requisitos de tiempo real. Actualmente sin uso.

* **Longitud** (*16*): Tamaño de la carga útil, hasta 65 KB, con valor 0 para paquetes de tamaño superior

* **Siguiente Cabecera** (*8*): Indica el protocolo encapsulado en la carga de datos. El valor es compatible con IPv4.

* **Limite de saltos** (*8*): Reemplazo del *TTL* de los paquetes IPv4.

* **Direcciones Origen** (*128*) y **Destino** (*128*)