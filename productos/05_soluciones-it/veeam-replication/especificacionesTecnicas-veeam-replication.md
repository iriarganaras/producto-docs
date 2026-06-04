# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - VEEAM REPLICATION

## 1. DESCRIPCIÓN GENERAL

Las empresas enfrentan hoy el desafío de resguardar sus datos ante la pérdida de los mismos, ya sea por un problema técnico en el servidor (físico o virtual) o por un borrado accidental de los datos. Dada la cantidad de información que las compañías manejan es fundamental contar con una solución de Disaster Recovery de manera automática y ordenada.

Veeam Replicacion de Metrotel es un servicio complementario a cualquier solución de virtualización <sup>(1*)</sup>, provee la funcionalidad y capacidad de armar un sitio de Disaster Recovery en la “nube”, permitiendo llevar sus datos a un sitio seguro fuera de sus dependencias físicas, alojando así la información crítica de su empresa dentro del Datacenter de Metrotel y cumpliendo con los estándares impuestos para el resguardo de la información.

Metrotel es el primer Veeam Cloud Provider en Argentina avalado por Veeam para cumplir con este rol.

<sup>(1*)</sup> *En casos de servidores físicos alojados en dependencias del cliente se deberá evaluar factibilidad técnica.*

## 2. CARACTERÍSTICAS
+ Veeam Replicacion minimiza la pérdida de datos (RPO) gracias al menor tiempo que utiliza para crear la réplica de las máquinas virtuales, permitiendo realizar la protección de los mismos en un sitio remoto, cumpliendo con las políticas de protección de datos que solicitan tener un sitio de recuperación ante desastres (Backup a sitio remoto en el Cloud de un Service Provider).
+ Permite realizar test de Disaster Recovery en un entorno de prueba totalmente aislado, sin la interrupción o modificación en los ambientes de producción.
+ No es necesario contar con almacenamiento propio.
+ Permite la encriptación de datos a resguardar.
+ Upgrade de recursos según las necesidades.
+ Políticas de control de tráfico entrante y saliente.
+ Fácil implementación.
  
## 3. ALCANCE Y ESPECIFICACIÓN TÉCNICA
+ Para implementar Veeam Replicacion sobre una solución de virtualización propia, el cliente deberá contar con licencias de “Veeam Replication” <sup>(2*)</sup>
+ Para la solución de réplica, Metrotel facilitara un repositorio y un pool de recursos llamado “Hardware Plan” para que el cli ente aloje sus réplicas en la nube. Esto permitirá que el cliente administre su plan de Disaster Recovery sobre la infraestructura virtual de Metrotel sin impactar en sus aplicaciones de producción.
+ En el momento de la puesta en marcha, el cliente y Metrotel deberán coordinar cómo será la configuración final de la solución para establecer la conexión al Cloud de Metrotel. La misma podrá ser realizada por medio de un enlace dedicado en L3 (RPV) o a través de Internet, esto dependerá del tipo de conectividad que el cliente disponga o quiera contratar <sup>(3*)</sup> 
+ El cliente será el responsable de realizar las pruebas sobre los Jobs de Réplica que el haya configurado.
+ El cliente tendrá acceso exclusivo al pool de recursos contratado (almacenamiento, CPU y memoria) para los Jobs de Réplica dichos recursos no serán compartidos con otros clientes.
+ Una vez finalizado el contrato con Metrotel, la información replicada será eliminada de la plataforma virtual de Metrotel y de los repositorios que el cliente haya contratado.
+ Si el cliente opta por el opcional de WAN Accelerator para el acceso por internet, deberá contar con licencia de “Veeam Repli cation” que avale dicho uso <sup>(4*)</sup> . No obstante Metrotel no aconseja dicha opción.

<sup>(2*)</sup> *Para poder conectarse al Cloud de Metrotel y su infraestructura virtual debe correr sobre la plataforma de virtualización de “VMware” Para el servicio de réplica, el cliente deberá contar con las licencias correspondientes. Dicho licenciamiento, no está incluido en la solución. Metrotel puede proveer dicho licenciamiento.*

<sup>(3*)</sup> *Previa factibilidad técnica Caso RPV, el cliente solo dispondrá de disaster recovery total, este enlace es indicado cuando el cliente tiene grandes volúmenes de cambio en sus replicas Caso Internet, el cliente contara con disaster recovery total y parcial, parcial corresponde a entrar en disaster maquinas particulares y no toda la estructura.*

<sup>(4*)</sup> *Caso del opcional WAN Accelerator, el licenciamiento de Veeam debe ser el Enterprise Plus*

**Arquitectura de referencia para Veeam Replication**

![Arquitectura veeam replication](../../../imagenes/veeam-replication/arquitectura%20veeam%20replication.png)

## 4. RECURSOS DISPONIBLES

El servicio podrá ser contratado en múltiples opciones de recursos disponibles de acuerdo a las necesidades de cada cliente.

El servicio Veeam Replication se compone de 1 licencia por cada servidor virtual que se quiera asociar a la solución. Además, se deberá contratar el almacenamiento, la memoria y el procesamiento, que se requiera para poder encender las máquinas virtuales en caso de necesitar ejecutar las pruebas de disaster recovery o entrar en contingencia finalmente. <sup>(5*)</sup>

<sup>(5*)</sup> *El servicio básico contempla la utilización de recursos de CPU y memoria RAM por 7 días cada 6 meses, el tiempo que se ex ceda se cobrara por uso en unidad por día sin fraccionamiento mientras se encuentre vigente el contrato de servicio. El uso de storage, está cubierto por la contratación del servicio actual. Se deberá contratar salida a internet, si hay servicios que lo requieran*

