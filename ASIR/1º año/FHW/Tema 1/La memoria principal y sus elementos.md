![[Pasted image 20221201214806.png]]

Capaz de retener o almacenar datos e instrucciones que son accesibles en cualquier
momento.

Es el dispositivo electrónico en el que están situadas los datos o instrucciones que manipulará la **ALU**, o los resultados que obtengan de estos tratamientos.

Tiene una capacidad limitada. Por ello y por otros factores, esta memoria se complementa con la **memoria externa** o **memoria secundaria**.

La memoria secundaria es un dispositivo que permite guardar grandes cantidades de información durante periodos generalmente
largos de tiempo.

La memoria principal está formada por chips de silicio. Los chips son dispositivos electrónicos formados por circuitos integrados.

Un circuito integrado es un conjunto de componentes electrónicos con funciones determinadas. Hay miles de componentes electrónicos en una integración en miniatura.

La memoria está formada por celdas o posiciones de memoria numeradas de forma consecutiva, que tienen la capacidad de retener la información mientras el ordenador está conectado a una fuente de energía eléctrica.

Cada celda tiene un nombre que se llama posición de memoria y un identificador o número de orden llamado dirección de memoria.

![[Pasted image 20221201214840.png]]

Celda de la memoria

Cada posición de la memoria está formada por dispositivos electrónicos de base binaria, de modo que, en cada instante, cada 1 puede adoptar uno de los 2 estados binarios: on para representar el 1 binario, y off para representar el 0 binario.

Como consecuencia de todo esto, el conjunto completo de los dispositivos de dos estados que forma cada posición de la memoria principal proporciona un método para codificar los datos de una forma similar al de una lámpara encendido o apagado.

Cada posición de una misma memoria tiene la misma cantidad determinada de bits (por ejemplo, 8 bits, 16 bits, 32 bits ...). Ese tamaño es la palabra.

La memoria principal dispone de los siguientes elementos para llevar a cabo sus
funciones:

* Registro de dirección de memoria (MAR). Antes de hacer cualquier operación de lectura o escritura en la memoria, se debe colocar la dirección de la celda que se utilizará en la operación en este registro, ya sea para grabar como si es para sacar datos.

* Registro de información o intercambio de memoria (MDR). Este registro recibe la información obtenida de la lectura de la memoria. Este registro contendrá la información que queremos escribir y guardar en la memoria.

* Selector de memoria o descodificador. Este dispositivo se activa cada vez que se produce una orden de lectura o escritura. Conecta la celda de memoria -indicada por la dirección del registro de dirección de memoria- con el registro de información de memoria, lo que hace posible la transferencia de datos en un sentido o en el otro (memoria a MDR, MDR a memoria).

Básicamente, hay 3 parámetros que permiten medir la velocidad de respuesta de una memoria:

* Tiempo de acceso (Ta). Es el tiempo máximo que se tarda en leer o escribir el contenido de una posición de memoria.

* Tiempo de ciclo (Tc). Es el tiempo mínimo entre dos lecturas.

* Ancho de banda (Ab). Es el número de palabras que se transfieren entre la memoria y la CPU en cada unidad de tiempo: Ab = 1 / Tc.

Secuencia de pasos para leer o escribir un dato en la memoria principal.

1) Leer: Para leer un dato se siguen los siguientes pasos:

	1) Se pone la dirección en el registro de dirección.
	2) Mediante el descodificador, se accede a la dirección de memoria.
	3) Se sitúan los datos en el registro de datos.

2) Escribir: Para escribir un dato se siguen los siguientes pasos:

	1) Se transfiere la dirección en que se escribirá en el registro de dirección.
	2) Se transfieren los datos al registro de información.
	3) Se decodifica la dirección de memoria.
	4) Se pasa el contenido del registro de información a la dirección que contiene el registro de dirección.
