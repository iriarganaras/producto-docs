# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - INTERNET MITIGADO

## 1. INTRODUCCIÓN

El servicio de Internet Mitigado permite detectar y mitigar los ataques de DDoS (Distributed Denial of Service o denegación de servicio distribuido) de forma automatica, a nivel capa de transporte (layer 4) ofreciendo al cliente continuidad del servicio en forma transparente, sin degradación parcial o total del enlace contratado. Este servicio Permite la monitorización pasiva y no intrusiva del tráfico Nacional e Internacional, debido a que se analiza la información en forma estadística. Una vez detectada una amenaza, el tráfico malicioso, se limpia, enviando solamente tráfico legítimo al cliente y asegurando la continuidad del servicio. 

## 2. DESCRIPCIÓN DEL SERVICIO
El sistema de detección y mitigación de ataques de denegación de servicios distribuidos (DDoS) consiste en una mitigación inteligente del tráfico malicioso o no deseado, mediante técnicas basadas en el análisis del comportamiento y patrones de la red, quienes permiten usar sistemas de monitoreo para la detección temprana de amenazas, proporcionando opciones de solución sin impactar el rendimiento de la red.

La solución de Mitigación incluye el monitoreo permanente y continuo de los patrones de tráfico, lo que permite la detección en forma temprana del ataque volumétrico proveniente de los enlaces nacionales e internacionales de Internet, este monitoreo proporciona la utilización de listas blancas y/o negras.

La solución de Mitigación esta implementada en la Red de Metrotel permitiendo la entrega de tráfico limpio al cliente, no afecta en ningún caso el ancho de banda, rendimiento o latencia de los vínculos contratados por el cliente. Cuenta con la capacidad de interactuar entre los nodos contratados por el cliente.

Ante un intento de ataque DDoS, y luego de que dicho ataque supere un porcentaje determinado del ancho de banda total contratado por el cliente, el sistema está preparado para redirigir la totalidad del tráfico hacia los puntos de mitigación del Backbone (zona de limpieza), donde se realizara un filtrado inteligente y mediante el cual se separara, en tiempo real, el tráfico legitimo del tráfico malicioso. El tráfico malicioso es descartado, mientras que el tráfico genuino se vuelve a dirigir a la red del cliente.

La solución de Internet Mitigado puede complementarse con Hardware especifico (APS) en el sitio del cliente para lograr la detección temprana de anomalías estadísticas, mal uso de protocolos, detección de avalanchas y la coincidencia de fingerprints. De esta forma se genera una defensa contra los ataques que pretenden agotar el ancho de banda (ataques volumétricos) y contra los que van dirigidos a la capa de chatchatchaaplicaciones en servicios IP críticos, tales como el sistema de nombres de dominio (DNS), HTTP o el protocolo de voz sobre Internet (VoIP). Esta solución no está incluida en el servicio descripto en el presente documento, es complementaria y requiere de un análisis técnico por parte de personal de Metrotel para su cotización y puesta en marcha.

### Ventajas y Beneficios de Internet Mitigado
- **Protección de servicios:** Protege sus servicios críticos, como los de voz, vídeo, Web, plataforma E-commerce y correo electrónico contra ataques volumétricos.
- **Protección de la infraestructura:** Detecta y elimina ataques en routers, conmutadores, firewalls, ancho de banda y servicios DNS, mantiene el tráfico ilegítimo fuera de la red
- **Optimización de recursos:** Visibilidad del tráfico e informes exhaustivos y periódicos para mejorar la ingeniería del tráfico y solucionar problemas de forma más rápida y eficaz.
- **Esquema de la solución de Mitigación**

![esquema de solucion de mitigación](../../../imagenes/int-mitigado/esquema%20de%20solucion%20de%20mitigacion.png)

## 3. PROCEDIMIENTO ANTE UN ATAQUE

