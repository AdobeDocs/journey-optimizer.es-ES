---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9d58e16bb6717c4aeccede84b1ccc5b4e777fad8
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 46%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos.

Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales.  En la sección [Últimas actualizaciones](#latest-updates) dedicada se destacan las nuevas funcionalidades y mejoras que se implementan en la producción, por lo que siempre se le informa de todos los cambios en tiempo real. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](#releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

<!-- DOCAC-13676
## Latest updates {#latest-updates}

New capabilities and improvements released recently are listed below, with their availability date.

### New capabilities {#latest-features}

<table>
<thead>
<tr>
<th><strong>Image to HTML converter</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The image to HTML converter is an AI-powered feature that converts static image designs into fully customizable, modular HTML email content templates. This no-code tool enables marketers to transform visual designs into responsive, editable email templates without requiring technical expertise—perfect for platform migration, rapid template creation, and building reusable template libraries.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../email/image-to-html.md">detailed documentation</a>.</p>
<p>Availability date: November 3, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

## Notas de la versión de octubre de 2025 {#oct-25-10-rn}

**Fecha de lanzamiento**: jueves, 22 de octubre de 2025

### Nuevas funciones {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Monitorización y creación de informes de acciones personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta capacidad proporciona una mejor visibilidad del estado y el rendimiento de los extremos de acciones personalizadas. Un nuevo panel de monitorización de acciones personalizadas y los campos correspondientes en el conjunto de datos de eventos de pasos de recorrido le ayudarán a monitorizar las llamadas, los errores, el rendimiento, el tiempo de respuesta y el tiempo de espera de cola correctos para los extremos de acciones personalizadas. Ahora puede comprender rápidamente cuándo, dónde y por qué se produce una situación anómala en una acción personalizada.</p>
<p>Actualmente, esta capacidad está en disponibilidad limitada para los clientes de.</p>
<p>Para obtener más información, consulte la <a href="../action/reporting.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: miércoles, 28 de octubre de 2025</p>
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
<p>Cree, diseñe y administre formularios personalizados adaptados a sus necesidades en función de un conjunto de datos específico. A continuación, puede utilizar estos formularios en páginas de aterrizaje para añadir los atributos de perfil que elija al conjunto de datos definido para cada formulario.</p>
<p>Actualmente, esta capacidad está disponible de forma limitada para clientes de Estados Unidos y Australia. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Para obtener más información, consulte la <a href="../landing-pages/lp-forms.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: viernes, 23 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Horas tranquilas/Exclusiones basadas en el tiempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las horas tranquilas le permiten definir exclusiones basadas en el tiempo para los canales de correo electrónico, SMS, push y WhatsApp. Garantizan que no se envíen mensajes durante períodos de tiempo específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento.</p>
<p>Puede aplicar horas tranquilas a través de conjuntos de reglas, que se pueden asignar a acciones individuales en campañas o recorridos para un control preciso.</p>
<p>Actualmente, las reglas de horario silencioso solo están disponibles para un conjunto de organizaciones (disponibilidad limitada). Para que se añada a la lista de espera, póngase en contacto con su representante de Adobe.</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/quiet-hours.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 22 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p>For more information, refer to the <a href="../start/get-started-sources.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Mensajería de alto rendimiento para campañas de correo electrónico activadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay disponible un nuevo modo de mensajería transaccional de alto rendimiento en campañas activadas por API. Este modo está diseñado para mensajes transaccionales a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Este modo también admite mensajes transaccionales sin hacer referencia ni crear perfiles de clientes, como cierre de compra de invitado, confirmación de pedido, restablecimientos de contraseña, notificaciones de seguridad y otras notificaciones de servicio/operacionales.</p>
<p>Esta funcionalidad solo está disponible para el canal de correo electrónico, para organizaciones que han adquirido la oferta del complemento Mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información.</p>
<p>Para obtener más información, consulte la <a href="../campaigns/api-triggered-high-throughput.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 22 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reglas de segmentación reutilizables</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para ahorrarle tiempo y esfuerzo, Journey Optimizer ahora le permite crear reglas reutilizables a partir de un menú de interfaz de usuario dedicado y aprovecharlas al crear objetivos, ya sea como parte de la optimización de contenido en una campaña o un recorrido, en la actividad Optimizar recorrido.</p>
<p>Actualmente, las reglas de segmentación están en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso. Tenga en cuenta que esta funcionalidad solo está disponible para las organizaciones que han adquirido la oferta de complementos de Decisioning. Se implementará progresivamente para todos los clientes.</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>Para obtener más información, consulte la <a href="../experience-decisioning/rules.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 22 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevas alertas de Recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay nuevas alertas preconfiguradas disponibles para controlar la ejecución del recorrido:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Tasa de descartes de perfiles superada</a>: la proporción de descartes de perfiles respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el umbral.</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Tasa de errores de acción personalizada superada</a>: la proporción de errores de acción personalizada respecto a las llamadas HTTP correctas durante los últimos 5 minutos ha superado el umbral.</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Tasa de error de perfil superada</a>: la proporción de perfiles en error respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el umbral.</li></ul> <p>Puede modificar los valores de umbral y suscribirse a alertas de nivel de recorrido individual o global.</p>
<p>Para obtener más información, consulte la <a href="../reports/alerts.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: miércoles, 14 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ayudante de metadatos de ejecución</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay una nueva función de ayuda executionMetadata disponible en el editor de personalización. Permite anexar información contextual a cualquier acción nativa y capturarla en un conjunto de datos para exportarla a sistemas externos.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>Para obtener más información, consulte la <a href="../personalization/functions/helpers.md#execution-metadata">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: martes, 13 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator con el agente de experimentación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator ahora incluye Experimentation Agent, una herramienta conversacional con tecnología de IA que le permite interactuar con sus experimentos, perspectivas y oportunidades. Mejora la experiencia de Journey Optimizer Experimentation Accelerator, lo que le ayuda a ejecutar experimentos de forma más eficiente, descubrir qué funciona y descubrir dónde optimizar a continuación.</p>
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=es" target="_blank">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: sábado, 10 de octubre de 2025</p>
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
<li>Para cualquier tamaño o volumen adicional, puede comprar un complemento de archivos PDF adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.</li>
</ul>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/pdf-attachments.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 30 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API pública para recuperar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una nueva API de Journey Optimizer para recuperar recorridos y sus objetos asociados, como campañas y superficies.</p>
<p>Para obtener más información, consulte la <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 25 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Mejoras {#updates-improvements}

<!--Availability date: October 22, 2025-->

**Campo de ejecución para el canal de WhatsApp**

Además de correo electrónico y SMS, puede saber cómo actualizar el campo de ejecución predeterminado para sus envíos de WhatsApp en el nivel de zona protegida. También es posible anular el campo de ejecución definido globalmente cambiándolo en los parámetros avanzados de la actividad de recorrido de WhatsApp o en la configuración del canal de WhatsApp. [Más información](../configuration/primary-email-addresses.md)

Fecha de disponibilidad: jueves, 22 de octubre de 2025

**Compatibilidad con atributos personalizados para la dirección Mailto (cancelar la suscripción)**

Con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer los puntos finales personalizados externos definiendo su propio vínculo para cancelar la suscripción con un solo clic y una dirección de correo electrónico de cancelación de suscripción personalizada en la configuración del correo electrónico. Cuando los destinatarios hacen clic en el vínculo Cancelar la suscripción, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

Para personalizar aún más los puntos finales personalizados, ahora puede definir atributos personalizados que se adjuntarán al evento de consentimiento. [Más información](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esta funcionalidad ya está disponible para la **[!UICONTROL URL de cancelación de suscripción de un solo clic]** desde agosto de 2025 y ahora está disponible para la opción **[!UICONTROL Mailto (cancelar la suscripción)]** en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Fecha de disponibilidad: 6 de octubre de 2025

<!--
### Coming soon {#oct-25-10-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

#### New capabilities {#oct-25-10-soon-features}

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved themes to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p>
</td>
</tr>
</tbody>
</table>

#### Improvements {#oct-25-10-soon-improvements}

**Decisioning in emails through AI models**

You can now use AI models to optimize the best content in your email through the use of Decisioning. For example, this capability allows you to offer the best content based on custom events such as Purchases, Button Clicks, Add to Cart, etc.
-->

<!--
<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

-->
