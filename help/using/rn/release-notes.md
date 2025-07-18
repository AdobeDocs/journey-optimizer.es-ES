---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: a587b8754e94781b7735f3d7d5abb9b9767a74a5
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 98%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.


## Últimas actualizaciones {#latest-updates}

### Cambio en las condiciones del recorrido {#ee-change@}

A partir del 8 de julio, en las nuevas organizaciones de clientes, la creación de expresiones mediante eventos de experiencia ya no se admite en el editor de expresiones utilizado en las condiciones de recorrido. Como resultado, no se pueden usar eventos de experiencia en la [fuente de datos de Experience Platform](../datasource/adobe-experience-platform-data-source.md) para crear expresiones. [Aquí](../building-journeys/exp-event-lookup.md) encontrará referencias a enfoques alternativos y prácticas recomendadas para crear expresiones y lógicas con eventos de experiencia.

No hay cambios en la forma de acceder a los datos de evento de contexto de recorrido en los recorridos unitarios. En los editores de expresiones y personalización, los usuarios pueden seguir accediendo a los datos pasados con el evento de recorrido inicial.

Obtenga más información [en estas preguntas frecuentes](../building-journeys/exp-event-lookup.md#faq-ee).


## Notas de la versión de junio de 2025 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Fecha de lanzamiento**: 18 de junio de 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nuevas funciones {#25-06-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Conjuntos de datos de Adobe Experience Platform en las tomas de decisiones (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los conjuntos de datos de Adobe Experience Platform, que anteriormente estaban disponibles para la personalización, ahora se pueden aprovechar para la toma de decisiones. Esto le permite ampliar la definición de los atributos de decisión a datos adicionales en conjuntos de datos para actualizaciones masivas que cambian periódicamente sin tener que actualizar manualmente los atributos de uno en uno. Por ejemplo, disponibilidad, tiempos de espera, etc.</p>
<p>Esta funcionalidad está actualmente disponible para todos los clientes en beta pública. Póngase en contacto con el representante de su cuenta si desea tener acceso.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/aep-data-exd.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 20 de junio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mensajería RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La mensajería de servicios de comunicación enriquecida (RCS) ahora es compatible con Journey Optimizer, lo que permite las siguientes funciones de mensajería mejoradas sujetas a la compatibilidad del proveedor y el operador:</p>
<ul>
<li>Compatibilidad con remitentes de marca y verificados: envía mensajes utilizando perfiles comerciales verificados con elementos de promoción de la marca (logotipo, nombre del remitente, etc.).</li>
<li>Información sobre el envío de mensajes: se reciben informes de envío detallados que incluyen actualizaciones del estado del mensaje (por ejemplo, enviado, entregado, leído).</li>
<li>Seguimiento de vínculos: incrusta y rastrea direcciones URL en mensajes RCS para el análisis de participación.</li>
<li>Reserva de SMS: recurre automáticamente a los SMS cuando el dispositivo del perfil no sea compatible con RCS o no se pueda acceder temporalmente mediante RCS.</li>
<li>Composición básica de mensajes: envía mensajes RCS basados en texto con medios opcionales y elementos enriquecidos, según la compatibilidad del proveedor.</li>
</ul>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campos de formulario en el contenido de la experiencia basada en código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir los campos editables específicos en las plantillas de contenido JSON o HTML que permitan a los usuarios no técnicos editar fácilmente el contenido en una vista de formulario dentro de la creación del canal de la experiencia basada en código, sin necesidad de manipular ningún código.<br />Más que eso, al definir las plantillas de contenido de la experiencia basada en código, ahora puede insertar directivas de decisión en la plantilla, lo que aumenta la reutilización y facilidad de uso.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Para obtener más información, consulte la <a href="../code-based/code-based-form-fields.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Actividad de decisión de contenido en los recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede incluir ofertas personalizadas en los recorridos mediante una actividad de decisión de contenido específica en el lienzo y utilizarlas en actividades de recorrido, incluidas las condiciones y las acciones personalizadas.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una futura versión.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/content-decision.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ensayo del recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El ensayo del recorrido es un modo especial de publicación de recorrido en Adobe Journey Optimizer que permite a los profesionales del recorrido probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar la información de perfil. Esta función ayuda a los profesionales del recorrido a confiar en el diseño del recorrido y en la segmentación del público antes de publicarlo en directo.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una futura versión.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-dry-run.md">documentación detallada</a>.</p>

</td>
</tr>
</tbody>
</table>

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
<img src="assets/do-not-localize/PauseResume.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una futura versión.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-pause.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Escalar el ganador de la experimentación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Escalar el ganador de la experimentación permite desplegar automática o manualmente la variación ganadora de un experimento para todo el público. Esta función garantiza que, una vez que se identifique al que tenga el mayor rendimiento, pueda maximizar su alcance y eficacia sin una supervisión manual constante.</p>
<p>Para obtener más información, consulte la <a href="../content-management/content-experiment.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 2 de junio de 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflicto y priorización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ahora ofrece varias herramientas para la administración de conflictos y la priorización - antes disponibles solo para organizaciones de acceso limitado (LA) que ahora están disponibles de forma general (GA).</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, se han introducido las siguientes mejoras:</p>
<ul>
<li>Compatibilidad ampliada: las herramientas de administración de conflictos ahora admiten tanto los recorridos unitarios como los recorridos de calificación de público, además de los recorridos de público de lectura.</li>
<li>Solución de problemas mejorada: ahora hay dos nuevos campos de evento de paso disponibles en el servicio de consultas, lo que le permite analizar por qué se rechazó un perfil de un recorrido o una campaña.</li>
<li>Informes mejorados: ahora los informes indican qué regla específica excluyó un perfil de un recorrido o campaña, lo que proporciona una mayor transparencia e información útil.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de junio de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#25-06-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Conjuntos de reglas de canal**

   * **Ventana de duración personalizada** para el límite: ahora hay un nuevo campo **Cada** disponible en la pantalla de configuración de conjuntos de reglas de canal, que le permite aplicar reglas de restricción de frecuencia durante varios días, semanas o meses, según la duración especificada.

   * **Frecuencia de restricción de restablecimiento por hora**: ahora puede aplicar una restricción por hora a los conjuntos de reglas de canal. Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Póngase en contacto con el Servicio de atención al cliente para activarlo.

   * **Duración diaria**: anteriormente disponible en disponibilidad limitada, la restricción de frecuencia “diaria” en los conjuntos de reglas de canal ya está disponible para todos los clientes.

  Para obtener más información, consulte la [documentación detallada](../conflict-prioritization/channel-capping.md).

* **Experiencias basadas en código**

   * Ahora es posible añadir una política de decisión en las plantillas de contenido de la experiencia basada en código, donde se puede utilizar para aprovechar las ofertas en campos de formulario editables. [Más información](../code-based/code-based-form-fields.md)

   * Desde la pantalla de recorrido de la experiencia basada en código o de edición de campaña, ahora puede añadir directamente una política de decisión, sin abrir el editor de personalización. [Más información](../code-based/create-code-based.md#edit-code)

* **Compatibilidad con CSS personalizado en el diseñador de correo electrónico**

  Journey Optimizer ahora le permite añadir CSS personalizado al contenido del correo electrónico directamente en el diseñador de correo electrónico. [Más información](../email/custom-css.md)

* **Nueva navegación con pestañas para las campañas**

  El nuevo patrón de navegación permite un acceso más rápido a la creación de contenido y admite una mayor ampliación de la configuración en todas las campañas. [Más información](../campaigns/create-campaign.md)

* **Toma de decisiones**

   * **Copia y toma de decisiones de zona protegida** (fecha de disponibilidad: 3 de junio de 2025): ahora se pueden copiar objetos de decisiones entre zonas protegidas, lo que agiliza los flujos de trabajo de prueba e implementación. [Más información](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **Compatibilidad con atributos de elementos de decisión para reglas de toma de decisiones** (fecha de disponibilidad: 4 de junio de 2025). Ahora puede aprovechar los atributos de elementos de decisión para crear reglas de toma de decisiones. [Más información](../experience-decisioning/rules.md#create)

* **Actualización de la API de ejecución de mensajes interactivos** - Fecha de disponibilidad: 6 de junio de 2025

  La API de ejecución de mensajes interactivos ahora le permite eliminar la programación de la próxima ejecución de campañas. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
