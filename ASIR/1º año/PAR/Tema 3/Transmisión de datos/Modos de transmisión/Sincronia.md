Para que **emisor** y **receptor** se entiendan, ambos deben estar sincronizados. Deben coincidir en el momento de reconocer cuando empieza un bit, cuánto dura, y mantener esa sincronía durante toda la transmisión. 

Si no mantiene la sincronización puede ocurrir que el emisor mande 10.000 bits y el receptor considere haber recibido 9.999 ó 10.001, malogrando la comunicación.

Partiendo de la necesidad de la sincronización, existen 2 modos de proporcionarla. Uno es mandar una señal de reloj, común a ambas estaciones, que vaya marcando los pulsos de inicio de cada bit, y por tanto su duración. 

Otra forma de realizar la sincronización consiste en marcar el inicio de 1 bloque de datos para poner en ese momento en marcha un reloj local que irá señalando las posiciones de inicio de cada bit, durante el tiempo de transmisión del bloque. El tamaño del bloque a transmitir vendrá limitado por la precisión de los relojes empleados en el proceso.
