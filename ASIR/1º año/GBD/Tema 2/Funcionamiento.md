Si se contempla desde la perspectiva del sistema informático, el SGBD
constituye un subsistema de éste y, más en particular, del software. El
funcionamiento del SGBD está muy interrelacionado con el de otros
componentes, especialmente con el Sistema Operativo.
Si comparamos la forma en la que los programas de aplicación
interaccionan con los datos en un sistema de ficheros y en una base de datos,
encontramos bastantes diferencias. En el primer caso los datos se organizan en
ficheros y las aplicaciones acceden a los ficheros con datos a través del sistema
operativo mientras que en las bases de datos, los datos se organizan en
conjuntos estructurados, sin redundancias perjudiciales, que pretenden ser una
representación del mundo real y que son utilizados por todas las aplicaciones. Las
aplicaciones se desarrollan mediante las facilidades del SGBD, y éste, a su vez, se
apoya en los métodos de acceso del S.O. La comparación de formas de acceso se
ve más claramente en la figura siguiente:
![[Pasted image 20221106164344.png]]

La interacción en un entorno concurrente entre el SGBD, el sistema
operativo y los programas de aplicación, se muestra de forma general en la figura
siguiente. Por cada programa de aplicación (PA) que se está ejecutando existe
una unidad de ejecución (UE) en la que se encuentra un área de trabajo de
usuario (ATU) con sus áreas de entrada / salida (E/S) y un área de comunicación
con el SGBD destinada a recibir los mensajes y la información de control
procedente de éste. Desde el programa de aplicación se hace referencia a la vista
externa (VE) utilizada por el correspondiente programa. En la biblioteca del
sistema se encuentran almacenados, además de los datos, la estructura
conceptual (lógica global) y la estructura interna que los describe, así como las
vistas externas que serán llamadas por los programas de aplicación de los
usuarios.
![[Pasted image 20221106164410.png]]

El flujo de datos e instrucciones entre estos elementos es el siguiente:
a) Se produce una llamada desde una UE al SGBD (1); en la llamada se
ha de hacer referencia a la vista externa implicada (2).
b) El SGBD analiza la llamada y completa los argumentos con la
información de la vista externa a la que se ha hecho referencia en
la llamada, así como con la correspondiente a la estructura lógica
global y la estructura interna con ella relacionadas. Esta
información se encuentra previamente almacenada en los ficheros
del sistema (Diccionario de Datos), desde donde pasa al SGBD (3 y
4).
c) Una vez comprobado el derecho del programa de aplicación a
utilizar esta vista, y después de verificar su corrección, el SGBD
traduce la llamada convirtiéndola en órdenes a los métodos de
acceso del sistema operativo (5). Si el sistema había utilizado
recientemente los mismos datos, es posible que éstos aún se
hallen en el área de almacenamiento intermedio (12).
d) El SO accede al soporte secundario (disco) donde se encuentran
almacenados los datos (6).
e) Los datos a recuperar pasan del soporte donde se encuentra
almacenada la base de datos al área de almacenamiento
intermedio (buffer); si se tratase de una inserción o modificación
pasarían en sentido contrario (7).
f) Los datos son transferidos desde el buffer al área de trabajo del
usuario de la UE que hizo la llamada (8), o en sentido contrario si
se trata de una inserción o modificación, realizándose las
correspondientes transformaciones entre las representaciones de
los datos.
g) El SGBD, una vez terminada la operación de manipulación, pasa al
área de comunicación los indicadores de estado (9); en los que se
señala si la operación ha acabado satisfactoriamente o no, al
tiempo que se dan otras informaciones sobre la operación
realizada.
h) El PA revisa el estado de los indicadores que se encuentran en el
área de comunicación de la unidad de ejecución desde la que se
efectuó la llamada y toma las decisiones oportunas (10).
i) En el caso de que la operación haya terminado satisfactoriamente,
los datos que se encuentran en el área de E/S de la
correspondiente unidad de ejecución ya pueden ser utilizados por
el PA (11).