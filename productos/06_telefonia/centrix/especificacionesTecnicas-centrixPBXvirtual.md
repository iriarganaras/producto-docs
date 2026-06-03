# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - CENTRIX PBX VIRTUAL (ATI)

## 1. DESCRIPCIÓN GENERAL
El Servicio de Central Virtual “Centrix Virtual PBX” de Metrotel, consiste en la provisión, en modalidad de servicio, de una Central Telefónica Privada IP (IP-PBX) hosteada en el Datacenter de Metrotel.

El servicio Centrix permite el procesamiento de llamadas internas y la conexión de troncales de Voz sobre IP (VoIP) provistos por Metrotel. Los clientes pueden optar por conectar teléfonos IP, analógicos tradicionales o una combinación de ambos, según se adapte mejor a sus necesidades.

El servicio Centrix es un sistema de comunicaciones distribuido que integra sofisticadas capacidades de voz y datos, gateway de Voz sobre IP (VoIP), seguridad, y todo un conjunto de aplicaciones multimedia habilitadas por IP. Debido a su arquitectura altamente flexible, El servicio permite a las empresas con múltiples sitios la capacidad de convergencia centralizando toda la operación en un solo punto. Opcionalmente, múltiples teléfonos IP pueden registrarse sobre la IP-PBX a través del vínculo privado o desde Internet con total independencia de su ubicación física.

El Servicio de Centrix es un servicio de valor agregado que se comercializa en pack, junto con alguno de los servicios de telefonía IP, por ejemplo, el ATI (Acceso Telefónico IP).

Los Packs Centrix, permitirán a su empresa recibir llamadas y establecer comunicaciones de voz, envío de fax, etc. hacia o desde la Red Conmutada de Telefonía Pública (PSTN). Se otorga con números geográficos que pertenecen al Plan Fundamental de Numeración Nacional y son provistos por Metrotel al cliente. El servicio también está habilitado para la realización de llamadas correspondientes a Servicios Especiales y de Emergencia (10Y, 11Y, 12Y y 911) y para la realización de llamadas a servicios de cobro revertido o compartido, prepago o pospago (08xy).

## 2. ALCANCE Y ESPECIFICACIÓN TÉCNICA
A continuación, se detallan las funcionalidades básicas incluidas en la presente solución.
+ Soporte hasta el 100% de llamadas sobre el troncal asociado
+ Soporte de la totalidad de internos registrados (teléfonos IP, analógicos, softphones)
+ Preatendedor e IVRs personalizados
+ Audio de bienvenida
+ Horarios de atención
+ Teclas de derivación (1 al 9)
+ Acceso a internos
+ Marcación saliente por código
+ Transferencia de llamadas
+ Detalle de llamadas salientes
+ Resumen de llamadas agrupado por interno (cantidad y duración)
+ Extracto de llamadas (filtrable por interno y exportable a CSV)
+ Redirección de llamada ocupada / no contesta
+ Grabación de llamadas entrantes a cola de atención
+ Grabación de llamadas salientes por interno
+ Descarga de grabaciones a repositorio externo vía FTP, el mismo debe ser en modo pasivo (Provisto por el cliente)Caller ID
+ Llamada en espera
+ Música en espera
+ Toma de llamada desde otro teléfono (Call Pick Up)
+ Límite de minutos mensuales por destino (Local, LDN, LDI, Celulares)
+ VoiceMail (acceso vía telefónica y/o recepción vía mail)<sup>1</sup>
+ Fax Server
+ Manual del Usuario (guía rápida con funciones básicas). Ver Anexo I.

<sup>1</sup> <small>La IP-PBX soporta una casilla de VoiceMail para cada interno. Cada casilla soporta 20 mensajes de 30 segundos de duración cada uno.</small>

### Funcionalidades opcionales
A continuación, se detallan las funcionalidades Opcionales que pueden incluirse bajo expresa solicitud del Cliente.
Cabe destacar que las mismas podrán tener un costo adicional.
+ Colas de Atención
+ Adaptadores analógicos FXS
+ Adaptadores analógicos FXO (Con restricciones)
+ Cola de llamadas selectivas por ANI
+ IVR adicional
+ Alquiler de SW Layer 2 (sin gestión ni monitoreo por parte de Metrotel)

