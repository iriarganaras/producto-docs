# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: INTERNET MITIGADO

## 1. INTRODUCCIÓN - INTERNET MITIGADO
El servicio de Internet Mitigado permite detectar y mitigar los ataques de DDoS (Distributed Denial of Service o denegación de servicio distribuido) de forma automática, a nivel capa de transporte (layer 4), ofreciendo al cliente continuidad del servicio en forma transparente y sin degradación del enlace contratado. El servicio de Internet Mitigado posibilita monitorización pasiva y no intrusiva del tráfico nacional e internacional, dado que el análisis se realiza de manera estadística. Una vez detectada una amenaza, el tráfico malicioso se limpia, enviando únicamente tráfico legítimo al cliente y asegurando la continuidad del servicio de Internet Mitigado.

## 2. DESCRIPCIÓN DEL SERVICIO - INTERNET MITIGADO
El sistema de detección y mitigación de ataques DDoS en el servicio de Internet Mitigado realiza un filtrado inteligente del tráfico malicioso mediante técnicas de análisis de comportamiento y patrones de red, utilizando sistemas de monitoreo para la detección anticipada de amenazas, brindando soluciones sin impacto en el rendimiento de la red. El monitoreo es permanente y continuo para detectar ataques volumétricos tanto de enlaces nacionales como internacionales, utilizando listas blancas y/o negras.

La solución de Mitigación de Internet Mitigado está implementada en la Red de Metrotel, lo que permite entregar tráfico limpio al cliente sin afectar el ancho de banda, rendimiento o latencia de los vínculos contratados. El sistema puede redirigir el tráfico a los puntos de mitigación del Backbone una vez que un ataque supera un porcentaje del ancho de banda, separando en tiempo real el tráfico legítimo del malicioso, descartando este último.

Internet Mitigado puede complementarse con hardware específico (APS) instalado en el sitio del cliente para la detección temprana de anomalías estadísticas, mal uso de protocolos, avalanchas y coincidencia de fingerprints, defendiendo contra ataques volumétricos y a la capa de aplicaciones en servicios críticos como DNS, HTTP o VoIP. Esta solución complementaria debe ser evaluada y cotizada aparte por personal de Metrotel.

### Ventajas y Beneficios de Internet Mitigado
- Protección de servicios críticos (voz, video, web, plataforma e-commerce, correo electrónico) contra ataques volumétricos.
- Protección de la infraestructura (routers, conmutadores, firewalls, ancho de banda, servicios DNS), manteniendo el tráfico ilegítimo fuera de la red.
- Optimización de recursos: visibilidad del tráfico e informes para mejorar la ingeniería y solución de problemas.

## 3. PROCEDIMIENTO ANTE UN ATAQUE - INTERNET MITIGADO
- El sistema genera alertas según los valores de "trigger rate" y "high severity rate", definidos en la planilla "shared host detection settings" entregada al cliente con criterios estándar, pero modificables.
- Si el tráfico supera el "trigger rate", se genera una alerta LOW.
- Las alertas HIGH sobre Managed Objects con auto-mitigación habilitada activarán la mitigación automática e inmediata.
- Los operadores del NOC reciben una alerta y analizan el ataque, comunicándose con los contactos del cliente definidos en la planilla de criterios para actuar de acuerdo a la realidad del ataque.
- Se utiliza el sistema Arbor para visualizar el tráfico malicioso mitigado y el legítimo permitiendo revisión detallada (por IP/puerto origen/destino y tipos de ataques).
- Se pueden descargar pcaps en tiempo real y estadísticas con información granular.
- El proceso de mitigación se aplica mientras el ataque esté vigente.

### Tiempos de respuesta de la solución de Internet Mitigado ante un incidente
- Detección del ataque DDoS: 5 minutos una vez detectado estadísticamente (*1). Si no hay equipo en el cliente, el promedio es de 60 minutos.
- Comunicación al cliente: 15 minutos posteriores a la detección.
- Reposición de servicio: 30 minutos de mitigación y entrega de tráfico limpio, pudiendo ser mayor según volumen.
- Para ataques que no superen los 10GB. Si el ataque es mayor/metió en riesgo la infraestructura Metrotel puede hacer blackhole.

### *1 Nota
El tiempo depende del tipo de ataque y el ancho de banda.

### Tipos de ataques cubiertos por Internet Mitigado
- Spoofed: Paquetes con dirección origen falsificada.
- Malformed: Paquetes anómalos en bits/flags.
- Floods: Grandes volúmenes de paquetes legítimos.
- Null: Paquetes sin contenido.
- Protocol: Paquetes con protocolos ilegítimos.
- Fragmented: Paquetes fragmentados que no serán completados.
Además, cubre variaciones de tráfico, mal uso de protocolos, escaneo de puertos, ataques según patrones y origen.

