Un SGBD de tipo jerárquico utiliza árboles para la representación lógica
de los datos. La figura siguiente muestra un diagrama de estructura de árbol con
dos tipos de registros: profesor y alumno, donde un profesor puede tener varios
alumnos y una posible ocurrencia de la BD:

![[Pasted image 20221106165823.png]]

Un SGBD jerárquico posee las siguientes características:
 Los registros (llamados segmentos) están dispuestos en forma de
árbol y no pueden existir ciclos.
 Los registros sólo pueden estar enlazados mediante relaciones
uno a uno o uno a muchos.
 Cuando se elimina un registro padre se deben borrar todos sus
registros hijos.
El SGBD jerárquico más conocido en el mercado es el IMS que utiliza el
lenguaje de consulta DL/I.