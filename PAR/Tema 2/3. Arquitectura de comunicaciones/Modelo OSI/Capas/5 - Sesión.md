#PAR #Arquitectura_redes #Modelo_OSI

Permite a los usuarios de máquinas diferentes establecer sesiones entre ellos. Una sesión permite el transporte ordinario de datos, como lo hace la [[4 - Transporte|capa de transporte]], pero también proporciona servicios mejorados que son útiles en algunas aplicaciones. Se podría usar una sesión para que el usuario se conecte a un sistema remoto de tiempo compartido o para transferir un archivo entre 2 máquinas. 

### Servicios

* ==Manejar el control del diálogo== --> Las sesiones pueden permitir que el tráfico vaya en ambas direcciones al mismo tiempo, o sólo en una dirección a la vez. Si el tráfico puede ir únicamente en un sentido a la vez (_en analogía con una sola vía de ferrocarril_), la __capa de sesión__ puede ayudar a llevar el control de los turnos. 

* ==Sincronización== --> Inserta puntos de verificación en la corriente de datos, de modo que después de cada interrupción sólo se deban repetir los datos que se transfirieron después del último punto de verificación. 
