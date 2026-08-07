---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: fcf7ea6d5d6ceaa02490e8cbaf807b9f670c63cc
workflow-type: tm+mt
source-wordcount: 2157
ht-degree: 20%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece de forma continua nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de agosto de 2026 {#august-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 18 y 19 de agosto de 2026

### Incorporación {#august-26-onboarding}

En esta versión se ha añadido la siguiente funcionalidad a la incorporación.

<table>
<thead>
<tr>
<th><strong>Funciones guiadas para incorporar correos electrónicos y recorridos (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transición a Adobe Journey Optimizer desde otra plataforma de marketing es más sencilla gracias a las funciones guiadas que le ayudan a trasladar el contenido y los recorridos de correo electrónico existentes a Journey Optimizer. Un espacio de trabajo dedicado le permite reutilizar lo que tiene en lugar de reconstruir desde cero.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Recorridos {#august-26-journeys}

En esta versión se han añadido las siguientes funciones y mejoras a los recorridos.

<table>
<thead>
<tr>
<th><strong>resistencia a nivel de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar un grupo de exclusión para los recorridos directamente desde las propiedades de recorrido. Una exclusión es un porcentaje configurable de la audiencia de destino que se excluye de la entrada al recorrido y que no recibe ninguna comunicación. Al comparar los perfiles de exclusión con los perfiles activos en los informes de Customer Journey Analytics, puede medir el alza incremental, el verdadero impacto, que ofrece su recorrido.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15162">DOCAC-15162</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Agregar nueva función dateDiff en el editor de expresiones de recorrido** - El editor de expresiones de recorrido ahora incluye la función `dateDiff`, que calcula la diferencia entre dos fechas en número de días. Esta función es útil para lógica basada en tiempo, como la creación de plazos, el cálculo de las duraciones del ciclo vital de los clientes o la creación de temporizadores de cuenta atrás en condiciones de recorrido. <a href="https://jira.corp.adobe.com/browse/DOCAC-15293">DOCAC-15293</a> <!-- Documentation link: TBD -->

* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido, ahora aparecen en el encabezado del recorrido junto al distintivo de estado. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado. <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">DOCAC-14702</a> <!-- Documentation link: TBD -->

### Campañas {#august-26-camp}

En esta versión se han añadido las siguientes funcionalidades y mejoras a las campañas de.

<table>
<thead>
<tr>
<th><strong>Simulación de experiencia entrante en campañas de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede simular acciones de canal entrante en campañas de acción antes de lanzarlas. Utilice el modo de simulación para probar la configuración con usuarios simulados y previsualizar la experiencia procesada, incluida una URL y un código QR generados, para poder validar reglas, decisiones y el procesamiento de contenido de principio a fin.</p>
<p>Actualmente, esta funcionalidad está en versión beta privada y está disponible para un conjunto limitado de organizaciones. Póngase en contacto con su representante de Adobe para obtener más información.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Carpetas para campañas**: ahora puede organizar sus campañas en carpetas para mejorar la navegación y la administración en la interfaz. <a href="https://jira.corp.adobe.com/browse/DOCAC-15098">DOCAC-15098</a> <!-- Documentation link: TBD -->

* **Puntuación de alineación de marca en el panel de control de campañas**: ahora puede evaluar la puntuación de alineación con la marca directamente en el panel de control de campañas para asegurarse de que el contenido sea coherente con la marca. Esto le permite comprobar las directrices de un vistazo sin tener que abrir el diseñador de contenido. <a href="https://jira.corp.adobe.com/browse/DOCAC-14516">DOCAC-14516</a> <!-- Documentation link: TBD -->

* **Anular el campo de ejecución predeterminado en las campañas**: anteriormente disponible en el nivel de recorrido, ahora se puede anular el campo de ejecución predeterminado establecido globalmente para los envíos de correo electrónico, SMS y WhatsApp en los parámetros de la campaña. <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">DOCAC-14718</a> <!-- Documentation link: TBD -->

### Campañas orquestadas {#august-26-oc}

En esta versión se han añadido las siguientes funcionalidades y mejoras a las campañas orquestadas.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con Horas de silencio para campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar horas tranquilas a las campañas orquestadas. Las horas tranquilas le permiten definir exclusiones basadas en el tiempo para evitar que los mensajes se envíen durante períodos específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento en los casos de uso de la orquestación de la campaña.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Capacidad para administrar dimensiones de destino de perfil**. Ahora puede eliminar un Dimension de destino de perfil o editar e intercambiar su área de nombres de identidad configurada, lo que proporciona mayor control y flexibilidad sobre las configuraciones de datos. <a href="https://jira.corp.adobe.com/browse/DOCAC-15018">DOCAC-15018</a> <!-- Documentation link: TBD -->

* **Soporte para Line (disponibilidad limitada)**: ahora puede agregar acciones de LINE directamente a sus campañas orquestadas. Esta nueva actividad le permite crear y ofrecer contenido altamente personalizado, incluidos texto, pegatinas, imágenes, vídeos, datos de ubicación y mensajes Flex enriquecidos, para atraer a sus clientes sin problemas en la plataforma LINE. Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe. <a href="https://jira.corp.adobe.com/browse/DOCAC-14905">DOCAC-14905</a> <!-- Documentation link: TBD -->

* **Nuevas API públicas de campañas orquestadas**. Ya están disponibles las nuevas especificaciones de la API para campañas orquestadas. Estas API le permiten crear, administrar y almacenar en déclencheur campañas orquestadas mediante programación, lo que permite una integración más profunda con sistemas externos y canalizaciones de automatización. <a href="https://jira.corp.adobe.com/browse/DOCAC-14308">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña**: las campañas organizadas ahora admiten la personalización de los campos de encabezado de correo electrónico, incluidos el nombre del remitente, la dirección del remitente y la respuesta a, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa. Los valores del encabezado se pueden establecer a nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso. <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">DOCAC-13761</a> <!-- Documentation link: TBD -->

* **Simplificación de la dimensión de destino en campañas orquestadas**: la dimensión de segmentación activa ahora se muestra en el lienzo del flujo de trabajo, para que pueda ver qué dimensión utiliza una actividad de canal. El flujo de segmentación de varias entidades es más sencillo, ya que ya no necesita una actividad &quot;Change dimension&quot; independiente. Además, ahora puede elegir explícitamente si los mensajes se envían en el nivel de perfil o en un nivel de dimensión secundario. <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">DOCAC-13554</a> <!-- Documentation link: TBD -->

* **Enviar mediante oleadas en campañas orquestadas**: ahora puede programar mensajes salientes de campañas orquestadas para que se entreguen en lotes controlados a lo largo del tiempo. Ideal para campañas de gran volumen o en las que el tiempo es un factor importante, la entrega de olas también ofrece una mejor capacidad de entrega y ayuda a mantener una sólida reputación de remitente, ya que reduce el riesgo de ser marcado como correo no deseado. <a href="https://jira.corp.adobe.com/browse/DOCAC-13990">DOCAC-13990</a> <!-- Documentation link: TBD -->

### Canales {#august-26-channels}

En esta versión se han añadido las siguientes funcionalidades y mejoras a los canales.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con Decisioning en el canal web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning ya está disponible para el canal Web. Puede utilizar las políticas de decisión directamente en el editor visual web para entregar las ofertas más relevantes a cada visitante.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Archivos adjuntos personalizados de PDF en correos electrónicos activados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora admite la asociación de hasta cinco PDF específicos de destinatarios por correo electrónico en campañas activadas por API. Los archivos PDF se recuperan de forma segura desde la zona de aterrizaje de datos y se adjuntan en el momento del envío, con la ubicación de cada archivo pasada directamente en la carga útil de la API. Esto permite que los sistemas existentes de generación de documentos de subida permanezcan en su sitio, con Journey Optimizer gestionando la entrega.</p>
<p>Los casos de uso admitidos incluyen facturas, extractos, tickets, contratos, etiquetas de envío y documentos similares que varían según el destinatario. Los archivos adjuntos personalizados de PDF solo están disponibles en campañas activadas por API y no son compatibles con recorridos o campañas orquestadas.</p>
<p>Los volúmenes y tamaños de archivos adjuntos más grandes son compatibles mediante el complemento de archivos adjuntos de PDF. Para obtener más información, póngase en contacto con su representante de Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canal LINE: creación de cambios**: la IU del canal LINE se ha actualizado con funcionalidades avanzadas de creación de mensajes. Esta versión incorpora compatibilidad con varios formatos de mensaje, incluidos Texto, Imagen, Mapa de imágenes, Carrusel y Flex (Editor JSON), además de vistas previas de dispositivos en tiempo real. Los usuarios ahora pueden administrar mensajes agrupados de hasta cinco mensajes ordenados (con controles de adición, eliminación y reordenación) y aprovechar el editor de personalización integrado para mensajes validados y dinámicos. <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">DOCAC-14869</a> <!-- Documentation link: TBD -->

* **Complemento de rendimiento para el rendimiento - Push** - Hay un nuevo modo de mensajería transaccional de alto rendimiento disponible en las campañas activadas por API. Este modo está diseñado para la mensajería transaccional a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Antes solo estaba disponible para el canal de correo electrónico, pero ahora también lo está para el canal push, para organizaciones que han adquirido la oferta de complementos de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información. <a href="https://jira.corp.adobe.com/browse/DOCAC-14717">DOCAC-14717</a> <!-- Documentation link: TBD -->

### Toma de decisiones {#august-26-decisioning}

En esta versión se ha añadido la siguiente mejora a Decisioning.

* **Límite de frecuencia de nivel de ubicación en Decisioning**: las reglas de límite de frecuencia en Decisioning ahora se pueden vincular a ubicaciones individuales, lo que le proporciona un control más preciso sobre la frecuencia con la que se muestra una oferta en una superficie determinada. Hay dos modos disponibles: límite específico de la ubicación, que define un límite que se aplica solo cuando la oferta se muestra en una ubicación seleccionada, y límite por ubicación, que aplica un límite de forma independiente en cada ubicación en la que aparece la oferta, de modo que cada ubicación mantiene su propio contador de límite. Tenga en cuenta que el límite relacionado con la ubicación no se aplica a las ofertas restringidas mediante reglas basadas en datos de Adobe Experience Platform. <a href="https://jira.corp.adobe.com/browse/DOCAC-14980">DOCAC-14980</a> <!-- Documentation link: TBD -->

### Diseñador de correo electrónico {#august-26-email}

En esta versión de se ha añadido la siguiente mejora al Designer de correo electrónico.

* **Nuevo componente Tabla en el Designer de correo electrónico**: El Designer de correo electrónico ahora incluye un componente Tabla integrado, que le permite estructurar el contenido en filas y columnas directamente dentro del correo electrónico. Arrastre y suelte el componente en el lienzo, personalice el número de filas y columnas y aplique estilo a cada celda de forma independiente para crear diseños claros y organizados sin depender del HTML personalizado. <a href="https://jira.corp.adobe.com/browse/DOCAC-15093">DOCAC-15093</a> <!-- Documentation link: TBD -->

### Administración {#august-26-administration}

En esta versión se ha añadido la siguiente mejora a la administración.

* **Proceso OTP del bucle de comentarios para subdominios personalizados**: el proceso de configuración del subdominio personalizado del Bucle de comentarios (FBL) se ha mejorado al mostrar la contraseña única (OTP) de Yahoo sender hub directamente dentro de la interfaz de usuario del producto. Los usuarios ahora pueden recuperar y mostrar automáticamente el OTP generado durante la verificación de propiedad del dominio del centro de remitentes de Yahoo. <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">DOCAC-14815</a> <!-- Documentation link: TBD -->

### Mejoras de uso {#august-26-usability}

En esta versión se han añadido las siguientes mejoras a la capacidad de uso.

* **Nueva experiencia de simulación de contenido para variantes de contenido** - El flujo de trabajo **Simular contenido** presenta una experiencia rediseñada: ahora todas las variantes se representan juntas en una sola cuadrícula desplazable (diseños paralelos, apilados o ajustados), reemplazando la vista de una variante a la vez. Una sola barra de acciones inferior consolida la navegación entre las variantes de prueba, el zoom, el cambio de ventanilla (escritorio/móvil), el cambio de configuración regional, la adición de entradas de muestra, la generación de variantes con IA, la selección y el guardado de usuarios simulados y la importación o exportación de variantes. Si se elimina el carril izquierdo y se contraen las capas de encabezado adicionales, las previsualizaciones tendrán mucho más espacio. La opción **Cambiar a experiencia clásica** de la barra de acciones inferior le permite volver a la experiencia anterior en cualquier momento. <a href="https://jira.corp.adobe.com/browse/DOCAC-15285">DOCAC-15285</a> <!-- Documentation link: TBD -->

* **Operaciones masivas en el inventario de recorrido**: ahora puede realizar nuevas acciones masivas directamente desde la lista de inventario de recorrido, lo que permite administrar varios recorridos a la vez con mayor rapidez. Seleccione varios recorridos y aplique cualquiera de las siguientes acciones nuevas en un solo paso: añadir a paquete, eliminar, mover a carpeta, editar etiquetas o administrar el acceso. Esto reduce la necesidad de repetir la misma acción un recorrido a la vez, lo que optimiza la administración de recorridos para equipos que trabajan con un gran número de recorridos. <a href="https://jira.corp.adobe.com/browse/DOCAC-15358">DOCAC-15358</a> <!-- Documentation link: TBD -->

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Notas previas al lanzamiento de julio de 2026 {#july-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 28 y 29 de julio de 2026

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### Recorridos {#july-26-journeys}

En esta versión se ha añadido la siguiente mejora a los recorridos de.


### Campañas {#july-26-campaigns}

En esta versión se han añadido las siguientes funcionalidades y mejoras a las campañas de.

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

### Campañas orquestadas {#july-26-oc}

En esta versión se han añadido las siguientes mejoras a las campañas orquestadas.

<!--

<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.

-->

### Canales {#july-26-channels}

En esta versión se han añadido las siguientes funcionalidades y mejoras a los canales.

### Toma de decisiones {#july-26-decisioning}

En esta versión se han añadido las siguientes mejoras a Decisioning.

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### Gestión de contenidos {#july-26-content}

En esta versión se han añadido las siguientes mejoras a la administración de contenido.

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### Personalización {#july-26-personalization}

En esta versión se han añadido las siguientes mejoras a la personalización.


### Diseñador de correo electrónico {#july-26-email}

En esta versión se ha añadido la siguiente funcionalidad al canal de correo electrónico.


### Administración {#july-26-administration}

En esta versión se han añadido las siguientes funcionalidades a la administración.


### Mejoras de uso {#july-26-usability}

En esta versión se incluyen las siguientes mejoras en la facilidad de uso.

* **Métodos abreviados de inicio rápido para los canales SMS, Push, In-App y Codebase en las plantillas de contenido**: el botón **Más acciones** de la lista Plantillas de contenido ahora proporciona métodos abreviados adicionales específicos del canal. En el caso de las plantillas SMS, edite rápidamente el mensaje o compruebe el recuento o los segmentos de caracteres. En las plantillas push, edite el título, el cuerpo o los medios. Para las plantillas en la aplicación, edite el encabezado del mensaje, el cuerpo del mensaje o la URL de medios. Para las plantillas de canal de Codebase, edite el código directamente. Estos métodos abreviados amplían los métodos abreviados de inicio rápido del canal de correo electrónico que ya están disponibles. <!-- Documentation link: TBD -->