### Funcionalidades no soportadas
Las funcionalidades detalladas a continuación no están soportadas por el equipamiento que forma parte de la presente solución.
+ Escucha de llamadas (en vivo)
+ Funcionalidades de Call Center tales como reportes (por hora, día, llamada, agente, logueo por interno)
+ Software para administración de Call Center (para monitorear y supervisar la atención al cliente)

### Diagrama de solución
En el siguiente diagrama se muestra un esquema conceptual de la solución propuesta.

![Diagrama de solución ATI Centrix](../../../imagenes/ati/diagrama%20de%20solucion%20ati%20centrix.png)

El servicio se ofrece solamente en modalidad OnNet con vínculo privado, incluyendo además el acceso por Internet para movilidad y redundancia. El servicio no se ofrece solo con acceso exclusivo desde Internet por cuestiones relacionadas a reglamentación de numeración de Argentina, como también a cuestiones relacionadas a la seguridad informática.

### Gestión del servicio a través de la Web (Autogestión)

Cada cliente cuenta con un usuario y contraseña para el ingreso a un sector privado de la web de Metrotel, desde donde puede administrar todos sus servicios, por ejemplo: Ver sus consumos y detalle de llamadas, solicitar nuevos servicios como bloqueos de llamadas a celulares, Larga Distancia Nacional o Internacional, configurar su cuenta de Fax Server para fax entrantes, etc.

### Definición de los servicios:

<u>Casilla de mensajes</u>

Facilidad mediante la cual el sistema es capaz de registrar mensajes de voz de las personas llamantes cuando uno no está presente o cuando la línea se encuentra ocupada, como un contestador en su domicilio tradicional. El cliente puede, si lo desea, configurar la casilla de mensajes para enviar avisos vía mail cuando hay mensajes nuevos, como también poder adjuntar los mensajes de Voz al mail, para poder ser escuchados directamente desde su PC.

<u>Servicio FAX Server</u>

Fax Server permite recibir los faxes directamente en su computadora en forma personalizada y por medio del e-mail. El usuario puede saber al instante cuando ha recibido un fax sin apartarse de su PC. Además, podrá reenviarlo, archivarlo o simplemente imprimirlo. El fax es recibido en el servidor de Fax de Metrotel, que lo relaciona con su cuenta de email y realiza la entrega del mismo con el archivo adjunto.

<u>Llamada en espera</u>

El servicio de llamada en espera le permite a un cliente atender una nueva llamada cuando se encuentra con una llamada en curso. Mientras el cliente se encuentra en una llamada, un tono de alerta le indica la presencia de esta nueva llamada.

<u>Desvío de llamadas “incondicional”</u>

Este servicio redirige en forma incondicional todas las llamadas entrantes al número telefónico que se haya configurado. Esta facilidad es controlada por el usuario y una vez activada permanece en ese estado hasta tanto él mismo la desactive. La persona que llama no podrá distinguir que su llamada ha sido desviada. El cliente, aún con la facilidad activada, puede realizar llamadas salientes en forma normal. Las llamadas se pueden desviar a un número dentro o fuera la red de Metrotel. Cada llamada de desvío será facturada en la misma forma que una llamada directa a ese destino sea local, celular, Larga Distancia, etc.

<u>Desvío de llamadas “por ocupado”</u>

Ídem anterior salvo que el desvío se produce en caso de que la línea esté ocupada.

<u>Desvío de llamadas por “no contesta”</u>

Ídem anterior salvo que el desvío se produce en caso de que al llamar a la línea no conteste.

<u>Identificación de llamadas</u>

Todas las líneas de Metrotel tienen Caller ID habilitado por lo que de contar con un dispositivo o teléfono con visualización de Caller ID, podrá observar el número del que se origina la llamada antes de responderla. Esta funcionalidad solo estará disponible para equipos compatibles con la tecnología de Metrotel.

