# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - CORREO ELECTRÓNICO

## 1. DESCRIPCIÓN GENERAL

El servicio de CORREO ELECTRÓNICO, en cualquiera de las variantes descriptas a continuación, ha sido diseñado para permitirle la comunicación vía Email utilizando una plataforma de servicio. Al contratar el servicio de CORREO ELECTRÓNICO que ofrece Metrotel usted accederá importantes beneficios, entre ellos:

+ Reemplazo de importantes inversiones en equipamiento y licencias de software por un accesible costo operativo mensual.
+ Reducción de riesgos operativos, asociados al manejo de la infraestructura.
+ Conectividad a Internet Nacional e Internacional multi-proveedor, permitiendo asegurar un alto nivel de disponibilidad de servicio.

## 2. VENTAJAS DEL PRODUCTO

+ Web mail para acceso Web desde cualquier dispositivo conectado a Internet
+ Políticas de control de SPAM
+ Cuentan con 2(dos) MX dedicados y 1 (uno) SMTP con direcciones exclusivas para canalizar el tráfico de toda la plataforma
+ Las cuentas e-mail soportan POP3/IMAP con tráfico seguro cifrado y todas pueden acceder al web mail vía webmail.metrotel.ar
+ La capacidad máxima de almacenamiento por cuenta es de 5GB, aunque se pueden reasignar espacio de cuentas no utilizadas hasta 20Gb por cuenta.

## 3. ESPECIFICACIÓN TÉCNICA

El cliente tendrá un usuario SuperAdmin cuentan con permisos para:
+ Crear usuarios Admins
+ Agregar direcciones IP en lista Blanca
+ Ampliar o reducir el tamaño general de adjuntos asi como las extensiones permitidas en los adjuntos
+ Puede solicitar recibir diariamente el resumen de e-mail que hayan quedado en cuarentena
+ Puede acceder a ver el tráfico de su Mailaudit y su cuarentena
+ Puede administrar su propio White/Blacklist a ver el tráfico de su Mailaudit y su cuarentena
+ El tráfico de e-mail entrante/ Saliente, cuarentena, análisis de Headers, descarga de emails cuarentena, lo pueden ver desde el Mailaudit con las diferentes vistas, también pueden operar la liberación de mails en caso de que sea necesario y tienen accesos rápidos para agregar o poner mails de listas blancas/negras
+ Por default tienen habilitado un límite de 1500 e-mail salientes diarios por remitente. El sistema además de descartar el tráfico por sobre este el límite establecido, aplicara filtros automáticos con lógicas automáticas para aceptar nuevos envíos del usuario. Todo esto en base al volumen de envío, periodicidad, etc. o para proteger a la plataforma de envíos no autorizados, ataques, etc.

## 4. PERFILES DE CONTROL DE SPAM

Cada usuario y también cada dominio, puede adoptar uno de cuatro perfiles de control de Spam, que reflejan su nivel de tolerancia. Si un usuario en particular no tiene perfil definido, toma el del dominio. Si un dominio no tiene perfil definido, toma el default de la instalación AVAS, que se configura en la etapa de Delivery del Producto.
+ Quiero todo el Spam en bandeja de Entrada.
+ Bajo control de Spam
+ Normal control de Spam
+ Alto control de Spam
+ 
A estos perfiles se agregan declaraciones de Whitelisting y Blacklisting (cuentas de mail individuales o dominios completos), que permiten contornear el proceso de clasificación de una manera personalizada.

La clasificación de Spam se basa en reglas dinámicas provenientes del framework Spamassassin, con una customización particular del sistema AVAS específicamente en lo que refiere a consultas a las RBLs (Real-Time Blacklists).

La clasificación de Virus y Banned (formatos de archivo prohibidos como, por ejemplo .exe) está más allá de la clasificación de Spam, y en caso de detectarse los mails infectados o prohibidos van a parar a la Cuarentena.

## 5. NIVELES DE CLASIFICACIÓN DE SPAM

La clasificación de Spam propiamente dicha tiene cuatro niveles posibles, de acuerdo al perfil elegido.

**Nivel 1: Networking – RBLs**

Este es el nivel de networking y consulta a RBLs específicas de transporte SMTP, que además cuenta con un módulo de firewall para prevenir ataques de diccionario y ataque de spambots cuando se detectan direcciones IP originantes de dichos ataques. Este nivel 1 es independiente del perfil de Spam, e inclusive de Black/Whitelisting, ya que en esta etapa es previa a la detección de remitente y destinatario.

**Nivel 2: Puntuación**

Este es el nivel de mails “limpios”, es decir mails cuya puntuación de análisis de Spam está en los umbrales tolerados por el perfil del usuario.

**Nivel 3: Spammy**

Este es el nivel de mails Spammy, también siempre según los umbrales del perfil del usuario, y que van a parar la carpeta “Spam” del maildrop. Si el maildrop no estuviera configurado para contener esta carpeta, normalmente el mail va a parar al Inbox pero con el agregado de la palabra “SPAM” al principio del Asunto del mail.

**Nivel 4: Cuarentena**

Este es el nivel de mails en Cuarentena, es decir mails que quedan en la base de datos central del AVAS, y que pueden ser “rescatados” tanto por el usuario final, el administrador de dominio o el superadmin. Aquí caen los mails blacklisteados, los mails con puntuación superior al umbral de tolerancia del perfil, y mails con Virus o contenidos prohibidos (Banned).

Los niveles 2 (Puntuación), 3 (Spammy), y 4 (Cuarentena) se graban en Mailaudit.

La información grabada es en ciertos encabezados de los mails junto con información de clasificación de Spam, pero no el contenido del email.

