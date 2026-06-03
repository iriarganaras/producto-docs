# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

Este documento contiene el detalle completo de las **especificaciones técnicas y alcance de servicio del producto INTERNET INT provisto por Metrotel**. El objetivo es ofrecer contexto autosuficiente por chunk, repitiendo el nombre del servicio (INTERNET INT) en cada sección para que nunca se pierda el hilo temático.

---

## 1. DESCRIPCIÓN GENERAL - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

El servicio **INTERNET INT** de Metrotel ha sido especialmente diseñado para proporcionar una conexión a Internet de alta calidad a Carriers y Empresas. INTERNET INT consiste en una conexión dedicada, permanente, simétrica, de excelente disponibilidad, con variantes de velocidades a la medida del cliente.

---

## 2. ALCANCE Y ESPECIFICACIÓN TÉCNICA - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

El servicio **INTERNET INT** se provee bajo la modalidad FTTO (Fiber To The Office), utilizando tecnología avanzada en redes de acceso de fibra óptica (*1).

- **Vínculo físico dedicado** para transmisión de información sobre la red Internet.
- Ancho de banda disponible en variantes hasta 10Gbps (o más en soluciones a medida).
- Velocidad simétrica: igual capacidad contratada tanto de subida como de bajada.
- Acceso a tráfico nacional e internacional en cualquier proporción.
- Asignación de direcciones IP fijas y públicas (no cambian con el reinicio).
- Posibilidad de ampliar la cantidad de IPs fijas (implica cambio de rango si no se pide al inicio).
- Migración de IPs: convivencia de rangos por 15 días corridos en la transición.
- Posibilidad de establecer sesiones BGP contra routers de peering de Metrotel para administración dinámica de redes.

Notas:
- (*1) En algunas localidades, la última milla puede ser provista por terceros aunque el backbone es fibra óptica.
- (*2) El cliente autoriza la registración del rango IP ante LACNIC. Metrotel asegura que dichas IPs no están en listas negras al momento de asignación. El cliente es responsable por el uso y acciones desde las IPs públicas otorgadas. Si no posee ASN propio, Metrotel podrá publicar las IPs bajo ASN Metrotel mediante rutas estáticas. Siempre se requiere autorización para publicar IPs o ASN del cliente.

---

## 3. OPCIONALES - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

Metrotel ofrece dos opciones principales del servicio **INTERNET INT**:

- **INTERNET INT sin Router**: opción económica que permite conectar directamente la red del cliente al acceso.
- **INTERNET INT con Router**: permite soluciones escalables, NAT o DHCP, configurándose siempre con BGP como protocolo de ruteo.

### Características Resumidas de INTERNET INT

| Producto        | INT Sin Router | INT Con Router     |
|-----------------|---------------|--------------------|
| Versiones       | Hasta 10 GB    |                    |
| Código Producto | INT           | INT                |
| Tecnología      | FO (fibra óptica, *1) |  FO (fibra óptica, *1) |
| Simetría        | Si            | Si                 |
| IP Fija         | Si (*2)       | Si (*2)            |
| IP Pública      | Si            | Si                 |
| IPs adicionales | Justificables (*3) | Justificables (*3) |
| Ruteo BGP       | Si (*4)       | Si, hasta 2 sesiones (*5) |
| Reglas NAT      | No            | SI (hasta 5, *6)   |
| DHCP            | No            | SI (hasta 1 pool)  |
| Redundancia física | No         | Soportada (*7)     |
| Monitoreo SNMP  | No           | Comunitario, limitado a 5 OID de necesidad del cliente |

