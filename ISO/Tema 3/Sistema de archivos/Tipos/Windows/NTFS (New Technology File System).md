* Nombres de archivo de hasta 256 caracteres, 
* ordenación de directorios
* atributos de acceso a archivos
* Volúmenes hasta --> 256 TiB 
* Tamaño máximo archivo --> 16 TiB, 
* bloque --> 64 KiB, pudiendo llegar 16 EiB (*futuro según su diseño*). 
* Distingue entre mayúsculas y minúsculas en los nombres de archivos/directorios.
* Menor tamaño de unidad de asignación que FAT32 para un volumen de la misma capacidad. Usa la tabla MFT (Master File Table, que se guarda en un fichero oculto $MFT por la zona central de la partición) para localizar los ficheros, siendo el equivalente a la FAT.
* reparto de unidades en varios discos duros, reflexión de discos duros y registro de actividades, Se puede acceder al Directorio Activo, dominios de Windows server 2000 y posteriores, utilizar cuotas en disco para cada usuario, cifrado y compresión de archivos, almacenamiento remoto, dispone de una herramienta de desfragmentación y utilización de enlaces de archivos similares a los de Linux. 

En Windows Server 2008 se incorporó un nuevo proceso de reparación de sistemas NTFS denominado Autocuración (*Self healing*) que actúa en 2º plano para reparar los archivos dañados. También incorpora el control completo de transacciones (*aunque ya era parcialmente transaccional desde su inicio pues controlaba que, en operaciones de borrar, renombrar, etc., un único fichero, un reinicio en mitad no lo dañará*).