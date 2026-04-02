---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión 2026
description: Notas de la versión de Journey Optimizer 2026
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: 559feb1d45abb287d5f4b0e2abae8f2ec663713b
workflow-type: tm+mt
source-wordcount: '2525'
ht-degree: 64%

---

# Notas de la versión de 2026 {#release-notes-2026}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzadas en 2026.



## Notas de la versión de febrero de 2026 {#feb-26-01-rn}

### Nuevas funciones {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>arbitraje de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede usar <strong>fórmulas de clasificación</strong> para aumentar automáticamente las puntuaciones de prioridad de recorridos en función de los atributos de perfil del cliente y los factores contextuales, asegurándose de que los clientes ingresen los recorridos más relevantes.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/journey-ranking-formulas.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: miércoles, 24 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de acción en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer admite una nueva actividad <strong>Action</strong> genérica que permite configurar tanto acciones únicas como grupos de acciones entrantes de varias acciones, lo que permite una configuración de acciones optimizada dentro del lienzo de recorrido. En particular, esta nueva función permite lo siguiente:</p>
<ul>
<li>Una configuración de acción nativa simplificada dentro del lienzo de recorrido.</li>
<li>La capacidad para crear grupos de acciones entrantes de varias acciones.</li>
<li>Capacidad de añadir optimización a cualquier acción de canal integrada.</li>
<li>La capacidad de añadir opciones de experimentación y multilingües a cualquier acción.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-action.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: sábado, 20 de febrero de 2026</p>
<p><strong>Nota:</strong> Ahora se puede acceder a todos los canales nativos a través de la actividad recorrido de acción. Las actividades heredadas del canal nativo quedarán obsoletas con la versión de marzo. Los recorridos existentes que incluyen acciones heredadas seguirán funcionando tal cual; no se requiere ninguna migración.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envío de ondas de mensajes salientes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede programar mensajes de campañas de Journey Optimizer o recorridos para que se entreguen en lotes controlados a lo largo del tiempo.</p>
<p>El envío de ondas ofrece las siguientes ventajas:</p>
<ul>
<li>Mejor capacidad de entrega: la propagación envía con el tiempo para ayudar a mantener una sólida reputación del remitente y reducir el riesgo de ser marcado como correo no deseado.</li>
<li>Control de carga: evite saturar los sistemas descendentes (por ejemplo, centros de llamadas, páginas de aterrizaje) limitando la cantidad de mensajes que se emiten a la vez.</li>
<li>Casos de uso de gran volumen y sensibles al tiempo: adecuados para audiencias grandes o cuando necesite controlar el tiempo (por ejemplo, capacidad del centro de llamadas, ampliación u ofertas con límite de tiempo).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>En <strong>campañas</strong>, esta capacidad está disponible para todos los entornos (disponibilidad general). Para obtener más información, consulte la <a href="../campaigns/send-using-waves.md">documentación detallada</a>.</p>

<p>En <strong>recorridos</strong>, esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada): para obtener acceso, póngase en contacto con su representante de Adobe. Para obtener más información, consulte la <a href="../building-journeys/send-using-waves.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: viernes, 19 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Migrar subdominios a delegación personalizada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede migrar subdominios utilizando el modo de delegación CNAME a delegación personalizada directamente desde la interfaz, de modo que pueda cumplir políticas de seguridad más estrictas en línea con las directrices de su empresa sin volver a crear configuraciones de canal.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../configuration/custom-subdomain-migration.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: viernes, 19 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de notificaciones push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora admite <strong>notificaciones push web</strong>, lo que expande el canal push más allá del móvil. Puede enviar notificaciones sin problemas a <strong>exploradores móviles y de escritorio</strong>, lo que permite llegar a los clientes directamente a través de sus dispositivos sin necesidad de una aplicación. Esta mejora le permite atraer a los usuarios con mensajes personalizados y oportunos en tiempo real, aprovechando los mismos flujos de trabajo de creación y las mismas funcionalidades de segmentación ya disponibles para las notificaciones push móviles.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Esta funcionalidad, lanzada anteriormente en Beta, estará disponible para todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../push/push-configuration-web.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: sábado, 13 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de decisión de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una nueva <strong>actividad de decisión de contenido</strong> en el lienzo de recorrido para integrar ofertas personalizadas directamente en las recorridos de los clientes. Esta actividad le permite entregar contenido basado en decisiones y hacer referencia a esas ofertas en todo el recorrido: en condiciones para crear ramas basadas en la idoneidad, en acciones personalizadas para pasar datos de ofertas a sistemas externos y en otras actividades para crear experiencias de cliente totalmente personalizadas.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/content-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: miércoles, 10 de febrero de 2026</p>
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
<p>Las API de herramientas de migración ya están disponibles para migrar mediante programación las entidades de <strong>Administración de decisiones</strong> a <strong>Toma de decisiones</strong>, que incluyen:</p>
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
<p>Obtenga información más detallada de insight sobre el estado y el rendimiento de los extremos de las acciones personalizadas con un nuevo tablero de monitorización y datos de eventos de pasos de recorrido enriquecidos. Rastree las llamadas, los errores, el rendimiento, los tiempos de respuesta y los tiempos de espera de cola correctos para comprender rápidamente cuándo, dónde y por qué se producen anomalías.</p>
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
<p>Ahora puede personalizar y optimizar el contenido de sus mensajes SMS con Decisioning. Utilice puntuaciones de prioridad, fórmulas o modelos de IA para mostrar el mejor contenido a sus clientes.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/create-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 2 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#feb-26-01-improv}

