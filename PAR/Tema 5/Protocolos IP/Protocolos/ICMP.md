#PAR #TEMA_5 

El [[¿Qué es una IP?|protocolo IP]] proporciona 1 *servicio no orientado a conexión*, y que los mensajes viajen de **router** a **router** hasta alcanzar su destino. El sistema funciona bien si todas las máquinas trabajan adecuadamente y los **routers** están de acuerdo en los *enrutamientos*. En caso contrario, ocurren errores.

Para permitir a las máquinas conectadas a Internet informar sobre errores o circunstancias inesperadas está el **protocolo ICMP** (considerado como parte de IP) definido por el [[rfc 792.pdf|RFC 792]].

Los **mensajes ICMP** viajan en la porción de los datos de los datagramas IP (*también facilitan el control de la congestión*). *Datagrama IP* encapsulando un **mensaje ICMP**:

| Cabezera IP | Mensaje ICMP tratado coma datos |
| ----------- | ------------------------------- |

Algunos de los **mensajes ICMP** más importantes son:

* **Destination Unreachable**: transportar un mensaje que es generado por un enrutador

	* Se envía al host de origen, que recibe el mensaje emitido por el **enrutador** (*Este router considera inalcanzable el destino al que quiere llegar el host*).

	* Se recibe del host de destino, el protocolo que se intentó acceder no está activo en el momento.

* **Time exceeded**: se envía cuando un paquete se descarta cuando su contador es 0. Ocurre cuando hay mucha congestión, los valores de temporización son demasiado bajos, o los paquetes se encuentran dando vueltas en un ciclo.

* **Echo request y reply**: mensaje de control que se envía a un host con la expectativa de recibir un **echo reply**. Es conocido como ***Ping*** (*utilidad del protocolo ICMP, subprotocolo de IP*). Todo host debe responder al **echo request** con un **echo reply** que contenga exactamente los mismos datos que el 1º.

* **Redirect**: Se usa cuando un **router** se da cuenta de que 1 paquete parece estar mal enrutado, de forma que el **router** informa al transmisor del posible error.
