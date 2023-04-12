#PAR #Arquitectura_redes #Modelo_OSI

Define los protocolos que usarán las aplicaciones y procesos de usuario.

Suministra servicios de red a las aplicaciones del usuario. Difiere de las demás capas debido a que no proporciona servicios a ninguna otra [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|capa OSI]], sino solamente a aplicaciones que se encuentran fuera del [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|capa OSI]].

Proporciona la interfaz entre las aplicaciones que utilizamos para comunicarnos y la red subyacente en la cual se transmiten los mensajes. Los protocolos de __capa de aplicación__ se utilizan para intercambiar los datos entre los programas que se ejecutan en los ___hosts___ de origen y destino.

El usuario normalmente no interactúa directamente con el nivel de aplicación. Interactua con programas que a su vez interactúan con el nivel de aplicación pero ocultando la complejidad subyacente. 

*Ejemplo* --> un usuario no manda una petición «GET /index.html HTTP/1.0» para conseguir una página en html, ni lee directamente el código html/xml o cuando chateamos con el ___Mensajero Instantáneo___, no es necesario que codifiquemos la información y los datos del destinatario para entregarla a la [[6 - Presentación|capa de Presentación]] para que realice el envío del paquete.

## Protocolos

* __HTTP__ (___HyperText Transfer Protocol___) para acceso a páginas web.

* __HTTPS__ (___Hypertext Transfer Protocol Secure___) .

* __FTP__ (___File Transfer Protocol___).

* __DNS__ (___Domain Name Service___).

* __DHCP__ (___Dynamic Host Configuration Protocol___).

* __POP__ (___Post Office Protocol___) para recuperación de correo electrónico.

* __SMTP__ (___Simple Mail Transport Protocol___) para envío de correo electrónico.

* __SSH__ (___Secure SHell___)

* __TELNET__ para acceder a equipos remotos.

* __TFTP__ (___Trival File Transfer Protocol___).