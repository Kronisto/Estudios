#GBD

# Ficheros internos y externos

==externos o permanentes== --> Se pueden guardar en una memoria externa puesto que sirven para almacenar datos que deben permanecer en el sistema aunque éste se apague.

==Internos o temporales== -->Durante la ejecución de un programa se trabaja con unas estructuras de datos análogas a los ficheros, se encuentran en la memoria interna, y almacenan aquellos datos que van a ser inmediatamente utilizados para desaparecer a continuación (*o se volverán a grabar en la memoria externa*).

# Según su uso

• ==Constantes== --> Información que no varia en el tiempo, o lo hace muy de cuando en cuando. Por ello, apenas se modifican, o nunca. _Ejemplos_: provincias de un país, los códigos postales...

• ==Maestros== --> Información que necesita actualizaciones frecuentes (_altas, bajas, modificaciones_). _Ejemplo_: ficheros de clientes, de alumnos...
    
• ==Históricos== --> Información sobre hechos pasados e inamovibles, solo se utilizan para consultas y estadísticas; así pues, no sufren cambios, excepto la incorporación de nuevos datos. *Ejemplo*: historial con las notas de años anteriores, cada año se añadirán las notas del curso que acaba. 

# Según su organización y acceso:

Un fichero está formado, por registros. Estos registros están ordenados físicamente, pero ese orden puede ser aleatorio o puede estar en función de alguno de los campos. *Ejemplo*, personas ordenadas alfabéticamente por su apellidos. 
    • ==Acceso secuencial por posición== --> El fichero debe leerse siempre empezando por el registro que ocupa físicamente el 1º  lugar y continuando de manera secuencial, de 1 en 1, hasta llegar al registro que se busca, o bien al final físico del fichero.
    • ==Acceso directo por posición== --> Si se conoce cuál es la posición exacta que ocupa un registro dentro del fichero, puede accederse directamente a dicho registro solicitando.
    • ==Acceso secuencial por valor== --> Siguiendo el orden de alguno de los campos.
    • ==Acceso directo por valor== --> El fichero está organizado de manera que dando el valor de un atributo o conjunto de ellos, generalmente formando una clave de tipo ir al alumno con expediente nº 12, se pueda acceder directamente al registro correspondiente.

![[Pasted image 20221105145635.png]]

Según el tipo de acceso que permita cada fichero, se puede hacer la siguiente clasificación, aunque está obsoleta:
    • ==Secuenciales== --> ficheros que sólo permiten el **acceso secuencial por posición**, de manera que cuando se abren únicamente es posible leer el 1º registro y, a continuación, el registro que ocupa la posición siguiente, y así sucesivamente hasta el final del fichero. Los registros nuevos se insertan siempre al final del fichero; por tanto, sólo hay un orden físico, sin ningún orden lógico, o por valor, equivalente. 
    • ==Relativos== --> ficheros donde cada registro se identifica por su posición relativa respecto al inicio del fichero y, por este motivo, se permite el acceso directo por posición si ésta es conocida. En caso contrario siempre puede utilizarse el **acceso secuencial por posición**, que también está admitido.
    • ==Calculados== --> Es una variante de los ficheros relativos donde la posición del registro viene determinada por el valor de algún o varios atributos o de un cálculo realizado a partir de dichos valores. En estos casos, se puede realizar tanto el acceso secuencial por valor como el acceso directo por valor. En los ficheros calculados es más problemático el acceso directo por posición, aunque es posible.
    • Indexados: Se trata de un tipo especial de ficheros que se presenta como una mezcla de los anteriores. Aparte del fichero que contiene los datos existe otros fichero, o a veces más de 1, denominado índice. 
        ◦ Fichero índice: guarda información relacionada con la posición que ocupan algunos registros, o a veces todos, y facilita la búsqueda de los mismos. Como el índice de un libro