+ El sistema generará alertas en base a los valores definidos para "trigger rate" y "high severity rate".
+ Estos valores se encuentran definidos en la planilla "shared host detection settings" que se entrega al cliente al momento de contratar el servicio, dentro de "Planilla de Criterios de Mitigación". Dicha planilla cuenta con los parámetros estándar pero el cliente puede pedir modificarlos.
+ En caso de detectarse tráfico que superan los valores definidos para "trigger rate" se generará una alerta del tipo LOW.
+ Las alertas de tipo HIGH que se generen sobre MOs (Managed Objects) de clientes los cuales tengan habilitada la auto-mitigación (valor por defecto - el cliente puede modificarlo si así lo prefiere), dispararán dicha auto-mitigación. Es decir, el sistema de manera automática e inmediata comenzará a aplicar las contramedidas al tráfico considerado espurio.
+ De manera simultánea al comienzo de la auto-mitigación, los operadores del NOC recibirán una alerta en el sistema de monitoreo y analizarán que acción tomar dependiendo si se considera un verdadero ataque o un falso positivo.
+ Para poder realizar dicho análisis se comunicarán con los contactos que el cliente completó en la "Planilla de Criterios de Mitigación". De esta manera se busca lograr una mitigación del ataque efectiva y afectar mínimamente dentro de lo posible el tráfico "legal" del cliente. La importancia de la comunicación con el cliente al momento del ataque radica en que este pueda aportar al NOC información sobre por ejemplo servicios nuevos que el cliente haya implementado accesibles desde internet.
+ Los operadores especializados del NOC activarán entonces la mitigación en el sistema Arbor y este nos permitirá visualizar de una manera clara y en tiempo real el tráfico malicioso mitigado (rojo) y el tráfico "legal" que se deja pasar (verde). Podrá observarse el tráfico malicioso en forma detallada (ip/puerto origen/destino) y que tipo de ataques incluye.
+ Pudiendo incluso descargarse un pcap en tiempo real de dicho tráfico (Sample Packets) y diversas estadísticas con información de ip/puerto-origen/destino, tipo de ataque detectado (tcp syn, invalid packets, DNS Amplification, etc), países/ASN origenes, etc.
+ El proceso de mitigación consiste en la aplicación de contramedidas y el sistema nos permite ver de manera clara, real-time y en base a gráficas, cuanto tráfico va mitigando cada una de estas contramedidas.
+ La mitigación se mantendrá hasta que se visualice que el ataque cesó.

### Tiempos de respuesta de la solución de Internet Mitigado ante un incidente

+ Tiempo aproximado de detección de un ataque DDoS: 5 minutos una vez detectado estadísticamente <sup>(*1)</sup>.
+ Tiempo aproximado de comunicación con el cliente para informar ataque: 15 minutos posterior a la detección.
+ El tiempo aproximado de reposición de servicio (mitigación y entrega de tráfico limpio al cliente): 30 minutos, (dependiendo del volumen de ataque este tiempo podrá ser mayor).
  
Los valores expresados anteriormente son para ataques que no superen los 10 GB, Metrotel se reserva el derecho de hacer blackhole cuando el ataque supere dicho volumen y/o ponga en riesgo la infraestructura propia.

<sup>(*1)</sup> *Cuando el servicio es del tipo sin equipo en cliente, el tiempo de detección toma en promedio unos 60 minutos en ser detectado. El tiempo es en promedio porque el mismo dependerá del tipo de ataque como también de la cantidad de ancho de banda de este.*

### Tipos de ataques

El sistema de detección y mitigación de ataques DDoS, se encuentra en capacidad de cubrir los siguientes tipos y modelos de ataque.
+ Variaciones del perfil de tráfico.
+ Mal uso de protocolos, paquetes mal formados.
+ Escaneo de puertos y direcciones no utilizadas.

Según la base de conocimiento, sobre informes de patrones, tipos de ataques y orígenes de estos.
El sistema de detección y mitigación de ataques DDoS, se encuentra en capacidad de detectar los siguientes tipos de ataques provenientes de enlaces nacionales o internacionales de Internet:

+ Spoofed: Envío de paquetes con una dirección de origen falsificada.
+ Malformed: Envío de paquetes con bits o flags encendidos de manera anormal.
+ Floods: Envío en gran cantidad de paquetes conformados de manera legítima.
+ Null: Envío de paquetes sin contenido.
+ Protocol: Envío de paquetes con protocolos ilegítimos.
+ Fragmented: Envío de paquetes fragmentados, los cuales nunca serán completados.
  
## 4. DASHBOARD Y REPORTES

![dashboard y reportes](../../../imagenes/int-mitigado/dashboard%20y%20reportes.png)

