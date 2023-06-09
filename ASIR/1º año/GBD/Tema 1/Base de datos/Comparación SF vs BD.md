#GBD

Algunos **SI** antiguos, encontramos sistemas en los que existe una gran cantidad de ficheros, específicos de una determinada aplicación. Se recogen los datos varias veces y se encuentran repetidos en distintos archivos:
    • Ocupación inútil de memoria secundaria.
    • Aumento del tiempo de proceso, al repetirse las mismas operaciones en los distintos ficheros.
    • Inconsistencias en los datos, al intentar actualizar datos repetidos en varios ficheros.
    • Falta de adaptabilidad a los cambios debido a la dependencia de los datos respecto al soporte físico y a los programas.
    • Imposibilidad de implementar un sistema de ayuda a la toma de decisión con esta configuración.
    • Anomalías con accesos concurrentes a los ficheros de datos. 
    • Costosa recuperación de ficheros por antigüedad de copias de seguridad.
    • Problemas de seguridad y confidencialidad: No todos los usuarios deben tener acceso a todos los datos. Como mucho ofrecen sistemas de protección a lvl de aplicación, pero nunca a lvl de usuario.
    
    ![[Pasted image 20221105150240.png]]

De esto se deduce la necesidad de una gestión más racional del conjunto de datos, surgiendo un nuevo enfoque que se apoya sobre una **BD**, en la cual los datos son recogidos y almacenados 1 sola vez, sin estar diseñados para una aplicación concreta, sino que tiende a satisfacer las necesidades de información de toda la organización.

![[Pasted image 20221105150253.png]]







