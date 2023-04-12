#PAR #Arquitectura_redes #Modelo_TCP-IP

Crearon una red de conmutación de paquetes basada en una __capa de interred__ carente de conexiones. Es el eje que mantiene unida toda la arquitectura. Permite que los nodos inyecten paquetes en cualquier red y los hagan viajar de forma independiente a su destino (_que podría estar en una red diferente_), incluso en un orden diferente a aquel en que se enviaron, en cuyo caso corresponde a las capas superiores reordenarlos, si se desea la entrega ordenada. 

El conjunto de protocolos **TCP/IP** es absolutamente independiente del método de acceso, de la codificación de señales y demás detalles que se podrían presentar en esta capa. La tecnología avanza y va proponiendo otras formas de acceso a la red; todas proporcionan conectividad a **IP**

La __capa de interred__ ==define un formato de paquete y protocolo oficial llamado IP== 

Rutea los paquetes, y también evita la congestión. Esta capa es muy parecida en funcionalidad a la [[3 - Red|capa de red OSI]].