## 4. DASHBOARD Y REPORTES - INTERNET MITIGADO
El sistema de Internet Mitigado provee:
- Monitoreo en tiempo real del tráfico y detección de variaciones.
- Alertas de ataques.
- Información de alarmas en curso y recientes.
- Clasificación de alarmas por impacto o severidad.
- Información detallada con gráficas sobre actividad, orígenes, destinatarios, puertos, protocolos y ancho de banda.
- Detalle de ataques por categoría incluyendo ancho de banda en bytes, bps, pps.
- Informe gráfico del porcentaje de ataque sobre tráfico total contratado.

## 5. RESPONSABILIDADES DEL CLIENTE - INTERNET MITIGADO
- El cliente debe mantener actualizada la información sobre las IPs y Prefijos a mitigar. Metrotel no es responsable sobre redes no informadas.
- Debe informar a Metrotel cualquier cambio en datos de contacto.
- Debe proveer un lugar adecuado (sala/rack) con condiciones de temperatura, sin polvo, restringido y seguro para el equipamiento, siendo responsable de cualquier daño.
- Debe proveer la energía para el equipamiento, siguiendo las especificaciones técnicas de Metrotel.
- Tiene la responsabilidad de conectar su red LAN al puerto Ethernet proporcionado por Metrotel y administrar su LAN. Las interconexiones deben hacerse con Switches configurables; está prohibido el uso de HUBs.
- La configuración y administración de Firewalls para distribuir el servicio internamente es responsabilidad del cliente, así como problemas asociados a este dispositivo, salvo que tenga el opcional de Router configurado por Metrotel.
- Metrotel no es responsable de reclamos por manipulación de redes internas por BGP, ni de cambios de tráfico en arquitecturas DUAL HOME con otros proveedores.

## 6. LIMITACIONES DEL SERVICIO - INTERNET MITIGADO
- La seguridad informática de los equipos del cliente ante malware, virus, hackers, etc. es exclusiva responsabilidad del cliente.
- Metrotel no es responsable por ataques dirigidos a la capa de aplicación (capa 7); estos están excluidos del servicio Internet Mitigado, aunque pueden cubrirse con soluciones complementarias que requieren hardware adicional.
- El servicio contempla mitigación de ataques DoS/DDoS volumétricos desde los vínculos internacionales de Metrotel, con un máximo de hasta 10 GB contra la plataforma de mitigación inteligente. Para casos mayores, Metrotel actúa con "mejores esfuerzos" sin garantías.
- Superado ese límite, Metrotel se reserva el derecho a "despublicar" (blackhole) el servicio de conexión a internet.

---

# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: INTERNET DEDICADO

## 1. DESCRIPCIÓN GENERAL - INTERNET DEDICADO
El servicio INTERNET INT de Metrotel está diseñado para ofrecer conexión dedicada, permanente, simétrica y de alta disponibilidad a Carriers y Empresas, con velocidades personalizables hasta 10Gbps o superiores bajo condiciones especiales.

## 2. ALCANCE Y ESPECIFICACIÓN TÉCNICA - INTERNET DEDICADO
El servicio INTERNET INT es provisto en modalidad FTTO (Fiber To The Office) usando tecnología de avanzada. Consiste en la provisión de un vínculo físico de transmisión de información con variantes de ancho de banda de hasta 10Gbps o superiores, con velocidad simétrica.

El servicio proporciona acceso a tráfico nacional e internacional, asignando rangos de IP fijas y públicas. Es posible ampliar la cantidad de IPs contratadas, pero si se realiza con posterioridad, implica cambio de rango que puede coexistir 15 días antes de dar de baja el anterior.

Permite establecer sesiones BGP para que el cliente administre dinámicamente sus redes.

**Notas técnicas**:
- Algunas locaciones pueden tener última milla sobre enlaces/redes de terceros.
- Para la asignación de IPs públicas, Metrotel gestiona el registro ante LACNIC.
- El cliente debe autorizar la publicación de IPs/ASN en Internet.

### OPCIONALES - INTERNET DEDICADO
- **Internet sin Router**: opción económica de conexión directa.
- **Internet con Router**: necesario para configuración de NAT, DHCP y soluciones escalables. Siempre se configura BGP para el ruteo.

## 3. CARACTERÍSTICAS DEL SERVICIO - INTERNET DEDICADO

| Producto         | INT Sin Router | INT Con Router    |
|------------------|---------------|-------------------|
| Versiones        | Hasta 10 GB    | Hasta 10 GB       |
| Código Producto  | INT           | INT               |
| Tecnología Red   | FO            | FO                |
| Simetría         | Si            | Si                |
| IP Fija/Pública  | Si            | Si                |
| IPs Adicionales  | Justificables | Justificables     |
| Ruteo BGP        | Si*4          | Si*5              |
| NAT              | NO            | SI*6              |
| DHCP             | NO            | SI                |
| Redundancia      | NO            | Soportada*7       |
| Monitoreo SNMP   | NO            | Comunidad restringida a 5 OID |

**Notas:**
- En IPv4 el cliente recibirá una IP útil si contrata un rango de 4 (el resto es para red, broadcast, gateway).
- Justificación de IPs adicionales requerida, sujeto a disponibilidad.
- BGP: solo una sesión sin router, hasta dos con router y con la administración de atributos según necesidades del cliente.
- NAT hasta 5 reglas + 5 ACL, configurable DMZ básica.
- Redundancia contratable y sujeta a disponibilidad.