## 5. ACEPTACIÓN DEL SERVICIO
Las actividades de pruebas de aceptación deberán ser realizadas por el Cliente en un plazo no mayor a cuarenta y ocho (48) horas hábiles contadas a partir de la fecha de finalización y comunicación de la puesta en marcha por parte de Metrotel. Las pruebas deberán basarse en el uso normal de la aplicación de acuerdo a las prácticas habituales de la actividad principal del Cliente y de acuerdo al relevamiento de uso y necesidades durante la etapa de preventa. Vencido el mencionado plazo, y de no mediar objeciones por parte del cliente, Metrotel procederá a la aceptación tácita del servicio para su posterior facturación.

## 6. PUESTA EN MARCHA DEL SERVICIO

En caso de que el servicio contratado no requiera presencia física del personal de Metrotel en el domicilio del cliente, Metrotel determinará el mejor medio para comunicar que se ha comenzado la prestación de dicho servicio.

## 7. LIMITACIONES DEL SERVICIO

El sistema de respaldo y réplica de Veeam Replica es una solución diseñada para minimizar la probabilidad de pérdida de información del cliente frente a un daño del equipo primario, no obstante, no se trata de un sistema infalible.

El cliente reconoce que considerando la criticidad o el impacto que pudiera ocasionarle este tipo de desperfectos, existen resguardos adicionales que puede tomar para reducir aún más la probabilidad de pérdidas. En el caso de que el sistema falle por causas imputables directamente a Metrotel y llegase a producirse algún tipo de pérdida de datos, la responsabilidad de Metrotel, previa sentencia judicial firme que así lo determine, quedará acotada como máximo al abono del servicio en cuestión. Por caso fortuito o causa mayor, no habrá responsabilidad alguna por parte de Metrotel.

Adicionalmente, el cliente reconoce que Metrotel no puede ejercitar control sobre el contenido de la información que circula a través de la red Internet. Por lo tanto, Metrotel no es responsable del contenido de ningún mensaje y/o información tanto si el envío fue hecho o no por un cliente de Metrotel. La seguridad informática en los equipos del cliente contra intrusos, virus, hackers, etc., es exclusiva responsabilidad del propio cliente. Metrotel recomienda el uso de programas Antimalware, Firewalls y cualquier software o hardware vigente y actualizado que evite estos ataques.

Metrotel no efectuará la gestión de los servidores a resguardar, entendiéndose por gestión a todas aquellas tareas derivadas de la propia operación y control de funcionamiento del mismo como ser administración del sistema operativo, aplicación de parches correctivos y/o de seguridad, instalación de aplicaciones, resolución de problemas sobre aplicaciones instaladas en el servidor virtual, análisis de performance sobre aplicaciones instaladas en el servidor, monitoreo de agentes, quedando dichas tareas bajo estricta responsabilidad del cliente.

Metrotel no efectuará la gestión de los Jobs de réplica, entendiéndose por Job toda gestión a todas aquellas tareas derivadas de la propia operación y control de funcionamiento de este, quedando dichas tareas bajo estricta responsabilidad del cliente.

Una vez finalizado el contrato con Metrotel, la información resguardada será eliminada del almacenamiento luego de 15 días. No se proveerán al cliente los archivos que conformen el/los backups correspondientes. Metrotel queda excluido de toda responsabilidad sobre el traspaso de la información contenida en los repositorios de backups y/o de su eliminación una vez finalizado el contrato.

Debido a las limitaciones de VMware vSphere, si cambia el tamaño de los discos de VM en la VM de origen, Veeam Backup & Replication elimina todos los puntos de restauración disponibles (representados como instantáneas de VM) en la réplica de VM durante la próxima sesión de trabajo de replicación.

Si asigna la función de un proxy de copia de seguridad a una máquina virtual, no debe agregar esta máquina virtual a la lista de máquinas virtuales procesadas en un trabajo que utiliza este proxy de copia de seguridad. Dicha configuración puede resultar en un rendimiento del trabajo degradado. Veeam Backup & Replication asignará este proxy de respaldo para procesar otras máquinas virtuales en la tarea primero, y el procesamiento de esta máquina virtual se pondrá en espera. Veeam Backup & Replication notificará el siguiente mensaje en las estadísticas del trabajo: VM es un proxy de respaldo, a la espera de que deje de procesar las tareas. El trabajo comenzará a procesar esta máquina virtual solo después de que el proxy de copia de seguridad implementado en la máquina virtual termine sus tareas.

Si usa etiquetas para categorizar objetos de infraestructura virtual, verifique las limitaciones de las etiquetas de VM.

Debido a las limitaciones de Microsoft, no puede usar las credenciales de Active Directory de Microsoft Azure para realizar el procesamiento de aplicaciones en máquinas virtuales que ejecutan Microsoft Windows 10.

En caso de licenciamiento de Microsoft, el cliente deberá firmar una denda que libere de responsabilidades a Metrotel ante cualquier mal uso de licenciamiento de los productos de Microsoft para Disaster Recover en Metrotel. Metrotel podrá tomar acciones para mitigar el problema de licenciamiento, pudiendo apagar dichos servidores, cobrar las licencias solicitadas por Microsoft o bien cualquier otra medida que asegure el cumplimiento de licenciamiento de Metrotel con Microsoft. El cliente acepta este tipo de acciones y libera a Metrotel de la responsabilidad ante todo reclamo directo o indirecto que pudiera realizar el Cliente o Microsoft. Cabe aclara que como licencias de Microsoft refiere a cualquier producto de dicha marca que Metrotel pueda incurrir en alguna falta, por citar ejemplos: Windows, SQL Server, Remote Desktop, o cualquier otro.

## 8. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto mediante el cual podrá realizar la gestión de eventuales reclamos. Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de la misma.
