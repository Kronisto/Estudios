Tras la transmisión de un bit, la señal no retorna al valor 0, sino que cuando se transmiten varios 1 seguidos, la señal se mantiene a valor alto durante el tiempo que dure la secuencia.

Es la forma más sencilla de codificar valores binarios mediante voltaje eléctrico. Consiste en mantener constante el nivel de voltaje durante el intervalo de tiempo que dura un bit. Cada lvl de voltaje representa un dígito binario distinto. A éste sistema se le denomina **NRZ-L**.

![[Pasted image 20221202094833.png]]

Es un método sencillo y fácil de implementar, proporciona un aprovechamiento total del [[ASIR/1º año/PAR/Tema 3/Transmisión de datos/Modos de transmisión/Banda ancha/Concepto|ancho de banda]] disponible. Presenta problemas cuando se transmiten grandes secuencias de valores idénticos. Al mantener el voltaje al mismo lvl durante gran cantidad de intervalos de bit, existe la dificultad del sincronismo de los relojes de emisor y receptor, lo que puede provocar errores en el reconocimiento de la secuencia. En definitiva, si existe una transmisión con varios miles de unos consecutivos, es muy difícil evitar errores en el nº de bits detectados, ya que los relojes que van marcando cada tiempo de bit deben ser extraordinariamente precisos.

* Otras variantes de **NRZ** que podemos encontrar:

	* ==NRZ-I==: Invierte los valores para “0” y “1”
	
	* ==NRZ Diferencial==: El voltaje para representar un valor depende del voltaje que tenga en el intervalo anterior y del valor que queramos representar. Existen 2 posibilidades:
	
		* ==NRZ-M==: Cambia el lvl de voltaje cuando el valor es un “1” y lo mantiene cuando es un “0”
		
		* ==NRZ-S==: Cambia el lvl de voltaje cuando el valor es un “0” y lo mantiene cuando es un “1”

![[Pasted image 20221202094754.png]]
