# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - ANEXO TÉCNICO RPV RED PRIVADA VIRTUAL

## 1.DESCRIPCIÓN GENERAL

El servicio de RPV (Red Privada Virtual) de Metrotel permite que su empresa interconecte sus oficinas remotas a través de un Backbone IP/MPLS (Multiprotocol Label Switching). Con este producto, el cliente obtiene una conectividad IP entre todas sus sucursales, donde Metrotel le asegura recursos de su propio backbone IP/MPLS a cada servicio de manera dedicada.

El producto RPV está especialmente orientado a clientes que tengan requerimientos de conectividad IP para sus redes con cualquiera de sus variantes (Full mesh, Hub & Spoke, centralized services, extranets, etc). Este producto brinda gran flexibilidad de manejo de redes permitiéndole al cliente administrar la conectividad de sus redes de modo granular. Adicionalmente cuenta con administración de calidad de servicio lo que le da al cliente la posibilidad de priorizar su propio tráfico de acuerdo con las aplicaciones utilizadas en su red.

El servicio RPV de Metrotel le brinda el mismo nivel de seguridad y privacidad para las redes de datos IP que las redes ATM o Frame Relay, dado que operan sobre un entorno virtualizado que impide que haya visibilidad entre los distintos clientes. Esto se logra mediante el uso de la tecnología MPLS-VPN (RFC 2547 del IETF) que asegura que las tablas de enrutamiento específicas de cada RPV sean mantenidas de modo privado asignadas a cada cliente individualmente. De este modo, es posible garantizar que el tráfico IP propio de cada RPV no sea enrutado a otros clientes que comparten el mismo backbone. La tecnología no permite que el tráfico de un sitio sea enrutado a otro sitio que no pertenece a la misma Red Privada Virtual por el uso de etiquetas diferenciadas.

Cada extremo conectado (sucursales u oficinas) tendrá la totalidad del ancho de banda contratado, no existiendo variaciones en la velocidad de transferencia de los paquetes de datos. Con los RPV de Metrotel es posible administrar redes, anchos de banda, calidad de servicio y conectividad contando con todo el soporte de un servicio administrado.

## 2. CARACTERÍSTICAS
+ Uso de tecnología MPLS-VPN a través de la implementación de la RFC 2547 del IETF. Los datos que son transportados por estas redes tienen la seguridad y privacidad de una red FR / ATM con la ventaja de un backbone que optimiza las trayectorias basadas en contenidos IP.
+ Basado en protocolo IP (capa 3 del modelo OSI) en todos los puntos de la red.
+ Permite esquemas de interconexión tanto centralizado como también descentralizado permitiendo transportar una gran variedad de servicios: Video conferencia, Voz sobre IP, file servers, correo corporativo, Internet y demás servicios que se puedan implementar en una red IP.
+ Es posible administrar esquemas de calidad de servicio (QOS - quality of service) utilizando DiffServ (Differentiated services) Esto permite clasificar el tipo de tráfico por extremo, basado en marcas “DSCP” para priorizar adecuadamente las aplicaciones. Esto se logra ya que dichas marcas “DSCP” serán reconocidas por los distintos equipamientos de ruteo en el cliente y de transporte de Metrotel, siendo encoladas de acuerdo con la prioridad elegida para cada marca. De este modo es posible definir el ancho de banda asegurado que debe tener cada una de las diferentes aplicaciones del cliente.
+ Soporta la interconexión entre diferentes entidades a través de extranets compartiendo solo aquellos servicios que las entidades acuerden. (Consultar por el opcional Extranet).
+ Al ser un servicio administrado, cuenta con monitoreo y gestión integrada. Esto implica un monitoreo Web por sitio conectado. Metrotel adicionalmente tiene gestión sobre todos los enlaces de su propia red, los cuales son monitoreados y gestionados en todo momento por personal altamente calificado las 24 hs del día, los 365 días del año.
+ A través de una arquitectura de backbone de anillos por fibra óptica, se consigue una restauración automática en el caso de eventuales fallas con mayores beneficios para los clientes en cuanto a su confiabilidad.
+ Es posible contratar soluciones desde 10 MB hasta 10 GB por última milla.
+ Posibilidad de configuración con o sin priorización de tráfico.

## 3. ALCANCE Y ESPECIFICACIÓN TÉCNICA

