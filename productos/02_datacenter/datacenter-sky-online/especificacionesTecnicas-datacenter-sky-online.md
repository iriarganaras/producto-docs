# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - DATA CENTER TIER 3 – SKY ONLINE

## 1. DESCRIPCIÓN GENERAL
Metrotel, en alianza con Sky Online, ofrece a sus clientes la posibilidad de alojar equipamiento en Datacenter con Infraestructura Tier 3 ubicado en Balcarce 479, CABA. El servicio contempla las siguientes prestaciones de comunicaciones:
+ Espacio físico en Datacenter en las versiones de Full Rack y Medio Rack <sup>(1*)</sup>
+ Conectividad a Internet de Metrotel (opcional)
  
<sup>(1*)</sup> *Para soluciones de jaulas o salas exclusivas se deberá evaluar las necesidades del cliente y proceder a la cotización, el medio Rack es compartido.*

## 2. CARACTERÍSTICAS TÉCNICAS DEL DATACENTER
A continuación, se describen las diferentes versiones del producto y las principales características técnicas del Datacenter sobre las cuales se apoya el servicio de Colocation Tier 3 – Sky.

![Colocation](../../../imagenes/datacenter-sky%20online/colocation.png)

## 3. SUMINISTRO ELÉCTRICO

El Datacenter cuenta con dos transformadores de media tensión de 2 MVA y 3 MVA respectivamente. El suministro de energía es realizado en media tensión (13,2 KV) por la empresa Edesur con conexión a dos subestaciones eléctricas diferentes.

**Energía ininterrumpida**

El sistema de energía ininterrumpida está diseñado con dos transformadores de media tensión (según lo explicado en el punto anterior) que pueden recibir media tensión de dos subestaciones de transformación eléctrica diferentes de la empresa Edesur.

A su vez el Datacenter cuenta con un sistema compuesto por dos UPS marca Eaton de 550 KVA, alimentando cada UPS una rama de energía IT y cada UPS posee 2 bancos de batería que garantizan el mantenimiento concurrente del equipamiento. Cada UPS tiene la capacidad para alimentar todo el consumo IT del Datacenter.

Para garantizar la continuidad de energía, ante una falta de suministro, el Datacenter tiene 2 generadores marca Caterpillar de 2 MVA cada uno. Cada generador tiene la capacidad para alimentar todo el consumo de energía del edificio y la provisión del combustible se hace por medio de dos tanques sisterna con capacidad de 35.000 litros cada uno lo que brinda una autonomía de más diez (10) días de generación ininterrumpida.

Todo el sistema de transferencia de energía entre la red, los generadores y el arranque y apagado de estos se realiza en forma automática mediante un sistema de PLC.
Los motogeneradores, el sistema de UPS y las baterías tienen una configuración N+1.

**Sala de baterías**

Los 4 bancos de baterías de las UPS y los dos bancos de batería correspondientes a los -48V DC se encuentran en una sala diferente y de uso exclusivo para las baterías.

**Fuente secundaria de generación de emergencia**

El Datacenter tiene dos generadores turbo diesel marca Caterpillar con una capacidad de generación de 2 MVA cada uno. Cada generador se encuentra precalentado para su arranque inmediato y asume la totalidad de la carga eléctrica en menos de 30 segundos. Ambos generadores se encuentran en una sala acondicionada para este tipo de equipamiento con extracción de gases, sistema de extinción de fuego CO2, dispositivos antivibraciones y canalizaciones para derrame de líquidos.

Los tanques principales de combustible (Gas Oil) se encuentran bajo tierra en una sala diferente a los generadores. La carga de combustible se realiza desde la calle donde se encuentra una válvula para la conexión de un camión cisterna. El contar con dos tanques permite el manejo del combustible permitiendo contar siempre con combustible apto (no envejecido) disponible para ser utilizado por los generadores. Dentro de nuestra rutina de mantenimiento está el análisis periódico del combustible para determinar el estado del mismo.

**Instalación eléctrica en las salas de Housing**

