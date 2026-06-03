# ESPECIFICACIONES TÉCNICAS - CLOUD BACKUP

## 1. DESCRIPCIÓN GENERAL

Cloud Backup Metrotel es una solución de copia de seguridad y recuperación
híbrida integral, simple y completa, que soluciona los problemas de protección de
datos proporcionando un servicio fiable y altamente personalizado.

La copia de seguridad de los datos podrá realizarse desde cualquier origen y
recuperase en cualquier destino y utilizando cualquier sistema. Cloud Backup
Metrotel está configurado sobre plataformas de almacenamiento de primer nivel
(EMC, HP, etc.).

El servicio de Cloud Backup Metrotel incluye la sincronización automática del
contenido en 2 centros de almacenamiento de Metrotel, geográficamente
separados. El proceso de sincronización es automático y transparente para el
usuario. Los contenidos en Cloud Backup Metrotel tienen 100% de disponibilidad, si
por algún motivo uno de los centros de almacenamiento tiene una falla, el
contenido del cliente va a seguir disponible <sup>1</sup>


<sup>1</sup> *Cabe destacar que la sincronización a centros alternativos de almacenamiento no funciona como backup de la información. Si el contenido que se sube al centro de
datos principal es borrado accidentalmente el mismo será borrado de todas las regiones donde se haya sincronizado.*

## 2. CARACTERÍSTICAS

+ La solución está diseñada con Acronis Backup Cloud.
+ Seguridad: encriptación de datos en origen, AES-256 como algoritmo de
encriptación.
+ Eficiencia: Múltiples esquemas de backup de datos; Full e incremental,
comprensión en origen, visualización de datos respaldados.
+ Compatibilidad: soporte multiplataforma compatible con la mayoría de los
S.O. Servidores y Workstations Windows, Linux y Mac.
+ Flexibilidad: Políticas de retención y almacenamiento completamente
configurables por el usuario.
+ Escalabilidad: Sin límites de storage.
+ Cloud Backup Metrotel tiene múltiples vías de administración, cada cliente
cuenta con una consola web. A su vez puede crear grupos de operadores
donde cada operador puede administrar individualmente los Jobs de backup y
restore.
+ Alertas y Reportes: Alertas por mail sobre Jobs de Backups y espacio
disponible. Creación de reportes sobre Jobs de backup y uso de disco.
+ Recuperación desde cero, de cualquier plataforma, desde la nube.
+ VM Flashback para restauraciones incrementales rápidas.
+ Copia de seguridad y recuperación de archivos y carpetas seleccionados o de
un sistema completo.
+ Copia de seguridad orientada a aplicaciones de Microsoft SQL Server,
Exchange, SharePoint, Active Directory y Estado del sistema de Windows.
+ Recuperación granular de datos de Microsoft Exchange, SQL Server y
SharePoint.
+ Compatibilidad con máquinas virtuales y contenedores de VMware
vSphere/Microsoft Hyper-V/RHEV/Linux KVM/Citrix XenServer/Oracle VM
Server/Virtuozzo.
+ Migración simplificada del entorno físico al virtual y viceversa, tanto in situ
como en la nube.

## 3. ESPACIO DISPONIBLE

Según las necesidades de cada cliente, existen múltiples opciones de espacio
disponible de almacenamiento. El servicio está compuesto por el uso de licencias
y espacio asociado.

## 4. PRIMEROS PASOS