Dichos registros pueden ser consultados via Mailaudit.

## 6. PALABRAS Y FRASES BLOQUEADAS

Desde la pestaña Palabras Bloqueadas de AVAS Users se puede hacer alta o baja de palabras a bloquear tanto en el Asunto como en el Cuerpo de un email entrante. Se recomienda utilizar frases completas en vez de sólo palabras por una cuestión de contexto.

![Palabras y frases bloqueadas](../../../imagenes/email/palabras%20y%20frases%20bloqueadas.png)

En caso de que llegue un correo que contenga al menos una de estas frases en el Asunto o en el Cuerpo del email (según lo especificado en el alta de la palabra) el mismo será enviado casi automáticamente a la cuarentena, ya que se le agregará un puntaje lo suficientemente alto.

Se recomienda cautela al momento de agregar una frase a esta lista, ya que al bloquear frases que tal vez sean comunes o que puedan tener distintos significados dependiendo del contexto se corre el riesgo de que se presenten falsos positivos.

También hay que tener en cuenta que estas palabras bloqueadas afectan al AVAS en su totalidad, y van a aplicar a todos los dominios protegidos de la Compañía en la que se configure.

Al tratarse de una configuración sensible esta operación también estará sujeta a la doble confirmación por email, y aquellos usuarios con permisos de Administración de Avas la van a localizar en el Auditlog.

Otro punto a tener en cuenta es que al existir idiomas con diferentes sets de caracteres tales como griego o cirílico, se debe observar un posible engaño visual que hace que el bloqueo de frases sea inocuo.

Este tipo de frases son extremadamente difíciles de bloquear debido a la codificación. AVAS detecta p.ej. caracteres extraños fuera de un charset declarado en un mail asignándole puntaje como mail sospechoso.

## 7. ALCANCE

Los servidores de correo electrónico AVASCLOUD establecen como standard y en línea con las buenas prácticas sugeridas por los grandes ESP un volumen de 1500 e-mails diarios exclusivamente para tráfico de correo corporativo, para prevenir sobre cargas, problemas de blacklist, grey listing o bloqueos temporales.

En caso de existir una notificación de alguna blacklist informando la existencia de correo saliente peligroso o notificación de bloqueo de alguna dirección IP que Metrotel dispone para el servicio, se solicitara que el responsable de servidor de e-mail del usuario final, dueño o responsable del dominio en cuestión se contacte con la blacklist para solicitar el desbloqueo. En caso de que prefiera que personal de Metrotel se ocupe de la gestión el cliente deberá enviar una nota formal con las explicaciones de caso, asegurando ya resolvió la problemática para que personal de Metrotel pueda respaldar la solicitud. Si luego de 72 horas de notificado el inconveniente el cliente no opto por ninguna de las alternativas y/o no tomo ninguna medida Metrotel podrá suspender el servicio para el dominio involucrado.

Si algún cliente envía SPAM o su dominio o IP asociada su dominio es parte de una blacklist, Metrotel recomendara la suspensión de servicio para dicha cuenta para evitar comprometer el correcto funcionamiento del resto de la plataforma en general ya es que una plataforma compartida.

Los servidores de protección de correo electrónico saliente provistos por Metrotel no aceptarán el envío de “correos masivos”, en caso de existir tráfico masivo Metrotel estará habilitado a suspender el servicio.

Los servidores rechazarán conexiones de remitentes que no pueden aceptar al menos el 90% de los mensajes de rebote de vuelta (mensajes de fallo/error mailer -daemon) destinados a sus sistemas.

## 8. SOPORTE TÉCNICO

Ubicado físicamente en la ciudad de Buenos Aires, el servicio de soporte técnico de Metrotel funciona las 24 horas del día, los 365 días del año para todo lo referido a plataforma, y en atención a clientes dependerá del tipo de segmento de el/los servicio/s contratado/s y de la categoría del cliente, por favor referirse al Contrato de dichos Servicios. Para acceder al mismo, el cliente dispone de un número gratuito de contacto (0800-362-1040) mediante el cual podrá realizar la gestión de eventuales reclamos, con las consideraciones de atención previamente mencionadas.

Desde la Mesa de Ayuda se ingresará el reclamo correspondiente y una vez identificada la falla se procederá con las tareas de resolución. El cliente será informado, ya sea por teléfono y/o mail, del estado y avance del reclamo ingresado, durante la existencia del mismo.

## 9. REQUISITOS POR PARTE DEL CLIENTE

Queda bajo su responsabilidad la realización de los trámites correspondientes al dominio que se desee utilizar para el servicio CORREO ELECTRONICO (Registración, renovación y/o Delegación de Dominio). Metrotel no se hará responsable por los tiempos de delegación, ni tampoco con problemas en el mismo.

## 10. RESPONSABILIDAD POR CONTENIDOS

El cliente es responsable por los contenidos enviados en sus correos electrónicos, reservándose METROTEL el derecho de provocar la indisponibilidad del servicio en caso de que considere se esté efectuando un uso indebido del servicio.

El cliente, a su vez, es responsable por efectuar el Backup de sus mails, estando resguardado así ante el caso fortuito que los servidores de Mail y sus respectivos servicios de Backup sufrieran daños irrecuperables. METROTEL no se hace responsable ante el caso fortuito de pérdida de datos en el servidor y su respectivo Backup.

El cliente es responsable de conservar su respectiva contraseña, Metrotel, no guarda contraseñas y no se hace responsable por la pedida de la misma.

El cliente no debe de borrar la cuenta admin@dominio.com ya que si lo hiciese quedaría sin acceso y Metrotel no se hace responsable por las pérdidas que esto ocasione.

