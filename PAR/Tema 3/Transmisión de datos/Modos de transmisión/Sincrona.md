**armonicos fourier** Los bits se envían a ritmo constante. No utilizan marcación de inicio y fin de cada byte. La sincronización puede hacerse mediante una señal de reloj, o bien mediante secuencias de marcación de los límites de un bloque de datos de transmisión (*compuesto de muchos bytes*).

* ==En caso de utilizar sincronización mediante reloj== se necesita una señal adicional a la de los datos, que se encargue de mantener la cadencia del envío, con el fin de mantener la sincronización de emisor y **receptor**. A esta señal se le denomina seña de reloj y puede ser generada por el **emisor** o el **receptor**.

* ==En caso de utilizar sincronismo mediante bloques== de información, la información a transmitir se divide en trozos (*tramas*), son señalizadas con bits indicadores, generalmente indiciando tanto su inicio como su final.

* Dependiendo de cómo se trate el contenido de los datos, si a lvl de carácter o de bit, distinguimos:

	* ==Transmisión síncrona orientada a carácter==: El bloque de datos se trata como una secuencia de caracteres. Toda la información de control está en forma de caracteres. El bloque debe ser tener un nº de bits múltiplo exacto del tamaño de un carácter.
	
	* ==Transmisión síncrona orientada a bit==: El bloque de datos se trata como una secuencia de bits. Ni la información de control, ni la de datos necesita tener sentido por caracteres. El tamaño del bloque puede ser cualquier valor de bits.