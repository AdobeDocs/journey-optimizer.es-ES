---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2afc9c4eb2a0433a22f1b369824086db2f5618ec
workflow-type: tm+mt
source-wordcount: '1776'
ht-degree: 44%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.


## Notas de versión preliminar de agosto de 2025 {#25-8-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en la fecha de la versión.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: miércoles, 19 de agosto de 2025


### Nuevas funciones {#Aug-25-8-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Pausar y reanudar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede poner en pausa y reanudar los recorridos. Esta funcionalidad proporciona a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando están en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda el recorrido.</p>
<p>Puede poner en pausa y reanudar solo un recorrido, o realizar pausas masivas y reanudar operaciones en un grupo de recorridos.</p>
<p>Además, puede aplicar filtros globales a los recorridos en pausa para excluir perfiles en función de sus atributos.</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vista de calendario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, la función incluye:</p>
<ul>
<li>Mejoras de diseño para la navegación en fechas,</li>
<li>La capacidad de ver borradores de campañas si ha establecido una fecha de inicio y de finalización,</li>
<li>Una nueva configuración para ocultar y mostrar los elementos de calendario que se ejecutan durante mucho tiempo.</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Uso de datos de Adobe Experience Platform para la personalización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveche los datos de [!DNL Adobe Experience Platform] en el editor de personalización para personalizar el contenido y los atributos de decisión. En particular, esto le permite ampliar la definición de sus atributos a datos adicionales en conjuntos de datos para actualizaciones masivas que cambian periódicamente sin tener que actualizar manualmente los atributos de uno en uno.</p>
<p>Con esta versión, se han introducido las siguientes mejoras:</p>
<ul>
<li>Compatibilidad con canales entrantes,</li>
<li>La función de ayuda "datasetLookup" ahora se puede utilizar dentro de la expresión y los fragmentos visuales para personalizar el contenido mediante datos de conjuntos de datos de Adobe Experience Platform,</li>
<li>Una opción del conjunto de datos ahora le permite habilitar conjuntos de datos para la personalización de la búsqueda, sin tener que realizar una llamada de API.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Optimización de ruta de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le ofrece las herramientas necesarias para optimizar sus recorridos mediante el uso de la IA y los marcos de experimentación, a la vez que garantiza una facilidad de uso y una diferenciación perfectas entre las funcionalidades de optimización y condición.</p>
<p>Utilice la optimización de rutas para segmentar, experimentar o utilizar IA para determinar la secuencia de comunicaciones, el tiempo entre ellas, las combinaciones de canales y cualquier cosa que pueda soñar en el lienzo del recorrido.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de acción en recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer admite una nueva actividad de acción genérica que permite configurar acciones únicas y grupos de acciones entrantes de varias acciones, lo que permite una configuración de acciones optimizada dentro del lienzo de recorrido. En particular, esta nueva función permite lo siguiente:</p>
<ul>
<li>Una configuración de acción nativa simplificada dentro del lienzo de recorrido.</li>
<li>Capacidad para crear nodos entrantes de varias acciones.</li>
<li>La capacidad de añadir optimización a cualquier acción de canal integrada.</li>
<li>La capacidad de añadir opciones de experimentación y multilingües a cualquier acción.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--img src="assets/do-not-localize/pdf-attachments.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Archivos adjuntos de PDF a correos electrónicos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede adjuntar un archivo PDF estático a un mensaje de correo electrónico enviado con Journey Optimizer.</p>
<ul>
<li>Puede enviar hasta 6 mensajes con un archivo adjunto de PDF por perfil y año.</li>
<li>El tamaño máximo de archivo permitido para cada archivo adjunto es 5 MB.</li>
<li>Para cualquier tamaño o volumen adicional, puede adquirir un complemento de paquete de archivos adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formularios personalizados de página de aterrizaje</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con [!DNL Journey Optimizer], ahora puede capturar atributos de perfil a través de sus páginas de aterrizaje.</p>
<p>Cree, diseñe y administre formularios personalizados adaptados a sus necesidades en función de un conjunto de datos específico. A continuación, puede aprovechar estos formularios en páginas de aterrizaje para agregar los atributos de perfil que elija al conjunto de datos definido para cada formulario.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimización en campañas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, Journey Optimizer le ofrece las herramientas necesarias para ofrecer contenido personalizado y optimizado al público de sus campañas, lo que le permite ejecutar experimentos de contenido, crear segmentación basada en reglas y utilizar combinaciones avanzadas de ambos para maximizar la eficacia de sus campañas.</p>
<p>Con Optimization, puede:</p>
<ul>
<li>Probar múltiples variaciones de contenido para identificar la mensajería más eficaz.</li>
<li>Ofrecer contenido personalizado basado en atributos de usuario y datos contextuales.</li>
<li>Combinar segmentación y experimentación para estrategias de campaña avanzadas.</li>
<li>Filtrar los usuarios que no coincidan con los criterios de variante.</li>
<li>Garantizar mecanismos de reserva para mantener la participación del usuario.</li>
</ul>
<P>Una vez que la campaña está activa, los perfiles se evalúan según los criterios definidos y, en función de los criterios coincidentes, se envían con la experiencia o el contenido adecuados de la campaña.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Fecha de lanzamiento: 8 de agosto de 2025</p>
<p>Para obtener más información, consulte la <a href="../campaigns/campaigns-message-optimization.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#Aug-25-8-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Administración**

   * **Alertas de supervisión de configuración de canal**: ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, en caso de que falte <!--a channel configuration failure happens or if -->un registro DNS.

