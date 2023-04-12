#PAR #Arquitectura_redes #Modelo_OSI 

# Mala sincronización

Los [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo TCP-IP/Concepto|protocolos de TCP/IP]] se usaban ampliamente en universidades que hacían investigación cuando aparecieron los [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|protocolos de OSI]]. Antes de que llegara la ola de inversión de millones de dólares, el mercado académico tenía el tamaño suficiente para que los proveedores empezaran a ofrecer con cautela los productos __TCP/IP__. Cuando __OSI__ llegó, no quisieron apoyar una segunda pila de protocolos hasta que se les forzó, de modo que no hubo ofertas iniciales. Al estar cada compañía en espera de que otra tomara la iniciativa, ninguna compañía lo hizo y __OSI__ nunca sucedió. 

# Mala tecnología

El modelo como los protocolos son imperfectos. La mayor parte de las explicaciones acerca del modelo de las 7 capas da la impresión de que la cantidad y el contenido de las capas finalmente seleccionadas eran el único camino. La [[5 - Sesión|capa de sesión]] tiene poco uso en la mayor parte de las aplicaciones, y la [[6 - Presentación|capa de presentación]] casi está vacía. 

El [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|modelo OSI]] tiene 7 capas porque en el momento en que se diseñó ___IBM___ tenía un protocolo patentado de 7 capas llamado __SNA__ (_Systems Network Architecture_). 

En esa época, ___IBM___ dominaba la industria de la computación a tal grado que las compañías de teléfonos, las compañías de computadoras de la competencia y hasta los principales gobiernos sentían pánico de que ___IBM___ usara su fuerza en el mercado para obligar prácticamente a todos a usar __SNA__, el cual podría cambiar en el momento que quisiera. Lo que se pretendía con [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|OSI]] era crear un modelo de referencia y pila de protocolos semejante al de __IBM__ que se pudiera convertir en el estándar mundial y estuviera controlado no por una compañía sino por una organización neutral, la [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|ISO]]. 

* Junto con las correspondientes definiciones y protocolos de servicios, es extraordinariamente completo. También son difíciles de implementar e ineficientes en su operación. 

* El direccionamiento, el control de flujo y el control de errores reaparecen una y otra vez en cada capa. Sin embargo, está demostrado que para ser eficaz, el control de errores se debe hacer en la capa más alta, de modo que repetirlo una y otra vez en cada una de las capas inferiores con frecuencia es innecesario e ineficiente. 

* Colocar ciertas funciones en capas particulares no siempre es obvia. La seguridad de los datos y el cifrado eran tan polémicos que nadie podía ponerse de acuerdo en qué capa ponerlos, así que se dejaron fuera. 

* Ignoró por completo los servicios y protocolos no orientados a conexión, a pesar de que casi todas las redes de área local trabajan de esa manera. 

# Mala instrumentación

Las implementaciones iniciales fueran enormes, inmanejables y lentas. Todos los que las probaron se arrepintieron. La gente asocio “[[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|OSI]]” con “_mala calidad_”.

En contraste, una de las 1º implementaciones de [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo TCP-IP/Concepto|TCP/IP]] fue parte del UNIX de Berkeley y era bastante buena (_gratuita_).

# Mala política

Gracias a la implementación inicial, mucha gente, en especial los académicos, pensaban en [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo TCP-IP/Concepto|TCP/IP]] como parte de UNIX, y UNIX en la década de 1980. En cambio, se veía a [[PAR/Tema 2/3. Arquitectura de comunicaciones/Modelo OSI/Concepto|OSI]] como una invención de los ministerios europeos de telecomunicaciones, de la Comunidad Europea y, más tarde, del gobierno de Estados Unidos 

