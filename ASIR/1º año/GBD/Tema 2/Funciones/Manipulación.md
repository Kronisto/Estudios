#GBD #Funciones 

- ==Totalidad de los datos== --> Se recuperan todos los datos de la **BD** o todos los de un determinado tipo. *Ejemplo*, para la confección de la nómina será preciso recuperar todos los registros de los empleados de la empresa.

- ==Consulta selectiva== --> Se tiene que localizar los registros que cumplan una determinada condición (*criterio de selección*). *Ejemplo*, obtener los empleados que sean informáticos y sepan inglés.

En ambos casos es preciso especificar la estructura lógica externa que se desea recuperar; así, nombre, datos bancarios y salario en el *ejemplo* de la nómina; nombre, departamento y categoría profesional en el ejemplo de la
consulta selectiva. El **SGBD** deberá, con estos datos, acceder a la estructura física de la **BD** donde se encuentran almacenados los datos, localizar aquellos registros indicados y ponerlos a disposición del usuario.

La actualización o puesta al día de una **BD** supondrá 3
tipos de operaciones distintas:

* ==Inserción== --> cuando aparezcan nuevos elementos; por ejemplo, en un fichero de personal es preciso dar de alta a los nuevos empleados.

* ==Borrado== --> porque hayan desaparecido algunos elementos; *Ejemplo* en el fichero de personal es preciso dar de baja a los empleados que ya no están en la empresa.

* ==Modificación de los datos== --> Aquellos registros en los cuales se hayan producido cambios; por ejemplo, cuando se ha alterado la categoría profesional de un empleado.

La función de manipulación permite a los [[Usuarios|usuarios]] de la base, informáticos o no, buscar, añadir, suprimir o modificar los datos de la misma, siempre de acuerdo con las especificaciones y normas de seguridad dictadas por
el [[Administradores|administrador]].

Se llevará a cabo por medio de un lenguaje de manipulación de datos (*LMD o DML - Data Manipulation Language*) que facilita los instrumentos necesarios para la
realización de estas tareas. Muchas veces se trata de un conjunto de comandos (*lenguaje huésped*) que se escriben en un lenguaje de programación (*lenguaje anfitrión*) mientras que otras veces se trata de un lenguaje autocontenido que no precisa apoyarse en ningún otro lenguaje, ya que dispone en sí mismo del conjunto de instrucciones necesarias para llevar a cabo tanto la recuperación como la actualización de los datos. La mayoría de los **SGBD** actuales tienen ambos tipos de lenguajes, huéspedes y autocontenidos; estos últimos, orientados a los [[Usuarios|usuarios]] no informáticos, suelen usarse de forma interactiva.