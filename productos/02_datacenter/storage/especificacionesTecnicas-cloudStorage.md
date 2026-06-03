# ESPECIFICACIONES TÉCNICAS - CLOUD BACKCUP

## 1. DESCRIPCIÓN GENERAL

Metrotel Cloud Storage es un servicio seguro para el almacenamiento de contenido, basado en la nube y diseñado para resguardar grandes volúmenes de datos, ofreciendo además un alto rendimiento compatible con la entrega de contenido online y de bajo costo.

Metrotel Cloud Storage está configurado sobre una plataforma EMC Isilon, el cual provee un alto grado de performance y almacenamiento. Esto brinda la capacidad al cliente de poseer almacenamiento scale-out para su plataforma y da la posibilidad de acceso a múltiples usuarios simultáneamente, todos trabajando sobre un mismo recurso.

## 2. CARACTERÍSTICAS

+ Replicación de contenido automático entre centros de datos alternativos.
+ Infraestructura escalable, rápido almacenamiento bajo demanda, ideal para eventos de Streaming o Archiving.
+ Flexibilidad de protocolos de transferencia de archivos para una amplia compatibilidad con los sistemas del cliente, nativamente soporta: NFS, SMB, CIFS, FTP, HTTP.
+ Disponible para Windows, y Linux.
+ El servicio podrá ser contratado en múltiples opciones de espacio de acuerdo a las necesidades de cada cliente.
+ Dependiendo del enlace contratado y la disponibilidad que se requiera alcanzar, se podrá optar por adquirir equipamiento para las dependencias del cliente, el cual proveerá una mejora en la transferencia de los datos.
+ Garantiza la transparencia a nivel L2 de un extremo a otro del cliente (end to end) sobre una red MetroEthernet.
+ El enlace se entrega en interfaces del tipo Ethernet cuyas velocidades pueden ser 10/100/1000 Mbps a la cual el cliente conectara sus equipos directamente

## 3. ALCANCE Y ESPECIFICACIÓN TÉCNICA

El servicio consiste en la provisión de un repositorio con espacio de almacenamiento, el cual dependerá de la contratación que haya realizado el cliente según sus necesidades. Este almacenamiento se presenta al cliente utilizando alguno de los protocolos de transporte estándar, tal como NFS<sup>1</sup> y físicamente a través del enlace que el cliente disponga o un enlace que haya contratado. Una vez asignados los recursos, el cliente podrá subir su contenido alojándolo en el repositorio que haya contratado.

El servicio de Metrotel Cloud Storage incluye la sincronización automática del contenido en 2 centros de almacenamiento de Metrotel, geográficamente separados. El proceso de sincronización es automático y transparente para el usuario.


<sup>1</sup> <small>Es responsabilidad del cliente realizar la subida / actualización del contenido en Metrotel Cloud Storage.</small>

Los contenidos en Metrotel Cloud Storage tienen 100% de disponibilidad, si por algún motivo uno de los centros de almacenamiento tiene una falla, el contenido del cliente va a seguir disponible<sup>2</sup>.

En el momento de la puesta en marcha, el cliente y Metrotel deberán coordinar cómo será la configuración final con la cual se presentará el repositorio contratado y la configuración de los extremos para establecer la conexión al Cloud de Metrotel. Está conexión podrá ser realizada por medio de un enlace (Layer2 o Layer3) de hasta 1 GB (según factibilidad técnica). El enlace dedicado incluye una transferencia mensual de al menos 10 Tb, en el caso que el cliente requiera mayor transferencia deberá ser especificado en la preventa del servicio para ver factibilidad técnica. En casos que el cliente requiera más ancho de banda se evaluara como proyecto especial, previo análisis de las áreas de ingeniería de red y de Datacenter de Metrotel.

Al tratarse de un servicio multipunto de conectividad total (full mesh), aquellas oficinas o sucursales conectadas entre sí podrán compartir el repositorio contratado, previo pedido de acceso vía ticket al NOC.

Los EWS de Metrotel garantizan la transparencia de los vínculos Layer 2 ofreciendo una gran eficiencia en comunicaciones a muy altas velocidades, con muy baja latencia, proporcionando una conexión bidireccional y flexible que le permitirá modificar simple y rápidamente el ancho de banda de acuerdo a sus necesidades.

Cada extremo contratado (sucursales u oficinas) tendrá la totalidad del ancho de banda contratado, no existiendo variaciones en la velocidad de transferencia de los paquetes de datos.

La red de METROTEL garantiza una disponibilidad de 99.7 % anual.

El cliente tendrá acceso exclusivo al espacio de almacenamiento que contrató. El mismo no será compartido con otros clientes. Una vez finalizado el contrato con Metrotel, la información resguardada será eliminada del almacenamiento. Se aconseja realizar la transferencia de la información a otro sitio unos 30 días antes de la baja del servicio para garantizar que la información no se pierda.


<sup>2</sup> <small>Cabe destacar que la sincronización a centros alternativos de almacenamiento no funciona como backup de la información. Si el contenido que se sube al centro de datos principal es borrado accidentalmente el mismo será borrado de todas las regiones donde se haya sincronizado.</small>

### Seguridad

<u>Transporte de los datos</u>