Metrotel cuenta con las siguientes opciones de RPV adaptándose a cada tipo de necesidad:
+ RPV sin router CE (customer edge): Es una opción económica que permite conectar la red del cliente directamente al acceso, brindando funcionalidades básicas de MPLS.
+ RPV con router CE (customer edge): Esta opción es necesaria cuando se necesitan implementar soluciones escalables, comportamientos complejos y políticas de calidad de servicio.

<table>
<th>Producto</th>
<th colspan="2">RPV (Red privada virtual)</th>

<tr>
<th>Versiones</th>
<th colspan="2">RPV de 10MB a 10GB</th>
</tr>

<tr>
<th>Código de producto</th>
<th colspan="2">RPV - Red Privada Virtual MPLS</th>
</tr>

<tr>
<th>Tecnología de red</th>
<td>VPN MPLS (RFC 2547)</td>
</tr>

<tr>
<th>Tiempo de respuesta </th>
<td>RTT < 20 ms <sup>(*1)</sup></td>
</tr>

<tr>
<th>Pérdida de paquetes</th>
<td> <= 0.01% <sup>(*1)</sup></td>
</tr>

<tr>
<th>SLA</th>
<td> 99.7% <sup>(*2)</sup></td>
</tr>

<tr>
<th rowspan="4">Servicios adicionales</th>
<th> Detalle</th>
<th> Tipo de contratación</th>
</tr>

<tr>
<td>Colas de priorización</td>
<td>En solución con Router</td>
</tr>

<tr>
<td>Equipamiento</td>
<td>Contratación Opcional</td>
</tr>

<tr>
<td>Soluciones de extranet (BCRA - Link - Visa - First Data) <sup>(*3)</sup></td>
<td>Contratación opcional</td>
</tr>
</table>

<sup>(*1)</sup> *Estos valores son válidos exclusivamente sobre tecnologías de fibra óptica. Son válidos en condición de uso menor al 50% del enlace (por cada última milla).*

<sup>(*2)</sup> *Solo válido para últimas millas propias en fibra óptica. En caso de requerirse redundancia consultar por las arquitecturas disponibles.*

<sup>(*3)</sup> *Por otro tipo de solución Extranet consultar a nuestro departamento comercial. Para más detalles sobre esta solución ver anexo “solución extranet sobre servicio RPV”*

## 4. OPCIONALES

A continuación, se detallan los servicios incluidos en cada opción
+ RPV sin router (Sin Calidad)
  + IP Secundarias o rutas estáticas: hasta 5 rutas en total
  + Protocolo de enrutamiento (BGP):
    + Se le publicara al cliente una red default 0.0.0.0/0.
    + Se recibirán del cliente hasta un máximo de 100 prefijos IP.
    + Una sola sesión BGP por servicio contratado. El cliente debe tener su propio AS (sistema Autónomo)
  + Direcciones MAC conectas al puerto: Hasta 500 MAC address.
  + Broadcast/Multicast: Hasta 300/500 Kbps.
  + Las marcas DSCP de los paquetes IP son transportadas sin modificaciones dentro de la red.

+ RPV con router (con Calidad)
  + Amplia oferta de equipamiento dependiendo del ancho de banda de la solución contratada.
  + IP Secundarias o rutas estáticas: Hasta 5 rutas en total.
  + Direcciones MAC conectas al puerto: Limite según especificaciones del router instalado.
  + Broadcast/Multicast: Sin filtros.
  + Calidad de Servicio (QOS).
    + 5 clases de servicios (2 priority, 2 bandwith y Best Effort).
    + Priority: Asegura el ancho de banda y una baja latencia (Voz y Video).
    + Clases "Priority" no deben superar el 50% del ancho de banda total.
    + Bandwith: Asegura solamente el ancho de banda (Datos críticos y transaccionales).
    + Las clases "Bandwith" más las "Priority" no deben superar el 75% del ancho de banda total.
    + Los paquetes serán marcados y priorizados según "DSCP".
    + Se aceptan y respetan las marcas DSCP enviadas por el cliente.
    + Clasificación y marcado de paquete según IP origen/destino.
  + DHCP (Dynamic Host Configuration Protocol): 1 Pool de IP.
  + NAT (Network Address Translation): total de 20 reglas (Nat/Pat/static/dynamic).
  + ACL (Access Control Lists): total de 10 reglas.
  + HSRP (Hot Standby Router Protocol): Un solo grupo standby en el router local.
  + Helper Address: Un solo Helper Address por extremo.
  + Protocolo de enrutamiento (EIGRP/OSPF/BGP)
    + Al cliente se le publicara una red default 0.0.0.0/0.
    + Se recibirán del cliente hasta un máximo de 100 prefijos IP.
    + Hasta dos sesiones BGP por servicio contratado. El cliente debe tener su propio AD (Sistema Autónomo).
  + Comunidad SNMP para monitoreo del cliente: Solo lectura restringida a 5 OID que necesite el cliente.
  + Soluciones Extranet para aquellos casos en los que se requiere unir una o más sucursales de la nube RPV de un mismo cliente con un punto externo perteneciente a otra entidad o Nube (este servicio se contrata en forma opcional).