El sistema de detección y mitigación de denegación de ataques DDoS, se encuentra en capacidad de proporcionar entre otros los siguientes reportes:
+ Monitoreo en tiempo real: Detecta las variaciones de tráfico en la red, permitiendo actuar en forma inmediata.
+ Alerta de ataques.
+ Información de alarmas en curso, de alarmas recientes.
+ Clasificación de alarmas según su grado de impacto o severidad (Alto, medio, bajo).
+ Información detallada sobre ataques y anomalías, proporcionando graficas de actividad, orígenes y destinatarios, puertos de entrada y salida, protocolos, ancho de banda del ataque.
+ Información detallada sobre cada ataque detectado y por categoría de ataque, detallando el ancho de banda en bytes, bit por segundo, paquetes por segundo.
+ Informe grafico del porcentaje de ataque sobre tráfico total del vínculo contratado.

## 5. RESPONSABILIDADES DEL CLIENTE

En el caso de que la intervención requiera que Metrotel se comunique con el Cliente, dicha comunicación se realizará en forma telefónica y/o vía e-mail. A tal fin el Cliente deberá especificar en la presente Solicitud la persona de contacto primario con Nombre y Apellido, Número Telefónico Fijo, Número de Teléfono Móvil, dirección de e-mail y un contacto secundario con la misma información.
+ El cliente es responsable de mantener actualizada la información sobre las Ips y Prefijos a mitigar. Metrotel no es responsable sobre redes no informadas durante el transcurso del contrato.
+ El Cliente es responsable de informar a Metrotel de cualquier cambio que se produzca en la información de las personas de contacto.
+ El cliente es responsable de proporcionar un lugar adecuado (sala, o rack) para la instalación del equipamiento provisto por Metrotel. El lugar debe tener condiciones de temperaturas adecuadas (-5 a +40 grados), libres de polvo, apartados del tránsito de personas y con restricciones de acceso. Cualquier daño o indisponibilidad producto de un mal ambiente será imputado al cliente.
+ La energía para el equipamiento provisto por Metrotel debe ser brindada por el cliente. Metrotel proporcionará las especificaciones técnicas de las necesidades de energía dejando a criterio del cliente el dimensionamiento de térmicas, la utilización de UPS, etc. Es responsabilidad directa del cliente la disponibilidad del servicio producto de la energización.
+ Metrotel proporcionará al cliente un puerto Ethernet físico donde conectar el servicio de INTERNET I Mitigado. Será responsabilidad del cliente conectar su red LAN al puerto proporcionado por Metrotel, así como también de la administración del equipamiento en su LAN. Las interconexiones entre el equipamiento de Metrotel y su red LAN debe ser por medio de Switches con capacidad de configuración manual de las características físicas del puerto (velocidad/dúplex). Se excluye explícitamente el uso de HUBs. Cualquier problema de performance en la red LAN interna del cliente será responsabilidad del Cliente.
+ La configuración y administración de Firewalls para distribuir el servicio internamente (ya sea con NAT/PAT para las PCs o DMZ para servidores) será responsabilidad del cliente. Cualquier problema asociado a este dispositivo no será imputable a Metrotel. Solo se exceptúa esta medida si se toma el servicio con opcional de Router y el servicio es configurado por Metrotel con las condiciones detalladas.
+ No será responsabilidad de Metrotel reclamos por tráfico que surjan por manipulación de redes por parte del cliente mediante BGP. Se recomienda realizar estos cambios juntamente con Metrotel o en su defecto informándolos.
+ Si el cliente tiene una arquitectura de DUAL HOME con otro proveedor de internet, cualquier cambio del tráfico producto de la variación de redes no será imputable a Metrotel. Es responsabilidad del cliente la administración de su tráfico a nivel BGP.

## 6. LIMITACIONES DEL SERVICIO

A excepción de los posibles ataques DDoS descriptos en el presenta documento, la seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Se recomienda el uso de programas Antimalware, Firewalls y cualquier software o hardware vigente y actualizado que evite estos ataques.

El cliente entiende que Internet es una red pública y expuesta a ataques. No será responsabilidad de Metrotel los ataques dirigidos en la capa de aplicación (capa 7), estos están excluidos en la solución de Internet Mitigado, descripta en el presente documento, no obstante, y como se detalló en párrafos anteriores, Metrotel dispone de soluciones complementarias que requieren hardware adicional en el sitio del cliente para mitigar este tipo de ataques.

El Servicio contempla la detección y mitigación de ataques de DoS y DDoS volumétricos, provenientes de los vínculos Internacionales a Internet que posee Metrotel. El ataque máximo que se podrá mitigar con la plataforma de mitigación inteligente es de hasta 10 Gigas; para cualquier otro tipo de ataque, Metrotel realizará sus mejores esfuerzos por detectarlo y mitigarlo sin garantizar ni comprometer su identificación y/ o filtrado.

