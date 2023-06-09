Las distintas funciones que ha de cumplir un SGBD hacen necesario
disponer de diferentes tipos de lenguajes y procedimientos que permitan la
comunicación con la base de datos; unos están orientados hacia la función
(definición o manipulación) y otros dirigidos a diferentes tipos de usuarios o de
aplicaciones. Si lo vemos esquemáticamente, tenemos los siguientes tipos de
lenguajes:
 Por tipo de función:
 Definición
 Manipulación
 Por tipos de usuarios y de aplicaciones
 Informáticos
 Finales
 Aplicaciones formalizables (como la gestión de personal).
 Aplicaciones no formalizables (como los procesos de toma de
decisiones).
Cuando se trata de procesos formalizables y muy repetitivos, el
programador se encarga en general de escribir los correspondientes programas,
que muchas veces son sometidos a un tratamiento por lotes, con periodicidad fija
(emisión diaria de recibos, obtención mensual de la nómina, etc.) o a un
tratamiento interactivo (consultas).
Por el contrario, si el proceso es difícilmente formalizable o no es lo
suficientemente repetitivo, escribir un programa puede no resultar rentable, y
suele ser más conveniente que el mismo usuario final resuelva directamente la
consulta mediante los instrumentos que el SGBD pone a su alcance.
También el SGBD debe proporcionar al administrador de la base de datos
un conjunto de procedimientos que le faciliten su tarea.
Los lenguajes de los SGBD habrán de tener, por tanto, un enfoque
distinto según el tipo de usuario, ya que las exigencias de un programador o del
administrador no tienen nada que ver con lo que puede necesitar un usuario no
informático.
En general, los usuarios informáticos (diseñador, administrador,
analistas, programadores, etc.) requerirán medios potentes y flexibles mediante
los cuales consigan definir, administrar, extraer o manipular los datos de la base.
En muchos casos desearán apoyarse en el lenguaje de programación que están
habituados a manejar (lenguaje anfitrión), para lo cual deberá permitir hacer
llamadas desde un programa de aplicación al SGBD. El conjunto de sentencias de
manipulación del SGBD que pueden ser llamadas desde un lenguaje de
programación, permitiendo así el acceso a la base de datos, se suele denominar
sublenguaje de datos y también lenguaje huésped o lenguaje embebido.
El usuario final requerirá medios simples para comunicarse con la base, lo
que se puede conseguir mediante un lenguaje de manipulación autocontenido
que tenga una sintaxis sencilla, pero lo suficientemente potente como para
soportar demandas de información muy variadas, o por medio de tratamientos
parametrizados que suelen presentarse al usuario en forma de menús.