<u>Bloqueo de ID Saliente</u>

El sistema por defecto envía información del abonado llamante en cada llamada realizada. Esta información es presentada en los terminales que poseen el servicio de Caller ID activado. Para evitar la presentación del número y nombre llamante, se puede utilizar el servicio de “Bloqueo de ID”. De esta manera las llamadas serán presentadas en destino como anónimas. La activación puede hacerse para todas las llamadas, como también para llamadas elegidas individualmente.

<u>Transferencia de llamadas</u>

Todas las llamadas que se encuentren en curso pueden derivarse, en vivo, a otras líneas dentro o fuera de la red de Metrotel.

<u>Música en espera</u>

Mientras una llamada entrante se encuentra retenida o en espera a ser atendido por una Cola de Atención, se reproduce música funcional, la cual es configurable en cada caso (depende del tipo de servicio).

<u>Caller ID</u>

Todos los equipos conectados a la Red Pública de Telefonía (PSTN) se encuentran identificados por un número perteneciente al Plan Fundamental. Al recibir llamadas en un terminal compatible, puede visualizarse el número del cual se está recibiendo la llamada.

<u>Call Pick Up</u>

En grupos de teléfonos puede configurarse la funcionalidad de capturar la llamada que se encuentra sonando en otro terminal remoto.

<u>Grabación de Llamadas</u>

Un grupo específico de llamadas puede ser grabado para posterior análisis o soporte de procesos de negocio. La central se encuentra provista con un espacio para grabar hasta 20 horas diarias de grabación. Una vez por día, en horas de baja utilización, las llamadas son transferidas por la red local a un repositorio externo de propiedad del cliente. Una vez transferidas las llamadas, el espacio queda nuevamente disponible para más grabaciones.


### Detalle de Opcionales

<u>Adaptadores Telefónicos FXS</u>

El servicio Centrix soporta la conexión de teléfonos analógicos tradicionales mediante la utilización de adaptadores telefónicos con puertos del tipo “FXS”.

<u>Adaptadores Telefónicos FXO</u>

El servicio Centrix permite la conexión de líneas analógicas de otros prestadores de servicios de telefonía. Para ello es necesario utilizar gateways (adaptadores telefónicos) externos para contar con puertos analógicos con interfaz FXO (Foreign Exchange Office). Por restricciones de las líneas analógicas de otros prestadores, se recomienda el uso de las mismas como numeración directa a internos de la central o sobre algún IVR con una corta espera. Esta condición optimizará el uso de las líneas a la vez que podrá evitar que llamadas entrantes o salientes queden en un estado desconocido por mucho tiempo.

<u>Teléfonos IP / Analógicos (Venta)</u>

El servicio Centrix soporta la conexión de teléfonos IP (IP Phone). Los teléfonos IP utilizan el protocolo SIP (Session Initiation Protocol), y serán provistos por Metrotel o por el Cliente, del mismo modo que los teléfonos analógicos.

<u>Garantía</u>

El equipamiento tiene una garantía por 12 (doce) meses a partir de la fecha de la firma del Documento de Entrega.

El Certificado de Garantía y el Manual de Uso del equipamiento serán entregados juntamente con la mercadería.

La garantía contempla la reparación o reemplazo de partes. Por tratarse de una unidad con componentes importados se aclara que de no contarse con los mismos el tiempo de reparación ó reemplazo estará condicionado a las normas vigentes de importación de esas partes.

<u>Cola de llamados selectivas por ANI</u>

En caso de contar con información de los orígenes de las llamadas entrantes, podrá configurarse para cada Cola de Atención un grupo de ANIs con funcionalidades diferenciadas, pudiendo así dando una atención más precisa. Esta funcionalidad viene acompañada de una API para poder lograrla funcionalidad requerida.

<u>IVR Adicional</u>

La central cuenta con un Preatendedor principal. Se podrán adicionar otros niveles de IVR para poder encadenarlos y lograr arboles de atención más complejos.

