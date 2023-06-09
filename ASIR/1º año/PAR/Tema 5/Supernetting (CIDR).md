#PAR #TEMA_5 

**CIDR** (***C**lassless **I**nter-**D**omain **R**outing*), técnica utilizada para reducir la cantidad de entradas en la 
*tabla de enrutamiento* de un **router** en una *WAN*.

Se puede utilizar una máscara de subred variable, permite una mayor flexibilidad y eficiencia 
en la asignación de IP’s. Ejem: Tenemos una red de clase C con una máscara de subred de 255.255.254.0, lo que permitiría que 2 redes de clase C adyacentes se combinen en 1 sola red más grande. 

Toma varias redes más pequeñas y las agrupar en 1 sola red más grande utilizando una máscara de subred más amplia. Esto reduce el nº de entradas en la *tabla de enrutamiento* y puede mejorar el rendimiento de la red al reducir el tráfico de enrutamiento. Pero puede aumentar el riesgo de congestión en red, especialmente si se sobrecarga 1 sola red con demasiados hosts o subredes.

# EJEMPLO

Tenemos los siguientes IP, las cuales hemos de pasar a binario para poder realizar el **Supernetting**

* 211.40.77.0/24
   
	11010011 11111111 01001101 00000000
   
* 211.40.78.0/24
   
	11010011 10100000 01001110 00000000
  
* 211.40.79.0/24
   
	11010011 10100000 01001111 00000000
  
* 211.40.80.0/24
  
	11010011 10100000 01010000 00000000
  
* 211.40.81.0/24
  
	11010011 10100000 01010001 00000000

Una vez todas pasadas a binario nos fijamos en la última columna de números en la que todos coincidan:

| ==11010011 10100000 010==01101 00000000 | 211.40.77.0/24 |
| --------------------------------------- | -------------- |
| ==11010011 10100000 010==01110 00000000 |  211.40.78.0/24 |
| ==11010011 10100000 010==01110 00000000 | 211.40.78.0/24 |
| ==11010011 10100000 010==01111 00000000 | 211.40.79.0/24 |
| ==11010011 10100000 010==10000 00000000 | 211.40.80.0/24 |
| ==11010011 10100000 010==10001 00000000 | 211.40.81.0/24 |

Una vez ya tengamos localizada la columna cogemos la parte izquierda y la parte derecha la rellenamos de 0 y ponemos como máscara de red los nº de bits de la izquierda en mi caso son 19:

==11010011 10100000 010==00000 00000000 

211.40.64.0/19