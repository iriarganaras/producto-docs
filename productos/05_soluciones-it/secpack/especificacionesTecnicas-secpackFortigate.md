# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - SECURITY PACK FORTIGATE

## 1. DESCRIPCIÓN GENERAL

Security Pack es una solución creada específicamente a medida de la creciente tendencia en ciberataques en la región. Cuenta con una configuración polivalente que responde a la mayoría de las necesidades de las empresas y con un soporte especializado en seguridad. También se ofrece un seguimiento en el caso de expansión de red e infraestructura. Con este servicio, siempre contara con la información necesaria en la protección de amenazas, reportes semanales sencillos sobre el estado del Firewall, y más detallados de analítica más compleja. Todo esto con un asesoramiento que tiene en cuenta el mejor aprovechamiento del presupuesto asignado a seguridad.

El servicio cuenta con:
+ Firewall
+ SSL VPN
+ Prevención de Intrusos
+ Antivirus para Trafico no cifrado
+ Antivirus para Trafico cifrado (Implica implementación disruptiva en los dispositivos del cliente)<sup>1</sup>
+ Filtrado Web básico basado en Categorías
+ Filtrado Web avanzado basado en Categorías. Implementación disruptiva en los dispositivos del cliente)<sup>1</sup>
+ Filtrado por Aplicaciones
+ Antispam<sup>2</sup>
+ Inspección SSL
+ Inspección SSL Profunda (Implica implementación disruptiva en los dispositivos del cliente)<sup>1</sup>
+ Analítica avanzada y fácil de interpretar enviada por Metrotel al cliente de manera semanal
+ Gestión desatendida 24 x7
+ Actualizaciones de Firmware y mantenimientos gestionados por Metrotel.
+ Zona Desmilitarizada con Protección de Firewall y Antivirus especializado en Servidores Web.
+ DHCP Server
+ Metrotel Fast DNS Caching Server
+ Servidor de Tiempo (NTP)
+ Limitación de Redes Sociales basadas en tiempo y autenticación para usuarios seleccionados. (Implica implementación disruptiva en los dispositivos del cliente)<sup>1</sup>
+ Virtual Switch de 6 puerto para conexiones directa al equipo o Uplinks a otros equipos del cliente (Limitado a 1 Gb/s)<sup>3</sup>

