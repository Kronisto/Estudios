#PAR #Arquitectura_redes 

El modelo de referencia [[ASIR/1º año/PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|OSI]] y la arquitectura [[ASIR/1º año/PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo TCP-IP/Concepto|TCP/IP]] tienen mucho en común. Ambos se basan en el concepto de un gran nº de protocolos independientes.

También la funcionalidad de las capas es muy similar. _Ejemplo_ --> en ambos modelos las capas por encima de la de transporte, incluida ésta, están ahí para prestar un servicio de transporte de extremo a extremo, independiente de la red, a los procesos que deseen comunicarse. Estas capas forman el proveedor de transporte. También en ambos modelos, las capas encima de la de transporte son usuarios del servicio de transporte orientados a aplicaciones. 

A pesar de estas similitudes fundamentales, los 2 modelos tienen también muchas diferencias. 

1) En el [[ASIR/1º año/PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|modelo OSI]], 3 conceptos son fundamentales: _servicios_, _interfaces_, y _protocolos_. Es probable que la contribución más importante del [[ASIR/1º año/PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|modelo OSI]] sea hacer explícita la distinción entre estos 3 conceptos. Cada capa presta algunos servicios a la capa que se encuentra sobre ella. 
	
	* __Interfaz__ --> les dice a los procesos de la capa de arriba cómo acceder a ella. Especifica cuáles son los parámetros y qué resultados esperar. 
	
	* los protocolos pares que se usan en una capa son asunto de la capa. 
	
	* La __arquitectura__ TCP/IP originalmente no distinguía de forma clara entre servicio, interfaz y protocolo, aunque se ha tratado de reajustarlo después a fin de hacerlo más parecido a OSI. 

2) El modelo de referencia OSI se desarrolló antes de que se inventaran los protocolos. Este orden significa que el modelo no se orientó hacia un conjunto específico de protocolos, lo cual lo convirtió en algo muy general. El lado malo de este orden es que los diseñadores no tenían mucha experiencia con el asunto y no supieron bien qué funcionalidad poner en qué capa. Lo contrario sucedió con TCP/IP: 1º llegaron los protocolos, y el modelo fue en realidad sólo una descripción de los protocolos existentes. 

3) Una diferencia obvia entre los 2 modelos es la cantidad de capas: el modelo OSI tiene 7 capas y TCP/IP 4. Ambos tienen capas de (inter)red, de transporte y de aplicación, pero las otras capas son diferentes. 

4) El modelo OSI apoya la comunicación tanto no orientada a conexión como la orientada a la conexión en la capa de red, pero en la capa de transporte donde es más importante (_porque el servicio de transporte es visible a los usuarios_) lo hace únicamente con la comunicación orientada a la conexión. La arquitectura TCP/IP sólo tiene un modo en la capa de red (_no orientado a conexión_) pero apoya ambos modos en la capa de transporte, con lo que ofrece una alternativa a los usuarios. 