Metrotel garantiza que los accesos por red a los recursos contratados por el cliente sean exclusivos, que no se comparta el “medio de transporte” con otro cliente, y que no sea posible poder “capturar” el tráfico de red. Para ello, Metrotel cumple con los estándares más altos sobre seguridad en la red de datos.

<u>Almacenamiento de los datos</u>

Para el caso de los datos almacenados en la nube, Metrotel utiliza la configuración de “zona” para brindar un servicio multi-tenant. Esto habilita que cada cliente quede aislado dentro de una nube lógica segura, permitiendo que los recursos compartidos para el almacenamiento sean exclusivos de éste y accedidos por los protocolos que configure. Al mismo tiempo, se utilizan diferentes proveedores de autenticación según sea necesario o el cliente lo requiera.
Los accesos finales a los datos, sobre el servidor, quedan asegurados por las políticas de seguridad que el cliente utilice (ACL o permisos UNIX), y por su metodología de resguardo de la información.

## 4. ACEPTACIÓN DEL SERVICIO

Las actividades de pruebas de aceptación deberán ser realizadas por el Cliente en un plazo no mayor a cuarenta y ocho (48) horas hábiles contadas a partir de la fecha de finalización y comunicación de la puesta en marcha por parte de Metrotel. Las pruebas deberán basarse en el uso normal de la aplicación de acuerdo a las prácticas habituales de la actividad principal del Cliente y de acuerdo al relevamiento de uso y necesidades durante la etapa de preventa. Vencido el mencionado plazo, y de no mediar objeciones por parte del cliente, Metrotel procederá a la aceptación tácita del servicio para su posterior facturación.

## 5. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, para acceder al servicio de soporte técnico de Metrotel, el cliente dispone de un número gratuito de contacto que funciona las 24 horas del día, los 365 días del año.

En la Mesa de Ayuda podrá realizar la gestión de eventuales reclamos.

Una vez ingresado el ticket técnico correspondiente se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá con las tareas de resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de la misma.

Las consultas y/o problemas relacionados con el servicio de Metrotel Cloud Storage se resolverán dentro del horario comercial (laboral).

En caso de requerir soporte 7x24 hs deberá solicitarlo por contrato.

## 6. LIMITACIONES DEL SERVICIO

El sistema de almacenamiento Cloud Storage Metrotel es una solución diseñada para minimizar la probabilidad de pérdida de información del cliente frente a un daño del equipo primario, no obstante, no se trata de un sistema infalible. El cliente reconoce que considerando la criticidad o el impacto que pudiera ocasionarle este tipo de desperfectos, existen resguardos adicionales que puede tomar para reducir aún más la probabilidad de pérdidas.

En el caso de que el sistema falle por causas imputables directamente a Metrotel y llegase a producirse algún tipo de pérdida de datos, la responsabilidad de Metrotel, previa sentencia judicial firme que así lo determine, quedará acotada como máxima al abono del servicio en cuestión. Por caso fortuito o causa mayor, no habrá responsabilidad alguna por parte de Metrotel. Adicionalmente, el cliente reconoce que Metrotel no puede ejercitar control sobre el contenido de la información que circula a través de la red Internet. Por lo tanto, Metrotel no es responsable del contenido de ningún mensaje y/o información tanto si el envío fue hecho o no por un cliente de Metrotel. La seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Metrotel recomienda el uso de programas Antimalware, Firewalls y cualquier software ó hardware vigente y actualizado que evite estos ataques.

Metrotel no efectuará la gestión sobre los servidores que utilicen el servicio contratado, entendiéndose por gestión a todas aquellas tareas derivadas de la propia operación y control de funcionamiento del mismo como ser administración del sistema operativo, aplicación de parches correctivos y/o de seguridad, instalación de aplicaciones, resolución de problemas sobre aplicaciones instaladas en el servidor, análisis de performance sobre aplicaciones instaladas en el servidor, monitoreo de agentes, etc., quedando dichas tareas bajo estricta responsabilidad del cliente.

Una vez finalizado el contrato con Metrotel, la información será eliminada del almacenamiento luego de 15 días. No se proveerá al cliente los archivos almacenados en los repositorios. Metrotel queda excluido de toda responsabilidad sobre el traspaso de la información contenida en los repositorios de almacenamiento y/o de su eliminación una vez finalizado el contrato.

Con el servicio de EWS Metrotel no se puede utilizar el protocolo IPX (propietario de redes Novell) ni el protocolo SNA (propietario de redes IBM). En caso de requerir la utilización de estos protocolos consultar con su representante de Ventas por la solución del servicio EWS Metrotel.

El cableado de red desde el sitio donde se encuentra el Equipo Terminal instalado por Metrotel, hasta el equipamiento del cliente, debe ser categoría 5 ó superior. El cliente es responsable por el cableado con lo cual deberá tener adecuadamente certificados los cableados.

Metrotel monitoreará su servicio a través del equipo instalado en el cliente. Será responsabilidad del cliente el mantenimiento, configuración y performance de su red LAN local. Cualquier degradación del servicio producida por el equipamiento del cliente (mala configuración, problemas de negociación), no será imputable a Metrotel.

El enlace que se provee para la conectividad del repositorio contratado es de uso exclusivo para la transferencia hacia dicho repositorio. En caso de detectar un uso incorrecto del enlace que no aplique al producto contratado, será aplicada una sanción económica a determinar.