Superada la capacidad arriba mencionada, Metrotel se reserva el derecho a la des publicación del Servicio de Conexión a Internet.

---



# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - INTERNET DEDICADO

## 1. DESCRIPCIÓN GENERAL

El servicio INTERNET INT provisto por Metrotel, ha sido especialmente diseñado para ofrecer una conexión a Internet de alta calidad para Carriers y Empresas. Se trata de una conexión dedicada, permanente, simétrica, de excelente disponibilidad y variantes de velocidades a la medida de su negocio.

## 2. ALCANCE Y ESPECIFICACIÓN TÉCNICA

El servicio de INTERNET INT será provisto en modalidad FTTO (Fiber To The Office) utilizando tecnología de avanzada en redes de acceso de fibra óptica. <sup>(*1)</sup>

El servicio consiste en la provisión de un vínculo físico para la transmisión de información sobre la red Internet. Este vínculo ofrece ancho de banda en múltiples variantes hasta 10Gbps. También pueden ser contratadas velocidades superiores a 10Gbps en soluciones diseñadas específicamente a la medida de cada cliente. La velocidad de acceso indica, en cualquiera de las versiones del producto, la capacidad máxima del vínculo de interconexión a Internet brindado por el servicio de Metrotel. Dicha velocidad es simétrica, lo que implica que se puede alcanzar la velocidad contratada tanto en sentido hacia como desde Internet, simultáneamente.

El servicio INT es un producto destinado a brindar acceso tanto a tráfico nacional como internacional en cualquier proporción, adicional al servicio se deberá incluir un rango de direcciones IP’s fijas y públicas. Esto significa que la IP no cambia al reiniciarse el equipamiento de acceso instalado en el cliente, como si ocurre con los servicios de IP dinámica (provistos mediante DHCP –Dynamic Host Configuration Protocol). También es posible ampliar la cantidad total de IPs fijas contratadas, aclarando que, si la contratación del adicional no se realiza en el momento inicial, implicará un cambio del rango de direcciones IP. <sup>(*2)</sup>

En caso de requerirse una migración de direcciones IP, Metrotel permitirá la convivencia del rango actual y el nuevo rango por un período de 15 días corridos, tras lo cual se dará de baja el rango original.

Por tratarse de un servicio especialmente pensado para Empresas y Carriers, el producto INTERNET INT cuenta con la posibilidad de establecer sesiones BGP contra routers de peering de Metrotel brindándole al cliente la flexibilidad de administrar dinámicamente sus redes.

<sup>(*1)</sup> *En algunas locaciones, si bien el backbone es de fibra óptica, la última milla se logra con enlaces y redes de terceros.*

<sup>(*2)</sup> *El cliente autoriza a Metrotel a proveer sus datos personales para la registración del rango IP asignado ante lacnic http://www.lacnic.net/ Metrotel asegura que al momento de la asignación de IPs, las mismas no se encuentran registradas en listas negras. Una vez entregadas las mismas es responsabilidad del cliente el uso y las acciones que se realicen desde las IPs Públicas otorgadas. En el caso que el cliente no posea ASN propio, Metrotel podrá publicar las IPs del cliente sobre el ASN de Metrotel mediante la utilización de rutas estáticas. En ambos casos se requiere el envío de la correspondiente autorización para realizar las publicaciones de IPs o ASN propiedad del cliente hacia internet.*

### Opcionales

Metrotel cuenta con las siguientes opciones de INTERNET INT adaptándose a cada tipo de necesidad:
+ **INTERNET sin Router:** Es una opción económica que permite conectar la red del cliente directamente al acceso brindando acceso a INTERNET
+ **INTERNET con Router:** Esta opción es necesaria cuando se necesitan implementar soluciones escalables, configuración de NAT o DHCP. Esta opción se configura utilizando siempre BGP como protocolo de ruteo hacia el Backbone.

## 3. CARACTERÍSTICAS DEL SERVICIO

