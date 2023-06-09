#PAR #TEMA_5

Un datagrama IP consta de una parte cabecera y otra de datos. La cabecera tiene el siguiente formato:

![[Cabezera IPv4.png]]

* **Versión (*4*)**. Registro de v. del protocolo a que pertenece el datagrama. Permite la convivencia de paquetes de distintas v. del protocolo en la red, ya que cada 1 es tratado correctamente en destino según la v. de origen.

* **IHL (*Internet Header Length*) (*4*)**. Longitud de la cabecera en palabras de 32 bits. Valor máx de 15, permite cabeceras de hasta 60 bytes (*20 ==obligatorias== y 40 ==opcionales==*).

* **Tipo de servicio (*8*)**. El enrutador puede escojer entre las líneas disponibles, la más adecuada. En la práctica lo ignoran. 

* **Longitud total (*16*)**. ==Longitud del datagrama== (cabecera y datos) en octetos (max 65535). 

* **Identificación (*16*)**. Valor que identifica el datagrama. Todos los fragmentos de un datagrama llevan el mismo valor en su campo identificación y serán identificados como fragmentos que deben reensamblarse. 

* **Flags (*3*)**. 3 bits:

	* **1º bit** no se utiliza y debe estar fijo a valor 0
	
	* **2º bit** se denomina bandera de no fragmentar **DF** (***D**on't **F**ragment*) e indica que el datagrama no debe fragmentarse para alcanzar el destino
	
	* **3º bit** es la bandera de más fragmentos **MF** (***M**ore **F**ragments*), lleva activado cada fragmento de 1 datagrama para indicar que no esta completo, excepto el último. 

* **Desplazamiento (*13*)**. Indica la posición del fragmento dentro del datagrama completo. 

* **TTL (*Time To Live*) (*8*)**. Tiempo en seg que le queda de vida al paquete. Su valor se decrementa cada salto de un *enrutador*. Evitar que paquetes perdidos circulen por la red indefinidamente. Cuando un *enrutador* pone a 0 el campo **TTL**, borra el paquete y crea un mensaje de control destinado al emisor del paquete drenado, para informarle del suceso. 

* **Protocolo (*8*)**. Protocolo de transporte que ha generado el datagrama; ejem TCP o UDP y algunos otros. Indica a que parte de la capa de transporte hay que entregar el datagrama, una vez reconstruido. 

* **CRC (*cyclic redundancy check*) (*16*)** comprobar los datos de la cabecera, sin incluir el resto del datagrama. Cada vez que se cambia un campo se recalcula y verifica. 

* **IP origen (*32*)** y **IP destino (*32*)** del datagrama. 

* **Relleno (*Variable*)**. bits 0 que se pueden añadir al final, para que la cabecera sea múltiplo de 32 bits. 

* **Opciones (*Variable*)**. Permite agregar información no contemplada en el diseño original del protocolo, para evitar incluir campos en la cabecera que se utilizan raramente, y para que los desarrolladores experimenten.

Las opciones son de longitud variable, y están identificadas por el 1º byte. Existen 5 opciones: 

* **Seguridad**: Indica lo secreta que es la información. Evita enrutar a través de redes inseguras, en la práctica se ignora su valor. 

* **Enrutamiento estricto desde origen**: Establece la secuencia **IP** que debe seguirse obligatoriamente para llegar al destino. 

* **Enrutamiento libre desde origen**: Establece los nodos **IP** por los que debe pasar el paquete y en ese mismo orden, pero se permite intercalar otros *enrutadores*. 

* **Registrar ruta**: Agrega al campo opción las **IP** de todos los *enrutadores* por los que pasa el paquete.

* **Marca de tiempo**: Como registrar ruta pero agregando además una marca de tiempo de 32 bits por cada *enrutador*