Las salas disponen de un suministro diversificado desde dos ramas (A y B) independientes de UPS, Tableros de distribución y PDUs. Cada una de las ramas A y B tiene la capacidad de soportar la carga total de IT. En caso de una falla en una rama aquellos equipos que dispongan de doble entrada de alimentación serán alimentados continuamente sin afectar su normal operación. Los circuitos a disposición del cliente se encontrarán en un tablero de distribución monofásico con circuitos de 36 A con interruptores curva C.

## 4. CLIMATIZACIÓN

La sala dispone de un sistema de climatización de precisión Liebert System 3 dotado de dos Unidades de Tratamiento de Aire capaces de refrigerar hasta 75 KW/H de IT insuflando aire frío por el bajo piso técnico, administrando la salida del mismo por medio de placas enrejadas en los pasillos fríos de acuerdo al layout y carga puntual de potencia.

Estas Unidades controlarán el paso de agua fría proveniente de la planta dual de Chillers situada en el segundo piso. Una de las unidades será la de punta, es decir que estará funcionando, mientras que la segunda estará en espera controlada por medio de un sistema de control y vigilia que permanentemente monitorean a las unidades, así como a los parámetros ambientales de la sala. Por ejemplo, la falta de presión de aire en la unidad principal ocasionará una alarma en este sistema que hará despachar a la unidad de espera para suministrar aire fresco a las instalaciones en forma inmediata. Ambas Unidades estarán alimentadas a partir de dos tableros seccionales en el piso 1 que a su vez están alimentados de dos tableros distintos de Baja tensión de Planta Baja.

**Redundancia de los sistemas**

Las redundancias de los sistemas de climatización ofrecidos contemplan los siguientes supuestos.

A) Falla de una unidad de tratamiento de aire, tal como fue mencionado en el punto anterior la falla de un equipo hará que el sistema despache a la unidad gemela de reserva, manteniendo de ésta forma la climatización del espacio.

B) Baja de rendimiento inesperado de una Unidad de tratamiento de aire. En éste caso la segunda unidad será despachada debido a que los parámetros ambientales del aire de retorno de la primera unidad están próximos a los valores de SLA. Estos valores pueden ser temperatura elevada, o humedad ya sea alta o baja respecto de los valores de SLA.

**Pasillo frío/caliente**

Considerando la cantidad de potencia prevista por el cliente el layout propuesto es de pasillos fríos / calientes no confinados. Para el apropiado manejo de las corrientes de aire de retorno los equipos deben disponerse en forma perpendicular a las Unidades de tratamiento de aire. La sala será ajustada en cuanto a cantidad de aire y presión en función de las cargas puntuales y verificando temperaturas específicas que permitan optimizar la performance tanto necesaria para los equipos como de eficiencia energética.

El ambiente solicitado por el cliente es aquel comprendido en el apartado de ASHRAE TC 9.9 en dónde las temperaturas de Bulbo seco deberán estar entre 20 y 25 grados centígrados y la humedad relativa ambiente entre el 30% y el 60% respectivamente. Debe señalarse que estas temperaturas sugeridas por el ASHRAE son aquellas de ingreso al frente de los equipos.

Como el monitoreo se efectuará en los retornos de las unidades de tratamiento de aire los umbrales serán entre 20 y 26 grados centígrados, mientras que la humedad se mantendrá entre el 30% y el 60% originales. Esta variación de un grado es necesaria en virtud que la muestra del aire de retorno en considerablemente más caliente que el aire de ingreso a los equipos en condiciones normales de operación.

## 5. SISTEMA DE SEGURIDAD

**Oficina de seguridad**

El Datacenter cuenta con una oficina de seguridad separada físicamente del resto de las áreas. En esta oficina se autorizan los ingresos, se administra el sistema de control de acceso y se toman las acciones de seguridad ante un evento.

**Cámaras de seguridad**

Las inmediaciones, los accesos, los pasillos, los medios de elevación y las salas se encuentran monitoreadas por medio de cámaras conectadas a un sistema de registro digital en discos rígidos 7 x 24 x 365.

**Almacenamiento de grabaciones**

