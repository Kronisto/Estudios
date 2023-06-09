#PAR #TEMA_5 

Establecen cómo son las **[[Tabla de encaminamiento]]**, qué datos contienen y cómo se obtienen, cómo se consultan, qué información pueden contener y cómo se decide el camino a escoger en base a toda esa información. 

**Objetivo** --> el paquete es reenviado por la línea más adecuada en cada encaminador de la subred y por tanto acabe llegando correctamente al destino. 

En una **[[Tabla de encaminamiento]]** puede haber más de un camino para llegar a un mismo destino. Este ***protocolo*** establece cuántas alternativas puede existir y cómo se tratan. 

Algunos de los **protocolos de enrutamiento** que podemos encontrar con más frecuencia en Internet son: 

* **RIP** (***R**outing **I**nformation **P**rotocol*): Estándar de Internet. Protocolo antiguo con diversas carencias y limitaciones. La métrica indica el nº de saltos hasta llegar al destino siempre que sea < 15 (*15 significa destino inalcanzable*). No comunica las máscaras de red ni las usa para la **[[Tabla de encaminamiento]]** por lo que no permite **[[Subnetting (VLSM)]]** ni **[[Supernetting (CIDR)]]**.

* **RIPv2**: Actualización de ***RIP***, añade la máscara de red a la **[[Tabla de encaminamiento]]**, permitiendo el uso de **[[Subnetting (VLSM)]]** y **[[Supernetting (CIDR)]]**.

* **OSPF** (***O**pen **S**hortest **P**ath **F**irst*). Protocolo avanzado que calcula las mejores rutas y las distribuye por la red. Estándar de Internet desarrolado por el ***IETF*** .

* **IGRP** (***I**nterior **G**ateway **R**outing **P**rotocol*). Propietario Cisco. Más avanzado que ***RIP***, utiliza una métrica donde se calcula la calidad de la ruta en base a varios parámetros como retardo, capacidad, carga, fiabilidad. No difunde información de las máscaras ni permite **[[Subnetting (VLSM)]]** y **[[Supernetting (CIDR)]]**.

* **EIGRP** (***E**nhanced **I**nterior **G**ateway **R**outing **P**rotocol*). Propietario Cisco. Contempla la difusión de máscaras con las rutas, mejora el cálculo de la métrica y evita congestionamientos con balanceo de carga entre rutas alternativas. 