#PAR #Arquitectura_redes #Modelo_OSI

_Ejemplo_ --> cómo se realiza el encapsulamiento de la información el [[ASIR/1º año/PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|modelo OSI]], para llegar a transmitir los datos entre el emisor y el receptor de la información. 

![[PDUs.png]]

El proceso remitente tiene algunos datos que quiere enviar al proceso receptor, así que entrega los datos a la [[7 - Aplicación|capa de aplicación]], la cual añade entonces al principio el encabezado de ==aplicación AH== (_puede ser nulo_) y entrega el elemento resultante a la [[6 - Presentación|capa de presentación]]. 

La [[7 - Aplicación|capa de presentación]] puede transformar este elemento de diferentes maneras y posiblemente añadir al principio un encabezado, entregando el resultado a la [[5 - Sesión|capa de sesión]]. Es importante darse cuenta que la capa de presentación no sabe qué porción de los datos entregados a ella por la capa de ==aplicación es la AH==, si existe, y cuáles son en verdad los datos del usuario. 

Este proceso se repite hasta que los datos alcanzan la [[1 - Física|capa física]], donde son transmitidos realmente a la máquina receptora. En esa máquina se retiran los distintos encabezados, 1 por 1, conforme el mensaje se propaga hacia arriba por las capas hasta que por fin llega al proceso receptor. 

La idea clave en todo este proceso es que aunque la transmisión real de los datos es vertical en la figura, cada capa se programa como si fuera horizontal. _Ejemplo_ --> cuando la [[4 - Transporte|capa de transporte]] _emisora_ recibe un mensaje de la [[5 - Sesión|capa de sesión]], le añade un encabezado de transporte y lo envía a la [[4 - Transporte|capa de transporte]] _receptora_. Desde su punto de vista, el hecho de que en realidad debe dirigir el mensaje a la capa de red de su propia máquina es un tecnicismo sin importancia. 

## Ejemplo

Desde lvl superior a inferior

![[AB.gif]] 

Desde lvl inferior a lvl inferior

![[BA.gif]]