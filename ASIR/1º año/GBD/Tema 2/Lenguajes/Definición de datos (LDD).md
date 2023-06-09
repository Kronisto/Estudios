El administrador de la base de datos ha de disponer de instrumentos que
le permitan describir los datos con facilidad y precisión, especificando sus
distintas estructuras; es lo que se denomina lenguaje de definición de datos. Los
lenguajes de definición de datos son autocontenidos y no necesitan apoyarse en
ningún lenguaje de programación.
El SGBD tendrá que facilitar medios para describir la estructura
conceptual (lógica global), para hacer las especificaciones relativas a la estructura
interna y para declarar las estructuras externas que sean requeridas para el
desarrollo de las diferentes aplicaciones.
Lenguajes de definición de la estructura lógica global
Desde el punto de vista conceptual, será necesario que el administrador
disponga de un instrumento de descripción que le permita asignar nombres a los
campos, a los agregados de datos, a los registros, etc., estableciendo sus
longitudes y características, así como las relaciones entre estos elementos;
especificar los identificadores, e indicar las restricciones semánticas que se han
de aplicar a los diferentes objetos descritos.
Lenguajes para la definición de la estructura interna
En un SGBD en el cual fuesen totalmente independientes las estructuras
físicas y conceptual (lógica global), y que consiguiese automáticamente la
optimización en el almacenamiento y recuperación de los datos, el SGBD podría
encargarse de, a partir de la estructura conceptual, definir la estructura interna
adecuada sin intervención del usuario (administrador), para lo cual habría que
suministrar al SGBD las informaciones precisas, como volúmenes, crecimiento
previsto, tipos de registros más accedidos con indicaciones sobre número medio
de accesos, relación entre actualizaciones y consultas, etc. Sin embargo, en la
práctica, y en el estado actual de la técnica, se puede mejorar considerablemente
el rendimiento de la base si el administrador especifica características respecto a
la estructura física que tiendan a conseguir una máxima eficiencia en el
almacenamiento y en la recuperación de los datos de la base. Para ello, tendrá
que disponer de un lenguaje de definición de la estructura interna o,
simplemente, deberá dar valores a ciertos parámetros.
Lenguaje de definición de estructuras-esquemas- externas
El SGBD debe poner a disposición de los usuarios medios que les
permitan recuperar o actualizar los datos contenidos en la base de acuerdo con la
visión lógica o estructura externa (vista) que precise cada aplicación.
Al definir una estructura externa es preciso darle un nombre e indicar
qué datos y qué interrelaciones de la estructura conceptual (lógica global) se
encontrarán en la misma. Cuando se desee utilizar un esquema externo ya
definido se podrá hacer referencia al mismo invocando su nombre desde el
lenguaje de manipulación.