#GBD #Funciones

Debe permitir al **diseñador** de la **BD** especificar los elementos de datos que la integran, su estructura y las relaciones que existen entre ellos, las reglas de integridad semántica... como las características de tipo físico y las vistas lógicas de los usuarios.

Esta función, realizada por el lenguaje de **descripción o 
definición de datos** (*LDD o  DDL- Data Description-Language*) propio de cada **SGBD**, debe suministrar los medios para definir las 3 estructuras de datos (*[[ASIR/GBD/Tema 1/Ficheros, concepto y clasificación/Clasificación|externa, conceptual e interna]]*), especificando las características de los datos a cada uno de estos lvl.

A [[Clasificación|lvl interno]], se ha de indicar el espacio (*volúmenes, cilindros y pistas*) reservado para la **BD**, la longitud de los campos o elementos de datos, su modo de representación (*binario, decimal, alfanumérico, punto fijo o flotante...*).

Se deben poder definir caminos de acceso, como punteros, índices... Para las estructuras [[Clasificación|externa y conceptual]], la función de descripción ha de proporcionar los instrumentos para la definición de los objetos (*entidades, tablas, registros...*), su identificación, atributos de los mismos, interrelaciones entre ellos, autorizaciones de acceso, restricciones de integridad... Las descripciones de las estructuras externas de los usuarios han de estar referidas a la estructura conceptual. 

El **SGBD**, además de suministrar facilidades de descripción, se ocupará de la función de correspondencia o transformación (*mapping*) de la estructura conceptual a las estructuras externas, y entre aquella y la estructura física.