Las funcionalidades detalladas anteriormente, ya incluidas en el abono del servicio, podrán ser configuradas durante la implementación o una vez que se encuentre operativo el enlace. Esta última opción deberá ser requerida mediante el ingreso de un ticket en nuestro centro de operaciones, quedando su implementación sujeta a la resolución de dicho ticket.

Por mes se podrán realizar, sin costo, hasta 3 modificaciones en la configuración del enlace. En caso de requerir más cambios deberán canalizarse los mismos con el área comercial.

Cabe aclarar que el producto RPV de Metrotel es un integrador de servicios u opcionales adaptable a las necesidades del cliente, por ello se mencionan las opciones más utilizadas las cuales se consideran un estándar dentro del producto.

Si la necesidad del cliente no se encuentra contemplada o supera los límites del alcance, deberá evaluarse la solución mediante especialistas de Metrotel, quienes encausaran el proyecto como “servicios administrados” en el cual se explicará cómo llevar a cabo el proyecto, adjuntando la documentación, los alcances y límites correspondientes.

## 5. LAG: PortChannel

Políticas de Link Aggregation Group (en adelante LAG), es un método que permite brindar redundancia de puertos o ampliar bandwidth (en adelante BW) para cuando no se cuenta con la interface de la velocidad apropiada o contratada. Metrotel recomienda que el número de interfaces sean par y de las mismas velocidades de BW (ejemplo: 4 interfaces de 1Gb).

En el caso de necesidad de ampliar BW, se recomienda no superar la cantidad de 4 interfaces en total debido a que el protocolo es deficiente para balancear tráfico entre interfaces y el mismo varia de forma impredecible dependiendo del tráfico generado por cada cliente.

Por lo expresado, Metrotel no aconseja utilizar LAG para el servicio contratado, en cambio recomendamos que se brinde con 1 única interfaz capaz de cubrir la totalidad del tráfico contratado. Metrotel no se responsabilizará por reclamos realizados a causa de un mal dimensionamiento de cantidad puertos en LAG.

## 6. ELEPHANT FLOW

En el caso que el cliente utilice "flujo continuo extremadamente grande" (elephantFlow) superior a 3Gbps, debe notificarse previamente a Metrotel. Superado este tamaño Metrotel se reserva el derecho de tomar acciones correctivas, si este afectara la calidad del servicio o de la red. El cliente no podrá alegar falla en el servicio en este caso, y no computará como falla en el SLA ni como causa para la solicitud de baja sin penalidad.

## 7. REDUNDANCIA - PUERTO ADICIONAL

Los puertos adicionales <sup>(*)</sup> existirán en el mismo equipo del puerto principal (sin excepción). El portal de Autogestión del cliente publicara solo el tráfico del puerto principal, no pudiendo dar visibilidad de los puertos adicionales. Cada puerto de forma independiente ya sea principal o adicional tiene la capacidad de brindar la totalidad del servicio, por lo cual ante la afectación de un puerto se podrá solicitar la reposición de este, pero no computara como indisponibilidad del servicio a menos que la totalidad de puertos estén afectados.

<sup>(*)</sup> *En caso de necesitar más de 1 (uno) puerto adicional, la habilitación de este estará sujeta a disponibilidad y análisis por parte de Metrotel.*

## 8. EQUIPAMIENTOS PARA ENLACES DE TERCEROS FUERA DE AMBA

En caso de que Metrotel provea un router propiedad de Metrotel para brindar el servicio sobre enlace por terceros, contratados por Metrotel para brindar el servicio, a más de 80 Km de CABA o Córdoba Capital, los reclamos asociados a reposición de este no computarán como falta del SLA contratado, mientras que el tiempo de reposición sea menor a 48 horas hábiles. El cliente acepta esta consideración como parte del servicio. No obstante, si se incluyera algún alcance particular, este último reemplazará y anulará lo mencionado previamente.

