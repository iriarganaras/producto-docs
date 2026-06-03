# ESPECIFICACIONES TÉCNICAS Y ALCANCE DE SERVICIO - PLATAFORMA DE CONCIENTIZACIÓN EN CIBERSEGURIDAD - ZULA

## 1. DESCRIPCIÓN GENERAL
La Plataforma de concientización en Ciberseguridad ZULA es una solución SaaS (Software como Servicio) integral diseñada para fortalecer la postura de ciberseguridad de las organizaciones. Su objetivo principal es transformar a los usuarios finales en la primera línea de defensa mediante un proceso continuo de capacitación, evaluación y concientización.
ZULA gestiona campañas de formación personalizadas, simulacros de phishing realistas y reportes analíticos detallados. Al integrarse con las plataformas de correo electrónico corporativo, ZULA asegura un alcance máximo y una efectividad superior en todas las iniciativas de concientización, elevando así el nivel de madurez en ciberseguridad de la organización.


### Componentes principales del servicio

<u>Portal Web Corporativo:</u> Interfaz personalizable para que cada empresa acceda a sus campañas, reportes, capacitaciones y evaluaciones.

<u>Campañas de Concientización:</u> Diseño y despliegue mensual de contenidos interactivos con videos, juegos, artículos y trivias.

<u>Simulacros de Phishing,Ransomware y QRishing:</u> Ejercicios programados para medir la exposición del personal frente a ataques de ingeniería social.

<u>Dashboard de Analítica:</u> Panel centralizado de métricas clave como tasas de clic, reportes de usuarios comprometidos y cumplimiento.

<u>Sistema de Evaluaciones:</u> Exámenes automatizados para reforzar el aprendizaje y registrar el nivel de asimilación.

## 2. ALCANCE Y ESPECIFICACIÓN TÉCNICA

### Requisitos del cliente

+ Proveer listado de usuarios con nombre, mail y área asignada.
+ Contar con un dominio de correo corporativo habilitado.
+ Permitir la inclusión de excepciones en filtros antispam internos.
+ Aceptar políticas de uso y condiciones del servicio ZULA.

### Implementación estándar incluye

+ Activación del portal personalizado.
+ Integración con correo electrónico institucional.
+ Subida de base de usuarios.
+ Diseño inicial de campaña.
+ Capacitación operativa básica para responsables.

### Periodicidad del servicio

+ Una campaña mensual de concientización.
+ Un simulacro de phishing mensual.
+ Reporte ejecutivo mensual.
+ Evaluación semestral de usuarios.

## 3. ALCANCE DEL SERVICIO 


<style>                         
  th {
    text-align: center;           <!-- Centra el contenido de la tabla -->
  }

table, th, td {                  <!-- Coloca bordes a la tabla -->
  border: 1px solid black;
  border-collapse: collapse;
}
</style>

<table>
  <tr>
    <th>Producto</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <th>Simulaciones</th> 
    <td>
    <ul>
        <li> Permite el envío ilimitado de campañas de simulación deRansomware, QR Phishing y Phishing para medir la madurez de los usuarios.</li>
        <li> Incluye la posibilidad de cargar contenido propio y generar plantillas a medida basadas en marcas populares, herramientas internas o servicios de uso cotidiano.</li>
        </ul>
        </td>
  </tr> 

  <tr>
    <th>Misiones</th>
    <td>
        <ul>
            <li>Esta sección incluye más de 100 videos tutoriales, juegos y cuestionarios, agrupados bajo el concepto de “Misiones”, sobre variados temas relacionados a la ciberseguridad para transmitir conocimientos de manera lúdica y poder evaluar de manera efectiva lo aprendido por los colaboradores.</li>
            <li>Los videos tutoriales tienen una duración de entre 1 y 5 minutos para captar la atención de los colaboradores.</li>
            <li>El contenido puede ser segregado para distintas categorías de colaboradores, a ser definidas por el cliente.</li>
            <li>Se elabora una tabla de posiciones individual y/o grupal con el puntaje adquirido por los colaboradores en función a la aprobación o no de las actividades realizadas.</li>
        </ul>
    </td>
  </tr>

  <tr>
    <th>Newsletters</th>
    <td>
        <ul>
        <li>Permite la creación y envío ilimitado de correos informativos.</li>
        <li>ZULA pone a disposición plantillas para comunicar contenido relacionado a buenas prácticas de ciberseguridad, que el cliente puede adaptar a su manual de marca.</li>
        </ul>
    </td>
  </tr>

   <tr>
   <th>Panel de Administración</th>
   <td>
    <ul>
