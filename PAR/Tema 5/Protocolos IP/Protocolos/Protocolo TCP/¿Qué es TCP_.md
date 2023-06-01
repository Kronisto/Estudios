#PAR #TEMA_5 

Crea conexiones dentro de una red de datos compuesta por redes de *nodos*, para intentar garantiza que los datos serán entregados en su destino sin errores y en el mismo orden en que se enviaron y proporciona un mecanismo que distingue las distintas aplicaciones dentro de una misma máquina, a través de los “***puertos***”

Proporciona un transporte de datos libres de errores a través de una subred no libre de errores. ==Diseñado para ser robusto ante fallos de la subred y adaptarse dinámicamente a las propiedades de la misma.==

Una entidad TCP acepta corrientes de Bytes de los procesos de la capa de aplicación, los fracciona en bloques que no excedan de 64 KB, y los entrega como datagramas independientes a la capa de red para su viaje hasta el destinatario. En el destino, TCP recibe los datagramas entregados por la capa de red, que son reensamblados para reconstruir la corriente de Bytes original.