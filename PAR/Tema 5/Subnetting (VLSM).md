#PAR #TEMA_5 

Aprovecha mejor las direcciones y resuelve los problemas de división rígida y poco flexible. Permite dividir una de las redes asignadas de ==clase A, B, o C==, en subredes con subconjuntos de las IP’s de la red que pueden ser enrutables. Se le denomina **VLSM** (***V**ariable **L**ength **S**ubnet **M**ask*). Para usar ***VLSM***, los **routers** deben ser capaces de trabajar con máscaras distintas a las de las clases definidas, y por ello deben utilizar los [[Protocolo de Encaminamiento|protocolos de encaminamiento]] que lo tengan en cuenta.

# Ejemplo

Queremos tener **2 subredes**, y en cada una queremos tener **máximo 64 hosts** con la IP **192.168.10.0/24**.

1º identificar el tipo de red que tenemos, en este caso es **/24** lo que significa que es clase C.

* Pasamos a bits dicha IP:

	11000000.10011110.00001010.00000000 / 24

* Una vez convertido en bits mediante la *mascara de red* (***/24***), vemos que bits son de red, vamos contando desde la izquierda hasta llegar a 24 (*24 es la **mascara de red***).

	==11000000.10011110.00001010==.00000000 / 24
	
* Ahora sabemos que podemos trabajar con los ultimos 8 bits disponibles

2º **DIRECCION DE HOST**: Despues de saber lo que podemos hacer con la IP que tenemos, que calcular el nº de bits que necesitamos para la *dirección de host*, en nuestro caso necesitamos **64 hosts**

* 2^1 = 2 | 2^2 = 4 | 2^3 = 8 | 2^4 = 16 | 2^5 = 32 | 2^6 = 64 | **2^7 = 128**

* Nos fijamos en el resultado de las operaciones y buscamos el nº más cercano al **64**, en este caso es **2^6**, pero no nos sirve ya que hemos de incluir la **dirección de red** (*para identificar la red*) y la **dirección broadcast**. es decir, tenemos que sumarle 2 al nº de hosts necesarios
	
	 * 2 + 64 = 66

* Por lo que necesitariamos ocupar **2^7** bits, ya que es el que más se acerca, con *2^6* nos quedariamos cortos y con *2^8* nos pasariamos

* (*he escrito los resultados de las operaciones para que sea más visual, no hace falta escribirlo, mentalmente se puede hacer*)

3º **SUBREDES**: Despues saber cuantos bits de host necesitamos, hemos de calcular cuantos bits necesitamos en la *parte de red* para ocupar 2 subredes

* Para sacarlo es igual que en la *dirección de host*. Tenemos que buscar el nº más cercano, en mi caso es **2^1**, pero se tiene que contar la *dirección de red* y *dirección de host*, ya que solo estamos contando subredes, ahora sumamos ese bit a la *mascara de red* (/24), es decir, ==24 + 1 = 25==, si tuvieramos que usar 4 bits para las subredes se quedaría así, ==/24 + 4 = 28==

4º Una vez calculado las cosas que necesitamos las escribimos aparte para tenerlo un poco más limpio
| Dirección de red | Mascara de red | Nº bits host |
| ---------------- | -------------- | ------------ |
| 192.168.10.0     | /25            | 7            | 

* Antes de seguir calculando nada, comprobamos si es posible crear dichas redes, para ello sumamos la mascara de red con los bits que necesitamos:
	
	 * 25 + 7 = 32

* En mi caso está bién hecho, si el resultado fuera superior a 32 tendríamos algo mal, ya que 32 son los bits que componen una IP 

5º Una vez comprobado si está bién ya podemos empezar a calcular las IP disponibles de cada subred

Hemos de calcular 4 campos, *Dirección de red*, *1º IP usable*, *Última IP usable* y la *Dirección Broadcast*

## 1º subred

**DIRECCION DE RED**: 192.168.10.0/25

Al ser la 1º subred, trabajaremos directamente con la  IP

192.168.10.0/25

==11000000.10011110.00001010==.*0*0000000 / 25

**1º IP USABLE**: 192.168.10.1

==11000000.10011110.00001010==.*0*0000001 / 25

	128+64     128+16+8+4+2       8+2               1

	192            .168           .10              .1

**ÚLTIMA IP USABLE**: 192.168.10.126

==11000000.10011110.00001010==.*0*1111110 / 25

	128+64     128+16+8+4+2       8+2        64+32+16+8+4+2

	192            .168           .10              .126
 
**DIRECCIÓN BROADCAST**: 192.168.10.127

==11000000.10011110.00001010==.*0*1111111 / 25

	128+64     128+16+8+4+2       8+2        64+32+16+8+4+2+1

	192            .168           .10              .127

| Dirección de red    | 1º IP usable | Última IP usable | Dirección Broadcast |
| ------------ | ------------ | ---------------- | ------------------- |
| 192.168.10.0/25 | 192.168.10.1 | 192.168.10.126    | 192.168.10.127     |

## 2º subred

**DIRECCION DE RED**: 192.168.10.128/25

Al ser la 2º subred, trabajaremos directamente con la siguiente dirección de la anterior subred es decir, 192.168.10.128

192.168.10.128/25

==11000000.10011110.00001010==.*1*0000000 / 25

**1º IP USABLE**: 192.168.10.129

==11000000.10011110.00001010==.*1*0000001 / 25

	128+64     128+16+8+4+2       8+2             128+1

	192            .168           .10             .129

**ÚLTIMA IP USABLE**: 192.168.10.254

==11000000.10011110.00001010==.*1*1111110 / 25

	128+64     128+16+8+4+2       8+2       128+64+32+16+8+4+2

	192            .168           .10              .254
 
**DIRECCIÓN BROADCAST**: 192.168.10.255

==11000000.10011110.00001010==.*1*1111111 / 25

	128+64     128+16+8+4+2       8+2        128+64+32+16+8+4+2+1

	192            .168           .10              .255
| Dirección de red    | 1º IP usable | Última IP usable | Dirección Broadcast |
| ------------ | ------------ | ---------------- | ------------------- |
| 192.168.10.128 | 192.168.10.129 | 192.168.10.254    | 192.168.10.255      |