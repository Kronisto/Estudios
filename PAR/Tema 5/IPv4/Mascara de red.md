#PAR #TEMA_5 

==Dato obligatorio==. Secuencia de 32 bits en la se pone a ==“1”== las posiciones correspondientes a **identificación de la red** y a ==“0”== todos los bits que corresponden a la **dirección del host**, y se interpreta todo como si fuera una **IP** con 4 cifras decimales separadas por puntos. 

Otra forma de especificarla consiste en indicar al final de la **IP** el nº de bits que corresponden a la red separado por el carácter “/”. Se le denomina la ==notación prefijo para la máscara de red==. 

![[Mascara de red.png]]

Para un **host**, la **máscara de red** define todas las **IP** de los equipos con los que se puede comunicar el **host** sin intervención de un **enrutador**. Si un **host** debe enviar un paquete a una **IP**, realiza una multiplicación binaria (“**and**”) con el valor de la máscara y el resultado lo compara con la **dirección LAN**. Si coincide, se trata de una **IP** ==local==, y puede ser enviada sin problemas por el interfaz. Si no coincide, se trata de una **IP** no alcanzable localmente y el paquete será enviado al **enrutador** para que lo encamine a su destino. 