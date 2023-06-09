Uno de los principales objetivos de las bases de datos es conseguir la
independencia entre las estructuras lógica y física de los datos, que tiene como
consecuencia la independencia entre datos y aplicaciones, de modo que los
cambios en la estructura de los datos (siempre necesarios, ya que las empresas,
como organismos vivos, son por su misma esencia cambiantes) tengan una
repercusión mínima en los programas de aplicación, y viceversa.
El concepto de independencia de los datos, elemento clave en las bases
de datos, implica la separación entre el almacenamiento y la organización lógica
de los datos tal como éstos se contemplan por los distintos programas de
aplicación que hacen uso de la base, con lo que se consigue una doble finalidad:
 Unos mismos datos se presentarán de formas distintas según las
necesidades de los usuarios.
 El almacenamiento de los datos, su estructura lógica y los
programas de aplicación serán independientes unos de otros, de
modo que un cambio en uno de ellos no obliga a modificar los
demás.
En relación con la independencia es posible considerar tres aspectos:
 Su influencia en la arquitectura del sistema (niveles de
abstracción que como hemos visto ayudan a aumentar la
independencia).
 Características físicas o lógicas que están implicadas en la
dependencia (grado de independencia), donde se indica cuáles
son las características que pueden alterarse en cada uno de los
niveles de abstracción sin que ello influya en los otros niveles.
 Fase o etapa del proceso (compilación, montaje, carga, ejecución)
en la que se efectúa la correspondencia o transformación
(mapping) entre los distintos niveles; el sistema de gestión de la
base de datos es el que se ocupa de llevar a cabo la vinculación
(binding) entre niveles, durante la cual se efectúa la resolución de
los símbolos.
La rápida evolución que se está produciendo en los ordenadores y las
profundas transformaciones que implica la actual concepción de la informática
ponen en un primer plano de actualidad el objetivo de independencia ante la necesidad de garantizar las costosas inversiones que las organizaciones han
realizado en el desarrollo e implantación de sus sistemas de información. Es
preciso aislar las aplicaciones existentes de las técnicas de almacenamiento y
acceso, pero al mismo tiempo es imprescindible dotar al sistema de la flexibilidad
suficiente para que pueda beneficiarse de los avances que suponen las nuevas
tecnologías.
Dentro de la independencia física/lógica, debemos distinguir dos tipos
distintos, que se corresponden con las dos principales funciones de los SGBD: la
independencia en la descripción y la independencia en la manipulación.
La independencia en la descripción permite separar la definición de los
datos a nivel físico y a nivel lógico, mientras que la independencia en la
manipulación se refiere a la de los programas de aplicación respecto a los
caminos de acceso y al soporte físico donde se almacenan los datos. Así como en
la independencia en la descripción es fundamental la arquitectura del SGBD (sus
niveles), en la independencia en la manipulación influye también el modelo de
datos, ya que ciertos modelos, como el Jerárquico y el Red, incluyen caminos de
acceso en el nivel lógico, por lo que los usuarios han de conocerlos y apoyarse en
ellos cuando escriben sus programas de aplicación.
Hay que insistir en que las arquitecturas basadas en distintos niveles de
abstracción están muy relacionadas con la independencia físico/lógica.
En una arquitectura a tres niveles, los usuarios están aislados de los
datos almacenados físicamente en la máquina por las pantallas X1 y X2, que
representan dos funciones de correspondencia (mapping). La primera -por medio
de la cual se representa la independencia lógica- realiza la transformación de la
estructura conceptual (EC) a los esquemas externos (EE), y la segunda -
independencia física- del esquema interno (EI) al conceptual.
![[Pasted image 20221106165448.png]]