Notas:
- (*1) Última milla puede ser por terceros donde no hay backbone directo.
- (*2) Direccionamiento público IPv4/IPv6. En IPv4 por subnetting: una IP para red, una broadcast, una gateway y resto para el cliente. Por ejemplo: en un rango de 4 IP, una para el cliente.
- (*3) IP adicionales sujetas a justificación y disponibilidad.
- (*4) Una sola sesión BGP. Cliente debe tener AS propio. No se aceptan publicaciones de redes más específicas que /24. Cliente puede manejar atributos AS_PATH y Local Preference. Metrotel publica redes del cliente por todos los proveedores. El tamaño de la tabla de ruteo está limitado por la capacidad del router del cliente.
- (*5) Hasta 2 sesiones BGP. Mismas reglas para /29. Si es redundante/principal de otro proveedor, aplica mismo límite de /24. Administración de tráfico por atributos y BGP queda a criterio del cliente.
- (*6) Hasta 5 reglas NAT y 5 ACL, permitiendo una DMZ básica (por ejemplo, Web/Mail Server con puerto abierto y resto filtrado).
- (*7) Redundancia de acceso físico con dos accesos a nodos distintos; requiere contratación separada y está sujeta a disponibilidad/análisis.

---

## 4. LAG: PortChannel - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

El **Link Aggregation Group (LAG)** en el servicio INTERNET INT permite proveer redundancia de puertos o ampliar el bandwidth cuando la interfaz apropiada no está disponible. Recomendaciones y limitaciones:

- Se aconseja un número par de interfaces, siempre del mismo ancho de banda.
- No se recomienda superar 4 interfaces por eficiencia del protocolo.
- Se prefiere una única interfaz del tamaño de BW adecuado.
- Metrotel no se responsabiliza por reclamos derivados de un mal dimensionamiento en puertos LAG.

---

## 5. Elephant Flow - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

Cuando el cliente de **INTERNET INT** utiliza flujos continuos extremadamente grandes (“elephant flow”, >3Gbps), debe notificar previamente a Metrotel. Si se supera este tamaño y afecta la calidad del servicio o red, Metrotel puede tomar acciones correctivas. En estos casos, la situación no será considerada falla en el SLA ni justificación de baja sin penalidad.

---

## 6. Redundancia – Puerto Adicional - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

En **INTERNET INT**, los puertos adicionales existen en el mismo equipo que el principal. Solo se publica el tráfico del puerto principal en el portal de autogestión. Cada puerto (principal/adicional) puede brindar la totalidad del servicio. Si un puerto falla, se puede solicitar reposición sin que se cuente como indisponibilidad, salvo que todos los puertos fallen.

*Nota: Más de un puerto adicional está sujeto a disponibilidad y análisis por parte de Metrotel.*

---

## 7. Equipos para Enlaces de Terceros fuera de AMBA - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

En caso de INTERNET INT sobre enlace de terceros (más de 80 km de CABA o Córdoba Capital), la reposición de router propiedad de Metrotel no cuenta como incumplimiento del SLA si se realiza en menos de 48h hábiles. El cliente acepta esta condición salvo que haya alcances particulares diferentes.

---

## 8. Servicio de DNS - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

**INTERNET INT** permite al cliente usar el servicio de DNS provisto por Metrotel para las direcciones IP públicas asignadas. La autogestión de dominios se realiza en un portal específico, pero solo para IPs de Metrotel.

---

## 9. Soporte Técnico - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

Metrotel ofrece soporte técnico para INTERNET INT en Buenos Aires, 24/7/365. El cliente tiene un número gratuito (0800-362-1040) para gestionar reclamos. La Mesa de Ayuda diagnostica, informa el estado y avanza en la resolución de fallas notificando por teléfono/mail.

---

## 10. Mantenimiento Programado - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

El mantenimiento programado de INTERNET INT es notificado con al menos 48h de anticipación, realizada en horario pactado con el cliente. El cliente puede solicitar modificación del horario si se ve afectado.

---

## 11. Puesta en Marcha del Servicio - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

La provisión de INTERNET INT con instalación física será realizada por personal de Metrotel/terceros autorizados y se dejará constancia mediante la firma del “Informe de Instalación del Cliente”. Dicha firma implica conformidad sobre la instalación y la capacidad de uso del servicio.

