#GBD

# Ventajas

* ==Reducción del espacio de almacenamiento== La desaparición (*o disminución*) de las redundancias, así como la aplicación de técnicas de compactación.

* ==Mayor eficiencia en la recogida, validación e introducción de los datos en el sistema==. Al no existir apenas redundancias, los datos se recogen y validan 1 sola vez, aumentando así el rendimiento de todo el proceso previo al almacenamiento.

* ==Coherencia de los resultados== Debido a que la información de la **BD** se recoge y almacena 1 sola vez, en los tratamientos se utilizan los mismos datos, por lo que los resultados de todos ellos son coherentes y perfectamente comparables. Al no existir (*o al menos disminuir en gran medida*) la redundancia en los datos, desaparece el problema que se presentaba en el enfoque clásico de que el cambio de un dato obligaba a actualizar una serie de ficheros. 

* ==Independencia de los datos respecto a los tratamientos y viceversa== Un cambio de los tratamientos no impone un nuevo diseño de la **BD**. La inclusión de nuevas informaciones, desaparición de otras, cambios en la estructura física o en los caminos de acceso, etc. no deben obligar a alterar los programas. La flexibilidad que proporciona la independencia de los datos y programas es muy importante para conseguir sin excesivos costes la continua adaptación del [[Concepto y función de un sistema de información (SI)|SI]] a la evolución de las organizaciones.

* ==Mejor disponibilidad de los datos para el conjunto de los usuarios== Cada usuario ya no es propietario de los datos, ya que se comparten entre el conjunto de aplicaciones, existiendo una mejor disponibilidad de los datos, siempre que estén autorizados para su acceso. Hay también una mayor transparencia respecto a la información existente, todos los datos que se encuentran en la **BD** se deben relacionar en un catálogo o diccionario que puede ser ampliamente difundido y accedido por medios informáticos.

* ==Mayor valor informativo== En ella se recogen las interrelaciones entre los datos. Por lo que el valor informativo del conjunto es superior a la suma del valor informativo de los elementos individuales que lo constituyen.

* ==Mejor y más normalizada documentación de la información, la cual está integrada con los datos== En el enfoque clásico los datos se encuentran separados de su contenido semántico; los 1º se almacenan en ficheros y su descripción se hace mediante un lenguaje de programación que se encuentra en los programas. La documentación de los datos, realizada por el analista o programador, es en general insuficiente, y a veces incluso inexistente. Además, por lo común la estandarización brilla por su ausencia. Este problema se atenúa en gran medida en las **BD**, ya que se incluyen no sólo los datos, sino también la semántica de los mismos

* ==Mejoras en el control, seguridad y tolerancia a fallos== La **BD** centraliza toda la información del sistema y proporciona mecanismos para que los usuarios utilicen los datos. De esta forma es posible controlar todos los accesos y operaciones que se realizan, permitiendo elaborar auditorias, controlar los permisos de acceso de cada usuario/grupo cuando realizan una petición de operación sobre los datos e instaurar mecanismos generales de protección de fallos y recuperación de errores para todas las operaciones. En el enfoque clásico, la implantación de cualquiera de estos controles obligaba a que cada usuario o aplicación realizara por sí mismo las tareas asociadas y resultaba prácticamente imposible en sistemas complejos o de gran tamaño debido al volumen de usuarios que se debían coordinar.

# Desventajas

* ==Instalación costosa== La implantación de una **BD** puede llevar consigo un coste elevado, tanto en equipo físico (*nuevas instalaciones o ampliaciones*), como en el lógico (*OS, programas, compiladores...*), además del mismo coste de adquisición y mantenimiento del **SGBD**.

* ==Personal especializado==

* ==Implantación larga y difíci ==

* ==Falta de rentabilidad a corto plazo== tanto por su coste en personal y en equipos como por el tiempo que tarda en estar operativo, no resulta rentable a corto plazo, sino a medio o, incluso, a largo plazo.

* ==Escasa estandarización== Pero han aparecido estándares, sobre todo en el campo de las BD relacionales.

* ==Desfase entre teoría y práctica== Al existir un considerable avance de la teoría en relación con la práctica, en muchas ocasiones los usuarios, especialmente los directivos, se engañan respecto a las prestaciones reales que pueden proporcionarles los **SGBD** actuales, creyendo que constituyen ya una realidad ciertos aspectos que todavía son sólo teóricos. Las **BD** no constituyen únicamente una nueva tecnología, más o menos avanzada, pero tecnología al fin y al cabo, sino que nacen de una concepción distinta del **SI**. Por lo que han de tener una influencia decisiva en las estructuras y organización de su entorno. Si esto no se tiene bien presente, muchas de las posibles ventajas de las **BD** no se harán realidad y, en cambio, se acentuarán sus inconvenientes y problemas.