* **Campañas**

   * **Control de tarifas en campañas salientes**: ahora puede habilitar el control de tarifas para campañas salientes (correo electrónico, SMS, notificaciones push), lo que le permite evitar sobrecargas en sistemas descendentes, como páginas de aterrizaje o plataformas de atención al cliente.

   * **Programación de campañas de acción** - Los programadores diarios, semanales y mensuales de la campaña se han actualizado para proporcionar un control más detallado sobre las programaciones recurrentes:

      * **Periodicidad semanal**: ahora puede elegir repetir la campaña cada semana o cada dos semanas y seleccionar los días de la semana en que debería ejecutarse.

      * **Periodicidad mensual**: ahora puede elegir repetir la campaña todos los meses o cada dos meses y seleccionar el día del mes en que debe ejecutarse.

      * **Programaciones diarias, semanales o mensuales**: Puede especificar si la programación recurrente debe detenerse en una fecha específica o después de un determinado número de incidencias.

   * **Campañas de acción transaccional programadas**: Ya están disponibles las campañas de acción transaccional programadas para enviar comunicaciones transaccionales por lotes y basadas en audiencias por correo electrónico, SMS y canales push.

* **Canal - Push**

   * **Fecha de caducidad de la notificación push**: ahora puede especificar una fecha de caducidad para cada notificación push, lo que evita que los mensajes con distinción de tiempo (como la venta del Black Friday) se envíen después de una fecha determinada y, por lo tanto, evita ofrecer una mala experiencia a sus clientes.

* **Canal - SMS**

   * **Exclusión parcial**: cuando está habilitada, la opción **Exclusión parcial** detecta mensajes entrantes que se parecen mucho a las palabras clave de exclusión definidas (por ejemplo, &quot;CANCIL&quot;) y envía automáticamente una respuesta de confirmación para comprobar la intención de cancelación de suscripción del usuario. Si el usuario lo confirma mediante el mensaje definido, se cancela su suscripción.

     Tenga en cuenta que **exclusión aproximada** solo está disponible con Sinch e Infobip.

   * **Verificar conexión de SMS**: ahora puede probar y comprobar fácilmente sus credenciales de API de SMS en Adobe Journey Optimizer enviando un mensaje de ejemplo a un dispositivo designado.

* **Configuración**

   * **Compatibilidad con dominios dinámicos**: Journey Optimizer ahora admite la personalización en las direcciones URL de seguimiento para los dominios predefinidos enumerados en el nivel de configuración de canal.

   * **Compatibilidad con atributos personalizados con la URL para cancelar la suscripción con un clic**: con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer un extremo personalizado externo definiendo su propio vínculo para cancelar la suscripción con un clic en la configuración del correo electrónico. Cuando los destinatarios hacen clic en el vínculo unsubscribe, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

     Para personalizar aún más el vínculo de cancelación de suscripción de un clic, ahora puede definir atributos personalizados que también se adjuntarán al evento de consentimiento.

* **Toma de decisiones**

   * **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar fragmentos a elementos de decisión que se pueden aprovechar en campañas de experiencia basadas en código mediante políticas de decisión.

