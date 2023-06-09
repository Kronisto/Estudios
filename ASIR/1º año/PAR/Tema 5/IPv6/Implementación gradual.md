#PAR #TEMA_5 

*IPv4* e *IPv6* conviviran durante un periodo de tiempo bastante largo, mientras todas las redes van migrando al nuevo estándar. Para proporcionar conectividad entre ambas redes se han diseñado diversas tecnologías:

* **Pila dual**: Se implementan ambos protocolos en cada nodo de la red. Conlleva un mayor costo de recursos al tener que manejar el x2 de direcciones, [[Tabla de encaminamiento|tablas de encaminamiento]] y procesos de [[Protocolo de Encaminamiento|encaminamiento]]. Pero está ampliamente extendido y es fácil de desplegar.

* **Tunelización**: Se encapsula el [[Direccionamiento IPv6|protocolo IPv6]] dentro de paquetes *IPv4*. Es un mecanismo sencillo y efectivo que permite conectar redes *IPv6* mediante la red *IPv4*, con una ligera penalización de rendimiento el x2 de cabeceras de cada paquete.

* **Traducción**: 1 nodo *IPv4* desea comunicarse con 1 nodo *IPv6*, necesita un proceso de compatibilización de los paquetes mediante diversos mecanismos de traducción. Es más compleja y costosa que la ***tunelización***, pudiendo ser difícil o imposible traducir todas las posibilidades que ofrece un *protocolo*, pero a cambio proporciona mejor rendimiento de la línea de comunicaciones que la tunelización al no x2 las cabeceras.