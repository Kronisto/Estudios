#ISO

## Archivos

Un nombre completo de **archivo** puede tener hasta 255 caracteres si se utiliza **LFN** (*Nombres Largos de Archivo*).

* **S** --> atributo de sistema (*system*). Indica si el **archivo** pertenece al **SO** o no.

* **H** --> atributo de oculto (*hidden*). Indica si el archivo está oculto. No se visualiza en un listado de **directorio**.

* **R** --> atributo de sólo lectura (*read only*). Indica si el archivo es de sólo lectura o se permite su escritura.

* **A** --> atributo de archivo. Se suele cambiar cuando se modifica el archivo. Su mayor utilidad es poder determinar qué [[Archivos|archivos]] se modificaron desde la última copia de seguridad y qué hay que añadir a la actual cuando se realiza una copia de seguridad incremental.

* **Fecha** --> Almacena la fecha de creación, modificación y último acceso del **archivo**.

* **Hora** --> Almacena la hora de creación, modificación y último acceso del archivo.

* **1º bloque** (*cúster o unidad de asignación*) del fichero.

* **Tamaño** --> Almacena el tamaño que ocupa el archivo.
Si empleamos el sistema de ficheros **NTFS** en Windows, se permite indicar si está cifrado o comprimido:

- **E**: atributo cifrado (*Encripted*). Indica si el archivo está cifrado o encriptado.

- **C**: atributo de compresión (*Compress*). Este atributo indica se está comprimido.

## Directorios

Junto con el nombre del [[Directorios|directorio]], el **SO** almacena también unos atributos que califican al [[Directorios|directorio]]. Estos [[ISO/Tema 3/Sistema de archivos/Atributos/Concepto|atributos]] varían también de un **SO** a otro, en el **SO** Windows y en MS-DOS se pueden encontrar los siguientes atributos:

* **H**: atributo de oculto (*hidden*). Indica si el [[Directorios|directorio]] está oculto. En este caso, no se visualizará al hacer un listado del [[Directorios|directorio]].

* **R**: atributo de sólo lectura (*read only*). Indica si los [[Archivos|archivos]] del [[Directorios|directorio]] son de sólo lectura o se permite también su escritura.

* **A**: atributo de archivo. Se suele cambiar cuando se modifica el [[Directorios|directorio]]. Su mayor utilidad es poder determinar qué [[Directorios|directorios]] se modificaron desde la última copia de seguridad y, por tanto, qué hay que añadir a la actual cuando se realiza una copia de seguridad incremental.

* **Fecha**. Es el atributo que almacena la fecha de creación o modificación del [[Directorios|directorio]].

* **Hora**. Es el atributo que almacena la hora de creación o modificación del [[Directorios|directorio]]. 
 
Si empleamos el **sistema de ficheros** **NTFS** sobre Windows, también se permite emplear los [[ISO/Tema 3/Sistema de archivos/Atributos/Concepto|atributos]] para indicar si los archivos de cada [[Directorios|directorio]] estarán ***cifrados*** o ***comprimidos***.

- **E**: atributo cifrado (*Encripted*). Indica si el archivo está cifrado o encriptado.

- **C**: atributo de compresión (*Compress*). Este atributo indica se está comprimido.gg

## Comandos

![[Pasted image 20221109092602.png]]