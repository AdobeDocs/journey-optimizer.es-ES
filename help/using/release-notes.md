---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
source-git-commit: 1c299ec022a3985c2e9b164bc57d36948f0941d5
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 11%

---


# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar las últimas [Actualizaciones de documentación](documentation-updates.md).


## Versión de agosto de 2021 {#august-2021-release}

### Nuevas funciones

<table>
<thead>
<tr>

<th><strong>Enviar mensajes en el mejor momento: Optimización del tiempo de envío</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Envíe automáticamente su mensaje push o correo electrónico en el mejor momento para cada cliente con el que interactúe con Adobe Journey Optimizer. La optimización del tiempo de envío, con tecnología de los servicios de IA de Adobe, predice el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de la apertura histórica y las tasas de clics predefinidas.</p>
<p>Actualmente, esta función está en versión beta y solo está disponible para los clientes de la versión beta. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.</p>
<p>Para obtener más información, consulte la <a href="building-journeys/journeys-message.md#send-time-optimization">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Aprovechar las relaciones de esquema en eventos empresariales: administración de tablas de búsqueda</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aprovechar las relaciones entre esquemas al configurar eventos empresariales. Esto se suma a la capacidad de aprovechar los campos de tablas vinculadas al configurar un evento unitario, al utilizar condiciones en un recorrido, en la personalización de mensajes y en la personalización de acciones personalizadas.</p>
<p>Para obtener más información, consulte la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Asegúrese de que los correos electrónicos lleguen a los usuarios: Reintento de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir el periodo de reintento por ajuste preestablecido para garantizar que los intentos de reintento ya no se realicen cuando ya no se necesiten. Por ejemplo, puede establecer el periodo de reintento en 24 horas para un mensaje transaccional de restablecimiento de contraseña que contenga un vínculo válido solo para un día. Tenga en cuenta que la configuración de reintentos solo se aplica al canal de correo electrónico.</p>
<p>Para obtener más información, consulte la <a href="configuration/retries.md#retry-duration">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Definir direcciones a excluir del envío: lista de supresión</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La adición de direcciones de correo electrónico y dominios a la lista de supresión ya está disponible en la interfaz de usuario, una a una, ya sea en modo masivo a través de una carga de archivo CSV.</p>
<p>Para obtener más información, consulte la <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Mejoras

**Recorridos**

