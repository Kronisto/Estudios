* Sin señal de reloj incorporada o externa que vaya marcando los puntos de inicio de los bits. Se envían pequeños bloques de bits (*palabras o caracteres*) que se sincronizan al principio.

* Es necesario un acuerdo en la temporalización a lvl de bit. (*Cuánto dura un bit*) y el uso de relojes locales que tengan suficiente precisión para mantener la **sincronía** hasta el fin del bloque. El bloque puede ser un bit, un byte, o una secuencia de ambos formando una unidad de sincronización.

* La **sincronía** se restaura en cada carácter, lo que origina que una vez fijada la velocidad de transmisión, es un método poco sensible a los problemas ocasionados por la falta de sincronismo.

* Un fallo de sincronismo, afecta como mucho a un carácter, pero no al siguiente, ya que su bit de start, produce una sincronización.

* *Ej*: la comunicación con terminales en modo texto. La unidad de datos utilizada es el byte, que puede ser enviado por el terminal en cualquier momento, marcando su inicio y fin para ser reconocido por el mainframe.

* Este tipo de transmisiones son útiles cuando no hay un flujo de datos constante que transmitir, y cuando las necesidades de [[PAR/Tema 3/Transmisión de datos/Modos de transmisión/Banda ancha/Concepto|ancho de banda]] no son muy grandes. Es un sistema sencillo que desaprovecha bastante el canal