Un SGBD se divide en módulos que se encargan de cada una de las tareas
del sistema. El Sistema Operativo proporciona únicamente los servicios más
elementales y el SGBD parte de ese fundamento.
Los componentes funcionales son:
 El gestor de archivos: encargado de asignar espacio en el disco
para las estructuras de datos. Puede ser más o menos grande,
según su grado de relación con el SO.
 El gestor de la BD: que constituye la interfaz entre los datos de
bajo nivel almacenados en la BD y los programas de aplicación.
 El procesador de consultas: que traduce las proposiciones en
lenguaje de consulta a instrucciones de bajo nivel que puede
entender el gestor de la BD. También se encarga de optimizar las
consultas.
 El precompilador de DML: que convierte las proposiciones en
DML incrustadas en un programa, a llamadas normales a funciones
en el lenguaje huésped. Debe interactuar con el procesador de
consultas para generar el código apropiado.
 El compilador de DDL: que convierte las proposiciones escritas en
DDL en un conjunto de tablas que contienen metadatos. Estas
tablas se almacenan en el Diccionario de Datos.
Además se requieren otras estructuras dentro del sistema:
 Archivos de datos: almacenan físicamente la Base de Datos.
 Diccionario de Datos: conjunto de archivos que contiene la
información relativa a la estructura de la BD. Es consultado
constantemente por el gestor de la BD.
 Archivos de índices: Permiten el acceso rápido a los datos. Al
igual que el diccionario están incluidos físicamente en los archivos
de datos.