Los registros en forma digital se mantienen en disponibilidad durante 3 meses, pudiéndose solicitar los backups de ese período para su posterior guarda.

**Sistema de monitoreo**

El sistema de monitores de seguridad es atendido 7 x 24 x 365 por personal contratado a través de una agencia registrada en el Gobierno de la Ciudad de Buenos Aires bajo la disposición número 00421-DGSPR/09 y disposición DI-2012-37-DGSPR.

## 6. PROTECCIÓN CONTRA INCENDIOS

**Sistema de detección y prevención**

El edificio cuenta con un sistema de detección y extinción controlados por medio de una central Fenwalnet serie 8000. Este sistema controla los detectores (iónicos, ópticos, monóxido de carbono e hidrocarburos), ANALASERS, alertadores, tampers, detención de los sistemas de ventilación forzada, presurización de escaleras y sistemas de extracción de humo. Asimismo, éste sistema controla el disparo de extinción por medio de agente limpio FM 200 o bien la inundación de cañerías secas preaction.

**Sistema de extinción por agua**
El edificio cuenta con un reservorio de agua exclusivamente para extinción de 40.000 litros que se encuentran a disposición de los sistemas de bombeo. Estos sistemas, uno para la cañería de Hidrantes (Mangueras) y otro para las cañerías de sprinklers cuentan cada uno con dos bombas independientes constituyendo dos sistemas de bombeo con capacidad de mantenimiento concurrente. Existen tres estaciones de separación agua / aire para los tramos de cañería seca preaction controladas por válvulas BERMAD. El sistema de Hidrantes se encuentra estratégicamente ubicado de modo de obtener un rápido acceso para la máxima eficacia en caso de un siniestro. Complementario al sistema húmedo cada sala y área cuentan con matafuegos de Halotron dispuestos claramente balizados.

**Sistema de extinción basada en gases limpios**

El área de Datacenter cuenta con un sistema primario de extinción por medio de agente limpio del tipo FM 200. Este agente no es peligroso para la salud de los eventuales ocupantes permitiendo la evacuación sin riesgos en caso de siniestro. El sistema de alerta temprana consiste en equipamiento del tipo ANALASER permitiendo una alerta previa a las instancias de detección óptica e iónica. La cañería de aspiración de muestras de aire se encuentra encima de las unidades de tratamiento de aire sobre el retorno. Esta detección temprana no acciona el proceso de extinción. El sistema de detectores ubicados en los cielorrasos y en el bajo piso técnico consiste de detectores ópticos y iónicos. Este sistema de detectores reporta al sistema de detección Fenwalnet 8000 y en caso de un determinado patrón de detecciones positivas desencadena el proceso de extinción. Este proceso inicia cuando la alarma recibe el patrón correcto de detección positiva, entonces acciona el sistema de presurización de escaleras, luego detiene las unidades de tratamiento de aire y simultáneamente confina la sala en cuestión por medio de tampers motorizados, 30 segundos después acciona los solenoides de liberación de las espoletas situadas en los tubos de nitrógeno que controlan el disparo de los tubos de FM 200. El FM 200 es desplegado a través de cañerías y boquillas situadas en el cielorraso y en el bajo piso técnico. Terminada la extinción se liberan los tampers y se activa el sistema de extracción de humo. Este proceso automático puede ser disparado en forma manual desde accionadores próximos a las salas, como abortado en accionadores situados en el mismo lugar.

En cuanto a la configuración de tubos de FM200 la configuración de todas las salas contiene una batería de tubos de FM 200 principal y otra idéntica de reserva constituyendo un sistema con capacidad de mantenimiento concurrente.

**Detección de fuga de agua**

Los bajos pisos cuentan con un sistema de drenaje por gravedad que conduce una supuesta descarga de agua hacia rejillas de desagüe situadas oportunamente en la losa. Debajo de todas las cañerías y serpentinas se encuentran desplegados los hilos del sistema de detección de fugas de agua Liebert modelo LDS 1000. Este sistema reporta una alarma al sistema de alarmas ambientales del edificio y en su display muestra la ubicación progresiva en metros respecto del detector de fugas dónde se ha detectado la presencia de agua.