| Producto        | INT Sin Router | INT Con Router     |
|-----------------|---------------|--------------------|
| Versiones       | Hasta 10 GB    |                    |
| Código Producto | INT           | INT                |
| Tecnología      | FO (fibra óptica, <sup>(*1)</sup> ) |  FO (fibra óptica, <sup>(*1)</sup> ) |
| Simetría        | Si            | Si                 |
| IP Fija         | Si <sup>(*2)</sup>       | Si <sup>(*2)</sup>            |
| IP Pública      | Si            | Si                 |
| IPs adicionales | Justificables <sup>(*3)</sup> | Justificables <sup>(*3)</sup> |
| Ruteo BGP       | Si <sup>(*4)</sup>       | Si, hasta 2 sesiones <sup>(*5)</sup> |
| Reglas NAT      | No            | SI (hasta 5, <sup>(*6)</sup> )   |
| DHCP            | No            | SI (hasta 1 pool)  |
| Redundancia física | No         | Soportada <sup>(*7)</sup>     |
| Monitoreo SNMP  | No           | Comunitario, limitado a 5 OID de necesidad del cliente |


<sup>(*1)</sup> *En algunas locaciones, si bien el backbone es de fibra óptica, la última milla se logra con enlaces y redes de terceros.*

<sup>(*2)</sup> *Metrotel ofrece direccionamiento público IPv4 / IPv6. En IPv4 por subneting (RFC 4632) se destina una dirección al segmento de red, otra para el broadcast y finalmente una para el default Gateway, dejando el resto de IPs dentro del rango utilizables al cliente. Ejemplo: En caso de que el servicio INT sea contratado con un rango de 4 IP, el cliente dispondrá de 1 IP (una) para su uso, las otras 3 serán utilizadas por Metrotel para la configuración del servicio.*

<sup>(*3)</sup> *En caso de requerir IP adicionales, el cliente deberá justificar su uso. La asignación estará sujeta a disponibilidad y análisis por parte de Metrotel.*

<sup>(*4)</sup> *a) Una sola sesión BGP por servicio contratado. El cliente debe tener su propio AS (Sistema Autónomo). b) Metrotel no publicará ni aceptará publicación de redes más específicas que /24 en el peering BGP con el cliente. A su vez se le permite al cliente manejar los atributos de AS_PATH (con prepends) y Local Preference a su criterio para adecuar su tráfico según sus necesidades. c) A fin de garantizar el servicio, Metrotel publicará las redes del cliente por todos sus proveedores nacionales e internacionales de acuerdo con la normal operación. Esto implica que el cliente no podrá requerirle a Metrotel de forzar su tráfico por un proveedor específico. d) El tamaño de la tabla de ruteo publicada al router de cliente será limitada de acuerdo con la capacidad de este.*

<sup>(*5)</sup> *a) Hasta dos sesiones BGP por servicio contratado. El cliente debe tener su propio AS (Sistema Autónomo). b) Metrotel manejara los prefijos del cliente (/29) en caso de que el servicio sea completamente suscripto a Metrotel. En caso de que el servicio sea principal o redundante de otro proveedor, no publicará ni aceptará publicación de redes más específicas que /24 en el peering BGP con el cliente. A su vez se le permite al cliente manejar los atributos de AS_PATH (con prepends) y Local Preference a su criterio para adecuar su tráfico según sus necesidades. c) A fin de garantizar el servicio, Metrotel publicará las redes del cliente por todos sus proveedores nacionales e internacionales de acuerdo a la normal operación. Esto implica que el cliente no podrá requerirle a Metrotel de forzar su tráfico por un proveedor específico. d) El tamaño de la tabla de ruteo publicada al router de cliente será limitada de acuerdo con la capacidad de este.*

<sup>(*6)</sup> *Hasta 5 reglas NAT y hasta 5 ACL. Con estas opciones se puede configurar una DMZ básica (un servicio en Internet como por ejemplo Web Server o Mail Server) con su puerto de servicio correspondiente abierto y el resto filtrado.*

<sup>(*7)</sup> *El producto INTERNET INT con Router soporta redundancia de acceso físico a través de dos accesos a dos nodos distintos, puede manejar a través de BGP dos sesiones brindando redundancia al servicio. Dicha redundancia se contrata por separado, estará sujeta a disponibilidad y análisis por parte de Metrotel.*

### LAG: PortChannel

Políticas de Link Aggregation Group (en adelante LAG), es un método que permite brindar redundancia de puertos o ampliar bandwidth (en adelante BW) para cuando no se cuenta con la interface de la velocidad apropiada o contratada. Metrotel recomienda que el número de interfaces sean par y de las mismas velocidades de BW (ejemplo: 4 interfaces de 1Gb).

En el caso de necesidad de ampliar BW, se recomienda no superar la cantidad de 4 interfaces en total debido a que el protocolo es deficiente para balancear tráfico entre interfaces y el mismo varia de forma impredecible dependiendo del tráfico generado por cada cliente.

