#PAR #Arquitectura_redes

El diálogo entre capas se realiza a través del [[División en niveles|interfaz]] existente entre ellas. 

La comunicación se encuentra normalizada en forma de un sistema de llamadas y respuestas que __[[ASIR/1º año/PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|OSI]]__ denomina ___primitivas___.

* Primitivas fundamentales: (_no todos los servicios necesitan las 4_)
	
	* __.request__ --> Una entidad solicita que un servicio realice un trabajo para ella. 
	
	* __.indication__ --> Una entidad es informada de que ha ocurrido un evento
	
	* __.response__ --> Una entidad responde a un evento.
	
	* __.confirm__ --> Una entidad es informada sobre una solicitud efectuada anteriormente. 

La invocación se realiza del siguiente modo: " _Nombre_del servicio.primitiva_ " 

## Ejemplo

![[Comunicación_capas.png]]