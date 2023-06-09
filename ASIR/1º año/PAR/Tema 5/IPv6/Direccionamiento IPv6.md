#PAR #TEMA_5 
Se suelen escribir en 8 grupos de 4 caracteres hexadecimales separados por 2 puntos.

* *2c09:0a93:0000:0000:3250:0010:f9a1:2b0a*

Existen simplificaciones que reducen la extensión de las direcciones a la hora de escribirlas.

* ***Ejem***: retirando los 0 no significativos, o agrupando secuencias de valores 0 mediante “::”

	* *2c09:a93:0:0:3250:10:f9a1:2b0a* --> *2c09:a93::3250:10:f9a1:2b0a*

Sólo se permite ==1 secuencia abreviada “::” en 1 IP==, de existir 2, podría ser imposible discernir el nº de términos ‘0’ abreviados con cada signo.

La dirección se compone de 2 partes de 64 bits: La 1º indica el prefijo de red, y la 2º el valor de host.

**Notación decimal con puntos**. Durante la transición de Internet de *IPv4* a *IPv6* será típico operar en entornos de 2x direccionamiento (*IPv4 e IPv6*). Por este motivo se ha introducido una notación especial para expresar direcciones *IPv6* que sean **IPv4-mapeada**, representando los últimos 32 bits de la dirección *IPv6* en el formato decimal con puntos usado en *IPv4*.

* ****Ejem***: la dirección *IPv6* del tipo *IPv4-mapeada* “*::ffff:c000:280*” se puede representar como “*::ffff:192.0.2.128*”, mostrando claramente la dirección *IPv4-mapeada* o *IPv6-compatible* dentro de la *IPv6*.

La dirección *IPv6* correlacionada con *IPv4* utiliza este formato alternativo. Este tipo de dirección se utiliza para representar los nodos *IPv4* como direcciones *IPv6*. Permite que las aplicaciones de *IPv6* se comuniquen directamente con las aplicaciones de *IPv4*. 

* ***Ejem***: “*00:0:0:0:0:ffff:192.1.56.100*” y “*0::ffff:192.1.56.10/96*” (formato abreviado).