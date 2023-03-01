---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9e8bac0c908646213a9d9a0598e3aa4750084b50
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 57%

---

# Notas de la versión {#release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

Las notas de la versión anteriores están disponibles en [esta página](release-notes-2022.md). También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Notas de la versión de febrero de 2023 {#feb-2023}

### Nuevas funciones{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal en la aplicación (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede enviar mensajes personalizados en la aplicación a los usuarios de la misma dentro de una campaña. Utilice Journey Optimizer para diseñar notificaciones y personalizar el diseño del mensaje, la visualización, el texto y los botones para crear una experiencia perfecta.</p>
<p><strong>Precaución</strong> : Actualmente, esta función está en versión beta y solo está disponible para los clientes de la versión beta. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Para obtener más información, consulte la <a href="../in-app/get-started-in-app.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportar conjuntos de datos de Journey Optimizer a destinos de almacenamiento en la nube (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede establecer una conexión activa con las ubicaciones de almacenamiento en la nube para exportar el contenido de los conjuntos de datos. Los destinos disponibles son: Amazon S3 Cloud Storage, Azure Blob, Azure Data Lake Gen 2, Data Landing Zone, Google Cloud Storage, SFTP.</p>
<p><strong>Precaución</strong> - Esta función se encuentra actualmente en versión beta y está disponible para todos los usuarios de Adobe Journey Optimizer. Póngase en contacto con su representante de Adobe para obtener acceso a Destinos si aún no tiene acceso.</p>
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

* El **Período de espera de reentrada** se ha añadido este campo a las propiedades del recorrido. Este campo le permite definir el tiempo de espera antes de permitir que un perfil introduzca de nuevo el recorrido en recorridos unitarios (empezando por un evento o una calificación de segmentos). Esto evita que los recorridos se activen varias veces de forma errónea para el mismo evento. De forma predeterminada, el campo se establece en 5 minutos. [Más información](../building-journeys/journey-gs.md#entrance)

* Se han realizado mejoras para **Fechas de inicio y finalización del recorrido**. Si no ha especificado una fecha de inicio, esta se añade automáticamente en el momento de la publicación. Para **Leer segmento** recorridos, ahora puede añadir una fecha de finalización. Esto permite que los perfiles salgan automáticamente cuando llega la fecha. [Más información](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Administración**

* **Lista de permitidos** - Ahora puede descargar la lista de permitidos como archivo .csv. [Más información](../configuration/allow-list.md#download-allowed-list)

* **Superficie del correo electrónico** - Se ha añadido una comprobación adicional a la configuración de la superficie de correo electrónico: si el registro MX del subdominio utilizado en el **Dirección de respuesta (correo electrónico)** o en el **Dirección de correo electrónico CCO** no se ha configurado correctamente, la superficie de correo electrónico ya no se puede crear. Debe tenerlo configurado o usar otro. [Más información](../email/email-settings.md#reply-to-email)

* **Superficie del correo electrónico** - En el **Parámetros de seguimiento de URL** de la configuración de la superficie del correo electrónico, el límite de cada **Valor** El campo se ha actualizado de 255 caracteres a 5 KB para garantizar la compatibilidad con el seguimiento de Adobe Analytics. [Más información](../email/email-settings.md#url-tracking)

**Gestión de decisiones**

* **Ubicaciones** : Se han añadido parámetros adicionales en la pantalla de creación de ubicaciones. Permiten controlar si una oferta se puede duplicar en varias ubicaciones y especificar si el contenido y los metadatos de la oferta deben incluirse en la respuesta de la API. [Más información](../offers/offer-library/creating-placements.md)

* **Personalizar URL** : Al añadir direcciones URL como contenido a las representaciones de sus ofertas, ahora puede personalizar estas direcciones URL con el Editor de expresiones. [Más información](../offers/offer-library/add-representations.md)

<!--
* **Capping** - You can now reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)

* **Capping** - You can now choose which Adobe Experience Platform event should be looked at for offer decisioning capping. [Learn more](../offers/offer-library/add-constraints.md#capping)
-->

## Lanzamiento de enero de 2023 {#jan-2023-release}

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