Por lo expresado, Metrotel no aconseja utilizar LAG para el servicio contratado, en cambio recomendamos que se brinde con 1 única interfaz capaz de cubrir la totalidad del tráfico contratado. Metrotel no se responsabilizará por reclamos realizados a causa de un mal dimensionamiento de cantidad puertos en LAG.

### Elephant Flow

En el caso que el cliente utilice "flujo continuo extremadamente grande" (elephantFlow) superior a 3Gbps, debe notificarse previamente a Metrotel. Superado este tamaño Metrotel se reserva el derecho de tomar acciones correctivas, si este afectara la calidad del servicio o de la red. El cliente no podrá alegar falla en el servicio en este caso, y no computará como falla en el SLA ni como causa para la solicitud de baja sin penalidad.

### Redundancia – Puerto Adicional

Los puertos adicionales <sup>(*)</sup> existirán en el mismo equipo del puerto principal (sin excepción). El portal de Autogestión del cliente publicara solo el tráfico del puerto principal, no pudiendo dar visibilidad de los puertos adicionales. Cada puerto de forma independiente ya sea principal o adicional tiene la capacidad de brindar la totalidad del servicio, por lo cual ante la afectación de un puerto se podrá solicitar la reposición de este, pero no computara como indisponibilidad del servicio a menos que la totalidad de puertos estén afectados.

<sup>(*)</sup> *En caso de necesitar más de 1 (uno) puerto adicional, la habilitación de este estará sujeta a disponibilidad y análisis por parte de Metrotel.*

### Equipamientos para enlaces de terceros fuera de AMBA

En caso de que Metrotel provea un router propiedad de Metrotel para brindar el servicio sobre enlace por terceros, contratados por Metrotel para brindar el servicio, a más de 80 Km de CABA o Córdoba Capital, los reclamos asociados a reposición de este no computarán como falta del SLA contratado, mientras que el tiempo de reposición sea menor a 48 horas hábiles. El cliente acepta esta consideración como parte del servicio. No obstante, si se incluyera algún alcance particular, este último reemplazará y anulará lo mencionado previamente.

### Servicio de DNS
En caso de que el cliente requiera resolución de nombres para servicios propios, podrá utilizar el servicio de DNS provisto por Metrotel. A tal efecto tiene disponible una página de autogestión donde puede administrar sus dominios. Este servicio es ofrecido exclusivamente para las direcciones IP publicas asignadas por Metrotel.

## 4. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto (0800- 362-1040) mediante el cual podrá realizar la gestión de eventuales reclamos.

Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de esta.

## 5.MANTENIMIENTO PROGRAMADO

El mantenimiento programado consistirá en toda intervención realizada en la red de Metrotel, la cual será notificada previamente (con más de 48 horas de anticipación) al cliente y se realizará dentro del horario de mantenimiento establecido. Si el horario del corte previsto afecta la labor del cliente, éste puede solicitar la modificación de este. Metrotel se compromete a realizar los máximos esfuerzos para mover el corte al nuevo horario solicitado. Este tipo de interrupciones se puede realizar para reemplazar o agregar elementos a la red a fin de ampliar y mejorar permanentemente el servicio.

## 6. PUESTA EN MARCHA DEL SERVICIO

En aquellos casos en los que la provisión del servicio contratado requiera una instalación física en el domicilio del cliente, la misma será realizada por el personal de Metrotel o terceros que actuarán en nombre de Metrotel, quienes dejarán el servicio en condiciones de ser prestado y solicitarán al cliente el conforme vía la firma del Formulario “Informe de Instalación de Cliente”.

La firma de dicho formulario asume la conformidad del cliente respecto de la instalación y de la capacidad de utilizar el servicio en cuestión. En caso de que el servicio contratado no requiera presencia física del personal de Metrotel en el domicilio del cliente, se determinará el mejor medio para comunicar que se ha comenzado la prestación de dicho servicio.

## 7. DISPONIBILIDAD

La disponibilidad del servicio contratado es una medida que indica cuanto tiempo el cliente puede acceder a Internet respecto del total de tiempo en el que se brinda el servicio.

También se considerará como falta de disponibilidad el lapso durante el cual la red de Metrotel no tenga ninguna interconexión con el resto de la Internet, y este problema afecte al servicio del cliente. En caso de que el cliente utilice un servicio de resolución de nombres asociados a sus IPs en DNS de Metrotel, será considerado como falta de disponibilidad el período en el cual el servicio de DNS impida al cliente hacer uso del servicio contratado.