**Reserva propia de agua contra incendio**

Tal como fue descripto en puntos anteriores, el edificio cuenta con un reservorio de 40.000 litros exclusivamente para el uso contra incendios. Son cisternas dedicadas a éste uso, no se usan para agua potable.

**Condiciones de la sala**

Los espacios asignados a Metrotel cuentan con las siguientes características. Losa y cielorraso de hormigón con doble pared externa de mampostería con ladrillos de molde y cámara de aire. Las puertas de acceso son del tipo RF-120. El piso elevado está constituido por un chasis de chapa estampada, relleno de cemento y revestimiento superior en HPL (High Pressure Layer) de baja emisión de humo.

## 7. SERVICIOS INCLUIDOS

La propuesta incluye 4 horas de manos remotas al mes no acumulables incluidas en el precio mensual. La propuesta de este servicio comprende:
+ Reboot y encendido/apagado de energía eléctrica
+ Chequeo de LEDs de estado
+ Verificación de circuitos eléctricos de los racks
  
El servicio será brindado de 9 a 18Hs en días habiles. Por tratarse de un servicio de operación remota, es fundamental que el cliente, en el momento de solicitar el servicio, indique correctamente el tipo de tarea y describa la forma en que debe realizarse la misma. Por fuera de este horario podrá ingresar a las instalaciones para realizar su propia revisión de los equipos.

## 8. SERVICIOS ADICIONALES

**Horas adicionales por servicio de manos remotas**

Para horas de manos remotas adicionales a las incluidas se contemplarán cargos adicionales.

**Pruebas de contingencia**

Posibilidad de contratar sala de DRP llamada Andrómeda equipada con boxes de trabajo con bocas de red LAN, telefonía, acceso a internet vía wifi, aire acondicionado, dispenser de agua y baños para ambos sexos. En su ingreso la sala cuenta con un control de acceso por tarjeta de proximidad conectado a la central de control de acceso del Datacenter. Este servicio tiene costos adicionales por cada día y por cada puesto de trabajo establecido.

## 9. PUESTA EN MARCHA
Todo rack utilizado para Colocation contará con las características dependientes de la opción del servicio elegido. En cuanto a la conectividad, se le entregará en todos los casos 1 (un) conector del tipo RJ-45 o en Fibra Optica según se requiera; en caso de necesitar conectar más de un equipo deberá contar con un dispositivo de interconexión similar a un Hub o a un Switch. Metrotel le proveerá toda la información necesaria para configurar sus equipos (dirección IP, mascara de red, default gateway, etc.).

Todo cliente tendrá a su disposición, un (1) monitor, un (1) teclado y un (1) mouse, ambos del tipo PS/2 o “minidin”. Estos elementos se entregan a modo de préstamo hasta tanto se termine la instalación. Se consideran fuera del servicio a las siguientes tareas:
+ Montado, rackeado o colocación de sus equipos en el rack.
+ Conexión del equipamiento a la red eléctrica.
+ Provisión de cables de tensión adecuados.
+ Configuración IP de los equipos que así lo requieran.
+ Configuración de sistemas operativos o software de equipos del cliente.
  
## 10.  ACCESO AL DATA CENTER

El Cliente debe completar el formulario de autorizaciones adjunto para el ingreso del personal técnico al DC, facilitando un listado que contenga nombre y apellido, Nro. de documento y Empresa. En caso de ser personal propio debe acompañar el pedido con Constancia de Inscripción en ART con la correspondiente inclusión de la clausula de no repetición a favor de Diveo Argentina S.A.. En caso de personal que no se encuentra en relación de dependencia se solicitarán los seguros de vida y riesgo de trabajo aplicables a las actividades autónomas. Dicho pedido debe ser efectuado con una antelación mínima de 48hs horas hábiles al ingreso. Las empresas deberán enviar mensualmente la nómina de técnicos autorizados para mantener los datos actualizados. Dicho formulario deberá ser enviado a **seguridad@skyonline.net** para su aprobación.

