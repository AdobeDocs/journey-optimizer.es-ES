---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 1071229582008d66b4184ec782aaf23bad111a93
workflow-type: tm+mt
source-wordcount: '1920'
ht-degree: 97%

---

# Notas de la versión {#release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

Las notas de la versión anteriores están disponibles en [esta página](release-notes-2022.md). También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.


## Notas de la versión de abril de 2023 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### Nuevas funcionalidades{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal web (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer está ampliando sus funciones en todos los canales añadiendo compatibilidad con canales web. Ahora puede crear, cambiar y previsualizar experiencias web como cualquier otro canal mediante una interfaz visual inteligente e intuitiva para personalizar la experiencia de los usuarios finales. Tenga en cuenta que actualmente en Journey Optimizer solo puede crear experiencias web en campañas.</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>Para obtener más información, consulte la <a href="../web/get-started-web.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Flujo de trabajo de inicio rápido de incorporación al dispositivo móvil (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible el nuevo flujo de trabajo de inicio rápido de incorporación al dispositivo móvil. Utilice esta nueva función de producto para configurar rápidamente el SDK móvil y empezar a recopilar y validar datos de eventos móviles, así como enviar notificaciones push móviles con Adobe Journey Optimizer. Se puede acceder a esta funcionalidad a través de la página de inicio de recopilación de datos como una versión beta pública.</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>Para obtener más información, consulte la <a href="../push/mobile-onboarding-wf.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevo panel de Recorrido (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> El panel de Recorrido ahora está dividido en dos pestañas:</p>
<ul><li>Utilice la variable <strong>Información general</strong> para acceder a un tablero nuevo que muestra las métricas clave relacionadas con sus recorridos.</li>
<li>Utilice la variable <strong>Examinar</strong> para acceder a la lista de todos los recorridos.</li></ul>
<p>Se puede acceder a esta funcionalidad en todos los recorridos como una versión beta pública.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-gs.md#journey-access">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Personalized Optimization AI ranking model (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized Optimization AI ranking models are now generally available in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### Mejoras {#april-2023-improvements}

**Recorridos**

