#PAR #Arquitectura_redes

* Características: 
	
	* Las funciones individuales a realizar son más simples, facilita la implantación de cada lvl (_por separado_).
	
	* Para cada lvl se define un servicio, construido sobre los servicios de lvl inferiores y que mejora los anteriores gracias a la funcionalidad aportada por el protocolo de ese lvl.

Los __protocolos__ se establecen entre lvl gemelos (_peer protocols_).

Los lvl son independientes, es posible sustituir el __protocolo__ de un determinado lvl por otro, siempre que el servicio no varié.

El propósito de cada capa es ofrecer ciertos servicios a las capas superiores de modo que no tengan que ocuparse del detalle de la implementación real de los servicios. 

## Protocolo 

Acuerdo entre las partes que se comunican sobre cómo va a proceder la comunicación. _Ejemplo:_ La capa n de una máquina lleva a cabo una conversación con la capa n de otra. Las reglas y convenciones que se siguen en esta conversación.

En esta imagen, se ve 1 red de 5 capas. Las entidades que comprenden las capas correspondientes en las diferentes máquinas se denominan __pares__ (_las que se comunican usando el protocolo de su capa_).

![[División de niveles.png]]

Los datos no se transfieren directamente de la capa ___n___ de una máquina a la capa ___n___ de otra. Cada capa pasa datos e información de __control__ a la capa que está inmediatamente debajo de ella, hasta llegar a la capa más baja. 

1. La __información de control__ indica a la capa inferior ___n-1___ lo que debe hacer con los datos. 
 
2. Despues construye una __cabecera de protocolo__ ___n-1___ mediante la que realiza las tareas solicitadas y la añade a los datos recibidos. 

3. Cogerá el bloque de información así construido y lo entregará a la capa inferior junto con información de control indicándole que debe hacer con ella (___encapsulamiento de la información___). Bajo la capa 1 está el medio físico a través del cual ocurre la comunicación real.

Entre cada par de capas adyacentes hay una __interfaz__. 

## Interfaz

define qué operaciones y servicios primitivos ofrece la capa inferior a la superior. Las __interfaces__ bien definidas también simplifican el reemplazo de la implementación de una capa con una implementación completamente diferente (_ejemplo, todas las líneas de teléfonos se reemplazan por canales de satélite_), pues todo lo que se requiere de la nueva implementación es que ofrezca a su vecino de arriba exactamente el mismo conjunto de servicios que ofrecía la implementación vieja. 

Ni los detalles de la implementación ni la especificación de las interfaces forman parte de la arquitectura porque se encuentran ocultas dentro de las máquinas y no son visibles desde fuera

## Ejemplo

![[Original.png]]

Cómo proveer la comunicación a la capa superior de la red de 5 capas. 

![[Capa_5.png]]

==Se produce un mensaje ___M___ por un proceso de aplicación que se ejecuta en la== __capa 5__ y se entrega a la __capa 4__ para su transmisión. 

![[Capa_4.png]]

La __capa 4__ coloca un encabezado al principio del mensaje para identificarlo (_encapsulando el mensaje __M__ dentro de una unidad de datos del protocolo de lvl 4_) y pasa el resultado a la __capa 3__. 

![[Capa_3.png]]

El __encabezado__ incluye información de __control__, como nº de secuencia, para que la __capa 4__ ==en la máquina de destino pueda entregar los mensajes en el orden correcto==. En algunas capas, los __encabezados__ contienen también tamaños, horas y otros campos de control. 

En muchas redes no hay límite al tamaño de los mensajes que se transmiten en el protocolo de la __capa 4__, pero casi siempre existe un límite impuesto por el protocolo de la __capa 3__. En consecuencia, la __capa 3__ ==debe dividir los mensajes que le llegan en unidades más pequeñas, paquetes, anexando un encabezado de la __capa 3__ a cada paquete==. En este ejemplo, ___M___ se divide en 2 partes, ___M1___ y ___M2___. 

![[Capa_3.png]]

La __capa 3__ ==decide cuál de las líneas que salen usará y pasa los paquetes== a la __capa 2__.

![[Capa_2.png]]

La __capa 2__ ==no solamente añade un encabezado a cada pieza sino también un apéndice, y entrega la unidad resultante a la== __capa 1__ para su ==transmisión física==. 

En la máquina receptora el mensaje se mueve hacia arriba, de capa en capa, perdiendo los encabezados conforme avanza.