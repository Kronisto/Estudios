#PAR #Arquitectura_redes #Modelo_OSI

Aceptar datos de la [[5 - Sesión|capa de sesión]], dividirlos en unidades más pequeñas si es necesario, pasarlos a la [[3 - Red|capa de red]] y asegurar que todos los pedazos lleguen correctamente al otro extremo. Todo esto se debe hacer de manera eficiente y en forma que aísle a las capas superiores de los cambios inevitables en la tecnología del hardware. 

Determina qué tipo de servicio proporcionará a la [[5 - Sesión| capa de sesión]] y, finalmente, a los usuarios de la red. 

En esta capa se manejan usualmente 2 protocolos, los cuales son el __TCP__ y __UDP__, sus caracteísticas principales son las siguientes:

### TCP vs UPD

TCP|UDP
---|---
Servicio con conexión, establece una sesión entre ambos host| Servicio sin conexión, no necesita establacer sesion entre host
Garantiza la fidelidad de los datos, creando una secuencia de datos para su entrega| No garantiza fidelidad de datos 
Lento, necesita comprobar que el paquete recibido este completo, si no reenviará el tramo faltante para completarlo| Rapido, solo entrega los paquetes en el menor tiempo posible
Comunicación 1 a 1| Comunicaciones de 1 a 1 y de 1 a muchos




