  # ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - DATACENTER VIRTUAL

  ## 1. DESCRIPCIÓN GENERAL

El producto Datacenter Virtual ofrece al cliente los recursos necesarios para ejecutar sus aplicaciones de negocio en instalaciones del Data Center de Metrotel.

Esto se logra utilizando tecnologías de virtualización, cuya función es abstraer la infraestructura de hardware sobre la cual se despliegan los sistemas operativos donde se realiza el procesamiento de la información.

Los componentes de la infraestructura siguen cumpliendo las funciones del procesamiento (CPU), almacenamiento (memoria y disco) y comunicación (networking), sin embargo lo hacen de forma emulada por un hipervisor que permite utilizar de una manera más eficiente el hardware de servidores, discos y red subyacentes, lo cual redunda en beneficios de distinta índole.

De esta manera, con los recursos virtualizados por este método, el cliente de Metrotel puede instanciar máquinas virtuales en las que se instalará el sistema operativo y las aplicaciones acordes a su necesidad.

 ## 2. VENTAJAS DEL PRODUCTO

+ Infraestructura escalable, rápido aprovisionamiento bajo demanda, ideal para procesos críticos.
+ Consola de administración vía web.
+ Disponible para la creación de servidores virtuales Linux que no requiriesen suscripciones de licenciamiento y en caso de Windows, previa contratación.
+ El servicio podrá ser contratado en múltiples opciones de recursos de acuerdo con las necesidades de cada cliente. Podrá ser expandido cuando se considere necesario sin interrupción del servicio (previa gestión comercial).
+ La gestión del centro de procesamiento de datos, como un pool de recursos, se encuentra disponible en la infraestructura de Metrotel.
+ Mejora en los procesos de clonación y copia de sistemas al presentar una mayor facilidad para la creación de entornos de prueba que permiten poner en marcha nuevas aplicaciones sin impactar a la producción, agilizando el proceso de las pruebas.
+ Permite aprovisionarse de infraestructura en modalidad de Opex en lugar de Capex, lo que genera flexibilidad financiera.
+ La plataforma de virtualización de Metrotel actualmente está desarrollada con microprocesadores Intel Xeon.
+ Actualmente VMware es el software de virtualización utilizado
+ Actualmente el servicio incluye Veeam Backup como solución para el resguardo de contenido.
+ Como el servicio es provisto en un Datacenter provee todos los beneficios de alojamiento de infraestructura del tipo IaaS (infraestructura as a Service). Instalaciones diseñadas para alojar equipamiento de misión crítica: esta es quizás la ventaja más importante del servicio, ya que el mismo se encuentra alojado en el Datacenter de Metrotel, el cual cuenta con seguridad física, climatización, energía estabilizada y asegurada mediante equipamientos UPS, generadores redundantes y conectividad en diversas variantes. Todo ello bajo la constante supervisión de los más avanzados sistemas y de especialistas altamente calificados.

## 3. ALCANCE Y ESPECIFICACIÓN TÉCNICA 

El servicio consiste en la provisión de un Virtual Data Center en donde se define una capacidad de procesamiento, almacenamiento y conectividad dependiendo de las necesidades de cada cliente.

Una vez asignados los recursos, el cliente podrá distribuirlos como él lo considere necesario. <sup>1</sup>

El servicio de Metrotel Datacenter Virtual incluye la sincronización automática de un catálogo en donde el cliente dispone de imágenes de sistema operativo Open Source para su utilización <sup>2</sup>, como así también la posibilidad de poder utilizar Templates de máquinas virtuales preinstaladas y disponibles para el cliente. El proceso de sincronización es automático y transparente para el usuario final.

El Datacenter Virtual se encuentra disponible en varias versiones según la cantidad de recursos que se necesiten. Cada versión tiene un número máximo de servidores virtuales que se pueden crear:

Las versiones disponibles son:
+ DC hasta 5 VM
+ DC Pool hasta 10 VM
+ DC Pool hasta 20 VM
+ DC Pool hasta 50 VM
+ DC Pool hasta 100 VM
  
Los recursos que se comercializan están expresados en:
+ Procesamiento (GHz)
+ Memoria RAM (GB)
+ Almacenamiento (GB)

