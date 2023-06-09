Capa de abstracción encima de un sistema de archivos concreto. 

Permite que las aplicaciones cliente tengan acceso a distintos tipos de sistemas de archivos de una manera uniforme. Se utiliza como un puente sobre los sistemas de archivos de **Windows**, de **Mac OS** y **Linux**, de modo que las aplicaciones accedan a los archivos sin saber a qué tipo de sistema de archivos están teniendo acceso.

Los archivos, normalmente, son de tipo texto o binarios. Sin embargo, el directorio */proc* de **Linux** contiene otro tipo de archivo llamado ***archivo virtual***, ya que contiene una gran cantidad de información con detalles sobre el hardware del sistema y cualquier proceso que se esté ejecutando en ese momento. Algunos de dichos archivos pueden ser manipulados por los usuarios y las aplicaciones para comunicar al kernel cambios en la configuración.

Por esta razón, a menudo se hace referencia al directorio /proc como un sistema de archivos virtual.