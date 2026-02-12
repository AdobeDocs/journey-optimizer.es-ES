---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b414d330a25a98c11b7417beda4536c54c41fd83
workflow-type: tm+mt
source-wordcount: '1884'
ht-degree: 85%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos.

Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Actualizaciones de febrero de 2026 {#feb-26-updates}

### Nuevas funciones {#feb-26-01-updates-features}

<table>
<thead>
<tr>
<th><strong>Actividad de decisión de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una nueva <strong>actividad de decisión de contenido</strong> en el lienzo de recorrido para la integración de <strong>ofertas personalizadas</strong> directamente en los recorridos de los clientes. Esta actividad le permite entregar contenido basado en decisiones y hacer referencia a esas ofertas en todo el recorrido, en condiciones para crear ramas basadas en la idoneidad, en acciones personalizadas para pasar datos de ofertas a sistemas externos y en otras actividades para crear experiencias de cliente totalmente personalizadas.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/content-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 11 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API de herramientas de migración de autoservicio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Las API de herramientas de migración</strong> ya están disponibles para migrar mediante programación las entidades de Gestión de decisiones a Toma de decisiones, que incluyen:</p>
<ul>
<li>Ámbitos de migración flexibles (zona protegida, nivel de oferta o de decisión)</li>
<li>Análisis y validación de dependencias automatizadas</li>
<li>Compatibilidad con reversiones para migraciones completadas</li>
<li>Informes de migración detallados con asignaciones de objetos</li>
</ul>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/decisioning-migration-api.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitorización de acciones personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Obtenga información más detallada sobre el estado y el rendimiento de sus <strong>puntos finales de acción personalizados</strong> con un nuevo panel de monitorización y datos de eventos de paso de recorrido enriquecidos. Rastree las llamadas, los errores, el rendimiento, los tiempos de respuesta y los tiempos de espera de cola correctos para comprender rápidamente cuándo, dónde y por qué se producen anomalías.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../action/reporting.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede personalizar y optimizar el contenido de sus <strong>mensajes SMS</strong> con <strong>Decisioning</strong>. Utilice puntuaciones de prioridad, fórmulas o modelos de IA para mostrar el mejor contenido a sus clientes.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/create-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 2 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#feb-26-01-updates-improv}

* **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar <strong>fragmentos</strong> a <strong>elementos de decisión</strong> que se pueden aprovechar en campañas de experiencia basadas en código mediante políticas de decisión. Esta mejora, lanzada anteriormente en disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general). [Más información](../experience-decisioning/fragments-decision-policies.md)

  Fecha de disponibilidad: 12 de febrero de 2026.