En el momento de la puesta en marcha, el cliente y Metrotel deberán coordinar cómo será la configuración final de su Pool de Recursos a nivel de conectividad para dejar listo el aprovisionamiento de los servidores virtuales.
La conectividad externa al Datacenter Virtual que el cliente contrate, podrá ser realizada por medio de un enlace dedicado (TLS o RPV) o a través de Internet, esto dependerá del tipo de conectividad que el cliente disponga o quiera contratar. <sup>3</sup>

<sup>1</sup>*Es responsabilidad del cliente realizar la creación y configuración de los servidores virtuales hasta el máximo contratado. Los recursos no incluyen la creación de las redes asociadas al servicio.*

<sup>2</sup>*El catálogo publicado por defecto en el Datacenter Virtual del cliente, contiene imágenes ISO y Templates basadas en sistemas operativos Linux.de uso libre Para poder utilizar sistemas operativos Windows, deberá contratar el catálogo Windows Server.*

<sup>3</sup>*Previa factibilidad técnica*

### Disco rígido

Este recurso podrá ser ampliado bajo demanda, ya sea en forma temporal o definitiva. Por el momento, las ampliaciones de este recurso se realizan con el agregado de nuevos discos al sistema. Este cambio se realiza con una breve interrupción programada del servicio.

El producto provisto, garantiza los siguientes parámetros (Throughput, IOPS y Latencia) dependiendo de la carga de trabajo a la cual se lo someta. En el cuadro adjunto se describe, los resultados que el disco puede garantizar según la configuración de cada carga de trabajo tomada como modelo.

<table>
  <th>Característica carga de trabajo</th>
  <th>Tamaño bloque I/O </th>
  <th>Modo de acceso</th>
  <th>% Write</th>
  <th>% Read</th>
  <th>Throughput (MBps)</th>
  <th>IOPS</th>
  <th>Latencia (ms)</th>

  <tr>
  <td>Configuración para base de datos</td>
  <td>4 KB</td>
  <td>Random</td>
  <td>33 %</td>
  <td>67 %</td>
  <td>17.32</td>
  <td>4227</td>
  <td>1.89</td>
  </tr>

  <tr>
  <td>Configuración para lograr máximo I/O</td>
  <td>512 Bytes</td>
  <td>Secuencial</td>
  <td>0  %</td>
  <td>100 %</td>
  <td>19.42</td>
  <td>37934</td>
  <td>0.21</td>
  </tr>

   <tr>
  <td>Configuración para lograr máximo throughput</td>
  <td>64 KB</td>
  <td>Secuencial</td>
  <td>0  %</td>
  <td>100 %</td>
  <td>194.35</td>
  <td>2965</td>
  <td>2.69</td>
  </tr>
</table>

La medición se realizó con IOmeter 1.1.0 en un servidor virtual con SO Microsoft Windows Server 2012 R2 Standard con 8 vCPU Intel Xeon CPU ES-2690 v3 @ 2.60 GHz y 12 GB RAM sobre un disco "no particionado" utilizando los parámetros indicados en la tabla adjunta (columnas de color celeste).

Debido a que el acceso a disco depende del tamaño de bloque de la operación, el % de lectura, % escritura y modo de acceso (aleatoria o secuencial), el cliente es responsable de realizar una medición en un entorno similar al descripto. Todo reclamo respecto de IOPS, Throughput y Response Time (Latencia) no serán computados como como parte del SLA, debido a la complejidad de medición respecto a la consideración de datos previamente descriptos, y del modo empleado/configurado por el cliente para el acceso al disco.

### Conectividad

La conectividad es independiente del servicio seleccionado, permitiéndole elegir entre las diversas alternativas que Metrotel posee:
+ Acceso a Internet dedicado: Mediante esta alternativa, se provee un acceso a Internet dedicado con la cantidad de IPs públicas que contrate.
+ Redes de datos MPLS: En caso de necesitar utilizar el servidor virtual como una extensión de su propia red, se provee un servicio de TLS (Transparent Lan Service), lo que le permite acceder al servidor de forma segura, sin tener contacto con Internet. Metrotel cuenta con otros servicios de conectividad en caso de ser necesario o no pueda brindarse el servicio TLS, ejemplo RPV, etc. (verificar estos servicios con el área comercial según las necesidades requeridas). Para utilizar más de una red que conecte los servidores virtuales, se deberá proveer un diagrama lógico de la conectividad que se desee realizar. Metrotel deberá aprobar dicha conectividad.