Cuando no se requiera instalación física se notificará por el mejor medio que el servicio está operativo.

---

## 12. Disponibilidad - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

La disponibilidad de INTERNET INT se mide como el tiempo de acceso a Internet respecto al total de tiempo del servicio.

- Se considera falta de disponibilidad: cuando no hay interconexión con Internet, o si el DNS de Metrotel asignado impide el uso.
- No se consideran: fallas de equipo del cliente, saturación por tráfico propio/espurio, o problemas debidos a la responsabilidad del cliente.
- Las mediciones de Metrotel son las bases para el cálculo; las de cliente solo se usan para diagnóstico.
- La fórmula de disponibilidad es:  
  ```Disponibilidad = (T – D) / T x 100```  
  Donde D = minutos de indisponibilidad y T = minutos del mes.

---

## 13. Tiempo Medio de Restauración - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

El tiempo medio de restauración de INTERNET INT es el promedio mensual desde la detección/notificación del problema hasta el restablecimiento del servicio.

---

## 14. Responsabilidad del Cliente - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

Responsabilidades del cliente para INTERNET INT:

- Proveer alojamiento adecuado (sala/rack) para equipos Metrotel: temperatura -5° a 40°C, sin polvo, restringido y sin tránsito.
- Brindar energía para los equipos (Metrotel entrega especificaciones; UPS y protección es a criterio del cliente).
- Conectar la LAN al puerto Metrotel, administrar su red interna y mantener el cableado (Cat 5 o superior, certificado).
- Monitorear, mantener y configurar la LAN local. Fallas en la red interna no son imputables a Metrotel.
- Configurar/firewallear el servicio a nivel interno, salvo que el router de Metrotel haya sido contratado y configurado por ellos.
- Manipulación de tráfico por BGP fuera de Metrotel es bajo responsabilidad del cliente. Cambios de tráfico por DUAL HOME no son reclamables a Metrotel.
- Reportar anomalías mediante ticket; los administradores del cliente deben colaborar para diagnóstico/corrección. Los tiempos debidos a disponibilidad del cliente no computan como reclamo.

---

## 15. Limitaciones del Servicio - ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO: ANEXO TÉCNICO INTERNET

Restricciones y recomendaciones del servicio INTERNET INT:

- Metrotel no controla el contenido que circula en Internet; no responde por mensajes/información que circulen, aún si son de clientes Metrotel.
- Seguridad informática contra intrusos/virus/hackers es responsabilidad del cliente (se recomienda software/hardware adecuado y actualizado).
- El resguardo y respaldo de información es responsabilidad exclusiva del cliente.
- INTERNET INT no garantiza el control sobre la velocidad de transferencia fuera de la red y carriers directos de Metrotel.
- No es responsabilidad de Metrotel las degradaciones de performance o denegaciones de servicio causadas por ataques DDoS u otros inteligentes, sin embargo, se actuarán mejores prácticas de mitigación.
- INTERNET INT soporta hasta 300 MAC address por servicio (*1); con router, según especificación técnica del equipo.
- El cliente puede usar DNS de Metrotel para resolución de nombres de IPs asignadas por Metrotel; su funcionamiento no cuenta como parte de la disponibilidad del sistema salvo para IP->nombre en DNS Metrotel.
- Metrotel puede modificar el servicio si el consumo de BW excede el uso corporativo. No permite reventa del servicio a terceros.
- Servicios adicionales serán facturados por separado.
- La tasa máxima de transferencia es menor a la velocidad física de puerto por overhead de Ethernet IEEE 802.3. No se reconocen reclamos por eficiencia del protocolo.

**Especificación adicional:**
- Jitter menor a 5 ms en condición 95 percentil (*2).

Notas:
- (*1) Si el límite de MAC address no es suficiente, se puede analizar con Metrotel.
- (*2) Jitter aplica para la última milla sin tránsitos y bajo fibra óptica, en condición de uso <50%.