El acceso al Datacenter puede producirse por tres motivos:
+ **Instalación, puesta en marcha del servicio:** Esta tarea se realizará una vez por cada cliente.
Si bien no existe un límite en la duración del proceso de instalación, debe evitarse que este supere los dos (2) días para no generar inconvenientes en la operación del resto de los servicios. Sólo pueden realizarse en el horario de 09.00 a 17.00 horas de lunes a viernes, previo aviso y coordinación.
+ **Tareas programadas**

Se denomina tarea programada a toda aquella que requiera una intervención del personal de Metrotel. Se incluyen en esta denominación a todas las tareas que impliquen configuraciones, controles o verificaciones por parte de personal de Metrotel.

El horario de estas tareas coincide con el de la instalación y puesta en marcha del servicio. Al igual que la tarea anterior, requieren un aviso y una coordinación previa.

+ **Tareas no programadas**

Incluyen aquellos trabajos relacionados con el mantenimiento correctivo de los equipos. Algunos ejemplos de estos son: configuraciones de los equipos, upgrades de hardware o software, etc.

No existe un límite de horario para estas tareas, pudiendo realizar las mismas durante las 24 horas del día, los 7 días de la semana. Las mismas no requieren de la coordinación con personal de Metrotel. Se sugiere, sin embargo, avisar de las visitas que se realizarán a fin de que el personal de Metrotel pueda prestar un mejor servicio.

*Nota: en cualquiera de los casos mencionados anteriormente, está permitido el ingreso de materiales cumpliendo los requisitos del punto siguiente ”Ingreso/egreso de materiales al Datacenter”.*

*Se requiere en todos los casos, que el personal propio o subcontratado por el cliente que concurra al Datacenter esté debidamente autorizado mediante el listado de personas autorizadas que se detalla en la sección “Responsabilidades del cliente”, ubicada más adelante en este documento.*

**Ingreso / egreso de materiales al Datacenter**

Para todo ingreso de material al Datacenter, que sean de su propiedad, es necesario entregar un remito cuyo emisor debe ser el cliente. En éste deben figurar las características del equipamiento ingresado incluyendo: la cantidad, la descripción y el número de serie de cada equipo más una firma y aclaración del emisor.

No está permitida ninguna de las siguientes acciones:
+ Ingresar equipos sin los remitos correspondientes
+ Ingresar o retirar equipos fuera del horario fijado.
+ Entregar remitos en donde el emisor sea distinto del cliente.
  
## 11.  MANTENIMIENTO PROGRAMADO

El mantenimiento programado consistirá en toda, la cual será notificada previamente (con más de 48 horas de anticipación) al cliente y se realizará dentro del horario de mantenimiento establecido. Si el horario del corte previsto afecta la labor del cliente, éste puede solicitar la modificación del mismo. Metrotel se compromete a realizar los máximos esfuerzos para mover el corte al nuevo horario solicitado.

Este tipo de interrupciones se puede realizar para reemplazar o agregar elementos a la red a fin de ampliar y mejorar permanentemente el servicio.

## 12. INTERVENCIONES

Las intervenciones no tienen costo alguno ni existe un número máximo de intervenciones que se pueda requerir, estas deberán ser requeridos través del soporte de Metrotel de 9 a 18Hs , en días hábiles. Algunas de las intervenciones aplicables al producto Colocation son:
+ **Reseteo del servidor:** esta acción se realiza sin loguearse al equipo, desde un botón de reset o desde el botón de power del mismo. Bajo ninguna circunstancia personal de Metrotel accederá a sus sistemas sin su autorización escrita. Las consecuencias generadas por esta tarea quedarán siempre bajo la estricta responsabilidad del cliente.
+ **Apagado / encendido de equipos:** al igual que en el caso del reseteo, esta acción se realizará sin loguearse al sistema, y las consecuencias generadas por esta tarea quedarán siempre bajo la estricta responsabilidad del cliente.
+ **Chequeo del estado del sistema:** el cliente puede solicitar una revisión de las luces testigo indicadoras del estado del equipo, esto puede aplicarse también al control de link o enlace de los servidores.
+ **Insertar / retirar un CD o disquete del equipo:** el cliente puede solicitar el ingresar o retirar un CD, disquete o algún otro medio de almacenamiento en sus equipos. También existe la posibilidad de que Metrotel facilite ocasionalmente cierto tipo de software mientras no se infrinja la ley de copyright, como ser el caso de freeware o shareware.
+ **Colocar / retirar un teclado o mouse al equipo:** este préstamo sólo se realizará en forma temporal y el cliente deberá entregarlo al finalizar la tarea.
+ **Prueba de conectividad:** podrá requerir una prueba de la conectividad del acceso a Internet.
  