### Servicio de Backup de Máquinas Virtuales

Servicio de Resguardo de Información para Máquinas Virtuales:

En la actualidad, Metrotel utiliza el software Veeam Backup & Replication (VBR) para realizar el respaldo de las máquinas virtuales en la infraestructura del producto Data Center Virtual. El objetivo de VBR es minimizar la pérdida de datos aplicando políticas de respaldo que se reflejan con la definición y uso de tareas de backup (“jobs de backup”).

Los jobs de backup realizados de manera estándar en la plataforma de Metrotel aplican al nivel de la máquina virtual y el hipervisor, de modo que no se utilizan agentes de software adicionales en el sistema operativo del cliente. La técnica utilizada para realizar el respaldo se basa en la utilización de snapshots con la finalidad específica de producir el respaldo de información, haciendo uso de vStorage APIs for Data Protection (VADP) de VMWare.

El respaldo de información se realiza de manera programada una vez por día, ejecutándose un job de backup en el cual VBR produce un snapshot de la máquina virtual para realizar la copia de la información de los discos virtuales desde el disco original hacia un repositorio de disco externo. Cada snapshot determina un punto de restauración posible.

De manera predeterminada, e incluido en el servicio estándar del producto Data Center Virtual de Metrotel, se tiene parametrizado quince (15) puntos de restauración para la política de resguardo de información, correspondientes a un ciclo de 15 días consecutivos de respaldos, realizándose uno completo (“full backup”) la primera vez que se activa la tarea de resguardo (“job de backup”). El respaldo completo, luego, se repite cada 7 días, mientras que el resto de los días del ciclo se realizan resguardos incrementales.

En caso de requerirse mayor tiempo de retención sobre los datos resguardados, antes de utilizar el servicio se deberá informar a Metrotel para evaluar la factibilidad técnica. El cambio de la retención estándar en la política de resguardo tendrá un costo adicional, como mínimo dependiendo del tiempo de retención que se requiera. De manera estándar, el producto de Metrotel incluye dos (2) restauraciones de información al mes, en caso de ser necesario mayor cantidad puede aplicarse cargos adicionales.

*Nota: Metrotel a su criterio podrá optar por solicitarle al cliente el cambio de servicio de datos que contrató, en caso de monitorear un consumo excesivo en dicho tráfico o un uso indebido del mismo. Además, Metrotel podrá optar por cortar todo el tráfico del servicio de datos contratado, hasta tanto el cliente solucione los problemas que causa dicho tráfico excesivo y que perjudica el buen funcionamiento de la plataforma. El cliente acepta que dicho corte del servicio no contará para el cálculo de disponibilidad del servicio y libera de responsabilidad a Metrotel de todo reclamo y/o cualquier otra pérdida que pudiera sufrir el cliente como consecuencia directa o indirecta.*

Metrotel no se responsabiliza si debido a algún motivo de fuerza mayor no se ejecuta la tarea de resguardo de información en alguno de los 15 días del ciclo mencionado. El Cliente acepta que el servicio de respaldo de información materializa un valor agregado por parte de Metrotel en el estándar del producto Virtual Data Center, y no podrá exigir o alegar falta alguna en el cumplimiento de las obligaciones del servicio contratado.

En caso de requerirse una restauración, Metrotel restaurará la máquina virtual por completo (íntegra) y de acuerdo con la existencia de puntos de restauración existentes en el ciclo activo. No se realizarán restauraciones de archivos contenidos dentro del sistema operativo de la máquina virtual. Para realizar la acción de restauración, deberá registrarse un ticket de tipo “Consulta” o “Mantenimiento” sobre el servicio contratado, en ninguna circunstancia dicho ticket será considerado “Reclamo Técnico (no computará SLA).

**Servicios opcionales/adicionales**