* **Recorridos**

   * **Operaciones masivas de Recorrido**: en la lista de recorridos, puede seleccionar varios elementos. Una vez seleccionados, puede pausar o reanudar hasta 10 recorridos a la vez.

   * **Compatibilidad con redireccionamiento (302) en acciones personalizadas**: ahora las acciones personalizadas pueden administrar redireccionamientos HTTP 302 por solicitud. Esto permite a los recorridos integrarse con API que redirigen las solicitudes a direcciones URL localizadas o específicas de la región. Las redirecciones se siguen automáticamente, lo que garantiza que el contenido correcto se envíe sin configuración adicional.

* **Conjuntos de datos**

   * **Repositorio de objetos de Experience Decisioning - Elementos de ofertas personalizados** - El conjunto de datos de exportación integrado ahora captura todos los atributos de ofertas y el estado del ciclo vital, lo que permite una personalización y un sistema de informes completos.

## Orquestación de campañas 

**Fecha de disponibilidad**: 4 de agosto de 2025

Journey Optimizer ahora incluye **orquestación de campañas**, una nueva funcionalidad diseñada específicamente para campañas por lotes iniciadas por la marca. Esta versión presenta un lienzo de orquestación de campaña y un modelado de datos mejorado, que funcionan juntos para permitir que los especialistas en marketing planifiquen, dirijan y entreguen campañas personalizadas en canales múltiples.

>[!IMPORTANT]
>
>Para acceder a Campaign Orchestration, la licencia debe incluir **Journey Optimizer - Campañas y Recorridos** o el paquete **Journey Optimizer - Campañas**. Póngase en contacto con su representante de Adobe para confirmar su licencia y actualizarla si es necesario.

![GIF de orquestación de campañas](assets/do-not-localize/release.gif)

Incluye [esquemas y conjuntos de datos relacionales](#oc-relational) y [lienzo de campañas](#oc-canvas). Juntas, estas dos innovaciones suponen un nuevo estándar a la hora de orquestar campañas por lotes en Journey Optimizer. A continuación se enumeran las funcionalidades clave.

### Funcionalidades clave {#oc-capabilities}

* **Flujos de trabajo de varios pasos**

  Dirija sofisticadas campañas por lotes multicanal con el nuevo lienzo de orquestación de campañas diseñado específicamente para este fin.

* **Públicos bajo demanda**

  Segmente públicos bajo demanda para su activación inmediata.

* **Segmentación de varias entidades**

  Cree públicos en un contexto empresarial (dimensiones que no sean personas), como productos, tiendas, renovaciones, reservas y mucho más.

* **Visibilidad previa al envío**

  Revise, perfeccione y optimice públicos y campañas antes del lanzamiento y mientras se ejecutan las campañas

### Lienzo de campaña {#oc-canvas}

Una interfaz de orquestación visual completamente nueva diseñada específicamente para campañas por lotes. Este lienzo permite lo siguiente:

* Planificación visual de flujos de campaña de varios pasos y canales

* Compatibilidad con públicos bajo demanda creadas a partir de consultas relacionales

* División de públicos avanzada, esperas y lógica condicional

* Recuentos precisos previos al envío después de aplicar reglas y filtros empresariales

### Esquemas relacionales y conjuntos de datos {#oc-relational}

Adobe Journey Optimizer ahora admite entidades relacionales (por ejemplo, productos, tiendas, reservas, contratos) vinculadas a perfiles basados en personas. Esto permite la segmentación y personalización en estructuras de datos multidimensionales, lo que permite casos de uso como:

* Un mensaje por reserva, suscripción o contrato

* Segmentación basada en atributos de entidad relacionados (por ejemplo, categoría de producto o ubicación de tienda)

* Mejor direccionamiento (por ejemplo, enviar a todos los contactos conocidos vinculados a una entidad)

### Por qué importa

Esta versión proporciona a los especialistas en marketing un control total sobre el marketing por lotes iniciado por la marca y basado en públicos, combinando un modelado de datos flexible con una experiencia de orquestación diseñada específicamente para este fin. Está diseñada específicamente para la orquestación de campañas por lotes desde recorridos en tiempo real, a la vez que ofrece personalización y escalabilidad avanzadas.

### Más información

Obtenga más información en la [Documentación de orquestación de campañas](../orchestrated/gs-orchestrated-campaigns.md).