El Panel de Administración permitirá la autogestión de la plataforma por parte del cliente. Desde el mismo se podrá:
    <li>Gestionar a los usuarios (altas, bajas y modificaciones), integración con AD.</li>
    <li>Generar las campañas y acceder a las métricas de simulaciónde phishing</li>
    <li>Acceder a las métricas de los videos tutoriales, juegos y cuestionarios</li>
    <li>Seleccionar el contenido de videos, juegos y cuestionarios a serdisponibilizadoa los colaboradores</li>
    <li>Generar las plantillas y acceder a las métricas de correos informativos</li>
    <li>Autogestionar la marca blanca de la plataforma, editando colores y logo.</li>
    <li>Parametrizar configuraciones generales en función a las preferencias particulares del cliente.</li>
    <li>Todos los reportes son descargables en formato PDF, JSON, XML, CSV, TXT, SQL, EXCEL</li>
        </ul>
    </td>
</tr>

   <tr>
     <th>Soporte</th>
     <td>
        <ul>
        <li>La plataforma incluye unaticketeradisponible 24x7 para poder generar pedidos de Soporte a personal especializado, de manera ilimitada.</li>
        <li>También tendrán a disposición un correo electrónico del ejecutivo asignado a su cuenta.</li>
        </ul>
    </td>
   </tr>

   <tr>
    <th>Arquitectura y Seguridad</th>
    <td>
        <ul>
        <li>ZULA se encuentra desplegada sobre la infraestructura de Google CloudPlatform(GCP) en Council Bluffs, Iowa, Estados Unidos.</li>
        <li>La plataforma se implementará en servidores en la nube.</li>
        <li>La utilización de Google Cloud provee a ZULA un alto nivel de seguridad por defecto gracias al sometimiento a controles independientes de seguridad, privacidad y cumplimiento con importantes estándares de seguridad, a saber: ISO/IEC 27001, 27017, 27018 y 27701, SOC1, 2 y 3, PCI DSS,FedRAMP, HIPAA, RGPD, CCPA.</li>
    </ul>
    </td>
   </tr>
</table>

## 4. SLA (ACUERDO DE NIVEL DE SERVICIO)
<table>
  <tr>
    <th>Métrica</th>
    <th>Valor estándar</th>
  </tr>

  <tr>
    <td>Disponibilidad del servicio</td>
    <td>99.7%</td>
  </tr>

   <tr>
    <td>Tiempo de activación inicial</td>
    <td>Hasta 5 días hábiles</td>
  </tr>

   <tr>
    <td>Tiempo de respuesta soporte L1</td>
    <td>Hasta 8 h hábiles</td>
  </tr>

  <tr>
    <td>Actualización de contenido</td>
    <td>Mensual automática</td>
  </tr>
</table>

## 5. SERVICIO GESTIONADO

### Adicionales

+ Campañas de Concientización Personalizadas
+ Workshops Presenciales de Cultura Segura (CABA y GBA)
+ Webinars Interactivos de Concientización
+ Bootcamp Presencial para Usuarios de Riesgo (CABA y GBA)
+ Diseño de Onboarding Seguro
+ Bootcamp Virtual para Usuarios de Riesgo (CABA y GBA)
+ Despliegue del Onboarding de Ciberseguridad

## 6. LIMITACIONES DEL SERVICIO

+ ZULA no reemplaza controles técnicos como NGFW o EDR.
+ El cliente debe mantener actualizados los datos de usuarios.
+ El éxito depende de la comunicación interna efectiva.
+ No incluye integración con SOC/SIEM salvo contratación adicional.

## 7. ACEPTACIÓN DEL SERVICIO

Las actividades de pruebas de aceptación deberán ser realizadas por el Cliente en un plazo no mayor a cuarenta y ocho (48) horas hábiles contadas a partir de la fecha de finalización y comunicación de la puesta en marcha por parte de Metrotel vía mail.Las pruebas deberán basarse en el uso normal de la aplicaciónde acuerdo alas prácticas habituales de la actividad principal del Cliente yde acuerdo alrelevamiento de uso y necesidades durante la etapa de preventa. Vencido el mencionado plazo, y de no mediar objeciones por parte del cliente, Metrotel procederá a la aceptación tácita del servicio para su posterior facturación.

## 8. ACERCA DE METROTEL

Metrotel es una empresa de telecomunicaciones que desde hace más de 25 años brinda servicios a empresas líderes del mercado argentino. Opera comercialmente, en el área de la Ciudad Autónoma de Buenos Aires, Gran Buenos Aires, Rosario, Córdoba, Mendoza y Neuquén. Cuenta con una red de fibra óptica propia (Red de Alta Velocidad) de 3.600 km, la cual permite ofrecer servicios de alta disponibilidad y con velocidades de transporte de datos.

El objetivo de Metrotel es brindar soluciones innovadoras, buscando la satisfacción de todos los clientes, el crecimiento continuo y la rentabilidad con innovación tecnológica.