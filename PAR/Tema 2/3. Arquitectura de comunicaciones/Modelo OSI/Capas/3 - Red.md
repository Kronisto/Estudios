#PAR #Arquitectura_redes #Modelo_OSI

Provee servicios para intercambiar secciones de datos individuales a través de la red entre dispositivos finales identificados, colocando dirección de origen y de destino de los datos. Para realizar este transporte de extremo a extremo, esta capa tiene 4 procesos básicos:

## Direccionamiento

1º, la capa de red debe proporcionar un mecanismo para direccionar estos dispositivos finales. Si las secciones individuales de datos deben dirigirse a un dispositivo final, este dispositivo debe tener una dirección única. En una red IPv4, cuando se agrega esta dirección a un dispositivo, al dispositivo se le llama ___host___. 

## Encapsulación

Debe proporcionar ___encapsulación___. Los dispositivos no deben ser identificados sólo con una dirección; las secciones individuales, las [[Interfaz entre capas y encapsulamiento#PDU (_Protocol Data Unit_)|PDU]] de la capa de red, deben, además, contener estas direcciones. 

Durante el proceso de ___encapsulación___, la capa 3 recibe la [[Interfaz entre capas y encapsulamiento#PDU (_Protocol Data Unit_)|PDU]] de la capa 4 y agrega un encabezado o etiqueta de capa 3 para crear la [[Interfaz entre capas y encapsulamiento#PDU (_Protocol Data Unit_)|PDU]] de la capa 3. Cuando nos referimos a la capa de red, denominamos paquete a esta [[Interfaz entre capas y encapsulamiento#PDU (_Protocol Data Unit_)|PDU]]. Cuando se crea un paquete, el encabezado debe contener, entre otra información, la dirección del host hacia el cual se lo está enviando. 

## Enrutamiento

Debe proporcionar los servicios para dirigir estos paquetes a su ___host___ de destino. Los host de origen y destino no siempre están conectados a la misma red. 

El paquete podría recorrer muchas redes diferentes. A lo largo de la ruta, cada paquete debe ser guiado a través de la red para que llegue a su destino final. Los dispositivos intermediarios que conectan las redes son los routers. La función del router es seleccionar las rutas y dirigir paquetes hacia su destino. Este proceso se conoce como enrutamiento.

## Desencapsulación

Finalmente, el paquete llega al host de destino y es procesado en la capa 3. El ___host___ examina la dirección de destino para verificar que el paquete fue direccionado a este dispositivo. Si la dirección es correcta, el paquete es desencapsulado por la capa de red y la [[Interfaz entre capas y encapsulamiento#PDU (_Protocol Data Unit_)|PDU]] de la capa 4 contenida en el paquete pasa hasta el servicio adecuado en la capa de ___Transporte___. 

Si en la subred se encuentran presentes demasiados paquetes a la vez, se estorbarán mutuamente, formando cuellos de botella. El control de tal congestión pertenece también a la capa de red. 

En esta capa son utilizadas las __IP__, ya que es el medio de comunicación por la cual se comunicara nuestro enrutador con Internet, existen 2 v. de __IP__ (_Protocolo de Internet_), la ___IPv4___ y la ___IPv6___. Las limitaciones de las direcciones son de:
 
* __Direcciones IPv4:__ 4,294,967,296 direcciones.

* __Direcciones IPv6__: muchas más direcciones.