## 3. CARACTERÍSTICAS DEL SERVICIO  


<style>                         /*centra los encabezados y datos de la tabla*/
  th, td {
    text-align: center;
  }

table, th, td {                 /*agrega bordes a la tabla*/
  border: 1px solid black;
  border-collapse: collapse;
}



</style>

<table>

  <tr>
    <th>Producto</th>
    <th colspan="4">ATI Centrix VPBX</th>
  </tr>

  <tr>
    <th>Versiones</th> 
    <th> 5 canales / 10 internos </th>
    <th> 10 canales / 25 internos </th>
    <th> 15 canales / 50 internos </th>
    <th> 30 canales / 100 internos </th>
  </tr> 

  <tr>
    <th>Código de Producto</th>
    <th> Centrix VPBX 5C/10Int </th>
    <th> Centrix VPBX 10C/25Int </th>
    <th> Centrix VPBX 15C/50Int </th>
    <th> Centrix VPBX 30C/100Int </th>
  </tr>

  <tr>
    <th rowspan= "13">Opcionales</th>
    <td>2,4,8,24 o 32 puertos FXS</td>
    <td>2,4,8,24 o 32 puertos FXS</td>
    <td>2,4,8,24 o 32 puertos FXS</td>
    <td>2,4,8,24 o 32 puertos FXS</td>
   </tr>

   <tr>
    <td>8 puertos FXO</td>
    <td>8 puertos FXO</td>
    <td>8 puertos FXO</td>
    <td>8 puertos FXO</td>
   </tr>

   </tr>
    <td>Cola de atención</td>
    <td>Cola de atención</td>
    <td>Cola de atención</td>
    <td>Cola de atención</td>
   </tr>

   <tr>
    <td>Cola de llamadas por ANI</td>
    <td>Cola de llamadas por ANI</td>
    <td>Cola de llamadas por ANI</td>
    <td>Cola de llamadas por ANI</td>
   </tr>

   <tr>
    <td>Grabación de llamadas</td>
    <td>Grabación de llamadas</td>
    <td>Grabación de llamadas</td>
    <td>Grabación de llamadas</td>
   </tr>

   <tr>
    <td>IVR adicional</td>
    <td>IVR adicional</td>
    <td>IVR adicional</td>
    <td>IVR adicional</td>
   </tr>
  
</table>

<small>*Consulte por otras versiones disponibles*</small>

### Conexión remota

Conexión Remota Conexión por Enlace privado: El cliente podrá contar con un enlace del tipo RPV – ATI (red privada Virtual) para conectarse desde cada una de sus oficinas, garantizando de este modo la calidad del servicio contratado. El servicio debe ser contratado con este servicio de vínculo privado.

Conexión por Internet: El servicio además del vínculo privado ofrece la posibilidad de conectar un dispositivo SIP (Software o Hardware) desde un sitio remoto a través de Internet. Este servicio se ofrece como valor agregado para permitir la movilidad de los internos, pero no se ofrece solo para acceso por internet por cuestiones reglamentarias y de seguridad informática.

Es importante verificar que el enlace de Internet del sitio remoto cumpla con las características que se detallan a continuación. Las mismas deben mantenerse constantes en el tiempo.
+ Ancho de Banda: al menos 32 kbps por cada canal de voz (Codec G.729) o 100 kbps por cada canal de voz (Codec G.711)
+ Packet Loss: debe ser menor a 1%
+ Delay: debe ser menor a 150 milisegundos
+ Jitter: debe ser menor a 15 milisegundos

Cuando este servicio se presta en un sitio que se encuentra fuera de la cobertura de Metrotel, el Cliente será responsable por la contratación y correcto funcionamiento del enlace de Internet.

Metrotel no será responsable por la interrupción o mal funcionamiento del servicio de telefonía originado por el enlace de Internet instalado en el sitio del Cliente.

