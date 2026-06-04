# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - VEEAM CLOUD CONNECT BACKUP

## 1. DESCRIPCIÓN GENERAL
Las empresas enfrentan hoy el desafío de resguardar sus datos ante la pérdida de los mismos, ya sea por un problema técnico en el servidor (físico o virtual) o por un borrado accidental de los datos. Dada la cantidad de información que las compañías manejan es fundamental contar con una solución de Backup de manera automática y ordenada.

Veeam Backup de Metrotel es un servicio complementario a cualquier solución de virtualización <sup>(1*)</sup>, provee la funcionalidad de repositorio en la “nube”, permitiendo llevar sus datos a un sitio seguro fuera de sus dependencias físicas, alojando así la información crítica de su empresa dentro del Datacenter de Metrotel y cumpliendo con los estándares impuestos para el resguardo de la información.

Metrotel es el primer Veeam Cloud Provider en Argentina avalado por Veeam para cumplir con este rol.

## 2. CARACTERÍSTICAS
+ Veeam Backup minimiza la pérdida de datos (RPO) permitiendo realizar la protección de los mismos en un sitio remoto, cumpliendo con las políticas de protección de datos que solicitan tener un sitio de recuperación ante desastres (Backup a sitio remoto en el Cloud de un Service Provider).
+ Copias de seguridad de instancias de Amazon EC2 creadas con Veeam Cloud Backup para Amazon
+ Con los trabajos de copia de seguridad, puede transportar copias de seguridad de instancias de EC2 a repositorios locales.
+ Copias de seguridad de máquinas físicas y virtuales creadas con Veeam Agent para Microsoft Windows
+ Copias de seguridad de máquinas físicas y virtuales creadas con Veeam Agent para Linux
+ Copias de seguridad de VM creadas con la disponibilidad de Veeam para Nutanix AHV
+ Permite realizar copias de seguridad de máquinas virtuales creadas con Veeam Backup
+ No es necesario contar con almacenamiento propio.
+ Upgrade de recursos según las necesidades.
+ Políticas de control de tráfico entrante y saliente.
+ Fácil implementación.

<sup>(1*)</sup> *En casos de servidores físicos alojados en dependencias del cliente se deberá evaluar factibilidad técnica.*

## 3. ALCANCE Y ESPECIFICACIÓN TÉCNICA
+ Para implementar Veeam Backup sobre una solución de virtualización propia, el cliente deberá contar con licencias de “Veeam Backup” <sup>(2*)</sup>  para poder conectarse al Cloud de Metrotel y su infraestructura virtual debe correr sobre la plataforma de virtualización de “VMware”
+ Para la solución de Backup, Metrotel facilitara un repositorio para que el cliente aloje sus backups en la nube y será el cliente quien administre la infraestructura de backup (Jobs, políticas de backup, retenciones).
+ En el momento de la puesta en marcha, el cliente y Metrotel deberán coordinar cómo será la configuración final de la solución para establecer la conexión al Cloud de Metrotel.
+ El cliente será el responsable de realizar las pruebas sobre los Jobs de copia de Backup que el haya configurado.<sup>(3*)</sup> 
+ El cliente tendrá acceso exclusivo al repositorio de almacenamiento contratado. Dichos recursos no serán compartidos con otros clientes.
+ Una vez finalizado el contrato con Metrotel, la información replicada será eliminada de la plataforma virtual de Metrotel y de los repositorios que el cliente haya contratado.

<sup>(2*)</sup> *Para el servicio de Repositorio de Backup, el cliente deberá contar con las licencias correspondientes. Dicho licenciamiento, no está incluido en la solución. Metrotel puede proveer dicho licenciamiento.*