A continuación, se detallan los opcionales que podrán ser contratados adicionalmente al Datacenter Virtual de Metrotel:
+ Procesamiento, Memoria RAM y Almacenamiento: El cliente podrá ampliar cualquiera de estas capacidades para ajustarlas a sus necesidades previa gestión comercial.
+ Para los casos de conectividad a través de Internet dedicado, TLS o RPV, dichos servicios se contratan adicionalmente al servicio de DC virtual, de acuerdo a la necesidad específica del cliente, previo análisis de factibilidad técnica por parte de Metrotel.
+ Firewall Virtual VMware NSX Edge: las especificaciones de este opcional se encuentran en el Anexo “Firewall Virtual VMware”.
+ El Sistema Operativo Windows se deberá contratar un Repositorio del mismo, el cual tendrá Templates de versiones vigentes en el ciclo de Vida de Microsoft (Windows Server Stándard de 64bits)
+ SQL Server Estándar (el mínimo recomendado de la VM es 2Vpu, 4Gb RAM y 150Gb de disco. El SQL se debe licenciar en Paquetes de 2 vCPU, Ej: para un servidor con 4 vCPU, deberán contratarse 2 opcionales.
+ Windows Remote Desktop, debe contratarse como opcional por unidad.
+ Office Proffesional Plus, debe contratarse como opcional por unidad.
+ Metrotel dispone de una oferta de Licencias de seguridad informática ESET (Endpoint AV, Endpoint Security y File Security).
  
Es aconsejable contratar un FW Virtual NSX Edge para este producto, caso contrario no podrá gestionar la seguridad y redes del servicio contratado. La otra opción es contratar un Internet Dedicado con la cantidad de IP Públicas por el total de servidores, Metrotel no aconseja esta opción ya que no incluye seguridad salvo en caso de Mitigado.

### Consola de administración vía web

El cliente dispondrá de una consola web para la administración de su Datacenter Virtual. Esta consola de administración puede ser accedida a través de un browser que sea soportado por la plataforma, que se esté utilizando para acceder a la consola web, soporte las siguientes características:

La consola de administración provee las siguientes funcionalidades:
+ Aprovisionamiento de Templates y ISO de Linux
+ Creación, eliminación y modificación de servidores virtuales.
+ Administración de Firewall Virtual: creación de reglas NAT y de FW. Creación de túneles VPN hasta el máximo contratado. (previa contratación)
+ Generar Snapshots de sus servidores virtuales, utilizara el espacio en disco asociado al pool de recursos contratados. <sup>(*)</sup> 
+ Operaciones de aprovisionamientos y modificaciones de Máquinas Virtuales

<sup>(*)</sup> *Si bien el producto permite realizar snapshot- dicho snapshot no puede superar los 300Gb y no puede durar más de 7 días, de lo contrario será eliminado de manera automática, de requerir un backup por tarea del cliente puede contratar el opcional de backup y mantenerlo por los días que requiera El snapshot consume memoria y disco de la propia vm, afectando su funcionalidad cuando pasa los limites anteriores por ello la precaución.*

### Características del licenciamiento

En sistemas operativos GNU/Linux, al tratarse de un sistema operativo de código abierto y GPL (General Public License), permiten el uso libre del S.0 en las versiones que contemplen este tipo de licencia. Frente a cualquier inconveniente con el sistema operativo puede solicitarse la reinstalación del mismo a través de soporte técnico.

Por otra parte, para el caso de sistemas operativos Windows, el servicio contempla la licencia original de Microsoft, la cual debe ser provista por Metrotel en todos los casos, no permitiéndose la instalación de licencias del cliente o terceras partes.

En el caso que el cliente contrate el opcional de SQL Server o de Remote Desktop, aplican las mismas condiciones referidas al sistema operativo Windows de Microsoft.

Si Metrotel no cuenta con el licenciamiento de la versión que el cliente solicite, y en caso de requerirse el traslado de uso de licencias del cliente, este deberá validarse de acuerdo al contrato y reglamentación de Microsoft. Se evaluará si la licencia del cliente aplica para el “Traspaso de Responsabilidad” de licenciamiento permitido (documentación en Anexo). Para el caso que, si lo aplique, el cliente deberá firmar un nuevo alcance que permita el traspaso de su propia licencia dentro de la infraestructura de Metrotel el cual será provisto oportunamente.

El cliente es responsable de mantener las versiones de sistemas operativos en versiones vigentes, con soporte tanto de la comunidad para versiones Linux como de Microsoft para versiones Windows o SQL Server. Además, el cliente es responsable de realizar las actualizaciones de seguridad que la marca del sistema operativo requiera o recomiende.

El cliente es total y único responsable del sistema operativo instalado en sus equipos, como así también del correcto licenciamiento del mismo, solicitando a Metrotel en el caso de productos Microsoft, la/slicencia/s correspondiente/s,según la oferta de opcionales de los productos de Metrotel.

Metrotel no se responsabiliza de versiones de sistema operativos invitados Microsoft que no estén actualizados a las versiones vigentes y bajo soporte por Microsoft.

Si Metrotel tuviese algún reclamo, notificación o multa por parte de Microsoft, la cual sugiere alguna infracción al uso indebido de licencias, versiones fuera de soporte, etc., Metrotel trasladará dicho reclamo al cliente pudiendo la misma ser económica. El cliente no podrá alegar en ningún momento desconocimiento alguno y deberá aceptar las condiciones respectivas.

Para cualquier software que no sea provisto por Metrotel, que sea instalado en el entorno de sistema operativo entregado por Metrotel, el Cliente deberá contar con la propiedad de la licencia y verificar que los mismos no violan ningún derecho de terceros, cumpliendo con todas las prescripciones de la ley 11.723 de propiedad intelectual y su modificación en la ley 25.036.

Frente a cualquier multa o costo que el fabricante del software en cuestión impute a Metrotel en su carácter de Hoster, Metrotel se reserva el derecho de trasladar dicho importe al cliente generador del incumplimiento.

Las versiones de sistema Operativo Windows deben ser las vigentes según Microsoft. En el siguiente Link, puede consultar la vigencia por versión: https://support.microsoft.com/es-bo/lifecycle/search/1163

Asimismo, las versiones a utilizarse deben ser las soportadas por Vmware. En el siguiente Link puede consultar cuales son:

https://www.vmware.com/resources/compatibility/search.php?deviceCategory=software&details=1&partner=110&releases=429 &productNames=15&page=1&display_interval=10&sortColumn=Partner&sortOrder=Asc&testConfig=16

Si el cliente utilizara cualquier otro licenciamiento no mencionado o no permitido, Metrotel no será responsable por los reclamos que reciba respecto al mal uso de licenciamiento, pudiendo Metrotel trasladar ese reclamo de cualquier índole directamente al cliente.


## 4. REQUISITOS DE USUARIO FINAL

**a. Cumplimiento.** Si Microsoft cree razonablemente que un Cliente de Metrotel no está cumpliendo con los términos presentes en esta sección, Metrotel cooperará de buena fe con Microsoft para investigar y subsanar el incumplimiento.

**b. Copias del Software Complementario.**  Dentro de un periodo de treinta (30) días después de la terminación de un servicio, Metrotel:

(i) retirará todas las copias de Software Complementario de los dispositivos del cliente o inutilizará el Software Complementario de forma permanente; y (ii) exigirá que el cliente devuelva o destruya todas las copias de Software Complementario que haya recibido.

**c. Requisitos y obligaciones adicionales.** 

**a. Aviso de propiedad intelectual, marca y patente.**  El Cliente no debe eliminar ningún aviso de propiedad intelectual, marca o patente incluido en los Productos o el Software o sobre ellos. El Cliente no tiene derecho alguno en virtud de estos términos a utilizar ningún logotipo de Microsoft de ninguna manera. Cada vez que se haga referencia por primera vez a un Producto en cualquier comunicación escrita o visual, el Cliente debe utilizar la marca, el descriptor de Productos y el símbolo de marca (“” o “®”) adecuados y debe indicar claramente la propiedad de Microsoft (o de los proveedores de Microsoft) de esas marcas. Para obtener información sobre las marcas de Microsoft, incluida una lista de las marcas actuales, consulte http://www.microsoft.com/trademarks. El Cliente no debe realizar ninguna acción que interfiera con, o disminuya, el derecho, la titularidad y el interés de Microsoft (o de los proveedores de Microsoft) en las marcas o los nombres comerciales.

**b. Antipiratería.**  El Cliente no debe participar en la fabricación, el uso, la distribución o la transmisión de software falsificado, pirateado o ilegal. El Cliente no puede distribuir ni transmitir Productos o Software propiedad de Microsoft. Metrotel debe informar a Microsoft de toda sospecha de falsificación, piratería u otra infracción de derechos de propiedad intelectual e industrial tan pronto como tenga conocimiento de ella. Metrotel cooperará con Microsoft en la investigación de cualquier parte que sea sospechosa de estas actividades y de los recursos relacionados.

**c. Permisos del gobierno.**  Metrotel debe ejercer sus derechos en virtud de estos términos, así como el cliente debe cumplir con los mismos y con todas las leyes y reglamentos aplicables.

**d. Indemnidad.** Defensa frente a reclamaciones de terceros. El Cliente debe defender a Metrotel ante cualquier reclamación de un tercero que se relacione con (1) cualquier virus de software introducido por el Cliente; (2) la infracción sustancial de los presentes términos por parte del Cliente, que no se relacionen con las denuncias ni los pagos; (3) la instalación, el uso, el acceso, la copia, la reproducción o la distribución no autorizados de cualquier parte de los Productos por parte de cualquier tercero, aun cuando éste preste servicios al Cliente); (4) la distribución continua de un producto presuntamente infractor, después de que Metrotel haya enviado un aviso al Cliente para que deje de hacerlo; o (5) un uso de los Productos por parte del Cliente en relación con un uso de alto riesgo. El Cliente pagará el importe de cualquier sentencia adversa que se dicte con carácter firme y definitivo o acuerdo transaccional aprobado que resulte de una reclamación cubierta por esta sección. Las obligaciones en virtud de esta sección no están sujetas a la limitación de responsabilidad ni a la exclusión de ciertos daños en virtud de ninguna Solicitud de Servicio o Contrato Marco.

