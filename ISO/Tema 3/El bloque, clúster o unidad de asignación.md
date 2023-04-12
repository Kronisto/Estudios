#ISO 

Compuesto por un determinado nº de sectores (*2^n sectores*) se asocian a un único archivo, se almacena en 1 o más bloques de sectores. Si se elige un tamaño de bloque de 2 KB en un disco cuyo sector tiene 512 bytes, cada bloque estará compuesto por 4 sectores.

Si el tamaño del bloque es grande, siendo el archivo de un tamaño pequeño, se le asignará el bloque entero con lo que se desperdiciará gran parte de la capacidad del disco. 

Si el tamaño del bloque es pequeño para almacenar un archivo, harán falta muchos bloques con lo que se producirá un retraso en la lectura del archivo al tener que localizar el disco todos los bloques que componen dicho archivo. 

Para manejar los bloques asociados a cada archivo, se pueden utilizar varias técnicas:

# Asignación adyacente

Almacenar los archivos mediante bloques adyacentes en el disco (*el directorio únicamente tendrá que guardar la dirección en la que comienza el 1º bloque, el resto se encuentran a continuación*). 

**Ventaja**: fácil implementación.

**Problema**: es necesario conocer con anterioridad el nº de bloques que ocupará el fichero y genera una gran fragmentación del disco, que produce una pérdida de espacio.

# Asignación en forma de lista ligada

Arregla algunas de las carencias de la **asignación adyacente**. 

El directorio contiene la dirección del 1º bloque y cada bloque contiene, a su vez, la dirección del siguiente bloque o el valor ***null*** en caso de que sea el último bloque del fichero. Se consigue aprovechar todos y cada 1 de los bloques del disco y se evita perder capacidad por la fragmentación.

# Asignación mediante una lista ligada y un índice 

Intenta eliminar los defectos de la **anterior**. 

Crea una tabla con un registro por cada 1 de los bloques del disco, en cada registro se indica si dicho bloque está libre (*null*) o cuál es la dirección del siguiente bloque (*en caso de que ese bloque pertenezca a un determinado archivo*). El **directorio** se asocia con el nombre del archivo el nº de bloque en el que comienza dicho **archivo**; con este dato y mediante la tabla, se puede averiguar la dirección de todos los bloques que componen dicho **archivo** simplemente siguiendo la lista ligada.

Se usa principalmente en **windows**, para **FAT** y **NTFS**.

La tabla de registros se la denomina **FAT** (*File Allocation Table*) y se puede encontrar en sus 2 versiones: **FAT16** y **FAT32** (bloques se direccionan con 16 o 32 bits). 

Con esta organización, todo el bloque está disponible para los datos. Además, el acceso a un determinado bloque es mucho más rápido, ya que, aunque también haya que seguir la cadena de bloques como en la asignación en forma de lista ligada, al estar la tabla en memoria, estas consultas son mucho más rápidas y no es necesario acceder al disco. 

La **FAT** está en la parte exterior de la partición. En **NTFS** no hay áreas de disco reservadas para datos como la **FAT**. Todos los datos, incluidos los usados en la estructura de archivos de sistema **SETUP**, están contenidos en archivos.

Todo en una partición es un archivo, incluso la **MFT** (*Master File Table*), que es una **BD** de los archivos y las carpetas de la partición que incluye su nombre, ubicación, tamaño, permisos, así como sus atributos y otra información. Se almacena en la parte central de la partición como un fichero inaccesible al usuario llamado ==$Mft== para evitar tener que acceder a la parte exterior como en el caso de la **FAT**

# Indexación 

Usada en **Linux**, utilizan un sistema de archivos basados en **inodos**. Se asocia una pequeña tabla llamada **inodo**, que contiene los atributos y direcciones en disco de los bloques (*datos=content=data y direcciones=addresses*) del archivo. 

Las últimas entradas del **inodo** se reservan para cuando el archivo ocupa más bloques de los que el **inodo** es capaz de almacenar y pueden contener la dirección de otro bloque en el que se guardan las demás direcciones de los bloques de datos del archivo. A este bloque se le llama **bloque indirecto** (*bloque de direcciones*). En caso de que con este bloque extra no haya suficiente espacio para guardar todas las direcciones de los bloques de datos del archivo, existe la posibilidad de utilizar un bloque doblemente indirecto, e incluso, un 3º bloque triplemente indirecto. 

Cuando **Linux** abre un archivo, carga su **inodo**.

![[Pasted image 20221124192744.png]]

![[Pasted image 20221124192748.png]]

## Ejemplo --> Tabla de registros de asignación de bloques

Un usuario solicita leer el fichero iso.txt, el SO lee el directorio activo (*ruta relativa*) en busca de la entrada correspondiente a dicho archivo. Si existe, se hallará un registro con cierta información relativa a dicho archivo (*atributos, fecha, hora, tamaño, y también el bloque del disco en el que empieza el archivo*). Con dicha información busca en la **FAT** que se encuentra en la memoria principal, el registro perteneciente a ese bloque, y en él se encontrará la dirección del siguiente bloque en que el archivo está escrito. Repitie esta operación hasta que la dirección del siguiente bloque sea 0 (*Fin archivo*), obtenemos la lista completa de bloques en los que el archivo está almacenado.

![[Pasted image 20221124192649.png]]

En la tabla se puede ver que el archivo que comienza en el bloque 6, continúa en los bloques 2, 3, 7, 1 y 13. Además se puede observar que los bloques 0, 5, 8, 9, 12 y n-1 están libres y que hay otro fichero almacenado en los bloques 10, 11, n-2 y 4.

==Windows==

* CHKDSK unidad:\ /F (*da información sobre el sistema de archivos en unidad, el tamaño del clúster y su nº, sectores defectuosos y nº de archivos; y /F repara errores*).

==Linux==

* ls –i  (*muestra el inodo de los archivos del directorio actual*)

* stat fichero (*muestra toda la información de un fichero (lo que se guarda en su inodo, incluyendo su número de inodo*).

* stat –f /dispositivo (*muestra toda la información del sistema de ficheros indicado (incluyendo el tamaño del, número de inodos y de bloques.)*)