No serán considerados como falta de disponibilidad problemas de conectividad causados fallas en el equipo del cliente ni aquellos debidos a saturación de enlace, ya sea por tráfico genuino del cliente o bien por tráfico espurio (computadoras infectadas, programas p2p, ddos, etc). Tampoco serán considerados problemas de disponibilidad aquellos causados por fallas atribuibles a responsabilidad del cliente (ver ítem correspondiente). No se considerarán mediciones propias del cliente a los fines de disponibilidad, pero si a los fines de diagnóstico. Para los casos no contemplados por mediciones propias de Metrotel se tomarán como base para el cálculo de indisponibilidades las fechas y horarios de las aperturas y cierres de los tickets correspondientes, luego de haber sido sometidos a V12 2024-03 consideración de Metrotel donde quede claramente demostrado que no fueron resultantes de alguna falta en las responsabilidades del cliente. Para este último caso no serán computados como indisponibilidad.

Los registros y datos recopilados por Metrotel serán la base sobre la que se calculará la disponibilidad correspondiente. Para el cálculo de disponibilidad no se tendrán en cuenta las interrupciones ocasionadas por los mantenimientos programados previamente comunicados al cliente.

La disponibilidad será calculada de acuerdo con la siguiente fórmula: 

> *Disponibilidad = (T – D) / T x 100*

Dónde: 

**D** = Duración de la indisponibilidad (en minutos)

**T** = Duración del mes en cuestión (en minutos)

**Disponibilidad** = En porcentaje.

## 8. TIEMPO MEDIO DE RESTAURACIÓN

El tiempo de restauración es el tiempo transcurrido entre la hora de detección del problema (Por parte de Metrotel o bien a través de la notificación del cliente al área de Servicio de Atención al Cliente) y la hora de restablecimiento del servicio. El tiempo medio de restauración se calculará obteniendo el promedio de los tiempos de restauración del mes.

## 9. RESPONSABILIDAD DEL CLIENTE

A continuación, se detallan las responsabilidades del cliente:

+ El cliente es responsable de proporcionar un lugar adecuado (sala, o rack) para la instalación del equipamiento provisto por Metrotel. El lugar debe tener condiciones de temperaturas adecuadas (-5 a +40 grados), libres de polvo, apartados del tránsito de personas y con restricciones de acceso. Cualquier daño o indisponibilidad producto de un mal ambiente será imputado al cliente.
+ La energía para el equipamiento provisto por Metrotel debe ser brindada por el cliente. Metrotel proporcionará las especificaciones técnicas de las necesidades de energía dejando a criterio del cliente el dimensionamiento de térmicas, la utilización de UPS, etc. Es responsabilidad directa del cliente la disponibilidad del servicio producto de la energización.
+ Metrotel proporcionará al cliente un puerto Ethernet físico donde conectar el servicio de INTERNET INT. Será responsabilidad del cliente conectar su red LAN al puerto proporcionado por Metrotel, así como también de la administración del equipamiento en su LAN. Las interconexiones entre el equipamiento de Metrotel y su red LAN debe ser por medio de Switches con capacidad de configuración manual de las características físicas del puerto (velocidad/dúplex). Se excluye explícitamente el uso de HUBs.
  
