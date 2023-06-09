El modelo orientado a objetos se basa en encapsular código y datos en
una única entidad, llamada objeto. El interfaz entre un objeto y el resto del
sistema se define mediante un conjunto de mensajes.
Un objeto tiene asociado:
 Un conjunto de variables que contiene los datos del objeto
 Un conjunto de mensajes a los que el objeto responde.
 Un método, que es un trozo de código para implementar cada
mensaje.
Los objetos similares en una BD se agrupan formando clases,
organizadas en forma jerárquica.
Un SGBD orientado a objetos permite:
 Herencia. Heredan características de su clase
y de sus
antecesores.
 Polimorfismo. Distintos métodos con el mismo nombre en el
mismo objeto.
 Objetos complejos. Objetos que contienen otros objetos, por
ejemplo, relaciones que pueden almacenarse en otras relaciones.
 Datos de comportamiento. Distintos objetos necesitan responder
de diferente manera a la misma orden. Por ejemplo, la eliminación
de ciertas tuplas puede requerir la eliminación de otras tuplas
asociadas.
 Metaconocimiento. A menudo son más importantes reglas
generales sobre la relación, más que las tuplas específicas. Por
ejemplo, la regla “Todas las cuentas con saldo mayor de 100000
pagan el 5% de interés”. Esta regla no se puede representar
fácilmente en un SGBD tradicional, mientras que en uno orientado
a objetos si se puede.