A continuación, se describen las mejoras incluidas en esta versión.

#### Configuración

* **Uso de eventos de experiencia en expresiones de recorrido**: a partir del 1 de abril de 2026, el uso de atributos de eventos de experiencia en expresiones de recorrido dejará de ser compatible con las organizaciones que no hayan utilizado esta capacidad en los últimos 90 días. Esta capacidad ya no está disponible para las nuevas organizaciones de clientes desde el 8 de julio de 2025. Para ver alternativas, consulte [Búsqueda de eventos de experiencia en recorrido](../building-journeys/exp-event-lookup.md).

#### Administración de contenido

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **Usar temáticas para convertir imágenes en plantillas de correo electrónico**: al convertir una imagen en una plantilla de correo electrónico en Journey Optimizer, ahora puede usar una temática como entrada para que el HTML generado siga los parámetros de su marca. El estilo, como el color de fondo, el color del botón, las fuentes, el interlineado, los márgenes y el relleno, se aplica automáticamente, lo que reduce el trabajo de diseño manual y proporciona una plantilla lista para usar con ediciones mínimas. [Más información](../content-management/image-to-html.md)

  Fecha de disponibilidad: 17 de febrero de 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### Diseñador de correo electrónico

* **Sangría de texto**: ahora puede aplicar sangría izquierda personalizable a la primera línea de párrafos de los componentes de texto directamente desde el panel de propiedades. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Esto mejora la legibilidad del contenido de formato largo, como editoriales y artículos. [Más información](../email/get-started-email-style.md)

  Fecha de disponibilidad: 18 de febrero de 2026.

#### Toma de decisiones

* **Compatibilidad de entrada de Edge con el uso de datos de Adobe Experience Platform en Decisioning**. El uso de datos de Adobe Experience Platform en Decisioning ahora admite casos de uso de entrada perimetral, además de acciones personalizadas y de correo electrónico en recorrido. [Más información](../experience-decisioning/aep-data-exd.md)

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

* **Vista previa de decisiones en el canal de experiencia basado en código**: ahora puede obtener una vista previa de los elementos de decisión al configurar Decisioning con el canal de experiencia basada en código. La vista previa está disponible directamente en la interfaz de creación antes de lanzarse. [Más información](../code-based/test-code-based.md#preview-code-based)

  Fecha de disponibilidad: jueves, 18 de febrero de 2026

<!--THIS WAS FINALLY NOT RELEASED IN FEBRUARY

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach fragments to decision items which can be leveraged in code-based experience campaigns through decision policies. [Read more](../experience-decisioning/fragments-decision-policies.md)

  Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.-->

#### Personalización

* **Asistente para metadatos de ejecución** - La función de ayuda `executionMetadata` ya está disponible para todos los clientes de Journey Optimizer. Utilícela para anexar dinámicamente información contextual a cualquier acción nativa y capturarla en un conjunto de datos para exportarla a sistemas externos. [Más información](../personalization/functions/helpers.md#execution-metadata)

  Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).

  Fecha de disponibilidad: 20 de febrero de 2026.

#### SMS

* **Webhooks de SMS**: ahora se admiten los webhooks en todos los proveedores de SMS. Puede configurar cada webhook en función de su objetivo: Los webhooks entrantes capturan los mensajes entrantes y los webhooks de comentarios para recibir las confirmaciones de entrega, las actualizaciones de estado y otros eventos relacionados con los mensajes. [Más información](../sms/sms-webhook.md)

  Fecha de disponibilidad: 2 de febrero de 2026.



## Notas de la versión de enero de 2026 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### Nuevas funciones {#jan-26-01-features}


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

  [Descubra esta función en vídeo](https://video.tv.adobe.com/v/3470544/?learn=on).

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