<sup>(3*)</sup> *La tarea de copia de seguridad es una tarea separada que debe diferenciarse de la tarea de copia de seguridad. El objetivo del trabajo de copia de seguridad es copiar un punto de restauración desde el repositorio de respaldo de origen al repositorio de respaldo de destino. Cada trabajo de copia de seguridad crea su propia carpeta en el repositorio de copia de seguridad de destino y almacena en ella todos los puntos de restauración copiados. La carpeta tiene el mismo nombre que el trabajo de copia de seguridad. Contempla varias fases, inactivo, sincronización, transformación y post-empleo.*

**Arquitectura de referencia para Veeam Backup**

![Arquitectura para veeam backup](../../../imagenes/cloud-connect/arquitectura%20para%20veeam%20backup.png)

## 4. RECURSOS DISPONIBLES

El servicio podrá ser contratado en múltiples opciones de recursos disponibles de acuerdo a las necesidades de cada cliente. El servicio Veeam Backup se compone de 1 licencia por cada servidor virtual que se quiera asociar a la solución. Además, se deberá contratar el almacenamiento que se requiera para poder alojar el backup <sup>(4*)</sup>

<sup>(4*)</sup> *El servicio básico contempla la utilización el uso de storage, que está cubierto por la contratación del servicio actual.*

## 5. ACEPTACIÓN DEL SERVICIO

Las actividades de pruebas de aceptación deberán ser realizadas por el Cliente en un plazo no mayor a cuarenta y ocho (48) horas hábiles contadas a partir de la fecha de finalización y comunicación de la puesta en marcha por parte de Metrotel. Las pruebas deberán basarse en el uso normal de la aplicación de acuerdo a las prácticas habituales de la actividad principal del Cliente y de acuerdo al relevamiento de uso y necesidades durante la etapa de preventa. Vencido el mencionado plazo, y de no mediar objeciones por parte del cliente, Metrotel procederá a la aceptación tácita del servicio para su posterior facturación.

## 6. PUESTA EN MARCHA DEL SERVICIO

En caso de que el servicio contratado no requiera presencia física del personal de Metrotel en el domicilio del cliente, Metrotel determinará el mejor medio para comunicar que se ha comenzado la prestación de dicho servicio.

## 7. LIMITACIONES DEL SERVICIO

El sistema de respaldo de Veeam Backup es una solución diseñada para minimizar la probabilidad de pérdida de información del cliente frente a un daño del equipo primario, no obstante, no se trata de un sistema infalible.

El cliente reconoce que considerando la criticidad o el impacto que pudiera ocasionarle este tipo de desperfectos, existen resguardos adicionales que puede tomar para reducir aún más la probabilidad de pérdidas. En el caso de que el sistema falle por causas imputables directamente a Metrotel y llegase a producirse algún tipo de pérdida de datos, la responsabilidad de Metrotel, previa sentencia judicial firme que así lo determine, quedará acotada como máximo al abono del servicio en cuestión. Por caso fortuito o causa mayor, no habrá responsabilidad alguna por parte de Metrotel.

Adicionalmente, el cliente reconoce que Metrotel no puede ejercitar control sobre el contenido de la información que circula a través de la red Internet. Por lo tanto, Metrotel no es responsable del contenido de ningún mensaje y/o información tanto si el envío fue hecho o no por un cliente de Metrotel. La seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Metrotel recomienda el uso de programas Antimalware, Firewalls y cualquier software o hardware vigente y actualizado que evite estos ataques.

Metrotel no efectuará la gestión de los Jobs de copia de Backup, entendiéndose por Job toda gestión a todas aquellas tareas derivadas de la propia operación y control de funcionamiento de este, quedando dichas tareas bajo estricta responsabilidad del cliente.

Una vez finalizado el contrato con Metrotel, la información resguardada será eliminada del almacenamiento luego de 15 días. No se proveerán al cliente los archivos que conformen el/los backups correspondientes. Metrotel queda excluido de toda responsabilidad sobre el traspaso de la información contenida en los repositorios de backups y/o de su eliminación una vez finalizado el contrato.

## 8. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto mediante el cual podrá realizar la gestión de eventuales reclamos. Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de la misma.


