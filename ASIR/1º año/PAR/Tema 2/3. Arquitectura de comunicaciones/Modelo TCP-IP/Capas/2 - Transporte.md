#PAR #Arquitectura_redes #Modelo_TCP-IP

Esta capa se diseñó para permitir que las entidades pares en los nodos de _origen_ y _destino_ lleven a cabo una conversación, lo mismo que en la [[4 - Transporte|capa de transporte OSI]]. Aquí se definieron 2 protocolos de extremo a extremo. 

## TCP (_Transmission Control Protocol_)

Definido en el RFC 793, ==protocolo seguro orientado a la conexión== que permite que una corriente de bytes originada en una máquina se entregue sin errores en cualquier otra máquina de la interred. __TCP__ también se encarga del control de flujo para asegurar que un emisor rápido no pueda abrumar a un receptor lento con más mensajes de los que pueda manejar. 

__TCP__ (_orientado a conexión_) permite establecer una conexión entre 2 puntos terminales en una red informática común que posibilite un intercambio mutuo de datos. En este proceso, cualquier pérdida de datos se detecta y resuelve, por lo que se considera un protocolo fiable. 

Está ahí para garantizar que todos los datos enviados por un ordenador a otro se reciban con éxito, sin errores ni fallos, y en el orden correcto.

Las conexiones __TCP__ suelen ser más lentas que las basadas en __UDP__.

![[Pasted image 20221027083704.png]]

## UDP (_User Datagram Protocol_)

definido en el RFC 768, es un ==protocolo no orientado a conexión y no seguro==, para aplicaciones que no necesitan la asignación de secuencia ni el control de flujo del [[2 - Transporte#TCP (_Transmission Control Protocol_)|TCP]] y que desean utilizar los suyos propios. Este protocolo también se usa ampliamente para consultas de petición y respuesta de una sola ocasión, del tipo __cliente-servidor__, y en aplicaciones en las que la entrega pronta es más importante que la entrega precisa, como las transmisiones de voz o vídeo. 