Una vez que tenemos una visión general de lo que es un SGBD, vamos a
ver los objetivos que un sistema debe cumplir para considerarse un SGBD:
 Abstracción de la Información: El primer objetivo de un SGBD es
proporcionar a los usuarios una visión abstracta de la información, es decir, el
sistema ahorra al usuario la necesidad de conocer los detalles de cómo se
almacenan los datos así como de su mantenimiento. Para ocultar estos
detalles, se definen varios niveles de abstracción tal y como se verá más
adelante.
 Independencia: La independencia de los datos se puede definir como la
capacidad para modificar un esquema de definición sin afectar a los
programas de aplicación. Existen dos niveles:
 Independencia física: Cuando es posible modificar el esquema interno sin
que afecte a las aplicaciones. Se realizan para mejorar el rendimiento.
 Independencia lógica: Cuando
es posible modificar el esquema
conceptual sin obligar a escribir de nuevo las aplicaciones. Se realizan
cuando cambia la estructura lógica de la BD (tamaño registros,
características de los campos, etc.).
La independencia lógica es más difícil de lograr que la física, ya que las
aplicaciones dependen en gran medida de la estructura lógica de los datos.
 Redundancia Mínima: La utilización de BD supone evitar la repetición o
redundancia de los datos en múltiples ficheros. En principio, puede parecer
que lo más conveniente es una redundancia nula, pero, en la práctica, ésta
comprobado que el mantener duplicados ciertos datos puede resultar
beneficioso a efectos de búsquedas más rápidas, por lo que se prefiere que
exista una redundancia mínima.
 Consistencia: Es consecuencia del punto anterior. Si existen datos duplicados
en varios ficheros, y se realiza una actualización de esos datos, será necesario
que el SGBD garantice la adecuada actualización del dato en todos los
ficheros, para evitar la inconsistencia del dato.
 Seguridad: Otro objetivo a conseguir por un SGBD es la protección de los
datos frente al acceso accidental o intencionado por parte de individuos no
autorizados. Para establecer esta seguridad se suele recurrir a establecer
claves de seguridad (passwords) necesarias para poder acceder a la BD.
 Integridad: Se refiere a las medidas necesarias para conservar la corrección
de los datos en la BD, es decir, mantener su validez y estructura física. Existen
varias circunstancias que pueden hacer que se estropeen los datos:
 Fallos del Hardware.
 Actualizaciones incompletas.
 Inserción de datos no válidos: El Administrador de la base de datos
define unas reglas de integridad (por ejemplo que el saldo de una cuenta
no sea inferior a una cantidad) y el SGBD se debe de encargar de hacerlas
cumplir al insertar un dato.
Una regla de integridad está constituida por tres componentes:
 La restricción propiamente dicha
 La respuesta a la violación, que especifica las acciones a tomar, como
rechazar la operación, informar al usuario, etc.
 La condición de disparo, que especifica cuando debe desencadenarse la
acción especificada: antes, después o durante cierto evento.
 Respaldo y Recuperación: El SGBD debe proporcionar mecanismos eficientes
para conservar Copias de Seguridad de cada fichero en prevención de
posibles fallos.
El proceso de copiar un fichero de forma periódica se llama respaldo (BACK-
UP). Estas copias de seguridad deben de realizarse regularmente y guardarse
en un lugar seguro. Se realizan sobre cintas o discos.
El proceso contrario, recuperar la información original a partir de las copias
de seguridad se llama recuperación. Para poder realizar estas recuperaciones
con la máxima rapidez y eficacia se recurre a un fichero especial llamado
Bitácora o Diario (archivo log). En este fichero (de movimientos) se registran
todos los datos que se vayan modificando debido a las operaciones con la BD.
Se guarda tanto el valor que tenía el dato antes de ser modificado como el
valor después de la modificación.
 Control de la Concurrencia: Lo más habitual es que la BD trabaje en un
entorno de multiprogramación y multiusuario. Esto presenta el problema de
que dos o más procesos (transacciones) distintos accedan al mismo dato de
forma simultánea.
El SGBD debe de controlar este problema para evitar la inconsistencia de los
datos. La solución consiste en utilizar una técnica denominada”candado”:
 Un proceso sólo puede acceder a un dato si tiene un candado para ese
dato. Existen dos tipos de candados:
 Compartido: si un proceso obtiene un candado compartido en un dato,
entonces puede leer ese dato pero no escribir en él.
 Exclusivo: si un proceso obtiene un candado exclusivo en un dato,
entonces puede leer y escribir ese dato.
 Las transacciones que deseen acceder a los datos deben solicitar un
candado y si no lo obtienen pasarán a una cola de espera.
El módulo encargado de los accesos concurrentes a los datos, es decir, de
proporcionar los candados, se llama Scheduler. También se encarga de definir
la granularidad, es decir, el tamaño de la unidad a la que se concede el acceso
concurrente. Esta puede variar considerablemente. En un Sistema Operativo
el tamaño mínimo suele ser el fichero, pero en un SGBD se puede establecer
el acceso a nivel de registro, o incluso de campo.
Algunas implementaciones de SGBD actuales (por ejemplo Interbase de
Borland-Inprise-Corel) utilizan otro mecanismo para el control de la
concurrencia consistente en mantener temporalmente varias versiones de los
mismos datos cuando éstos sufren procesos de actualización.
 Tiempo de Respuesta: Las bases de datos están diseñadas para ser utilizadas
por los usuarios finales, por lo que deben de asegurar un tiempo de respuesta
idóneo a las peticiones de los usuarios. Cuando se trata de procesos por lotes,
el tiempo de respuesta no tiene importancia, pero cuando se trata de
procesos on-line críticos (reserva de plazas, terminal bancaria) el SGBD debe
de proporcionar un tiempo de respuesta suficientemente corto.