Cabe destacar que, por cuestiones de seguridad, los puertos: 80 (Web) y 5060 (Telefonía IP) se entregan bloqueados para el acceso a través de internet. En caso de requerir el desbloqueo de los mismos tendrá que solicitarlo a nuestro centro de operaciones previa firma de un documento que autoriza la habilitación.

### Softphones (Webphones)

El servicio Centrix soporta la conexión de softphones a través de la red local (LAN) o remotamente a través de Internet. El Cliente deberá disponer de las PC para la instalación del softphone. Cabe destacar la instalación y configuración de dicho software en las PCs o Laptops deberá ser realizada por el Cliente.

## 4. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto (0800-362- 1040) mediante el cual podrá realizar la gestión de eventuales reclamos. Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de la misma.

Toda central virtual Centrix incluye un soporte técnico general con modalidad 7*24 y efectivo en el NOC de Metrotel, este soporte resolverá solo cuestiones de enlace y generalidades.

Así mismo cada Centrix incluye un soporte especializado de 4 consultas mensuales de 1 hora, o 4 horas mensuales, no acumulables en los meses calendario.

Estas consultas incluyen temas de configuración de equipos, configuraciones específicas de la central, modificaciones que se encuentren dentro de las especificaciones del producto al momento de la instalación y ampliaciones previstas en el contrato. La configuración de equipos nuevos sea por ampliación o por reemplazo de los mismos, está incluido dentro de estas 4 horas, a excepción de las incluidas en la garantía del equipo. Estas consultas serán por email o teléfono y no incluyen visitas al domicilio de instalación u otro donde se preste el servicio, las visitas tendrán un costo por hora sujeto a la lista vigente.

Este documento no incluye CENTRIX LITE.

## 5. ALTA DEL SERVICIO

Para la instalación y alta del servicio se entregará al cliente una planilla con la información que Metrotel requiere para la puesta en marcha inicial. Esta planilla contempla los datos de red, numeración y configuraciones del servicio.

Toda configuración fuera de esta planilla es específica y queda sujeta a disponibilidad y/o desarrollo de la misma, pudiendo representar un cargo adicional para el servicio.

Una vez completada y entregada la planilla, se inicia el alta del servicio que contempla: el soporte necesario para la configuración de la central, equipos telefónicos IP (comprados / Alquilados a Metrotel exclusivamente), la asistencia y asesoramiento para la adquisición de equipamiento IP y las configuraciones necesarias inherente al servicio y siempre relativas al tipo VoIP. No se incluyen configuraciones de la red LAN, cableados ni equipos del cliente afectados a la prestación del servicio Centrix.

En el caso que el cliente posea equipamiento telefónico IP de su propiedad, Metrotel provee la asesoría en forma remota de hasta un 10% de la cantidad de dispositivos. Los restantes equipos deberán ser configurados por el cliente exceptuando los casos que el cliente solicite el servicio adicional de SADM para la configuración del equipamiento, previa cotización por parte del Ejecutivo de Cuentas y según tarifa vigente al momento de la contratación.

Toda consulta se recibirá por correo electrónico a la cuenta soportecorporativo@metrotel.com.ar o en casos más específicos al número de soporte asignado en ese momento por el ejecutivo de servicio (EESS). En ningún caso está prevista la visita al domicilio y de ser solicitada la misma tiene un costo por hora sujeto a la lista de precios vigente y consecuente al trabajo a realizar.

Se considera por finalizado el proceso de alta y el alcance técnico incluido en el momento de la firma del informe de instalación o la recepción de la notificación del alta por parte del departamento ABM.

## 6. MANTENIMIENTO PROGRAMADO

El mantenimiento programado consistirá en toda intervención realizada en la red de Metrotel, la cual será notificada previamente (con más de 48 horas de anticipación) al cliente y se realizará dentro del horario de mantenimiento establecido. Si el horario del corte previsto afecta la labor del cliente, éste puede solicitar la modificación del mismo. Metrotel se compromete a realizar los máximos esfuerzos para mover el corte al nuevo horario solicitado. Este tipo de interrupciones se puede realizar para reemplazar o agregar elementos a la red a fin de ampliar y mejorar permanentemente el servicio.