Una vez que ha configurado el Backup, el ciclo comenzará automáticamente en el
horario indicado. La primera vez que se ejecuta un ciclo de backup se realiza un
full backup de toda la información (toda la información seleccionada es
transferida a la plataforma de Cloud Backup Metrotel. A partir del segundo ciclo
de backup en adelante, se realizará un backup incremental de forma tal que solo
los cambios producidos respecto del backup anterior se transfieran hacia la
plataforma de Cloud Backup (esta modalidad reduce significativamente el
tiempo requerido para ejecutar un backup dado que la mayoría de los usuarios
actualizan menos del 5% del total de sus datos cada día).

Antes de comenzar la transferencia de archivos a la plataforma de Cloud Backup
Acronis, los datos son comprimidos y encriptados localmente. Esto no solo reduce
el espacio de almacenamiento en la plataforma de Cloud Backup Acronis y el
consumo de ancho de banda, sino que también asegura la privacidad de sus
datos.

## 5. ACEPTACIÓN DEL SERVICIO

Las actividades de pruebas de aceptación deberán ser realizadas por el Cliente
en un plazo no mayor a cuarenta y ocho (48) horas hábiles contadas a partir de
la fecha de finalización y comunicación de la puesta en marcha por parte de
Metrotel. Las pruebas deberán basarse en el uso normal de la aplicación de
acuerdo a las prácticas habituales de la actividad principal del Cliente y de
acuerdo al relevamiento de uso y necesidades durante la etapa de preventa.

Vencido el mencionado plazo, y de no mediar objeciones por parte del cliente, Metrotel procederá a la aceptación tácita del servicio para su posterior facturación.

## 6. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto mediante el cual podrá realizar la gestión de eventuales reclamos. Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de la misma.

## 7. PUESTA EN MARCHA DEL SERVICIO

En caso que el servicio contratado no requiera presencia física del personal de Metrotel en el domicilio del cliente, Metrotel determinará el mejor medio para comunicar que se ha comenzado la prestación de dicho servicio.

Para comenzar a realizar Backups o Restores, se debe instalar el agente correspondiente a la versión de sistema operativo que se quiera resguardar.

Para la instalación del Agente de Backup el Cliente deberá disponer en sus Workstation o Servidores de los siguientes requisitos del Sistema:

Sistema Operativo instalado:

Microsoft Windows Soportados:

+ Windows Server 2016 Technical Preview 4
+ Windows Server 2012/2012 R2, 2008/2008 R2, 2003/2003 R2
+ Windows Small Business Server 2011, 2008, 2003/2003 R2
+ Windows MultiPoint Server 2012, 2011, 2010
+ Windows Storage Server 2012/2012 R2, 2008/2008 R2, 2003
+ Windows 10, 8/8.1, 7
+ Windows Vista
+ Windows XP Professional SP2+ (x86, x64)
+ Windows 2000 SP4 <sup>*</sup>

Linux Soportado:

+ Linux with kernel from 2.4.20 to 4.4 and glibc 2.3.2 or later
+ Various 32-bit (x86) and 64-bit (x86_64) Linux distributions, including:
+ Red Hat Enterprise Linux 4.x - 7.x
+ Ubuntu 9.10 - 15.10
+ Fedora 11 – 23
+ SUSE Linux Enterprise Server 10 – 12
+ Debian 4 - 8.2
+ CentOS 5.x - 7.x
+ CloudLinux 7, 7.1
+ ClearOS 5.x, 6.x, 7, 7.1
+ Oracle Linux 5.x - 7.x (including UEK)

Hypervisors Soportados:
+ VMware vSphere ESX(i) 6.0, 5.5, 5.1, 5.0
+ Microsoft Hyper-V Server 2012/2012 R2, 2008/2008 R2
+ Microsoft Windows Server 2016TP4, 2012/2012 R2, 2008/2008 R2 with Hyper-V
+ Microsoft Windows 10, 8/8.1 (x64) with Hyper-V
+ Citrix XenServer 4.1 - 6.5
+ Red Hat Enterprise Virtualization 2.2 - 3.5
+ Oracle VM Server 3.x
+ Linux KVM

Aplicaciones Soportadas
+ Microsoft Exchange Server 2016*, 2013, 2010, 2007, 2003 SP2
+ Microsoft SQL Server 2014, 2012, 2008 R2, 2008, 2005
+ Microsoft SharePoint 2013
+ Microsoft SharePoint Server 2010 SP1
+ Microsoft SharePoint Foundation 2010 SP1
+ Microsoft Office SharePoint Server 2007 SP2
+ Microsoft Windows SharePoint Services 3.0 SP2
  
File Systems Soportados:
+ FAT16/32
+ NTFS • ReFS <sup>*</sup>
+ Ext2/Ext3/Ext4
+ ReiserFS3 <sup>*</sup>
+ ReiserFS4 <sup>*</sup>
+ XFS <sup>*</sup>
+ JFS <sup>*</sup>
+ Linux SWAP

<sup>*</sup> *Algunas limitaciones pueden existir. Consultar con el área de soporte.*


Metrotel recomienda a sus clientes limitar la cantidad de personas que vayan a administrar el sistema de backup, dada la importancia de la información crítica de su empresa. El administrador será quien tenga la cuenta de usuario para acceso a la programación y configuración del sistema. El Cliente es responsable de configurar la planificación de respaldos y políticas de retención desligando a Metrotel de cualquier responsabilidad.

## 8. LIMITACIONES DEL SERVICIO

El sistema de respaldo de backup es un sistema diseñado para minimizar la probabilidad de pérdida de información del cliente frente a un daño del equipo primario, no obstante, no se trata de un sistema infalible. El cliente reconoce que considerando la criticidad o el impacto que pudiera ocasionarle este tipo de desperfectos, existen resguardos adicionales que puede tomar para reducir aún más la probabilidad de pérdidas. En el caso de que el sistema falle por causas imputables directamente a Metrotel y llegase a producirse algún tipo de pérdida de datos, la responsabilidad de Metrotel, previa sentencia judicial firme que así lo determine, quedará acotada como máximo al abono del servicio en cuestión. Por caso fortuito o causa mayor, no habrá responsabilidad alguna por parte de Metrotel.

Adicionalmente, el cliente reconoce que Metrotel no puede ejercitar control sobre el contenido de la información que circula a través de la red Internet. Por lo tanto, Metrotel no es responsable del contenido de ningún mensaje y/o información tanto si el envío fue hecho o no por un cliente de Metrotel. La seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Metrotel recomienda el uso de programas Antimalware, Firewalls y cualquier software ó hardware vigente y actualizado que evite estos ataques.

Metrotel no efectuará la gestión de los agentes instalados en los servidores, entendiéndose por gestión a todas aquellas tareas derivadas de la propia operación y control de funcionamiento del mismo como ser administración del sistema operativo, aplicación de parches correctivos y/o de seguridad, instalación de aplicaciones, resolución de problemas sobre aplicaciones instaladas en el servidor virtual, análisis de performance sobre aplicaciones instaladas en el servidor, monitoreo de agentes, quedando dichas tareas bajo estricta responsabilidad del cliente.

Una vez finalizado el contrato con Metrotel, la información resguardada será eliminada del almacenamiento luego de 15 días. No se proveerán al cliente los archivos que conformen el/los backups correspondientes. Metrotel queda excluido de toda responsabilidad sobre el traspaso de la información contenida en los repositorios de backups y/o de su eliminación una vez finalizado el contrato.