Cualquier problema de performance en la red LAN interna del cliente será responsabilidad del Cliente.
+ El cableado de red desde el sitio donde se encuentra el Equipo Terminal instalado por Metrotel, hasta el equipamiento del cliente, debe ser categoría 5 ó superior. El cliente es responsable por el cableado con lo cual deberá tener adecuadamente certificados los cableados.
+ Metrotel monitoreará su servicio ya sea a través del equipo instalado en el cliente o bien en su equipamiento de BackBone. Será responsabilidad del cliente el mantenimiento, configuración y performance de su red LAN local. Cualquier degradación del servicio producida por el equipamiento del cliente (mala configuración, problemas de negociación), no será imputable a Metrotel.
+ La configuración y administración de Firewalls para distribuir el servicio internamente (ya sea con NAT/PAT para las PCs o DMZ para servidores) será responsabilidad del cliente. Cualquier problema asociado a este dispositivo no será imputable a Metrotel. Solo se exceptúa esta medida si se toma el servicio con opcional de Router y el servicio es configurado por Metrotel con las condiciones detalladas.
+ No será responsabilidad de Metrotel reclamos por tráfico que surjan por manipulación de redes por parte del cliente mediante BGP. Se recomienda realizar estos cambios juntamente con Metrotel o en su defecto informándolos.
+ Si el cliente tiene una arquitectura de DUAL HOME con otro proveedor de internet, cualquier cambio del tráfico producto de la variación de redes no será imputable a Metrotel. Es responsabilidad del cliente la administración de su tráfico a nivel BGP.
+ Será responsabilidad del cliente informar a Metrotel de cualquier anomalía percibida en el funcionamiento del servicio mediante la apertura del ticket correspondiente. A partir de este punto, corresponderá al cliente poner a disposición a los administradores de la red para que juntamente con personal calificado de Metrotel se pueda realizar el correcto diagnóstico y corrección de la falla. Cualquier reclamo sobre el servicio será tomado sobre la base de fechas y horarios de apertura de tickets dejando a consideración de Metrotel la revisión de su contenido. Todo tiempo adicional entre la apertura y cierre de ticktet que sea consecuencia de indisponibilidad de los administradores de red del cliente (en caso de requerirse) no será computado a los fines del reclamo.

## 10. LIMITACIONES DEL SERVICIO

El cliente reconoce que Metrotel no puede ejercitar control sobre el contenido de la información que circula a través de la red Internet. Por lo tanto, Metrotel no es responsable del contenido de ningún mensaje y/o información tanto si el envío fue hecho o no por un cliente de Metrotel.

La seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Se recomienda el uso de programas Antimalware, Firewalls y cualquier software ó hardware vigente y actualizado que evite estos ataques.

El resguardo de la información en los equipos / sistemas del cliente queda bajo su exclusiva responsabilidad. Se recomienda el uso de software ó hardware para resguardo y respaldo de la información almacenada en los equipos y sistemas del cliente.

El cliente reconoce que Metrotel no tiene el control absoluto, extremo a extremo, en una conexión INTERNET siendo que la velocidad de transferencia trasciende la red de Metrotel y sus interconexiones directas. No obstante, Metrotel se compromete a mantener el extremo de la red bajo alcance, hasta la frontera con los diversos “Carriers” de interconexión local e internacional, con los más altos niveles de prestación de servicio, conforme la variante de producto.

El cliente entiende que Internet es una red pública y expuesta a ataques. No será responsabilidad de Metrotel degradaciones de performance del sistema o denegaciones de servicio producto de ataques del tipo distribuido, ya sean volumétricos o inteligentes. Aun así, Metrotel actuará con las mejores prácticas administrativas de red para mitigar los daños, pudiendo resultar que durante períodos de ataque no se reestablezcan correctamente todos los servicios.

El servicio INTERNET INT soporta hasta 300 MAC Address por servicio. <sup>(*1)</sup>. En el caso que se utilice el opcional de Router, este valor será el que cumpla el equipo por especificación técnica.

Para la resolución de nombres Metrotel brinda el servicio de DNS. Dicho servicio está disponible para que el cliente lo utilice libremente como así también propios o disponibles en Internet. Es por esto por lo que no será considerado parte de la disponibilidad del sistema. Esto último no aplica para el caso de asociar IPs a nombres, residiendo dicha configuración en los DNS de Metrotel.

Metrotel se reserva el derecho de realizar cambios y/o modificaciones del servicio de INTERNET si el consumo de ancho de banda supera límites de consumo netamente corporativo. Este servicio no está definido para la reventa de conectividad de Internet a terceros.

Cualquier servicio adicional al especificado en este documento requerido a Metrotel, será facturado como adicional al cargo de instalación y abono mensual convenido.

La tasa de transferencia máxima de un servicio siempre es menor a la velocidad física de puerto. Esto es debido a los overheads, gaps interframes y tamaño del paquete correspondiente al estándar IEEE 802.3. Metrotel no tomará reclamos producto de la eficiencia propia del protocolo Ethernet.

Jitter: Menor a 5 ms en condición 95 percentil <sup>(*2)</sup>

<sup>(*1)</sup> Si este valor no se ajusta a lo requerido por el cliente, dicho valor estará sujeto a disponibilidad y análisis por parte de Metrotel.
<sup>(*2)</sup> Estos valores son válidos para la última milla (sin tránsitos) exclusivamente sobre tecnologías de fibra óptica y solo pueden verificarse desde la red del cliente en una condición de uso menor al 50% del enlace