## 7. RESPONSABILIDADES DEL CLIENTE

Para una correcta instalación del servicio, el cliente deberá tener en cuenta lo solicitado a continuación:

<u>Instalación en domicilio del cliente:</u>

El cableado desde el sitio donde se encuentra el Equipo Terminal instalado por Metrotel, hasta cada uno de los puestos de trabajo, debe ser categoría 5e ó superior. Deben existir tomacorrientes para PCs, monitores y cualquier otro dispositivo electrónico, incluyendo un tomacorriente disponible donde se instalará el equipamiento que soporta el servicio provisto por Metrotel.

Se recomienda disponer de un lugar acondicionado para centralizar todo el cableado y equipos de comunicaciones de forma prolija (idealmente un rack en una sala con refrigeración).

El cliente reconoce que Metrotel no puede ejercitar control sobre el contenido de la información que circula a través de la red Internet. Por lo tanto, la seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., así como los fraudes y daños que estos pudieran ocasionar sobre el mismo cliente o terceras partes, es exclusiva responsabilidad del propio cliente. Para aumentar la seguridad, Metrotel recomienda el uso del presente servicio desde una única IP pública perteneciente al cliente y no desde cualquier IP pública de Internet, así como el uso de programas Antimalware, Firewalls y cualquier software ó hardware vigente y actualizado que evite estos ataques.

## 8. LIMITACIÓN DEL SERVICIO

Metrotel garantizará el correcto funcionamiento de la plataforma de telefonía que se utilizará para interconexión del servicio con la red pública de telefonía (PSTN). La responsabilidad de Metrotel en su calidad de prestador del servicio de telecomunicaciones y de conformidad con la normativa vigente, se extiende hasta la prestación del servicio y no dentro de los límites internos de las redes informáticas y/o de telecomunicaciones del Cliente.

Si a causa de un ataque informático y/o un ataque telefónico, se generaran llamados telefónicos, el Cliente reconoce que: i) Metrotel no podrá discernir si los llamados son realizados por el Cliente en el marco del servicio brindado o si los mismos son a consecuencia de un ataque sufrido por el Cliente, y ii) que es su responsabilidad establecer reglas de seguridad de comunicaciones telefónicas y adoptar todas aquellas medidas de seguridad que sean necesarias a fin de evitar ataques informáticos, por tal motivo Metrotel estará habilitado a facturar de igual forma las comunicaciones al valor que corresponda según el destino, y el Cliente deberá abonar dichas comunicaciones.

Sin perjuicio de lo expuesto, Metrotel se reserva el derecho de realizar controles periódicos y ante situaciones inusuales, a solo criterio de Metrotel, de intentos de llamada, tanto fructíferos como infructuosos, entrantes y/o salientes en el servicio, Metrotel se reserva la facultad de realizar en forma preventiva bloqueos parciales o totales a los efectos de proteger al Cliente. El consumo de llamadas efectivamente cursado previo a cualquier acción de bloqueo que Metrotel pudiera efectuar será facturado normalmente y en su totalidad en función de los destinos accedidos y según lista de precios vigentes a la fecha.

El Cliente no podrá alegar incrementos súbitos de tráfico y/o acceso a destinos inusuales comparado con el histórico de tráfico debidos a un ataque informático, ni cualquier otro argumento como excusa para no efectuar el pago de ese tráfico incremental y/o inusual.

El cliente reconoce que no será responsabilidad de Metrotel cualquier daño generado por la interrupción o corte del servicio que sea consecuencia de una interrupción, programada o no, de energía eléctrica o de la interrupción de otro recurso o medio técnico que intervenga en el funcionamiento del servicio en la medida que no se deba a responsabilidad directamente atribuible a Metrotel.

En ningún caso Metrotel será responsable por daño emergente, lucro cesante y/o cualquier otra pérdida que pudiera sufrir el Cliente como consecuencia directa o indirecta de la prestación de los Servicios aquí detallados.