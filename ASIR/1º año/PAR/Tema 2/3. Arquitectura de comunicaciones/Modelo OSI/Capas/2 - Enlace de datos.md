#PAR #Arquitectura_redes #Modelo_OSI

Codifica las tramas recibidas desde la [[3 - Red|capa de red]] para su transmisión desde la [[1 - Física|capa física]], controlando el acceso al medio y los posibles errores en la transmisión.

La [[1 - Física|capa física]] solamente acepta y transmite una corriente de bits sin preocuparse por su significado o estructura, esto le corresponde a la ___capa de enlace de datos___ crear y reconocer los límites de las tramas. Añadiendo patrones especiales de bits al principio y al final de la trama. Si estos patrones de bits ocurrieran en los datos por accidente, se debe tener cuidado especial para asegurar que estos patrones no se interpreten incorrectamente como delimitadores de tramas. 

## Características: 

- Añadir patrones de bits al principio y al final de la trama para reconocerla 

* En caso de fallo, este ha de resolverlo

- Evitar que un transmisor veloz sature de datos a un receptor lento. Se debe emplear algún mecanismo de regulación de tráfico para que el transmisor sepa de cuánto es el buffer que tiene el receptor en ese momento. Con frecuencia esta regulación de flujo y el manejo de errores están integrados.

Las redes de difusión tienen una consideración adicional en la ___capa de enlace de datos___: controlar el acceso al canal compartido. En redes de difusión, el problema de repartir el canal para evitar que 2 o más emisores se interfieran se denomina "_el control de acceso al medio_", y se suele abreviar __MAC__ (_Media Access Control_), es crítico en el funcionamiento de las redes de difusión, y puede llegar a ser muy complejo.

Cuando 2 transmisiones coinciden en un medio, las señales que las forman se mezclan y dejan de ser interpretables, la información se pierde. Se dice entonces que se ha producido una colisión entre tramas. Cuando 2 o más dispositivos están conectados a un mismo medio compartido, es necesario que regulen su método de acceso a dicho medio para que sus transmisiones no se mezclen.

Los objetivos de los métodos de acceso al medio son:

* Regular el acceso a un medio compartido para tratar de impedir o reducir al máximo las colisiones entre tramas.

* Utilizar el canal de forma eficiente aprovechando al máximo la capacidad del canal

La capa de enlace de datos realiza 2 servicios básicos:

* Permite a las capas superiores acceder a los medios usando técnicas, como tramas

* Controla cómo los datos se ubican en los medios y son recibidos desde los medios usando técnicas como control de acceso a los medios y detección de errores.

Las formas tradicionales de Ethernet usando este método. __CSMA/Prevención de colisiones__, el dispositivo examina los medios para detectar la presencia de una señal de datos:

Si el medio está libre:

* El dispositivo envía una notificación a través del medio, sobre su intención de utilizarlo.

* El dispositivo luego envía los datos.