#PAR #TEMA_5 

Las aplicaciones y procesos de la capa de aplicación obtienen el servicio TCP haciendo que el transmisor y el receptor creen puntos terminales denominados sockets. Cada socket es un nº de 48 bits compuesto por una IP del host y un nº de 16 bits local a ese host llamado puerto.

Podemos definir un puerto como la porción de un socket que especifica el canal lógico de I/O por el que se asocian datos a un proceso.

Para obtener servicio TCP, es necesario establecer explícitamente una conexión entre un socket del emisor y un socket del receptor. Un socket puede usarse para varias conexiones al mismo tiempo, o varias conexiones pueden terminar en el mismo socket.

Los nº de puerto por debajo del 1024 se llaman well known ports y se reservan para servicios estándar.

Una conexión TCP es una corriente de bytes, no de mensajes. Ejem: un transmisor hace 4 escrituras de 512 bytes, al receptor pueden llegar 4 bloques de 512 bytes, 2 bloques de 1024 bytes, un bloque de 2048 bytes, o cualquier otra combinación.