**e. Leyes anticorrupción.** (i) Cumplimiento de las leyes de lucha contra la corrupción por parte del Cliente. El Cliente cumplirá con todas las leyes aplicables contra el soborno, la corrupción, los libros y registros imprecisos, los controles internos inadecuados y el blanqueo de dinero, incluyendo la Ley Estadounidense sobre Prácticas Corruptas en el Extranjero (“Leyes Anticorrupción”). Ningún representante del Cliente ofrecerá ni pagará, de forma directa ni indirecta, nada de valor (bajo lo que se incluyen regalos, viajes, atenciones, donaciones de caridad o empleo) a ningún funcionario o empleado de ninguna agencia gubernamental (incluidos los funcionarios elegidos o cualquier particular que actúe en nombre de dicha entidad), partido político ni organización internacional pública, así como tampoco a ningún candidato con cargo político (“Funcionario Público”), con el propósito de (1) influenciar de forma incorrecta cualquier acto o decisión de dicho Funcionario Público para promocionar, de cualquier forma, los intereses empresariales de la otra parte, o de (2) promocionar indebidamente de cualquier otra forma los intereses empresariales de la otra parte. El Cliente tiene prohibido pagar gastos en concepto de viajes, alojamiento, regalos, atenciones o contribuciones de beneficencia a funcionarios públicos en nombre de Microsoft. El Cliente también tiene prohibido utilizar los fondos proporcionados por Microsoft, así como cualquier ganancia obtenida a partir de cualquier negocio de Microsoft, para pagar gastos de viajes, alojamiento, regalos, atenciones o contribuciones de beneficencia a funcionarios públicos. Microsoft prohíbe sobornos de todo tipo, incluidos los pagos de facilitación. Un pago de facilitación es un pequeño pago para garantizar o agilizar una acción rutinaria del Gobierno por parte de un funcionario público. El Cliente no tomará represalias contra nadie que, de buena fe, informe de una posible infracción de este apartado o se niegue a participar en actividades que infrinjan este apartado. Si el Cliente incumple este apartado, tanto Microsoft como Metrotel podrán denunciar al Cliente ante las autoridades argentinas, de los EE. UU. o extranjeras para su procesamiento penal u otras medidas de ejecución, o para presentar una demanda por daños y perjuicios.