* El lienzo del recorrido muestra ahora el ID de actividad en las actividades de mensajes y las etiquetas finales. Esto mejora la creación de informes y la segmentación
* Se ha mejorado el diseño del panel de configuración, que aparece en acciones, fuentes de datos, eventos y recorridos.
* Se han añadido nuevos mecanismos de protección a los recorridos:
   * El número de actividades en un recorrido ahora está limitado a 50. [Más información](../start/guardrails.md#journeys-guardrails-journeys)
   * El número de **recorridos en directo** en una organización está limitado ahora a 100 por zona protegida. No se tienen en cuenta los recorridos en el modo de prueba. [Más información](../start/guardrails.md#journeys-guardrails-journeys)

* Al añadir un [Correo electrónico](../email/create-email.md), [SMS](../sms/create-sms.md) o [Push](../push/create-push.md) en un recorrido, la superficie se rellena ahora previamente, de forma predeterminada, con la última superficie utilizada para dicho canal, en el recorrido actual.
* Ahora puede definir parámetros de consulta estáticos o dinámicos en sus acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#url-configuration)

**Creación de informes**

* Ahora puede exportar informes de Journey Optimizer como PDF. [Más información](../reports/global-report.md#export-reports)

**Diseñador de contenido**

* Se ha actualizado el Diseñador de contenido de Adobe Journey Optimizer y ahora es más fácil acceder a los estilos y componentes de diseño. Esta nueva versión ofrece una experiencia de usuario mejorada e incluye un mayor rendimiento, compatibilidad parcial en modo oscuro y compatibilidad con nuevos estándares de accesibilidad.



## Notas de la versión de marzo de 2023 {#mar-2023}

### Nuevas funcionalidades{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal en la aplicación (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, puede enviar mensajes personalizados en la aplicación a los usuarios de la aplicación dentro de una campaña. Utilice Journey Optimizer para diseñar notificaciones y personalizar el diseño, la visualización, el texto y los botones del mensaje para crear una experiencia perfecta.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Para obtener más información, consulte la <a href="../in-app/get-started-in-app.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rastreo de clics de SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el rastreo de clics de SMS, puede monitorizar el rendimiento de las URL acortadas, identificar quién hizo clic en ellas y utilizar estos datos para redirigirse a esos clientes con campañas posteriores.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Para obtener más información, consulte la <a href="../sms/create-sms.md#sms-content">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso de etiquetas en los recorridos (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como profesional de Journey Optimizer, ahora puede organizar los objetos de negocio mediante etiquetas. Las etiquetas son una forma rápida y sencilla de clasificar objetos para mejorar la búsqueda. Actualmente, esta funcionalidad está en versión beta y solo está disponible para recorridos.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/tags.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>



### Mejoras {#mar-2023-improvements}

**Recorridos**

* La nueva **API de limitación** le permite establecer un límite en la cantidad de eventos enviados por segundo, lo que evita picos de tráfico abrumadores en sus sistemas externos o API. Cuando se alcanza el límite establecido, todas las llamadas a la API subsiguientes se ponen en cola y se procesan lo antes posible en el orden en que se recibieron. Tenga en cuenta que esta función solo admite una configuración de limitación en todas las zonas protegidas. [Más información](../configuration/external-systems.md)
* El lienzo de recorrido se ha mejorado para que la experiencia del usuario sea más sencilla y mejorada. Al final de cada ruta en el lienzo, se han eliminado los marcadores vacíos. Ahora puede simplemente agregar sus actividades arrastrándolas al final de una ruta.
* En el lienzo del recorrido, la etiqueta de **Fin** ya no se configura automáticamente con el nombre de la actividad anterior. Los usuarios pueden agregar manualmente una etiqueta personalizada si es necesario.
* El tiempo de espera predeterminado y la duración del error en las propiedades del recorrido han cambiado de 5 a 30 segundos. [Más información](../configuration/external-systems.md#timeout)
* La tasa de limitación predeterminada en las actividades de segmentos de lectura ha cambiado de 20 000 a 5000 mensajes por segundo. [Más información](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Se ha añadido un mecanismo de protección al modo de prueba para escuchar solo los eventos enviados a través de la interfaz. Los eventos enviados a través de una herramienta externa no se tienen en cuenta. [Más información](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Gestión de decisiones**

* Para evitar cualquier posible confusión con la reciente versión de la funcionalidad de etiquetas en Adobe Experience Platform, se ha cambiado el nombre de las etiquetas de Gestión de decisiones a &quot;Calificadores de colección&quot;.

   Tenga en cuenta que, aunque el término &quot;etiqueta&quot; ya no se utiliza en la interfaz de usuario de Gestión de decisiones, se sigue utilizando en servicios backend como API y conjuntos de datos.

* Ahora puede restablecer el contador de límite de oferta diariamente, semanalmente o mensualmente. [Más información](../offers/offer-library/add-constraints.md#capping)

* También puede elegir qué evento de Adobe Experience Platform se debe tener en cuenta para el límite de Offer Decisioning. [Más información](../offers/offer-library/add-constraints.md#capping)

* Se han añadido parámetros adicionales en la pantalla de creación de ubicaciones. Permiten controlar si una oferta se puede duplicar en varias ubicaciones y especificar si el contenido y los metadatos de la oferta se deben incluir en la respuesta de API. [Más información](../offers/offer-library/creating-placements.md)

**Personalización**

* Ahora puede incluir texto alternativo predeterminado para atributos de perfil basados en cadenas en el Editor de expresiones. Estos valores se mostrarán si los atributos seleccionados no devuelven ningún resultado. [Más información](../personalization/personalization-build-expressions.md#add)

**Creación de informes**

* La funcionalidad del widget de creación de informes se ha mejorado con la capacidad de personalizar la forma en que los usuarios ven sus datos. Con esta mejora, los usuarios ahora pueden elegir entre varias opciones de visualización, incluidos gráficos, tablas y gráficos circulares.

   Para tener acceso a las últimas utilidades, tenga en cuenta que tendrá que restablecer los distintos paneles de creación de informes. Para obtener más información sobre la personalización de tableros, consulte la [documentación detallada](../reports/global-report.md#modify-dashboard).

## Notas de la versión de febrero de 2023 {#feb-2023}

### Nuevas funcionalidades{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal en la aplicación (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, puede enviar mensajes personalizados en la aplicación a los usuarios de la aplicación dentro de una campaña. Utilice Journey Optimizer para diseñar notificaciones y personalizar el diseño, la visualización, el texto y los botones del mensaje para crear una experiencia perfecta.</p>
<p><strong>Precaución</strong>: Actualmente, esta funcionalidad está en versión beta y solo está disponible para los clientes de la versión beta. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Para obtener más información, consulte la <a href="../in-app/get-started-in-app.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportación de los conjuntos de datos de Journey Optimizer a los destinos de almacenamiento en la nube (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, puede establecer una conexión activa con las ubicaciones de almacenamiento en la nube para exportar el contenido de los conjuntos de datos. Los destinos disponibles son: almacenamiento en la nube Amazon S3, Azure Blob, Azure Data Lake Gen 2, zona de aterrizaje de datos, almacenamiento en la nube de Google, SFTP.</p>
<p><strong>Precaución</strong>: Esta funcionalidad está actualmente en versión beta y está disponible para todos los usuarios de Adobe Journey Optimizer. Póngase en contacto con su representante de Adobe para obtener acceso a los destinos si todavía no tiene acceso.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Para obtener más información, consulte la <a href="../data/export-datasets.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Mejoras {#feb-2023-improvements}

**Recorridos**

* El campo **Período de espera de reentrada** se ha añadido a las propiedades del recorrido. Este campo permite definir el tiempo de espera antes de permitir que un perfil vuelva a entrar en el recorrido en recorridos unitarios (empezando por un evento o una calificación de segmentos). Esto evita que los recorridos se activen varias veces por error para el mismo evento. De forma predeterminada, el campo se establece en 5 minutos. [Más información](../building-journeys/journey-gs.md#entrance)

* Se han realizado mejoras para las **fechas de inicio y finalización del recorrido**. Si no ha especificado una fecha de inicio, se añadirá ahora automáticamente en el momento de la publicación. Para los recorridos **Lectura de segmento**, ahora puede añadir una fecha de finalización. Esto permite que los perfiles salgan automáticamente cuando se alcanza la fecha. [Más información](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Administración**

* **Lista de permitidos**: ahora, puede descargar la lista de permitidos como un archivo .csv. [Más información](../configuration/allow-list.md#download-allowed-list)

* **Superficie de correo electrónico**: se ha añadido una comprobación adicional a la configuración de la superficie del correo electrónico: si el registro MX del subdominio utilizado en el campo **Responder a la dirección (correo electrónico)** o **Dirección de correo electrónico en CCO** no está configurado correctamente, la superficie del correo electrónico ya no se podrá crear más. Debe tenerlo configurado o utilizar otro. [Más información](../email/email-settings.md#reply-to-email)

* **Superficie de correo electrónico**: en la sección **Parámetros de seguimiento de URL** de la configuración de la superficie del correo electrónico, el límite de cada campo **Valor** se ha actualizado de 255 caracteres a 5 KB para la compatibilidad con el seguimiento de Adobe Analytics. [Más información](../email/email-settings.md#url-tracking)

**Gestión de decisiones**

* **Ubicaciones**: se han añadido parámetros adicionales en la pantalla de creación de ubicaciones. Permiten controlar si una oferta se puede duplicar en varias ubicaciones y especificar si el contenido y los metadatos de la oferta se deben incluir en la respuesta de API. [Más información](../offers/offer-library/creating-placements.md)

* **Personalización de URL**: al añadir direcciones URL como contenido a las representaciones de las ofertas, ahora puede personalizar estas direcciones URL con el Editor de expresiones. [Más información](../offers/offer-library/add-representations.md)

## Notas de la versión de enero de 2023{#jan-2023-release}

### Nuevas funciones{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Higiene de los datos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform proporciona un conjunto de funcionalidades de higiene de datos que le permiten administrar los datos almacenados mediante eliminaciones programáticas de registros de consumidores y conjuntos de datos. Esta funcionalidad ya está disponible para Adobe Journey Optimizer. </p>
<p>Puede administrar los almacenes de datos para asegurarse de que la información se utiliza según lo esperado, se actualiza cuando es necesario corregir datos incorrectos y se elimina cuando las políticas organizativas lo consideran necesario.</p>
<p><strong>Precaución</strong>: Actualmente, las funcionalidades de higiene de los datos solo están disponibles para las organizaciones que han adquirido las ofertas de complementos <strong>Escudo de atención sanitaria</strong> y <strong>Escudo de seguridad y privacidad</strong>.</p><p>Para obtener más información, consulte la <a href="../privacy/data-hygiene.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Plantillas de contenido de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear plantillas de contenido independientes que se pueden aprovechar en distintos recorridos y campañas para que las pueda reutilizar rápidamente.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Obtenga información sobre cómo crear, editar y utilizar plantillas de contenido en <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=es">este vídeo</a>. Para obtener más información, consulte la <a href="../email/content-templates.md">documentación detallada</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-2023-improvements}

**Recorridos**

* Al añadir **Clasificación del segmento** o **Leer segmento** en un recorrido, el área de nombres ahora se rellena previamente, de forma predeterminada, con la última utilizada. Consulte las secciones [Clasificación del segmento](../building-journeys/segment-qualification-events.md#about-segment-qualification) y [Leer segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* En el lienzo del recorrido, hay un nuevo botón disponible en la barra de herramientas que le permite descargar una captura de pantalla del recorrido.

**Diseñador de correos electrónicos**

* Ahora puede exportar el contenido del correo electrónico desde el menú **Exportar HTML**. Los archivos exportados están disponibles en un archivo de compresión (.ZIP).

**Administración**

* Una nueva subsección ofrece recomendaciones sobre la creación de la dirección **Responder a (correo electrónico)** y la gestión adecuada de las respuestas. [Más información](../email/email-settings.md#reply-to-email)

* Al crear o editar **Grupos de IP**, los registros PTR asociados ahora se muestran en la lista de IP y al pasar el ratón por encima de las direcciones IP seleccionadas. [Más información](../configuration/ip-pools.md#create-ip-pool)

* Después de seleccionar un grupo de IP en una superficie de canal, la información de registro PTR ahora es visible al pasar el ratón por encima de las direcciones IP. [Más información](../email/email-settings.md#subdomains-and-ip-pools)

* La interfaz de usuario para editar [Registros PTR](../configuration/ptr-records.md#edit-ptr-record) y [campos de ejecución](../configuration/primary-email-addresses.md) se ha actualizado.

* Se ha mejorado la interfaz de usuario para crear y editar subdominios. [Más información](../configuration/delegate-subdomain.md)

* La lista de supresión **Cargas recientes** se ha actualizado. [Más información](../configuration/manage-suppression-list.md#recent-uploads)

**Campañas**

* Ahora se genera automáticamente una solicitud cURL de ejemplo que permite la ejecución de campañas activadas por API y está disponible en la pantalla de la campaña. [Más información](../campaigns/api-triggered-campaigns.md)


**Personalización**

* Hay disponibles nuevas funciones de ayuda: formatCurrency, charCodeAt, stringToDate, toString, formatNumber y toHexString. Además, la función toDateTimeOnly ahora acepta tipos de campo de cadena, fecha, larga e int. [Más información](../personalization/functions/functions.md)
