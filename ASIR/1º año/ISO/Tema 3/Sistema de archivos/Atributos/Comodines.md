#ISO

En cualquier [[ASIR/1º año/ISO/Tema 3/Sistema de archivos/Concepto|sistema de archivos]] existen formas de recortar y facilitar las busquedas de ficheros o directorios,  pudiendo usar un **comodín** en el nombre o la extensión del fichero. Para ello, se dispone de los comodines que son de 2 tipos:

- * --> Sustituye a TODOS los caracteres (delante, detrás o en medio del nombre), 0 o más caracteres.
	
	- "\*data" - Identifica cualquier nombre de archivo terminado en data file.data.

- ? --> Sustituye a un CARÁCTER para que coincida con el resto que esté escrito, 1 carácter exactamente.
	
	* "n?te.txt" - falta un caracter en la posición indicada y mostrara cualquier nombre que empieze con *n* y termine en *te.txt*.