(ii) Contabilidad y conservación de registros. El Cliente establecerá y mantendrá un sistema de contabilidad razonable. El Cliente mantendrá un sistema de controles internos para impedir el pago de sobornos y proporcionar una garantía razonable de que los estados y los informes financieros son exactos. El Cliente no tendrá cuentas ocultas ni sin registrar, con ningún fin. Se prohíben las entradas falsas, engañosas, incompletas, imprecisas o artificiales en los libros y registros.
(iii) Aprendizaje. El Cliente proporcionará formación anual sobre el cumplimiento de las Leyes Anticorrupción a sus empleados.

**f. Protección de datos.** El cliente es responsable por la integridad y resguardo de su información. En ningún caso Metrotel será responsable por daño emergente, lucro cesante y/o cualquier otra pérdida que pudiera sufrir el cliente como consecuencia directa o indirecta de la prestación de los servicios aquí detallados. En el caso de que el sistema falle por causas imputables directamente a Metrotel y llegase a producirse algún tipo de pérdida de datos, la responsabilidad de Metrotel, previa sentencia judicial firme que así lo determine, quedará acotada como máxima al abono del servicio en cuestión. Por caso fortuito o causa mayor, no habrá responsabilidad alguna por parte de Metrotel.

Metrotel entrega el servidor virtual al cliente con un usuario administrador y una contraseña de dicho usuario. Es responsabilidad del cliente cambiar la contraseña y resguardar la misma, para evitar inconvenientes en la operatoria del servidor virtual. Metrotel no guarda las contraseñas que se entregan al cliente. En caso de extravió o pérdida de la misma, es responsabilidad del cliente tener los procedimientos correctos para la recuperación de la misma, dependiendo del sistema operativo instalado en el servidor virtual. Es su responsabilidad establecer reglas de seguridad y adoptar todas aquellas medidas o políticas de seguridad que sean necesarias a fin de evitar ataques informáticos.