## 9. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto (0800- 362-1040) mediante el cual podrá realizar la gestión de eventuales reclamos. Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de esta.

## 10. MANTENIMIENTO PROGRAMADO

El mantenimiento programado consistirá en toda intervención realizada en la red de Metrotel, la cual será notificada previamente (con más de 48 horas de anticipación) al cliente y se realizará dentro del horario de mantenimiento establecido. Si el horario del corte previsto afecta la labor del cliente, éste puede solicitar la modificación de este. Metrotel se compromete a realizar los máximos esfuerzos para mover el corte al nuevo horario solicitado. Este tipo de interrupciones se puede realizar para reemplazar o agregar elementos a la red a fin de ampliar y mejorar permanentemente el servicio.

## 11. PUESTA EN MARCHA DEL SERVICIO

En aquellos casos en los que la provisión del servicio contratado requiera una instalación física en el domicilio del cliente, la misma será realizada por el personal de Metrotel o terceros que actuarán en nombre de Metrotel, quienes dejarán el servicio en condiciones de ser prestado y solicitarán al cliente el conforme vía la firma del Formulario “Informe de Instalación de Cliente”. La firma de dicho formulario asume la conformidad del cliente respecto de la instalación y de la capacidad de utilizar el servicio en cuestión. En caso de que el servicio contratado no requiera presencia física del personal de Metrotel en el domicilio del cliente, Metrotel determinará el mejor medio para comunicar que se ha comenzado la prestación de dicho servicio.

En la instalación, personal de Metrotel ejecutará las siguientes pruebas básicas con el fin de poder certificar el correcto funcionamiento.
+ Medición de RTT (tiempo de respuesta).
+ Medición de Perdida de paquetes.
+ Prueba de conectividad contra la nube RPV.

## 12. DISPONIBILIDAD

La disponibilidad del enlace contratado es una medida que indica cuanto tiempo se encuentra el sistema operativo respecto del total de tiempo en el que se brinda el servicio.

No serán considerados como falta de disponibilidad aquellos problemas de conectividad causados por fallas en el equipo del cliente ni aquellos originados por saturación del enlace, ya sea por tráfico genuino del cliente o bien por tráfico espurio (computadoras infectadas, programas p2p, ataques DDoS, etc). Tampoco serán considerados problemas de disponibilidad aquellos causados por fallas atribuibles a responsabilidad es del cliente (ver ítem correspondiente). No se considerarán mediciones propias del cliente a los fines de disponibilidad, pero si a los fines de diagnóstico. Para los casos no contemplados por mediciones propias de Metrotel se tomarán como base para el cálculo de indisponibilidades las fechas y horarios de las aperturas y cierres de los tickets correspondientes, luego de haber sido sometidos a consideración de Metrotel donde quede claramente demostrado que no fueron resultantes de alguna falta en las responsabilidades del cliente. Para este último caso no serán computados como indisponibilidad.

Los registros y datos recopilados por Metrotel serán la base sobre la que se calculará la disponibilidad correspondiente.

Para el cálculo de disponibilidad no se tendrán en cuenta las interrupciones ocasionadas por los mantenimientos programados previamente comunicados al cliente.

La disponibilidad será calculada de acuerdo con la siguiente fórmula: Disponibilidad = (T – D) / T x 100

Dónde:

D = Duración de la indisponibilidad (en minutos)

T = Duración del mes en cuestión (en minutos)

Disponibilidad = En porcentaje.

## 13. TIEMPO MEDIO DE RESTAURACIÓN

El tiempo de restauración es el tiempo transcurrido entre la hora de apertura de ticket por la detección del problema (Por parte de Metrotel o bien a través de la notificación del cliente al área de Servicio de Atención al Cliente) y la hora de restablecimiento del servicio.
El tiempo medio de restauración se calculará obteniendo el promedio de los tiempos de restauración del mes.

## 14. RESPONSABILIDAD DEL CLIENTE

