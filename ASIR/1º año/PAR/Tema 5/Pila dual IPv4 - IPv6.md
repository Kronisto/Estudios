#PAR #TEMA_5 

**dual stack**: *IPv6* mantiene casi todo el funcionamiento de *IPv4*, es relativamente fácil escribir una pila de protocolos que implemente ambos protocolos compartiendo gran parte del código.

Las implementaciones dual stack *IPv4/IPv6* soportan normalmente 1 tipo de dirección llamado “**dirección *IPv4* mapeada**”. Esta dirección se caracteriza por tener sus primeros 80 bits a 0, los siguientes 16 a 1 y los útimos 32 representan una dirección IPv4:

- **::ffff:0:0/96** Dirección *IPv4 mapeada*.

- **::1.2.3.4** Dirección *IPv4 compatible (obsoleto)*.

Ejem: **::ffff:c0a8:a78** = **192.168.10.120** y otra forma de expresarla **::ffff:192.168.10.120** (*IPv4 compatible*).