<sup>1</sup> (https://docs.fortinet.com/document/fortigate/6.0.0/cookbook/181341/importing-the-certificate-into-webbrowsers)

<sup>2</sup> Solo están soportados los protocolos SMTP, POP3 e IMAP.

## 2. ALCANCE Y ESPECIFICACIÓN TÉCNICA

Para implementar Security Pack se necesita que el sitio de instalación del equipamiento reúna todas las condiciones de climatización, energía, disipación de calor, baja exposición al polvo y otras <sup>3</sup> requeridas por el fabricante del equipo que será proporcionado por Metrotel.

El cliente deberá tener un vínculo de “INTERNET INT” Dedicado provisto por Metrotel con una o más IP Publicas. <sup>4</sup>

El cliente será el responsable de proveer a Metrotel mediante el documento de personalización del Servicio la siguiente información:
+ Las rutas de las redes de los equipos ubicados en su intranet que tendrán acceso al Fortigate.
+ Categorías de Filtrado Web, ej.: Drogas, porno, armas, Redes sociales, citas <sup>5</sup>
+ Si desea hacer empleo de la Zona Desmilitarizada (DMZ) proporcionada por el Fortigate.
+ Direcciones de E-mail a la cual serán enviados los reportes semanales.

En caso de hacer empleo de la funcionalidad de “SSL-VPN” o “Limitación de Redes Sociales basadas en tiempo y autenticación para usuarios seleccionados” el cliente deberá enviará a Metrotel en el “Documento de Personalización de Servicios” la relación de usuarios e Emails <sup>6</sup> para ser cargados en la plataforma. El nombre de usuario es prestablecido por Metrotel, está le dará a conocer a la cliente pasada la puesta en marcha la relación de usuario y Contraseña. En caso de no contar con los parámetros anteriores, el servicio se brindará con la configuración estándar, la cual cumple con las buenas prácticas de seguridad y calidad de servicio.

Configuración estándar:
+ Firewall
+ SSL VPN
+ Prevención de Intrusos
  
<sup>3</sup> (https://www.fortinet.com/content/dam/fortinet/assets/data-sheets/fortigate-fortiwifi-60f-series.pdf https://www.fortinet.com/content/dam/fortinet/assets/data-sheets/fortigate-100f-series.pdf)

<sup>4</sup> (https://www.metrotel.com.ar/internet-dedicado/)

<sup>5</sup> Consultar documento de “Categorías de FortiGuard”: (https://fortiguard.com/webfilter/categories)

<sup>6</sup> Consultar documento de “Personalización de Servicios

+ Antivirus para Trafico no cifrado
+ Filtrado Web básico basado en Categorías
+ Filtrado por Aplicaciones
+ Antispam
+ Inspección SSL
+ Analítica avanzada y fácil de interpretar enviada por Metrotel al cliente de manera semanal
+ Gestión desatendida 24x7
+ Mantenimientos gestionados por Metrotel.
+ Zona Desmilitarizada con Protección de Firewall y Antivirus especializado en Servidores Web.
+ DHCP Server
+ Metrotel Fast DNS Caching Server
+ Servidor de Tiempo (NTP)
+ Virtual Switch de 6 puerto para conexiones directas al equipo o Uplinks a otros equipos del cliente (Limitado a 1 Gb/s). <sup>7</sup>
  
En caso de necesitarse habilitar los opcionales de “Antivirus para Tráfico cifrado”, “Filtrado Web avanzado basado en Categorías”, “Inspección SSL” y “Limitación de Redes Sociales basadas en tiempo y autenticación para usuarios seleccionados” el cliente deberá importar el certificado de Fortigate en todos los equipos(PC/Notebook/Tablet/Cel) utilizaran el producto Security Pack mediante instalación manual o Políticas de Dominio (GPO) <sup>8</sup> , Metrotel no se hace responsable de la configuración de estos equipos del cliente.

La funcionalidad de “SSL VPN” embebida en el producto requiere la instalación y configuración del FortiClient <sup>9</sup> por parte del Cliente, Metrotel solo se hará responsable del mantenimiento de las cuentas utilizadas para la misma.

El producto permite en dependencia de la banda contratada el siguiente máximo de usuarios de “SSL VPN” y para “Limitación de Redes Sociales basadas en tiempo y autenticación para usuarios seleccionados”.


<sup>7</sup> (https://www.fortinet.com/content/dam/fortinet/assets/data-sheets/fortigate-fortiwifi-60f-series.pdf - https://www.fortinet.com/content/dam/fortinet/assets/data-sheets/fortigate-100f-series.pdf)

<sup>8</sup> Chequear documentación del fabricante: (https://docs.fortinet.com/document/fortigate/6.0.0/cookbook/181341/importing-the-certificate-into-web-browsers)

<sup>9</sup> Cliente gratis: (https://www.forticlient.com/downloads o https://ip-Publica_del_Fortigate_del_Producto/)

<table>
<th colspan="5">Cantidad de usuarios</th>
<tr>
<td></td>
<th colspan="2">Fortigate 60F</th>
<th colspan="2">Fortigate 100F</th>
</tr>

<tr>
<td></td>
<th>Inicial</th>
<th>Máximo</th>
<th>Inicial</th>
<th>Máximo</th>
</tr>
<th>Cantidad de usuarios a proteger</th>
<td>01</td>
<td>100</td>
<td>100</td>
<td>200</td>
</tr>


<tr>
<th>Máximo de usuarios seleccionados a autenticar para limitar redes sociales en reglas basadas en tiempo en el portal cautivo On-Demand</th>
<td>40</td>
<td>100</td>
<td>100</td>
<td>200</td>
</tr>

<tr>
<th>Usuarios de SSL VPNs</th>
<td>40</td>
<td>100</td>
<td>100</td>
<td>200</td>
</tr>
</table>



<table>
<th colspan="2">Paquete de adquisición de usuarios (Escalado en cantidad de usuarios)</th>
<tr>
<th>Usuarios seleccionados a autenticar para limitar redes sociales en reglas basadas en tiempo en el portal cautivo On-Demand</th>
<td>20</td>
</tr>

<tr>
<th>Usuarios de SSL VPNs</th>
<td>20</td>
</tr>
</table>


Cada banda sea “Básica” o “Avanzada” si y solo si podrá escalar en cantidad de usuarios mediante el “Paquete de adquisición de usuarios”, teniendo un límite de cantidad de paquetes a adquirir por banda contratada (tiene costos asociados por cada paquete adquirido):

<table>
<th colspan="3">Cantidad de máxima de "Paquete de adquisición de usuarios" por banda</th>
<tr>
<td></td>
<th colspan="2">Banda</th>
</tr>

<tr>
<td></td>
<th>Básico (Fortigate 60F)</th>
<th>Avanzado (Fortigate 100F)</th>
</tr>

<tr>
<th>Cantidad de máxima de paquete de adquisición de usuarios</th>
<td>3</td>
<td>3</td>
</tr>
</table>

El Fortigate es 100% gestionado por el SoC de Metrotel, de acuerdo con el plan contratado.

<table>
<th colspan="3">Empresa mediana (Empresa de 1-100 usuarios</th>
<tr>
<th colspan="2">Cantidad de modificaciones mensuales<th>
</tr>

<tr>
<th rowspan="2">Tipo de modificación</th>
<th colspan="2">Banda</th>
</tr>

<tr>
<th>Básico</th>
<th>Avanzado</th>
</tr>

<tr>
<th>ACL de Firewall</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Rutas (añadir o modificar)</th>
<td>1</td>
<td>5</td>
</tr>

<tr>
<th>Filtrado web</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Alta de usuario</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Cambio de contraseña</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Modificaciones en la DMZ</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Publicación de puertos (DNAT)</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Modificaciones en las interfaces de red</th>
<td>1</td>
<td>5</td>
</tr>
</table>



<table>
<th colspan="3">Empresa grande (Empresa de 100-200 usuarios)</th>
<tr>
<th colspan="2">Cantidad de modificaciones mensuales<th>
</tr>

<tr>
<th rowspan="2">Tipo de modificación</th>
<th colspan="2">Banda</th>
</tr>

<tr>
<th>Básico</th>
<th>Avanzado</th>
</tr>

<tr>
<th>ACL de Firewall</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Rutas (añadir o modificar)</th>
<td>1</td>
<td>5</td>
</tr>

<tr>
<th>Filtrado web</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Alta de usuario</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Cambio de contraseña</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Modificaciones en la DMZ</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Publicación de puertos (DNAT)</th>
<td>5</td>
<td>10</td>
</tr>

<tr>
<th>Modificaciones en las interfaces de red</th>
<td>1</td>
<td>5</td>
</tr>
</table>

<table>
<th colspan="3">Máximo de reglas y funcionalidades</th>
<tr>
<th>Regla/Funcionalidad</th>
<th>(Fortigate 60F)</th>
<th>(Fortigate 100F)</th>
</tr>

<tr>
<th>ACL de Firewall</th>
<td>15</td>
<td>30</td>
</tr>

<tr>
<th>ACL de Firewall basadas en tiempo y con autenticación de usuarios (limitación de redes sociales basadas en tiempo y autenticación para usuarios seleccionados</th>
<td>2</td>
<td>2</td>
</tr>

<tr>
<th>Interfaces de red lógicas hacia la red del cliente  </th>
<td>4</td>
<td>8</td>
</tr>

<tr>
<th>Servicio de DNS listado en interfaces de red</th>
<td>4</td>
<td>8</td>
</tr>

<tr>
<th>Servicio de DHCP listado en interfaces de red</th>
<td>4</td>
<td>8</td>
</tr>

<tr>
<th>Servicio de NTP listado en interfaces de red</th>
<td>4</td>
<td>8</td>
</tr>

<tr>
<th>Portales de VPN</th>
<td>1</td>
<td>1</td>
</tr>

<tr>
<th>DMZ</th>
<td>1</td>
<td>1</td>
</tr>

<th colspan="3">Security Profiles</th>
<tr>
<th>Presencia de antivirus en ACL</th>
<td>5</td>
<td>20</td>
</tr>

<tr>
<th>Presencia de Aplication Control en ACL</th>
<td>5</td>
<td>20</td>
</tr>

<tr>
<th>Presencia de antispam en ACL</th>
<td>5</td>
<td>20</td>
</tr>

<tr>
<th>Presencia de IPS en ACL</th>
<td>5</td>
<td>10</td>
</tr>

<th colspan="3">SSL inspection</th>
<tr>
<th>Certificate inspection</th>
<td>15</td>
<td>30</td>
</tr>

<tr>
<th>Certificate Deep Inspection</th>
<td>1</td>
<td>1</td>
</tr>

<th colspan="3">Loggin Options en ACL Firewalls</th>
<tr>
<th>Eventos de seguridad</th>
<td>15</td>
<td>30</td>
</tr>

<tr>
<th>Todas las sesiones</th>
<td>0</td>
<td>0</td>
</tr>

</table>






**Recursos disponibles**

El servicio cuenta con una retención de 7 días de los logs del Fortigate en la Nube de Metrotel para la generación de Analítica e Informes que serán enviados al cliente, pasado 7 días expira los Logs y los Reportes enviados al cliente.

**Diagrama lógico del producto**

![Diagrama lógico del producto](../../../imagenes/secpack-fortigate/diagrama%20logico%20del%20producto.png)

## 3. INSTALACIÓN, PUESTA EN MARCHA Y ACEPTACIÓN DEL SERVICIO

El servicio contratado requiere presencia física del personal de Metrotel en el domicilio del cliente e interrupción del servicio de Internet en caso de existir. El Cliente se compromete a estar presente durante la instalación o bien designar a una persona que actúe en su representación.

La puesta en marcha del Servicio será realizada por el personal de Metrotel o terceros que actuarán en nombre de Metrotel, quienes realizarán las tareas de instalación y solicitarán al Cliente o a la persona por él autorizada, el conforme vía la firma del Formulario de Aceptación de Servicios y el Formulario de entrega en Comodato de Equipos. La firma de dichos formularios por parte del Cliente y/o de la persona por él designada para estar presente al momento de la instalación, implica la conformidad del Cliente respecto de la instalación y de la capacidad de utilizar el servicio en cuestión, así como del carácter en que se entregan los equipos al Cliente, quien será responsable de éstos con el compromiso de devolverlos en buen estado de conservación y mantenimiento a la finalización de la prestación del servicio.

**Condiciones generales de instalación**

Se definen las siguientes pautas concernientes a la instalación:

Tomando los datos provistos, se configurarán los equipos según los requerimientos del cliente de acorde al producto, tales como funcionalidades, excluyéndose la provisión de consultoría por el rediseño de la solución, redefinición de parámetros, o migración a otros protocolos no especificados al momento de la instalación.

Las tareas por realizarse durante la instalación y/o puesta en funcionamiento, que no afecten la operación de la red, se realizarán en horario laboral (lunes a viernes de 9 a 18 Hs), las tareas que afecten la operación normal de la red serán debidamente programadas fuera de los horarios laborales.

El Proveedor no será responsable del funcionamiento de aplicaciones externas al equipamiento a instalar, siendo el único responsable de esta operación el personal técnico del cliente final (Por ej. Proxys, Routers, Switches, Módems, Servidores LDAP, Servidores RADIUS, etc.).

El cliente final configurará por su cuenta todo tipo de aplicaciones, equipos, etc. (BAJO SU TOTAL RESPONSABILIDAD) que sean necesarios conectar al Firewall Fortinet. Cualquier afectación a la configuración/software del sistema, que requiera arreglo/trabajo/parches será facturado de acuerdo con el trabajo, tiempo y jerarquía del personal que se requiera para remediar el problema, Metrotel se reserva el derecho de determinar si lo hace o no. Esta situación no afectará el SLA convenido, en ningún sentido.

Para la coordinación de las fechas y horas de instalaciones y/o puesta en funcionamiento, el líder del proyecto del cliente deberá comunicar las mismas con 96 hs hábiles de antelación como mínimo, a efectos de gestionar los recursos adecuados.

Las actividades de pruebas de aceptación deberán ser realizadas por el Cliente en un plazo no mayor a cuarenta y ocho (48) horas hábiles contadas a partir de la fecha de finalización y comunicación de la puesta en marcha por parte de Metrotel. Las pruebas deberán basarse en el chequeo de la conectividad y navegación del cliente a Internet y el chequeo de las reglas de seguridad habilitadas por defecto validando que él producto bloquea el EICAR Test File. <sup>10</sup>

Vencido el mencionado plazo, y de no mediar objeciones por parte del cliente, Metrotel procederá a la aceptación tácita del servicio para su posterior facturación.

**Aclaraciones**

En caso de ser necesaria la instalación de ítems no contemplados en el producto Security Pack Fortigate, Metrotel se reserva el derecho de hacer la evaluación del requerimiento y de presentar o no una propuesta.

<sup>10</sup> *(http://metal.fortiguard.com/generated/eicar.com)*

## 4. SOPORTE

El soporte contempla:
+ La asistencia a sitio, solo para cambiar partes defectuosas. Excepcionalmente, para otros problemas (a criterio de Metrotel) cuando aparezcan fallas que requieran la presencia física de un técnico.
+ Fallas originadas por el software, sistema operativo y otros atribuibles al equipo Fortinet (que no requieran cambio de partes), serán verificadas remotamente, a través del vínculo que provee Metrotel/cliente final al sistema.
+ Otras fallas del sistema, como problemas de conexión, etc., serán resueltas por Metrotel según corresponda.
+ 
El servicio de mantenimiento técnico correctivo incluye: 1) la provisión de repuestos; 2) mano de obra; 3) supervisión técnica, y todo otro elemento que garantice la correcta prestación del servicio a partir de su efectiva puesta en marcha y mientras dure la vigencia del contrato. Los cargos por mantenimiento técnico correctivo están incluidos en el abono mensual.

Metrotel contará con un sistema de monitoreo del equipamiento Fortinet instalado en el cliente para poder detectar las alarmas y poder tomar acciones proactivas a los efectos de solucionarlas.

El cliente colaborará con Metrotel en todo lo que esté a su alcance, tendiente a reducir el plazo de solución del problema, así como también facilitando el acceso a los Data Center o salas dentro del mismo cuando sea necesario ingresar.

## 5. TIPOS DE INCIDENCIA Y TIEMPO DE RESPUESTA

Para los tiempos de respuestas se considerará según el tipo de falla:
+ Fallas MAYORES: estas fallas afectan los servicios / equipos directamente por indisponibilidad total o parcial (mayor al 75%).
+ Fallas MENORES: estas fallas no afectan la operación normal de los servicios / equipos / sistemas de gestión o lo hacen en forma irrelevante, ni afectan a la calidad del servicio, pero dificultan las tareas de operación y mantenimiento.
  
A continuación, se detalla el diagrama de escalamiento:

![Diagrama lógico del producto](../../../imagenes/secpack-fortigate/diagrama%20de%20escalamiento1.png)
![Diagrama lógico del producto](../../../imagenes/secpack-fortigate/diagrama%20de%20escalamiento2.png)

## 6. CALIDAD DE SERVICIO (SLA)

La disponibilidad del servicio contratado es una medida que indica cuanto tiempo se encuentra el sistema operativo respecto del total de tiempo en el que se brinda el servicio.

No serán considerados como falta de disponibilidad problemas de conectividad causados por fallas en la transmisión o recepción de los equipos del cliente. Tampoco serán considerados problemas de disponibilidad aquellos causados por fallas atribuibles a responsabilidades del cliente.

Metrotel tomará únicamente como base para el cálculo de indisponibilidades las fechas y horarios de las aperturas y cierres de los tickets correspondientes, luego de haber sido sometidos a consideración de Metrotel donde quede claramente demostrado que no fueron resultantes de alguna falta en las responsabilidades del cliente. Para este último caso no serán computados como indisponibilidad.

Los registros y datos recopilados por Metrotel serán la base sobre la que se calculará la disponibilidad correspondiente. Para el cálculo de disponibilidad no se tendrán en cuenta las interrupciones ocasionadas por los mantenimientos programados previamente comunicados al cliente. La disponibilidad será calculada de acuerdo con la siguiente fórmula:

Disponibilidad (%) = (1-(Tiempo fuera de servicio en hs/Período de medición en hs)) *100%.

El producto tiene un SLA de 99.7%

## 7. TIEMPO PEDIO DE RESTAURACIÓN

El tiempo de restauración es el tiempo transcurrido entre la hora de detección del problema (Por parte de Metrotel o bien a través de la notificación del cliente al área de Servicio de Atención al Cliente) y la hora de restablecimiento del servicio. El tiempo medio de restauración se calculará obteniendo el promedio de los tiempos de restauración del mes.

## 8. LIMITACIONES DEL SERVICIO

Security Pack es un producto diseñado para ciber seguridad y minimizar la probabilidad de pérdida de información del cliente frente a daños, no obstante, no se trata de un sistema infalible.

El cliente reconoce que considerando la criticidad o el impacto que pudiera ocasionarle este tipo de desperfectos, existen resguardos adicionales que el cliente puede tomar para reducir aún más la probabilidad de pérdidas.

Adicionalmente, el cliente reconoce que Metrotel no puede ejercitar control sobre el contenido de la información que circula a través de la red Interna e Internet. Por lo tanto, Metrotel no es responsable del contenido de ningún mensaje y/o información tanto si el envío fue hecho o no por un cliente de Metrotel. La seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Metrotel recomienda el uso de programas Antimalware, Antivirus y cualquier software o hardware vigente y actualizado que evite ataques en todos sus dispositivos informáticos. Sugerimos además que contrate al menos el servicio de Internet Mitigado el cual ofrece protección de ataques DDoS de capa 3.

Metrotel no efectuará la gestión de los servidores y dispositivos, entendiéndose por gestión a todas aquellas tareas derivadas de la propia operación y control de funcionamiento del mismo como ser administración del sistema operativo, aplicación de parches correctivos y/o de seguridad, instalación de aplicaciones, resolución de problemas sobre aplicaciones instaladas en el servidor virtual, análisis de performance sobre aplicaciones instaladas, monitoreo de agentes, quedando dichas tareas bajo estricta responsabilidad del cliente.

Metrotel considera como “Proyecto Especial” con cargo al cliente, el querer añadir funcionalidades soportadas por los Equipos que no estén mencionadas en los listados de “Características” y “Alcance y especificación técnica” ejemplo:

+ SD-WAN
+ Direccionamiento avanzado (BGP, etc.).
+ Clúster HA, Activos/Activos, Activos/Pasivos.
+ Integración con productos de terceros.
  
Metrotel se reserva el considerar añadir otras funcionalidades.

## 9. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto (0800-362-1040) mediante el cual podrá realizar la gestión de eventuales reclamos. Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de esta.

## 10. MANTENIMIENTO PROGRAMADO

El mantenimiento programado consistirá en toda intervención realizada en la red de Metrotel, la cual será notificada previamente (con más de 48 horas de anticipación) al cliente y se realizará dentro del horario de mantenimiento establecido. Si el horario del corte previsto afecta la labor del cliente, éste puede solicitar la modificación del mismo. Metrotel se compromete a realizar los máximos esfuerzos para mover el corte al nuevo horario solicitado. Este tipo de interrupciones se puede realizar para reemplazar o agregar elementos a la red a fin de ampliar y mejorar permanentemente el servicio.

## 11. ACERCA DE METROTEL

Metrotel es una empresa de telecomunicaciones que desde hace más de 25 años brinda servicios a empresas líderes del mercado argentino. Opera comercialmente, en el área de la Ciudad Autónoma de Buenos Aires, Gran Buenos Aires, Rosario, Córdoba, Mendoza y Neuquén. Cuenta con una red de fibra óptica propia (Red de Alta Velocidad) de 3.600 km, la cual permite ofrecer servicios de alta disponibilidad y con velocidades de transporte de datos.
El objetivo de Metrotel es brindar soluciones innovadoras, buscando la satisfacción de todos los clientes, el crecimiento continuo y la rentabilidad con innovación tecnológica.