* **Encabezados dinámicos** : ahora puede pasar datos dinámicos en parámetros de encabezado HTTP. Estos parámetros los pueden utilizar los sistemas de integración que reciben las llamadas HTTP de acción de recorrido, por ejemplo, la marca de tiempo o el ID de seguimiento. [Más información](action/about-custom-action-configuration.md#url-configuration)
* **Rutas URL dinámicas** : ahora puede configurar rutas URL dinámicas para acciones personalizadas. [Más información](action/about-custom-action-configuration.md#url-configuration)
* La tasa de regulación general de los segmentos leídos ha cambiado de 17.000 a 20.000 mensajes por segundo. [Más información](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interfaz de usuario**

* **Búsqueda** : Ahora, en todas las páginas, puede buscar objetos empresariales y artículos de ayuda directamente desde el campo de búsqueda Experience Cloud unificado. [Más información](user-interface.md#unified-search)
* **Actualizaciones** : la visualización de elementos recientes de la página principal de Adobe Journey Optimizer ahora se amplía a objetos comerciales adicionales. Con esta actualización, los accesos directos a los mensajes, Recorridos, segmentos, esquemas, conjuntos de datos, fuentes de datos, eventos, acciones, fuentes y destinos a los que se ha accedido recientemente incluyen: [Más información](action/about-custom-action-configuration.md#passing-collection)

**Diseño de contenido**

* **Fondo** : las imágenes de fondo ahora se admiten en la vista previa en vivo. [Más información](preview.md)
* **Vínculo de no participación de un clic** : Puede insertar un nuevo tipo de vínculo en el contenido del correo electrónico: el  **desenlace de** exclusión permite a los usuarios cancelar la suscripción para recibir sus comunicaciones con solo un clic, sin ser redirigido a una página de aterrizaje para confirmar la exclusión. [Más información](message-tracking.md#one-click-opt-out-link)

<!--**Personalization**

* **Expression Editor** - You can now easily add a fall-back value when defining personalization: when personalization field is empty for a profile, the fall-back value will display. [Learn more](documentation-updates.md)-->

**Configuración de correo electrónico**

* **Lista de permitidos** : Ahora, la lista de permitidos se puede habilitar y deshabilitar en un entorno limitado que no sea de producción mediante una llamada de API. [Más información](allow-list.md#enable-allow-list)
* **Navegación** : la lista de supresión, a la que se puede acceder desde  **Administración > Canales > Configuración de correo electrónico > Menú** General, se ha movido al nuevo submenú  **Lista de** supresión, que reúne todas las funciones relacionadas para facilitar el acceso. [Más información](configuration/manage-suppression-list.md#access-suppression-list)
<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->

### Correcciones

* Se ha corregido un problema de accesibilidad en la navegación por pestañas de mensajes.
* Se ha corregido un problema de localización en las etiquetas del diseñador de correo electrónico.
* Se ha corregido un problema que se producía al seleccionar más de un nodo en un recorrido y al hacer clic en Eliminar en el panel de propiedades.
* Se ha corregido un problema que impedía añadir un nuevo encabezado a una acción utilizada en un recorrido.
* Ahora puede averiguar el motivo por el que la creación de un ajuste preestablecido de mensaje falló a través de una advertencia más explícita en la interfaz de usuario.


## Versión de julio de 2021 {#july-2021-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Uso de metadatos en los mensajes: administración de tablas de búsqueda</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Enriquezca sus experiencias con los datos de referencia que ha cargado en Journey Optimizer. Algunos ejemplos son la búsqueda de metadatos sobre un ID de reserva en un evento de experiencia o la búsqueda de información de producto desde un SKU en un evento de experiencia para su uso en el lienzo. </p>
<p>Ahora puede aprovechar las relaciones entre esquemas para utilizar un conjunto de datos como una tabla de búsqueda para otro. A continuación, puede aprovechar todos los campos de las tablas vinculadas al configurar un evento unitario, al utilizar condiciones en un recorrido, en la personalización de mensajes y en la personalización de acciones personalizadas.</p>
<p>Para obtener más información, consulte la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lista de permitidos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir una lista específica de seguridad de envío a nivel de entorno limitado para disponer de un entorno seguro para realizar pruebas. En una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a sus clientes. Esta función se habilita aprovechando las API de supresión.</p>
<p>Para obtener más información, consulte la <a href="allow-list.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* La tasa de regulación general de todos los segmentos de lectura que se ejecutan simultáneamente en el mismo entorno limitado está limitada a 17.000 mensajes por segundo. [Más información](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* El campo **Cache duration** se ha eliminado del panel de configuración del origen de datos. [Más información](datasource/about-data-sources.md)
* Para las fuentes de datos externas, ahora se define automáticamente una regla de límite de 15 llamadas por segundo. [Más información](configuration/external-systems.md#capping)
* En el caso de los recorridos activos, la pantalla de propiedades de recorrido ahora muestra la fecha de publicación y el nombre del usuario que publicó el recorrido. [Más información](building-journeys/journey-gs.md#change-properties)
* En la pantalla de la lista de recorridos, se ha añadido el filtro de tipo de recorrido. [Más información](user-interface.md#section_lgm_hpz_pgb)
* El parámetro **[!UICONTROL Throttling rate]** se ha agregado en la actividad Leer segmento . [Más información](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Vista previa y prueba de mensajes**

* La identidad y el área de nombres ahora están visibles en la pantalla **[!UICONTROL Preview]**. [Más información](preview.md#preview-your-messages)
* El número de correos electrónicos de prueba para pruebas ahora está restringido a 10.
* Los caracteres permitidos para el **Subject line prefix** en las pruebas ahora están limitados. [Más información](preview.md#send-proofs)

**Editor de expresiones de personalización**

* Se ha cambiado el nombre de la lista desplegable de ayuda y se ha reorganizado.

### Correcciones

* Se ha corregido un problema que hacía que se enviaran mensajes duplicados para la entrega por lotes de correo electrónico.
* Los eventos ahora se generan de forma acorde cuando el envío de correo electrónico no se realiza una vez finalizado el periodo de reintento.
* Se ha corregido un problema por el que faltaba información de IP en la pantalla Registros de PTR .
* Ya está implementada la localización en el carril de la oferta dentro del Editor de expresiones.
* Se ha corregido un espaciado incorrecto en las ventanas emergentes de información.
* Se ha corregido un problema en el Diseñador de correo electrónico al cargar un archivo HTML en el que la hoja de estilo interna con propiedad `background-image` no era compatible.