* **Validación de fragmento de expresión de tipo JSON**: los fragmentos de expresión de tipo JSON ahora se validan sintácticamente al guardarse. Los errores de validación se tratan como advertencias y se muestran como alertas después de guardarlos. [Más información](../content-management/create-fragments.md#content)

  Fecha de disponibilidad: 12 de febrero de 2026.

* **Webhooks de SMS**: ahora se admiten los webhooks en todos los proveedores de SMS. Puede configurar cada webhook en función de su propósito, los webhooks entrantes para capturar los mensajes entrantes y los webhooks de comentarios para recibir confirmaciones de entrega, actualizaciones de estado y otros eventos relacionados con los mensajes. [Más información](../sms/sms-webhook.md)

  Fecha de disponibilidad: 2 de febrero de 2026.

## Notas de la versión de enero de 2026 {#latest-rn}

<!--**Release date**: January 27-28, 2026-->

Las secciones [Características](#jan-26-01-features) y [Mejoras](#jan-26-01-improv) cubren funcionalidades ya disponibles, mientras que [Próximamente](#jan-26-01-coming-soon) enumera elementos programados para una fecha de disponibilidad posterior.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nuevas funcionalidades {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede personalizar y optimizar el contenido de sus <strong>notificaciones push</strong> con <strong>Decisioning</strong>. Utilice puntuaciones de prioridad, fórmulas o modelos de IA para mostrar el mejor contenido a sus clientes.</p>
<p>Experience Decisioning con notificaciones push requiere una versión específica de Mobile SDK. Antes de implementar esta característica, compruebe <a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">las notas de la versión</a> para identificar la versión requerida y asegúrese de haber actualizado según corresponda. También puede ver todas las versiones de SDK disponibles para su plataforma en <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">esta sección</a>.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/create-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 30 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a las campañas, el canal de <strong>correo directo</strong> ya está disponible en el lienzo del recorrido, lo que le permite incorporar correo directo a los recorridos. Ahora se puede usar el correo directo en <strong>escenarios de recorrido 1:1 y por lotes</strong>, con compatibilidad con la configuración de extracción de archivos y la configuración de frecuencia basada en el tiempo.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Para obtener más información, consulte la <a href="../direct-mail/get-started-direct-mail.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: viernes, 29 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Horas tranquilas (exclusiones basadas en el tiempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Las horas tranquilas</strong> le permiten definir exclusiones basadas en el tiempo para los canales de correo electrónico, SMS, push y WhatsApp. Garantizan que no se envíen mensajes durante períodos de tiempo específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento. Puede aplicar horas tranquilas a través de <strong>conjuntos de reglas</strong>, que se pueden asignar a acciones individuales en campañas o recorridos para un control preciso.</p>
<p>Esta función, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, la función ahora incluye la posibilidad de que el cliente ponga en cola una acción de campaña hasta que se completen las horas tranquilas y también de previsualizar la regla de horas silenciosas activada.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/quiet-hours.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: viernes, 29 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportación de mensajes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una nueva funcionalidad <strong>Exportación de mensajes</strong> para canales de correo electrónico y SMS. Esta función le permite exportar automáticamente el contenido de los mensajes enviados a un conjunto de datos de Experience Platform dedicado, lo que le permite:</p>
<ul>
<li>Cumplir los requisitos de cumplimiento normativo (como HIPAA)</li>
<li>Archivar mensajes para reclamaciones legales y consultas del servicio de atención al cliente</li>
<li>Conservar copias del contenido personalizado enviado a particulares</li>
</ul>
<p>Los registros se conservan en el conjunto de datos de exportación de mensajes de AJO durante 7 días naturales a partir de la ingesta. Durante este período de retención, puede exportarlas a su propio almacenamiento a través de destinos de Experience Platform. La característica se habilita a nivel de configuración de canal, lo que le proporciona <strong>control granular</strong> sobre los mensajes que se exportan.</p>
<p>Esta funcionalidad solo está disponible para el canal de correo electrónico y SMS, para organizaciones que han adquirido la oferta de complemento de Exportación de mensajes. Para obtener más información, contacte con su representante de Adobe.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Para obtener más información, consulte la <a href="../configuration/message-export.md#message-export">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 28 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo en campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El canal de correo directo ya está disponible para campañas orquestadas. La <strong>actividad de correo directo</strong> facilita el envío de correo directo dentro de la campaña orquestada, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de generación del <strong>archivo de extracción</strong> requerido por los proveedores de correo directo. Puede combinar actividades de canal en el lienzo de la campaña orquestada para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Para obtener más información, consulte la <a href="../orchestrated/activities/channels.md#channel">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 28 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: creación de un recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent ahora ofrece funcionalidades de creación, lo que permite a los usuarios de Journey Optimizer crear y configurar recorridos de marketing a través de una <strong>interfaz en lenguaje natural</strong>. Con estas nuevas habilidades, los profesionales pueden crear recorridos rápidamente con solo describir sus necesidades en <strong>indicaciones de conversación</strong>. Esta innovación optimiza el proceso de creación de recorridos, lo que permite a los especialistas en marketing centrarse en la estrategia en lugar de en la configuración técnica.</p>
<p>Para obtener más información, consulte la <a href="../start/ai-features.md#journey-agent">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 12 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API de recuperación de campaña de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible una nueva API de Journey Optimizer, que le permite recuperar e inspeccionar mediante programación <strong>datos relacionados</strong> con la campaña, como detalles, versiones y configuraciones.</p>
<p>Para obtener más información, consulte la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas del diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar rápidamente <strong>temas aprobados anteriormente</strong> para garantizar la <strong>coherencia de marca</strong> en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir de forma independiente correos electrónicos de alta calidad, mientras que se reduce la dependencia en los equipos de diseño.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Esta funcionalidad, que se publicó anteriormente en la versión Beta, ya está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 5 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-26-01-improv}

#### IA

* **Comprobaciones de calidad del contenido del Asistente de IA**: además de la alineación de marca, ahora puede evaluar la <strong>calidad del contenido</strong> general para descubrir posibles problemas con la <strong>legibilidad</strong>, la coherencia y la eficacia, independientemente de las directrices de marca. Estas comprobaciones automatizadas ayudan a identificar mensajes poco claros, tonos incoherentes o lagunas estructurales. [Más información](../content-management/brands-score.md#validate-quality).

  [Descubra esta función en vídeo](https://video.tv.adobe.com/v/3470549/?captions=spa&learn=on).

#### Recorridos

* **Combinar acciones de mensajes nativas y de Adobe Campaign**: Journey Optimizer ahora le permite combinar acciones de mensajes de <strong>las versiones 7 y 8 de Adobe Campaign</strong> con <strong>acciones de canales nativos</strong> en el mismo recorrido. [Más información](../building-journeys/using-adobe-campaign-v7-v8.md)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

* **Carga útil de respuesta de error de acción personalizada**: ahora puede definir una <strong>carga útil de respuesta de error</strong> opcional para las acciones personalizadas. Cuando falla una llamada, la carga útil del error se expone en el contexto de recorrido (bajo el nodo errorResponse de la acción) y está disponible en la <strong>rama de tiempo de espera/error</strong>, junto con `jo_status_code`, para admitir una lógica de reserva y una depuración más completas. [Más información](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

* **Validación del tamaño de la carga útil de Journey en recorridos**: Journey Optimizer ahora valida <strong>los tamaños de carga útil</strong> para ayudar a garantizar un rendimiento óptimo y la estabilidad del sistema. Al crear o publicar recorridos, recibe <strong>advertencias y errores</strong> si el tamaño de la carga útil se acerca o supera los límites recomendados, junto con instrucciones procesables para optimizar la configuración de la recorrido. Esta validación proactiva le ayuda a identificar problemas potenciales de forma temprana y a mantener el rendimiento del recorrido. [Más información](../start/guardrails.md#journey-payload-size)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.


* **Alertas de recorrido**: hay nuevas <strong>alertas preconfiguradas</strong> disponibles para los recorridos.
   * <strong>Se ha superado la tasa de descarte de perfiles</strong>: la proporción de descartes de perfil para los perfiles introducidos durante los últimos 5 minutos ha superado el límite
   * <strong>Se ha superado la tasa de errores de acciones personalizadas</strong>: la proporción de errores de acciones personalizadas respecto a las llamadas HTTP correctas durante los últimos 5 minutos ha superado el límite
   * <strong>Se ha superado la tasa de errores de perfiles</strong>: la proporción de perfiles erróneos respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el límite

  Para obtener más información, consulte la [documentación detallada](../reports/alerts.md).

  Fecha de disponibilidad: 14 de octubre de 2025.

#### Campañas orquestadas

* **Herencia de etiquetas de uso de datos para públicos**: las etiquetas aplicadas en Adobe Experience Platform ahora se transfieren automáticamente al guardar <strong>público</strong> en campañas orquestadas, lo que reduce el <strong>etiquetado DULE</strong> manual. [Más información](../orchestrated/activities/save-audience.md)

* **Filtros predefinidos con parámetros**: ahora puede crear <strong>filtros predefinidos</strong> con <strong>parámetros</strong> en campañas orquestadas para reglas reutilizables y editables. [Más información](../orchestrated/predefined-filters.md)

* **Seleccionar atributos y copiar valores de distribución**: ahora puede <strong>seleccionar o copiar valores</strong> directamente desde la vista <strong>distribución de valores</strong> en campañas orquestadas. [Más información](../orchestrated/build-query.md)

* **Confirmación de mensaje antes del envío**: se ha habilitado un <strong>paso de confirmación</strong> de forma predeterminada antes de enviar campañas orquestadas para reducir los envíos accidentales. [Más información](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtros de redireccionamiento predefinidos**: para admitir una resegmentación más sencilla en los casos de uso de campañas orquestadas, esta versión introduce los nuevos <strong>filtros de comentarios de campaña</strong>. Estos filtros le permiten segmentar público destinatario directamente según la <strong>participación del mensaje</strong>, como enviado, abierto solamente, abierto o hecho clic, o abierto y hecho clic, y seleccionar la campaña específica o la campaña en transición que desea redireccionar. [Más información](../orchestrated/retarget.md)

* **Compatibilidad con control de tarifa**: las campañas orquestadas ahora admiten <strong>control de tarifa</strong> para ayudarle a acelerar los envíos y alinearse con las <strong>restricciones de volumen</strong>. [Más información](../orchestrated/activities/channels.md#rate-control)

* **Botón de reinicio**: las campañas orquestadas ahora incluyen un <strong>botón de reinicio</strong> para que pueda <strong>reiniciar ejecuciones</strong> cuando sea necesario antes de publicar la campaña. [Más información](../orchestrated/start-monitor-campaigns.md)

* **Compatibilidad con metadatos generados por el usuario**: <strong>la función de ayuda executionMetadata</strong> ya está disponible en el editor de personalización para campañas orquestadas, lo que le permite adjuntar información contextual a cualquier acción nativa y almacenarla en un conjunto de datos para exportarla a sistemas externos. [Más información](../personalization/functions/helpers.md#execution-metadata)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

* **Revertir campañas en vivo al estado de borrador**: ahora puede revertir las campañas orquestadas en vivo al estado de borrador cuando encuentren errores de ejecución o cuando necesite modificar las campañas programadas antes de que comiencen a ejecutarse. Esta opción está disponible hasta que se envía el primer mensaje. [Más información](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Campañas

* **Programar campaña usando la zona horaria del perfil**. La programación de campañas ahora puede usar la <strong>zona horaria</strong> de cada perfil para enviar mensajes a la hora local prevista. [Más información](../campaigns/campaign-schedule.md)

  **Nota**: esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

#### Permisos

* **Evitar la autoaprobación para recorridos y campañas**: se ha añadido una opción al crear o establecer <strong>directivas de aprobación</strong> para evitar que los creadores de recorridos o campañas <strong>aprueben sus propios objetos</strong>. [Más información](../test-approve/approval-policies.md)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

<!--
## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

### Features


<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both <strong>mobile and desktop browsers</strong>, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Previously released in Beta, this capability will be available to all environments (General Availability).</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

### Improvements


-->