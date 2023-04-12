Para cumplir los objetivos asignados a la función de manipulación se ha
de contar con lenguajes que ofrezcan a los usuarios la posibilidad de referirse a
determinados conjuntos de datos, que cumplan ciertas condiciones (criterio de
selección), como que un atributo tenga un determinado valor, o que un conjunto
de atributos y valores satisfagan cierta expresión lógica. Además del criterio de
selección, es preciso indicar la estructura externa que se desea actualizar o
recuperar.
Una vez especificados el criterio de selección y los datos a actualizar o
recuperar, el SGBD debe ocuparse de acceder al correspondiente soporte físico
de donde se extraerán los datos definidos para su transferencia a un dispositivo
de salida, o en donde se insertarán, modificarán o borrarán los datos si se trata
de una actualización.
En la figura (siguiente página) se presenta la estructura de un programa
escrito en un lenguaje anfitrión que interactúa con una base de datos mediante
un lenguaje huésped. En la parte declarativa se hace una llamada a la vista de
usuario; además, se definirán, dentro del programa de aplicación, una áreas de
entrada / salida y un área al que se pasarán los mensajes enviados por el SGBD
para informar sobre distintos aspectos relativos a la ejecución de una sentencia
(si se ha producido algún error durante la ejecución, sí ésta ha terminado
normalmente, etc.). En la parte de proceso se hace una llamada a la base de datos
(mediante las sentencias de recuperación o actualización del LMD), la cual, si se
trata de unas sentencia de recuperación, copia los datos desde la base de datos
al área de entrada del programa de aplicación; si la sentencia es de inserción, los
datos pasan del área de salida del programa a la base de datos; cuando la
sentencia es de modificación, los datos se trasfieren al área de entrada/salida del
programa donde se realizan los cambios y desde allí se devuelven a la base de
datos; en las operaciones de borrado no existe transferencia de datos, sino que
éstos son eliminados de la base de datos. En todos los casos habrá que
comprobar el contenido del área de mensajes, a fin de saber si la
correspondiente sentencia ha finalizado o no con éxito.
![[Pasted image 20221106164109.png]]

Pero al igual que el programador precisa de un lenguaje de manipulación
que se embeba en un lenguaje de programación, el usuario no informático
deberá disponer también de un instrumento análogo, pero mucho más sencillo,
para comunicarse con la base y extraer de ella (o introducir) las informaciones
que precise. Para atender a estas necesidades, los SGBD suelen contar con
lenguajes autocontenidos que ofrecen facilidades a los usuarios con pocos
conocimientos de programación, para, desde un terminal y en modo interactivo,
acceder a la base y manipular los datos almacenados en ella sin necesidad de
apoyarse en un lenguaje de programación.
Los lenguajes autocontenidos suelen incluir no sólo los medios de
manipulación, sino también facilidades para describir los datos que se desean
recuperar o actualizar.
A veces, el mismo lenguaje de manipulación puede actuar como huésped
y como autocontenido, así ocurre, por ejemplo con el SQL, que puede ser llamado
desde un lenguaje anfitrión (por ejemplo C), o bien puede interactuar
directamente con la base de datos sin necesidad de estar apoyado en ningún
lenguaje de programación. Esta característica aumenta la productividad de los
sistemas que dispongan de esta clase de lenguajes duales.
Los LMD admiten, además, otro tipo de clasificaciones que es
interesante comentar. Un LMD puede ser procedimental o no procedimental. Un
lenguaje es más procedimental cuanto con más detalle sea preciso especificar el
procedimiento necesario para acceder a la base de datos a fin de recuperar o
actualizar los datos. Los lenguajes orientados al usuario deben ser poco
procedimentales, mientras que los lenguajes que utilizan los programadores
suelen ser bastante más procedimentales. En un lenguaje poco procedimental
basta con decir qué se quiere, sin explicar cómo obtenerlo; mientras que si el
lenguaje es más procedimental no es suficiente con que se le indique el qué, sino
que es necesario, además, precisar el algoritmo.
Aunque algunos LMD se utilizan en diferido (tratamiento por lotes), en la
actualidad, la mayoría de los LMD permiten su uso en modo conversacional desde
un terminal.
Existen lenguajes de manipulación de datos llamados navegacionales que
recuperan o actualizan los datos registro a registro, y es el programador quien
debe indicar el camino que se ha de recorrer, a través de la estructura definida,
hasta llegar al registro buscado; en este caso, cada sentencia o llamada al
lenguaje de manipulación de datos produce la recuperación o actualización de un
registro único (tal es el caso de los lenguajes Codasyl o Jerárquicos). En cambio
otros lenguajes actúan sobre conjuntos de registros (lenguajes de especificación),
de forma que una única sentencia puede dar lugar a la recuperación actualización
del conjunto de registros que cumpla el criterio de selección especificado (como
ocurre en los lenguajes relacionales, por ejemplo en el SQL).
En general, los lenguajes de tipo huésped son procedimentales, se
explotan en diferido y actúan registro a registro, mientras que los
autocontenidos suelen ser no procedimentales, se usan en conversacional y
recuperan conjuntos de registros. Por ejemplo, el DL/I (IMS de IBM) es de tipo
huésped, muy procedimental, diferido y navegacional; el lenguaje SQL, es poco
procedimental, de especificación (actúa sobre conjunto de registros) y puede
usarse en modo autocontenido o como huésped desde un lenguaje anfitrión, ya
que goza de la propiedad dual. Un ejemplo de sentencia SQL es:
SELECT nombre,apellido
FROM persona
WHERE fecha_nac=”11/09/01”
En la actualidad, la mayoría de los SGBD disponen además de lenguajes
de cuarta generación (4GL), en general muy poco procedimentales, que permiten
la consulta y actualización de la base de datos, para desarrollar aplicaciones
(informes, gráficos) de una forma rápida, intuitiva y fácil. Un ejemplo serían las
herramientas SQL Forms, SQL Reports, SQL/PL, etc. de Oracle.
La figura (siguiente página) presenta la clasificación de los lenguajes de
datos que acabamos de ver:
![[Pasted image 20221106164155.png]]