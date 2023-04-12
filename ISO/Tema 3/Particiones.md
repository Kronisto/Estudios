#ISO

Independiente del **SO**. División física de la unidad de almacenamiento desde un determinado cilindro (*misma pista en todas las caras del disco*) a otro. Los sistemas de particiones que podemos emplear:

![[Pasted image 20221109081314.png]]

### MBR (Master Boot Record)

* Ocupa el 1º sector del disco, el sector 0 (512 Bytes), para transformarlo en un sector de arranque . 

* Admite 4 particiones como máximo: de 0 a 4 primarias, y de 0 a 1 extendida. En la extendida podemos crear **particiones** lógicas que son las que se formatean, al igual que las primarias. 

* Se lee con el **BIOS** (*Basic Input Output System*) tradicional o **EFI** (*Extensible Firmware Interface*).

* Tamaño máximo de una partición 2 TiB

![[Pasted image 20221109081258.png]]

### GPT (GUID Partition Table) GUID: Globally Unique Identifier)

* Puede llegar a ocupar los primeros 32 sectores del disco (16 KiB), y se guardan 2 copias del **GPT** en disco.

* Es necesario **EFI**, y un **SO** moderno. Se suelen crear automáticamente las particiones **ESP** o **EFI** (*unos 100 MB de Fat32*), y en Windows modernos una partición **MSR** (*de unos 128 MB, para recuperar el sistema*), una vez que ha seleccionado este gestor de particiones. 

* Permite hasta 128 particiones, que pueden ser mayores de 2 TiB, y es mucho más seguro que **MBR**.

![[Pasted image 20221109082951.png]]