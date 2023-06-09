#ISO 

División lógica de almacenamiento de [[Archivos|archivos]] u otros subdirectorios.

Constituyen una estructura jerárquica en forma de árbol. En cualquier momento, el usuario se encuentra en un determinado **directorio** y, a menos que se indique otra cosa, todos los [[Archivos|archivos]] se buscan o se crean en ese **directorio**.

En todo [[ASIR/1º año/ISO/Tema 3/Sistema de archivos/Concepto|sistema de archivos]] hay un *directorio especial*
llamado **raíz**, es el **directorio** que contiene todos los demás **directorios** y [[Archivos|archivos]] (*también se le puede identificar con la barra inclinada*). 

* **Ruta absoluta**:
	
	* Windows --> C:\Windows\notepad.exe
	
	- Linux --> /etc/passwd

* **Ruta relativa**:

	* Carecen de caracter inicial por lo que el [[Archivos|archivo]] se busca partiendo del directorio en el que se esté trabajando o directorio activo.

	* Ejemplo --> ../notepad.exe o bin/calc

Muchos de los **SO** que implementan un sistema jerárquico de **directorios** tienen 2 entradas especiales en cada uno de sus directorios:

* "." para el Directorio Activo o de trabajo

* ".." referencia respectivamente al Directorio Padre

Los nombres de los **directorios** pueden tener extensión al igual que el nombre de un [[Archivos|archivo]] y es recomendable que sea lo más descriptivo posible de los [[Archivos|archivo]] que contiene.