Metrotel no realiza ningún monitoreo de los recursos de CPU, RAM o almacenamiento del servicio prestado, es responsabilidad del cliente realizar los monitoreos necesarios según corresponda. Sin perjuicio de lo cual, Metrotel podrá informarle o sugerir al cliente, a modo informativo, para que tome medidas para asegurar un buen funcionamiento del servicio.

## 5. RESPONSABILIDAD POR PARTE DEL CLIENTE
El cliente es responsable por la seguridad de su Data Center Virtual.

El cliente podrá acceder a la plataforma en forma remota por medio de una conexión a Internet con IP fija. Para ello contara con una interfaz web para acceder al Datacenter Virtual (pool de recursos de su organización) y disponer de acceso directo al servidor sin necesidad de acceder por conexión remota al equipo. De esta forma y a través de la consola del Datacenter Virtual podrá crear, eliminar, reiniciar, apagar o suspender el servidor virtual sin necesidad de llamar al centro de operaciones de Metrotel.

El cliente es total y único responsable del sistema operativo instalado en sus equipos, como así también del correcto licenciamiento del mismo, solicitando a Metrotel en el caso de Microsoft la licencia correspondiente.

El Cliente es responsable, ante un pedido de reinstalación del Sistema Operativo, de realizar un Backup de la información previamente contenida en el Servidor y de la subsecuente restitución de la misma y reconfiguración de aplicativos, herramientas, etc. que vaya a utilizar en el mismo. El cliente no podrá alegar que el Backup realizado por Metrotel lo exime de dicha responsabilidad.

Metrotel no realizará la configuración ni dará soporte técnico sobre el enrutamiento de red que disponga el cliente. El cliente es el responsable de enrutar todo el tráfico entre las máquinas virtuales que contrató.

El cliente es responsable por la integridad y resguardo de su información. En ningún caso Metrotel será responsable por daño emergente, lucro cesante y/o cualquier otra pérdida que pudiera sufrir el cliente como consecuencia directa o indirecta de la prestación de los servicios aquí detallados. En el caso de que el sistema falle por causas imputables directamente a Metrotel y llegase a producirse algún tipo de pérdida de datos, la responsabilidad de Metrotel, previa sentencia judicial firme que así lo determine, quedará acotada como máxima al abono del servicio en cuestión. Por caso fortuito o causa mayor, no habrá responsabilidad alguna por parte de Metrotel.

Metrotel entrega el Portal de administración al cliente con un usuario administrador y una contraseña de dicho usuario. Es responsabilidad del cliente cambiar la contraseña y resguardar la misma, para evitar inconvenientes en la operatoria. Metrotel no guarda las contraseñas que se entregan al cliente. En caso de extravió o pérdida de la misma.

