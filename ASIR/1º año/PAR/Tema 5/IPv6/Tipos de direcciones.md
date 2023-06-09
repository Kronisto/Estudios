#PAR #TEMA_5 

* **Unicast**: Es la dirección más clásica, se designa 1 interfaz única en *IPv6*. Cualquier paquete que tenga como destino esta dirección se entregará únicamente a la interfaz que posea esta dirección.

* **Enlace Local**: Se utiliza en un *enlace simple* y no debe ser enrutada nunca. Se usa en mecanismos de autoconfiguración, descubrimiento de vecinos, y en redes sin enrutadores. Útil para crear redes temporales. Puede ser utilizada sin un *prefijo global*.

* **Sitio Local**: Contiene información de subred dentro de la dirección. Son enrutadas dentro de un sitio, pero los **enrutadores** no deben enviarlas fuera de éste. Es utilizada sin un *prefijo global*.

* **Anycast**: se trata de designar 1 dirección que puedan poseer varias interfaces (*sobre un mismo dispositivo o sobre dispositivos diferentes*). 1 paquete enviado a una dirección **Anycast** se procesa únicamente por 1 de estas interfaces, a menudo la que está más próxima topológicamente.

* **Multicast**: como en *IPv4*, todo paquete enviado a una dirección de este tipo se recibe y procesa por el conjunto de interfaces que pertenecen a un grupo de difusión designado por esta dirección. Las IP **multicast** se identifican por tener:

	* Octeto más significativo a valor 1 todos sus bits (***FF***).
	
	* Los ***flags*** indican si la dirección de multicast es permanente (valor 0) o temporal (valor 1). En cuanto al alcance, los valores posibles son:

	    * **0**: Reservado
	    
	    * **1**: Nodo-local
	    
	    * **2**: Enlace-local
	    
	    * **3**: Reservado
	    
	    * **4**: Organización-local
	    
	    * **5**: Sitio-local
	    
	    * **6**: Reservado
	    
	    * **7**: Reservado
	    
	    * **8**: Organización-global
	    
	    * **9 - 14**: Reservado
	    
	    * **15**: Administrador-local

	* Siguiente octeto identifica el alcance (***scope***).
	
	* Entre los ámbitos comúnmente implementados tenemos: 
	
		* Nodo (***interfaz***)
		
		* Local (***0x1***)
		
		* Enlace local (***0x2***)
		
		* Sitio local (***0x5***)
		
		* Organización local (***0x8***)
		
		* Global (***0xE***).
		
		* Los siguientes *112 bits* forman el identificador de grupo de multidifusión. Identificadores de grupos definidos tenemos:

			* ***0x1*** dirección de multidifusión para todos los **nodos**
			
			* ***0x2*** dirección de multidifusión para todos los **routers**.

| 8 bits   | 4 bits | 4 bits | 112 bits |
| -------- | ------ | ------ | -------- |
| 11111111 | Flags  | Scope  | ID Grupo |

