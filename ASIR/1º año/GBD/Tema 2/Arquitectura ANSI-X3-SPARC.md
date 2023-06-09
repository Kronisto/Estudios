La arquitectura a tres niveles del grupo ANSI en sus estudios de la
normativa ANSI/X3/SPARC (Comité de Planificación y Requerimientos del
Instituto Nacional Americano de estándares que , a su vez, depende del
organismo ISO, surgida en el año 1977) ha marcado una clara línea de
investigación en el campo de las bases de datos. Aun cuando en propuestas de
normalización anteriores ya se había indicado la conveniencia de separar los tres
niveles de estructuras (externo, conceptual e interno), ninguno de estos trabajos
profundizó tanto en el tema.

![[Pasted image 20221106165326.png]]

Del esquema conceptual (descripción global de los datos) se deriva una
colección de esquemas externos que son la visión que tienen de la base de datos
las distintas aplicaciones; el esquema interno es la descripción de los datos de
cara a la máquina. La transformación de unos esquemas en otros (funciones de
correspondencia) los lleva a cabo el SGBD.

La arquitectura ANSI/X3/SPARC está parcialmente basada en el concepto
de máquinas anidadas (tipo cebolla). El flujo de datos pasa a través de distintas
capas, que están separadas por interfaces y cuyas funciones se describen con
detalle en la documentación. Las múltiples interfaces, cuyo número se ha
considerado excesivo, tienden a aislar los diversos componentes del sistema con
vistas a conseguir el objetivo de independencia.
En la arquitectura propuesta se distinguen dos partes: la superior para la
definición de la base de datos, y la inferior para su manipulación. En esta
arquitectura se describen distintas funciones: humanas, representadas en la
figura por hexágonos; funciones de programa, que se presentan por medio de
rectángulos; interfaces, que se representan mediante líneas y para cuya
instrumentación el informe no dicta ninguna norma, pudiendo ser, por tanto,
interfaces físicas, lógicas, microprogramadas, etc., y metadatos o diccionario de
datos que desempeñan un papel fundamental en esta arquitectura y que se
representa por medio de un triángulo.

![[Pasted image 20221106165347.png]]

Definición de la base de datos. La definición se realiza a través de una
serie de funciones de programa e interfaces, dando lugar a un conjunto de datos
llamados metadatos (datos acerca de los datos) que se almacenan en el
diccionario. Este diccionario de datos es el eje principal de la arquitectura
alrededor del cual giran los demás elementos, en el diccionario de datos se
almacenarán:
 Las descripciones interna, conceptual y externa de la BD así como
las reglas de correspondencia necesarias para el paso de un
esquema a otro.
 Las descripciones de los campos, registros y referencias cruzadas
entre los registros de varios ficheros.
 Los códigos de autorización y seguridad de los datos.
 Los esquemas externos que son empleados por cada aplicación,
quiénes son sus usuarios y qué autorizaciones tienen.
Una base de datos se define especificando primeramente el esquema
conceptual a través de la interfaz 1, que podría ser un lenguaje de definición del
esquema conceptual – o bien una herramienta CASE integrada. Este esquema
conceptual es compilado por el procesador del esquema conceptual y se
almacena por medio de la interfaz 2 en el diccionario de datos.
El procesador del esquema conceptual es capaz de mostrar la
información acerca del esquema conceptual utilizando la interfaz 3, que podría
consistir, por ejemplo, en un conjunto de menús. Utilizando esta información
pueden definirse los esquemas externo e interno a través de las interfaces 4 y 13,
que serían controlados por los procesadores correspondientes, y almacenados en
la base de datos a través de las interfaces 5 y 14. Estos tres tipos de esquemas,
claramente diferenciados, llevan a ANSI/SPARC a proponer la existencia de tres
tipos de administradores: el administrador de la empresa, el administrador de la
base de datos y el administrador de aplicaciones; triple funcionalidad que puede
ser asumida por una única persona o grupo de personas.
Manipulación de la base de datos. El usuario puede entonces manipular
(insertar, borrar, modificar y recuperar) los datos utilizando la interfaz 12, que
podría ser un lenguaje de manipulación, por ejemplo SQL. Una petición de datos
por parte del usuario es ejecutada por los transformadores externo/conceptual,
conceptual/interno y interno/almacenado, que utilizan los metadatos por medio
de las interfaces 38,36 y 34, respectivamente. La solicitud del usuario en la
interfaz 12 la convierten los transformadores en peticiones a las interfaces 31,30
y 21, que devuelven el resultado al usuario. Estas últimas interfaces constituyen
la función de vinculación entre los distintos niveles (conceptual, interno y
almacenado).
Todas las interfaces las ha de suministrar el SGBD, pero ANSI no
especifica la forma de implementación.
La arquitectura a tres niveles de ANSI/SPARC responde positivamente a
las exigencias de independencia, flexibilidad y capacidad de evolución. La
transformación del esquema conceptual por cambios en el sistema de
información de la empresa, siempre que no sean demasiado drásticos, será
admitida por el SGBD que proporcionará nuevas funciones de correspondencia(mapping) de forma que los programas de usuario no adviertan siquiera que
dichos cambios se han producido. De igual modo, el añadir vistas externas que
permitan abordar nuevas funciones de la empresa o el introducir cambios en el
esquema interno, sólo afectará a los procesadores del SGBD que, mediante las
correspondientes interfaces, tendrán que modificar las funciones de
correspondencia adaptándolas a las nuevas circunstancias.
