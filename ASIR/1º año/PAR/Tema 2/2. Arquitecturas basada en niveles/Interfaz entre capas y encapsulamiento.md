#PAR #Arquitectura_redes

Las __entidades__ (_elementos activos de cada capa_) de la misma capa en máquinas diferentes se llaman __entidades pares__. Las entidades de la capa ___n___ implementan un servicio que usa la capa ___n+1___. En este caso la __capa__ ___n___ se llama __proveedor del servicio__ y la __capa__ ___n+1___ es el usuario del servicio. La capa ___n___ puede usar los servicios de la capa ___n-1___ con el fin de proveer su propio servicio puede ofrecer varias clases de servicio.

Los servicios están disponibles en los __SAP__ (_Service Access Points_). Los __SAP__ de la capa ___n___ son los lugares en los que la capa ___n+1___ puede tener acceso a los servicios ofrecidos. Cada __SAP__ tiene una dirección que lo identifica de manera única.  

En el servicio telefónico, un __SAP__ son los enchufes en donde se conectan los teléfonos y las direcciones de los __SAP__ son los nº de abonado correspondientes a esos enchufes.

Para que haya intercambio de información entre 2 __capas__, debe existir un conjunto de reglas acerca de la interfaz. 

En una interfaz típica, la entidad de la __capa__ ___n+1___ pasa un __IDU__ (_Interface Data Unit_) de la interface a la __capa__ ___N___, a través del __SAP__,

El __IDU__ está formado por una __SDU__ (_Service Data Unit_) y de __ICI__ (_Information Control Interface_). 

![[IDU.png]]

### ICI (_Interfaz Control Information_)

información de control destinada a la __capa__ que la recibe en su __SAP__, que es necesaria para que la __capa__ inferior realice su trabajo (*ejemplo, la cantidad de bytes en la __SDU__*) pero no forma parte de los datos mismos. 

### SDU (_Service Data Unit_)

información que se pasa mediante la red a la entidad par de la estación destino y que esta entidad par entregará a la __capa__ ___n+1___. La __capa__ ___n___ puede dividir la __SDU__ en varios trozos o encadenar varias __SDU__ para formar una de mayor tamaño. Todo depende de lo que se solicite en la __ICI__, de las especificaciones del protocolo de __capa__ ___n___, y de la configuración del protocolo para ese servicio. 

### PDU (_Protocol Data Unit_)

información que la __capa__ ___n___ envía a su entidad par. Se compone de la __SDU__ entregada por la __capa__ superior a la que se le añade una cabecera de la __capa__ ___n___ con información de control destinada a entidad par, que le indica cómo tratar la información recibida. 
