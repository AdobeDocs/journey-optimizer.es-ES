---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c4aa1a6ecabb7b742bce084bb96865f965531d77
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 88%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Actualizaciones del 25 de septiembre {#sep-updates}

### Nuevas funciones {#Sep-25-features}

<table>
<thead>
<tr>
<th><strong>Modo oscuro en el Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Diseñador de correo electrónico de Journey Optimizer ahora permite cambiar a la vista en modo oscuro, donde además puede definir configuraciones personalizadas específicas que se mostrarán solo para los destinatarios que lean sus correos electrónicos en modo oscuro.</p>
<p>Tenga en cuenta lo siguiente:</p>
<ul>
<li>El renderizado final del modo oscuro puede variar y depende del cliente de correo electrónico del destinatario.</li>
<li>No todos los clientes de correo electrónico admiten el modo oscuro personalizado. Además, algunos clientes de correo electrónico solo aplican su propio modo oscuro predeterminado a todos los correos electrónicos recibidos. En ambos casos, no se puede procesar la configuración personalizada que definió en el Diseñador de correo electrónico.</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/dark-mode.md">documentación detallada</a>.</p>
 <p>Fecha de disponibilidad: 16 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimización de la ruta del recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilice el nuevo nodo Optimizar para dirigirse a públicos específicos o ejecutar pruebas A/B para determinar la mejor ruta para satisfacer los KPI empresariales.</p>
<p>Esta herramienta le permite probar y variar, así como personalizar las comunicaciones, la secuencia y el tiempo para llegar mejor a sus clientes.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/optimize.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 4 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Método de delegación personalizada para subdominios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Además de la delegación completa y del método CNAME, ahora hay disponible un nuevo método de configuración de subdominios: el método de delegación personalizada, que le permite controlar y mantener por completo todos los aspectos de DNS necesarios para enviar, procesar y rastrear mensajes.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p>Para obtener más información, consulte la <a href="../configuration/delegate-custom-subdomain.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 4 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso de datos de Adobe Experience Platform para la personalización y la toma de decisiones: disponibilidad limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta capacidad, que se publicó anteriormente en la versión beta pública, ya está disponible para todos los entornos con disponibilidad limitada. Con esta versión, se han introducido las siguientes mejoras:</p>
<ul><li>Compatibilidad con la personalización de la búsqueda de conjuntos de datos en canales entrantes.</li>
<li>Ahora, la función de ayuda "datasetLookup" se puede utilizar dentro de los fragmentos de expresiones. Por ahora, esta capacidad está disponible para un conjunto limitado de clientes. Para obtener acceso, póngase en contacto con su representante de Adobe.</li>
<li>Una opción de la interfaz de administración de conjuntos de datos ahora le permite habilitar conjuntos de datos basados en registros para la personalización de búsquedas, sin tener que realizar una llamada de API.</li>
<li>Monitorización mejorada para rastrear el estado de ingesta de datos y saber cuándo los conjuntos de datos están listos para la búsqueda.</li>
<li>Se han actualizado las directrices y protecciones de uso para garantizar un rendimiento y una fiabilidad óptimos.</li>
<li>Los conjuntos de datos de Adobe Experience Platform ahora se pueden aprovechar en las reglas de límite de Decisioning.</li></ul></p>
<p>Para obtener más información, consulte la <a href="../data/lookup-aep-data.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 1 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#Sep-25-improv}

* **Compatibilidad con dominios dinámicos**: Journey Optimizer ahora admite la personalización completa/básica de direcciones URL para dominios predefinidos aceptados por Adobe. [Más información](../personalization/personalization-build-expressions.md#where) <!--Availability date: September 12-->

  >[!NOTE]
  >
  >Esta capacidad está disponible en disponibilidad limitada para un conjunto de clientes.

* **Expresión para reglas de límite de Decisioning**: ahora puede crear sus propias expresiones para definir el umbral de una regla de límite para un elemento de decisión. [Más información](../experience-decisioning/items.md#capping)

  >[!NOTE]
  >
  >Actualmente, esta capacidad está disponible como disponibilidad limitada para todos los usuarios.

* **Alertas de monitorización de configuración de canal**: ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, en caso de que se produzca un error de configuración de canal de correo electrónico al usar el tipo de delegación de subdominio personalizado. [Más información](../reports/alerts.md#alert-dns-record-missing)

## Notas de la versión de agosto de 2025 {#25-8-rn}

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
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-pause.md">documentación detallada</a>.</p>
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
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-ui.md#calendar">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

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
<th><strong>Actividad de acción en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer admite una nueva actividad de acción genérica que permite configurar acciones únicas y grupos de acciones entrantes de acciones múltiples, lo que permite una configuración de acciones optimizada dentro del lienzo de recorrido. En particular, esta nueva función permite lo siguiente:</p>
<ul>
<li>Una configuración de acción nativa simplificada dentro del lienzo de recorrido.</li>
<li>La capacidad para crear grupos de acciones entrantes de varias acciones.</li>
<li>Capacidad de añadir optimización a cualquier acción de canal integrada.</li>
<li>Capacidad de añadir opciones de experimentación y multilingües a cualquier acción.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-action.md">documentación detallada</a>.</p>
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
<li>El tamaño máximo para cada archivo adjunto es 5 MB.</li>
<li>Para cualquier tamaño o volumen adicional, puede adquirir un complemento de paquete de archivos adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/pdf-attachments.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Optimización en campañas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, Journey Optimizer le ofrece las herramientas necesarias para ofrecer contenido personalizado y optimizado a su público, lo que le permite ejecutar experimentos de contenido, crear segmentación basada en reglas y utilizar combinaciones avanzadas de ambos para maximizar la eficacia de sus campañas y recorridos.</p>
<p>Con Optimization, puede:</p>
<ul>
<li>Probar múltiples variaciones de contenido para identificar la mensajería más eficaz.</li>
<li>Ofrecer contenido personalizado basado en atributos de usuario y datos contextuales.</li>
<li>Combine segmentación y experimentación para estrategias de campaña avanzadas.</li>
<li>Filtrar los usuarios que no coincidan con los criterios de variante.</li>
<li>Garantizar mecanismos de reserva para mantener la participación del usuario.</li>
</ul>
<P>Una vez que el recorrido o la campaña están activos, los perfiles se evalúan según los criterios definidos y, en función de los criterios coincidentes, se envían con la experiencia o el contenido adecuados.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Esta capacidad, que se publicó anteriormente el 8 de agosto solo en campañas, ahora también está disponible en recorridos a partir del 22 de agosto.</p>
<p>Para obtener más información, consulte la <a href="../campaigns/campaigns-message-optimization.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#Aug-25-8-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Administración**

   * **Alertas de monitorización de configuración de canal**: ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, en caso de que <!--a channel configuration failure happens or if -->falte un registro DNS. [Más información](../reports/alerts.md#alert-dns-record-missing)

* **Asistente de IA**

   * **Generación de contenido en varios idiomas**. Ahora el contenido se puede generar en francés, español, alemán, italiano, japonés, sueco, holandés y noruego. [Más información](../content-management/generative-uc.md#languages)

     Fecha de disponibilidad: 25 de agosto


* **Campañas**

   * **Control de velocidad en las campañas de salida**: ahora puede habilitar el control de la velocidad de las campañas de salida (correo electrónico, SMS, notificaciones push), lo que le permite evitar sobrecargas en sistemas descendentes, como páginas de aterrizaje o plataformas de servicio de atención al cliente. [Más información](../campaigns/campaign-schedule.md#rate-control)

   * **Programación de campañas de acción**. Los programadores diarios, semanales y mensuales de la campaña se han actualizado para proporcionar un control más detallado sobre las programaciones recurrentes:

      * **Periodicidad semanal**: ahora puede elegir repetir la campaña cada semana o cada dos semanas y seleccionar los días de la semana en que debería ejecutarse.

      * **Periodicidad mensual**: ahora puede elegir repetir la campaña todos los meses o cada dos meses y seleccionar el día del mes en que debe ejecutarse.

      * **Programaciones diarias, semanales o mensuales**: Puede especificar si la programación recurrente debe detenerse en una fecha específica o después de un determinado número de incidencias.

   * **Campañas de acción transaccional programadas**: ya están disponibles las campañas de acción transaccional programadas para enviar comunicaciones transaccionales por lotes y basadas en público por correo electrónico, SMS y canales push.

* **Canal - Tarjetas de contenido**

   * **Plantillas de diseño de tarjeta de contenido**: el canal de tarjeta de contenido ahora proporciona diseños de mensajes OOTB que optimizarán su experiencia de creación. Esta versión incluye plantillas de diseño de Imagen pequeña, Imagen grande y Solo imagen. [Más información](../content-card/design-content-card.md)

* **Canal: Push**

   * **Fecha de caducidad de la notificación push**: ahora puede especificar una fecha de caducidad para cada notificación push, lo que evita que los mensajes con limitación de tiempo (como las ofertas de Black Friday) se envíen después de una fecha determinada y, por lo tanto, evita ofrecer una mala experiencia a sus clientes.

* **Canal: SMS**

   * **Exclusión aproximada**: cuando está habilitada, la opción **Exclusión aproximada** detecta mensajes entrantes que se parecen mucho a las palabras clave de exclusión definidas (por ejemplo, “CANCILAR”) y envía automáticamente una respuesta de confirmación para comprobar la intención del usuario de cancelar su suscripción. Si el usuario confirma esta decisión a través de la indicación definida, se cancela su suscripción. [Más información](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >La **Exclusión aproximada** solo está disponible con Sinch e Infobip.

   * **Verificar conexión de SMS**: ahora puede probar y comprobar fácilmente sus credenciales de API de SMS en Adobe Journey Optimizer enviando un mensaje de ejemplo a un dispositivo designado. [Más información](../sms/sms-configuration-sinch.md)

* **Configuración**

   * **Compatibilidad con atributos personalizados con la URL de cancelación de suscripción de un solo clic**: con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer un punto final personalizado externo definiendo su propio vínculo para cancelar la suscripción con un solo clic en la configuración de correo electrónico. Cuando los destinatarios hacen clic en el vínculo Cancelar suscripción, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

     Para personalizar aún más el vínculo de cancelación de suscripción de un solo clic, ahora puede definir atributos personalizados que se adjuntarán al evento de consentimiento. [Más información](../email/list-unsubscribe.md#custom-attributes)

* **Conjuntos de datos**

   * **Repositorio de objetos de Decisiones sobre experiencias - Elementos de oferta personalizados**: el conjunto de datos de exportación integrado ahora captura todos los atributos de ofertas y el estado del ciclo vital, lo que permite una personalización y un sistema de informes completos. [Más información](../data/export-datasets.md)

   * Se ha introducido la comprobación de versiones a través del campo `etag` para mejorar la coherencia y rastrear los cambios a fin de ofrecer los elementos de forma más fiable.

* **Toma de decisiones**

   * **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar fragmentos a elementos de decisión que se pueden aprovechar en campañas de experiencia basadas en código mediante políticas de decisión. Esta capacidad está disponible en disponibilidad limitada para un conjunto de clientes. [Más información](../experience-decisioning/create-decision.md#fragments)

* **Recorridos**

   * **Operaciones masivas de recorridos**: en su lista de recorridos, ahora puede seleccionar varios elementos. Una vez seleccionados, puede pausar o reanudar hasta 10 recorridos a la vez.

   * **Compatibilidad con redireccionamiento (302) en acciones personalizadas**: ahora las acciones personalizadas pueden administrar redireccionamientos HTTP 302 por cada solicitud. Esto permite a los recorridos integrarse con API que redirigen las solicitudes a direcciones URL localizadas o específicas de la región. Las redirecciones se siguen automáticamente, lo que garantiza que el contenido correcto se envíe sin configuración adicional.

   * **Varias acciones entrantes en recorridos**: para simplificar la orquestación de recorrido, ahora puede definir varias acciones entrantes en un solo recorrido. Esta capacidad, disponible previamente en campañas, le permite enviar varias experiencias basadas en código, mensajes in-app, tarjetas de contenido o acciones web a diferentes ubicaciones al mismo tiempo, y cada acción con un contenido específico. [Más información](../building-journeys/journey-action.md#multi-action)

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


