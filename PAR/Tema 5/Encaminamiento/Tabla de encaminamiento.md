#PAR #TEMA_5 

Será distinta según el **router** de que se trate y de su protocolo de enrutamiento, pero todas tienen la misma estructura básica de tabla con las siguientes informaciones: 

* **Red de destino**: Identificación de un rango de **IP’s** y se puede especificar bien con 1 **IP** y tomando la mascara predefinida **RIP** (***R**outing **I**nformation **P**rotocol*) o con la **IP** de la red junto con su correspondiente máscara (*RIPv2*). Es el criterio de búsqueda con el que se compara la ==IP de destino== de un paquete cuando el encaminador trata de determinar la línea por la que enviarlo. 

* **Línea de salida**: Identificación de la línea de datos del **encaminador** la cual nos acerca al destino de las **IP** que define la entrada de la tabla “**red de destino**”. Hay diversas formas de especificarla.

	* Especificar la IP que el encaminador tiene definida para dicha línea (*un encaminador debe tener al menos 1 **IP** distinta asignada a cada línea*). 

	* Especificar la identificación física del interfaz según el OS del router (*Cisco utiliza un identificador de tipo y un nº de orden “Serial0” o “Ethernet1”*).

	* Indicar la IP del siguiente enrutador al que se debe reenviar el paquete. De cualquier modo, el dato “línea” de salida sirve para identificar por dónde enviar el paquete. 

* **Métrica**: Medida de la calidad de la ruta. Nº que se utiliza para comparar distintas entradas de la tabla y nos permite escoger 1 de ellas. Trata de sintetizar en un nº la medida de la “*calidad*” de la ruta que parte de esa línea hasta la red de destino. Cómo se calcula la métrica y qué valores puede tener, depende del protocolo de **enrutamiento** utilizado. 

	* *Ejem*: En **RIP**, la métrica cuenta el nº de encaminadores que se encuentran en la ruta al destino  y su longitud es de 4 bits pudiendo representar un valor entre 0 y 15. 