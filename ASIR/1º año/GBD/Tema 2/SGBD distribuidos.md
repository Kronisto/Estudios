La forma tradicional de tratar los datos consiste en que todo el SGBD está
concentrado en un solo ordenador. Esto no significa que no pueda servirse a
varios usuarios conectados de manera remota, pero esta operación se efectúa
compartiendo los recursos del servidor de la misma manera que se hace con
cualquier otro tipo de aplicación. De esta forma, el servidor asume la carga de
todo el trabajo.
En los sistemas de tipo distribuido el SGBD se divide en partes y cada
parte puede estar instalada en una máquina diferente. Esta división admite
diferentes variantes como, por ejemplo, tener los datos en una máquina y el
software del SGBD en otra, tener una copia exacta del SGBD en cada servidor de
manera que el usuario se conecte al que menos tráfico tenga en cada momento,
o dividir la propia base de datos entre diferentes máquinas en función del uso
que vaya a hacerse desde cada una de ellas, entre otras.
Las posibilidades son muchas, pero vamos a centrarnos en dos: la
arquitectura cliente/servidor y las bases de datos distribuidas.
 Arquitectura Cliente/Servidor
Consiste en dividir dicho SGBD en dos partes:
 Servidor. Se trata de la parte principal del SGBD, la que gestiona la
base de datos. Se relaciona con la máquina y con el sistema
operativo.
 Cliente. Es la parte que utilizan los usuarios, las aplicaciones, los
lenguajes y, en ocasiones, las herramientas de gestión y
administración.
La división de las funciones en servidor y cliente puede hacerse
incluso en la misma máquina, separando los programas que hacen las
funciones de servidor de los programas cliente, que son los que utilizará el
usuario para de esta forma trabajar con aplicaciones no sobrecargadas de
opciones que no va a usar.
La máxima ventaja de esta distribución se obtiene cuando el servidor
y el cliente se encuentran en máquinas diferentes: a los terminales
remotos (clientes) les corresponde la parte del SGBD que pueden utilizar
los usuarios, y desde allí se mandan las peticiones al servidor, que las
procesa, hace las consultas o los cambios pertinentes y devuelve al cliente
el resultado. De esta manera, instalando la parte servidor del SGBD sólo en
una máquina y la parte cliente sólo en los terminales que usan los usuarios,
todos los ordenadores quedan descargados de tareas que no les
corresponden, y así se aprovechan todos sus recursos. El tráfico entre el
servidor y los clientes se limitará a las peticiones de éstos, y a la respuesta
correspondiente.
En la actualidad, se intenta evitar instalar parte del SGBD en los
ordenadores de los usuarios finales y se prefiere crear un nivel intermedio:
los servidores de aplicaciones (son ordenadores que sólo se emplean como
servidores de las aplicaciones que los clientes usan y a los cuales acceden
desde sus terminales).
 Bases de Datos Distribuidas
En el subapartado anterior se ha mencionado la posibilidad de
distribuir entre varias máquinas el SGBD. También es posible hacer lo
propio con los datos.
Una base de datos distribuida es aquella donde los datos están
repartidos entre diferentes máquinas. Cada máquina dispone de un SGBD
(o una parte de él) para dar el servicio correspondiente a los datos que
contiene.
Lo más habitual es que algunos de los datos estén repetidos en los
diferentes servidores, y entonces se habla de base de datos replicadas. En
ocasiones, toda la base de datos se encuentra repetida en todos los
servidores. La ventaja de esta opción es que se puede dar un mejor servicio
a los clientes; las desventajas son, por un lado, que se necesita una
continua actualización de los datos entre los diferentes servidores y, por
otro, su coste económico, tanto en hardware como en comunicaciones.
Según la utilización que se vaya a hacer de la base de datos, existen
diversas posibilidades para distribuir la información.
 Toda la base de datos replicada. Consiste en que cada servidor
tiene una copia completa de la base de datos.
 Toda la información distribuida sin replicación. Se basa en que
la información se encuentra fragmentada y cada fragmento se
guarda en un servidor.
 Combinar distribución y replicación. Se trata de un servidor con
toda la base de datos completa y otros con sólo las partes que
más se emplean. También es posible tener replicada en varios
servidores la parte más utilizada y el resto en uno solo. Por último,
otra opción es dejar en la máquina del cliente una copia de la
parte que más usa.
Un objetivo básico de un SGBD distribuido es que el usuario lo perciba
como si de una BD centralizada se tratase, es decir, el usuario no tiene que saber
dónde se encuentran almacenados los datos físicamente.