Es su responsabilidad establecer reglas de seguridad y adoptar todas aquellas medidas o políticas de seguridad que sean necesarias a fin de evitar ataques informáticos. El cliente es responsable de actualizar parches de seguridad que requiera la versión de sistema operativo que utilice como así también de cualquier otro software instalado en el mismo.

En el caso que el servicio sufriese algún ataque informático, el cliente será el único responsable de la perdida de información, daños o perjuicios que esto conlleve, desligando a Metrotel de toda responsabilidad ante cualquier denuncia o penalidad que estos daños provoquen.

## 6. LIMITACIONES DEL SERVICIO

Metrotel no se hace responsable por la integridad, inconsistencia y/o pérdida de los datos que puedan ocasionar las fallas que involucren a los componentes del equipo adquiridos (hardware o software) ni errores humanos de terceros ajenos a Metrotel.

El servicio no incluye firewall, salvo que el cliente los contrate adicionalmente los productos de Seguridad de Metrotel. El servicio no incluye la importación ni exportación de imágenes de VMs propias (formato OVF soportado), si requiere este servicio deberá contratarse otro producto SADM (Servicios Administrados) para tal fin.

Para cualquier software que no sea provisto por Metrotel, que sea instalado en el entorno de sistema operativo o Sistema Operativo licenciado que no sea provisto por Metrotel, el Cliente deberá contar con la propiedad de la licencia y verificar que los mismos no violan ningún derecho de terceros, cumpliendo con todas las prescripciones de la ley 11.723 de propiedad intelectual y su modificación en la ley 25.036. Frente a cualquier multa o costo que el fabricante del software en cuestión impute a Metrotel en su carácter de Hoster, Metrotel se reserva el derecho de trasladar dicho importe al cliente generador del incumplimiento.

Una vez finalizado el contrato con Metrotel, la información resguardada será eliminada del almacenamiento luego de 15, salvo que el cliente defina lo contrario que, en dicho caso, no podrá hacer reclamo alguno hacia Metrotel si este lo requiriese luego de desistir a dicho resguardo, una vez pasado dicho lapso no se podrá recuperar la información. No se proveerán al cliente los archivos que conformen el/los servidores virtuales ni sus backups correspondientes. El cliente solo tendrá acceso a descargar la información contenida en los servidores virtuales a través del enlace contratado en el servicio que está efectuando la baja. Metrotel queda excluido de toda responsabilidad sobre el traspaso de la información contenida en los servidores virtuales y/o de su eliminación una vez finalizado el contrato, salvo contratación aparte de los servicios necesarios.

## 7. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto (0800-362- 1040) mediante el cual podrá realizar la gestión de eventuales reclamos.

Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de la misma.

Metrotel no brinda soporte técnico de ningún tipo sobre el sistema operativo o aplicaciones que corren dentro del servidor virtual. Sólo se brinda soporte técnico sobre la infraestructura virtual o la conectividad de los datos que el servicio incluya. Los enlaces contratados por separado para la prestación del servicio tendrán su propio alcance según lo contratado.

En el caso que se provea las contraseñas de acceso al servidor virtual para realizar alguna prueba, el cliente libera de toda responsabilidad a Metrotel de cualquier problema, perdida de información o modificación de la información que puede suceder por haber brindado dicha información crítica.

El servicio de consulta o mantenimiento solo incluye 5 consultas por mes no acumulativas. El horario de atención de dichas consultas es en días y horario laboral pudiendo demorar hasta 96 hs. hábiles.

En caso de requerir soporte sobre consultas 7x24 hs. deberá contratarlo como Servicios Administrados, previa aprobación técnica de Ingeniería de Datacenter.

## 8. ACEPTACIÓN DEL SERVICIO

Las actividades de pruebas de aceptación deberán ser realizadas por el Cliente en un plazo no mayor a cuarenta y ocho (48) horas hábiles contadas a partir de la fecha de finalización y comunicación de la puesta en marcha por parte de Metrotel vía mail. Las pruebas deberán basarse en el uso normal de la aplicación de acuerdo a las prácticas habituales de la actividad principal del Cliente y de acuerdo al relevamiento de uso y necesidades durante la etapa de preventa. Vencido el mencionado plazo, y de no mediar objeciones por parte del cliente, Metrotel procederá a la aceptación tácita del servicio para su posterior facturación.