A continuación, se detallan las responsabilidades del cliente:
+ El cliente es responsable de proporcionar un lugar adecuado (sala, o rack) para la instalación del equipamiento provisto por Metrotel. El lugar debe tener condiciones de temperaturas adecuadas (-5 a +40 grados), libres de polvo, apartados del tránsito de personas y con restricciones de acceso. Cualquier daño o indisponibilidad producto de un mal ambiente será imputado al cliente.
+ La energía para el equipamiento provisto por Metrotel debe ser brindada por el cliente. Metrotel proporcionará las especificaciones técnicas de las necesidades de energía dejando a criterio del cliente el dimensionamiento de térmicas, la utilización de UPS, etc. Es responsabilidad directa del cliente la disponibilidad del servicio producto de la energización.
+ Metrotel proporcionará al cliente un puerto Ethernet físico donde conectar el servicio RPV. Será responsabilidad del cliente conectar su red LAN al puerto proporcionado por Metrotel, así como también de la administración del equipamiento en su LAN. Las interconexiones entre el equipamiento de Metrotel y su red LAN debe ser por medio de Switches con capacidad de configuración manual de las características físicas del puerto (velocidad/dúplex). Se excluye explícitamente el uso de HUBs. Cualquier problema de performance en la red LAN interna del cliente será responsabilidad del Cliente.
+ El cableado de red desde el sitio donde se encuentra el Equipo Terminal instalado por Metrotel, hasta el equipamiento del cliente, debe ser categoría 5 ó superior. El cliente es responsable por el cableado con lo cual deberá tener adecuadamente certificados los cableados.
+ Metrotel monitoreará el servicio RPV a través del equipo instalado en el cliente. El punto de demarcación del servicio RPV es el puerto Ethernet provisto por Metrotel. Será responsabilidad del cliente el mantenimiento, configuración y performance de su red LAN local. Cualquier degradación del servicio producida por el equipamiento del cliente (mala configuración, problemas de negociación), no será imputable a Metrotel.
+ Será responsabilidad del cliente informar a Metrotel de cualquier anomalía percibida en el funcionamiento del servicio mediante la apertura del ticket correspondiente. A partir de este punto, corresponderá al cliente poner a disposición a los administradores de la red para que juntamente con personal calificado de Metrotel se pueda realizar el correcto diagnóstico y corrección de la falla. Cualquier reclamo sobre el servicio será tomado sobre la base de fechas y horarios de apertura de tickets dejando a consideración de Metrotel la revisión de su contenido. Todo tiempo adicional entre la apertura y cierre de ticket que sea consecuencia de indisponibilidad de los administradores de red del cliente (en caso de requerirse) no será computado a los fines del reclamo.

## 15. LIMITACIONES DEL SERVICIO

La seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Metrotel recomienda el uso de programas Antivirus, Firewalls y cualquier software o hardware vigente y actualizado que evite estos ataques.

El resguardo de la información en los equipos / sistemas del cliente queda bajo su exclusiva responsabilidad. Metrotel recomienda el uso de software o hardware para resguardo y respaldo de la información almacenada en los equipos y sistemas del cliente.

El servicio de RPV de Metrotel es exclusivamente IP. Esto implica que no se puede utilizar el protocolo IPX (propietario de redes Novell) ni el protocolo SNA (propietario de redes IBM). Cualquier variante de protocolos podrá ser transportada solo si es encapsulada en IP. En caso de requerirse, dicho análisis debe ser adecuadamente escalado a través de especialistas de Metrotel quienes evaluarán la factibilidad de implementación.

La tasa de transferencia máxima de un servicio siempre es menor a la velocidad física de puerto. Esto es debido a los overheads, gaps interframes y tamaño del paquete correspondiente al estándar IEEE 802.3. Metrotel no tomará reclamos producto de la eficiencia propia del protocolo Ethernet.

Este producto no soporta Multicast (IGMP snooping, ni ruteo PIM).

Jitter: Menor a 5 ms en condición 95 percentil. Estos valores son válidos exclusivamente sobre tecnologías de fibra óptica y solo pueden verificarse desde la red del cliente en una condición de uso menor al 50% del enlace. Dado que no se trata de un servicio administrado (por ser transparente), no se realizan mediciones recurrentes de estos valores.

Las políticas aplicadas en ruteo y calidad de servicio serán totalmente válidas dentro de la red de Metrotel. En caso de que el cliente integre uno o más puntos de su red IP a través de terceros contratados por el cliente, Metrotel no podrá garantizar que el tráfico sea tratado del mismo modo que dentro de su red. Es por esto por lo que las redes integradas por terceros no estarán sujetas a las mediciones de disponibilidad ni de alcance reduciendo su funcionamiento al “mejor esfuerzo”.

Para el caso de que la última milla no sea parte de la red de FO de Metrotel, no se garantizará la calidad de servicio (QoS).