Esta se realizará probando la conectividad IP desde dos puntos distintos:
  + Un equipo ubicado dentro de la red de Metrotel.
  + Un equipo ubicado en Internet, preferentemente uno conectado mediante el enlace internacional.

Para el segundo caso, pueden utilizarse sitios de Internet o equipamiento que pertenezca a otras redes.

Durante las pruebas de conectividad se analizarán los siguientes resultados:
+ Nivel de utilización del vínculo de acceso global (uso del ancho de banda global).
+ Pruebas de conexión TCP/IP contra hosts ubicados fuera de la red de Metrotel (como se indicó en el párrafo anterior).
+ Medición de los tiempos de respuesta del punto anterior.
+ Si existieren, el nivel de pérdida de paquetes ICMP.
  
Debe tenerse en cuenta que las pruebas de conectividad no incluyen el funcionamiento de su equipamiento, como se indicó en la sección “Conectividad con Internet”.

## 13. TAREAS NO INCLUIDAS

No se consideran intervenciones, y por lo tanto no serán realizadas por personal de Metrotel, las siguientes acciones:
+ Logueo (inicio de sesión) en servidores del Colocation.
+ Configuración de cualquier tipo en equipos de su propiedad.
+ Armado o conexión de cables de red.
+ Provisión definitiva de mouses, monitores o teclados (sólo está permitido el préstamo).
+ Provisión de elementos de networking tales como Hubs, Switches, etc.
+ Cualquier otra tarea que no haya sido mencionada fehacientemente.

## 14.  PRÁCTICAS NO PERMITIDAS

Las siguientes acciones se consideran como prácticas no permitidas y no serán admitidas en ningún caso:
+ Utilizar “zapatillas”, alargues o adaptadores eléctricos.
+ Utilizar cables de conexión armados por el cliente en lugar de los originales que acompañan el equipo.
+ Superar el valor máximo de consumo permitido.
+ Colocar elementos que restrinjan la visión dentro del rack.
+ Alojar dentro del espacio asignado elementos volátiles, inflamables o sistemas de alimentación interrumpida (SAI/UPS), rectificadores que por cualquier cuestión representen peligro de cortocircuito o incendio. Dentro de esta categoría están incluidos todos los líquidos.
+ Utilizar equipamiento que presente potenciales problemas al sistema eléctrico del complejo.
+ Ingresar o retirar equipamiento sin la documentación requerida o sin control del personal de Metrotel.
+ Alojar o distribuir información que infrinja leyes o regulaciones Internacionales, Nacionales o Provinciales actuales o futuras. Esto incluye a las leyes de copyright y a las de propiedad intelectual.

## 15.  RESPONSABILIDADES DEL CLIENTE
+ Listado de personas autorizadas: todo cliente deberá encargarse de mantener un listado actualizado de personas autorizadas a requerir intervenciones (incluidas las visitas al Datacenter) para trabajar en los equipos de su propiedad.
+ Cumplimiento de normas de ingreso / egreso de materiales: todo cliente que desee ingresar o retirar equipos del Datacenter deberá cumplir con los procedimientos ideados para tal fin. Estos están orientados a llevar un control adecuado del listado de equipos.

## 16. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año. Para acceder al mismo, el cliente dispone de un número gratuito de contacto (0800-362-1040) mediante el cual podrá realizar la gestión de eventuales reclamos.

Desde la Mesa de Ayuda se realiza el diagnóstico para aislar la falla. Una vez identificada la misma, se procederá a realizar su inmediata resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance de la falla en particular, durante la existencia de la misma.