### LAG: PortChannel – INTERNET DEDICADO
La agregación de enlaces (LAG) permite redundancia o ampliación de BW. Se recomienda no más de 4 interfaces iguales en velocidad. Preferible usar una única interfaz para cubrir el tráfico contratado.

### Elephant Flow – INTERNET DEDICADO
El uso de flujo continuo superior a 3Gbps debe ser notificado a Metrotel, reservándose el derecho de tomar acciones si afecta calidad.

### Redundancia – Puerto Adicional – INTERNET DEDICADO
Puertos adicionales existen en el mismo equipo, la visibilidad será solo del principal desde el portal. Cada puerto puede dar total capacidad de servicio y sólo si todos fallan es indisponibilidad.

### Equipamiento para enlaces de terceros (fuera de AMBA) – INTERNET DEDICADO
Para servicios sobre enlaces prestados por terceros a más de 80 Km de CABA o Córdoba Capital, la reposición está fuera de SLA siempre que se resuelva en menos de 48hs hábiles.

### Servicio de DNS – INTERNET DEDICADO
El cliente puede usar el servicio de DNS de Metrotel para dominios sobre IPs públicas asignadas por Metrotel.

## 4. SOPORTE TÉCNICO – INTERNET DEDICADO
El soporte opera 24x7 todo el año, con número gratuito (0800-362-1040). Diagnóstico y resolución se comunican telefónica y/o por mail.

## 5. MANTENIMIENTO PROGRAMADO – INTERNET DEDICADO
Las intervenciones se notifican 48hs antes y se coordinan con el cliente en caso de afectar operación. Se utilizan para actualizar y mejorar el servicio.

## 6. PUESTA EN MARCHA DEL SERVICIO – INTERNET DEDICADO
Las instalaciones físicas son realizadas por Metrotel o terceros, dejando el servicio operativo y requiriendo firma de conformidad del “Informe de Instalación de Cliente”. Si no requiere presencia, la activación se comunica por otro medio.

## 7. DISPONIBILIDAD – INTERNET DEDICADO
La disponibilidad mide el tiempo de acceso a Internet respecto del tiempo total brindado. Problemas de conectividad causados por falla de equipo del cliente o saturación de enlace (genuina o por ataque/virus/p2p) no son indisponibilidad. Solo se toma en cuenta la información de tickets y el reporte de Metrotel, con la fórmula:  
**Disponibilidad = (T-D)/T x 100**  
Donde D = duración de la indisponibilidad (minutos) y T = duración del mes (minutos).

## 8. TIEMPO MEDIO DE RESTAURACIÓN – INTERNET DEDICADO
Se calcula como promedio entre notificación y restablecimiento del servicio por mes.

## 9. RESPONSABILIDADES DEL CLIENTE – INTERNET DEDICADO
- Proveer lugar adecuado (temperatura, polvo, tránsito, acceso restringido) para el equipamiento.
- Proveer energía bajo especificaciones de Metrotel.
- Conectar su red LAN al puerto Ethernet de Metrotel y administrar su LAN, usando switch configurado (no HUBs).
- Cableado de red categoría 5 o superior, certificado.
- Mantenimiento, configuración, performance de la LAN local: cualquier degradación por equipamiento propio es responsabilidad del cliente.
- Configuración y administración de Firewalls/NAT/DMZ es responsabilidad del cliente, salvo con router opcional.
- Cambios en BGP deben hacerse idealmente con Metrotel.
- Cambios de tráfico por DUAL HOME con otros proveedores son responsabilidad del cliente.
- Informar cualquier anomalía mediante apertura de ticket, colaborar con el diagnóstico.
- Reclamos sobre el servicio tomarán el horario de apertura del ticket como referencia.

## 10. LIMITACIONES DEL SERVICIO – INTERNET DEDICADO
- Metrotel no tiene control sobre el contenido que circula por Internet ni es responsable del mismo.
- Seguridad informática de equipos del cliente es su responsabilidad.
- El resguardo de información de equipos/sistemas es responsabilidad exclusiva del cliente.
- Metrotel solo garantiza entrega hasta la frontera con Carriers; no garantiza velocidad de extremo a extremo.
- No es responsable por degradaciones/performance por ataques DDoS volumétricos ni inteligentes, aunque aplica mejores prácticas de mitigación.
- Hasta 300 MAC Address por servicio (*1); con router opcional varía según equipo.
- El DNS de Metrotel se recomienda pero puede usarse cualquiera; no computa a disponibilidad salvo para nombres asociados a IPs en los servidores de Metrotel.
- El servicio no está diseñado para reventa de conectividad y puede modificarse si el consumo es superior al perfil corporativo.
- Tasa de transferencia máxima es menor que la velocidad física de puerto por overheads propios de Ethernet.
- Jitter < 5 ms en 95 percentil para la última milla en fibra óptica (en condiciones detalladas).
```
