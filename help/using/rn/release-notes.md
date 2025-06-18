---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 024356ca30728611d1d32ba72172711e4714b64c
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 46%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.


## Notas de la versión de junio de 2025 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Fecha de lanzamiento**: jueves, 18 de junio de 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nuevas funciones {#25-06-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.


<table>
<thead>
<tr>
<th><strong>Mensajería RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La mensajería de servicios de comunicación enriquecidos (RCS) ahora es compatible con Journey Optimizer, lo que permite las siguientes funciones de mensajería mejoradas sujetas a la compatibilidad del proveedor y el operador:</p>
<ul>
<li>Compatibilidad con remitentes de marca y verificados: envía mensajes utilizando perfiles comerciales verificados con elementos de marca (logotipo, nombre del remitente, etc.).</li>
<li>Perspectivas de entrega de mensajes: reciba informes de entrega detallados que incluyan actualizaciones del estado del mensaje (por ejemplo, enviado, entregado, leído).</li>
<li>Seguimiento de vínculos: incruste y rastree direcciones URL en mensajes RCS para el análisis de participación.</li>
<li>Volver a SMS: volver automáticamente a SMS cuando el dispositivo del perfil no admite RCS o no se puede acceder a él temporalmente mediante RCS.</li>
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
<th><strong>Campos de formulario en contenido de experiencia basado en código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir campos editables específicos en plantillas de contenido JSON o HTML que permitan a los usuarios no técnicos editar fácilmente el contenido en una vista de formulario dentro de la creación del canal de experiencia basado en código, sin necesidad de manipular ningún código.<br />Más que eso, al definir las plantillas de contenido de experiencia basadas en código, ahora puede insertar directivas de decisión en la plantilla, lo que aumenta la reutilización y facilidad de uso.</p>
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
<th><strong>Actividad de decisión de contenido en recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede incluir ofertas personalizadas en los recorridos a través de una actividad de Content Decisioning específica en el lienzo de recorrido y utilizarlas en actividades de recorrido, incluidas condiciones y acciones personalizadas.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.</p>
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
<p>Recorrido Dry run es un modo especial de publicación de recorrido en Adobe Journey Optimizer que permite a los profesionales del recorrido probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar información de perfil. Esta función ayuda a los profesionales del recorrido a confiar en el diseño del recorrido y la segmentación de audiencia antes de publicarla en directo.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.</p>
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
<p>Ahora puede pausar y reanudar las recorridos. Esta capacidad proporciona a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando está en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda la recorrido.</p>
<p>Puede pausar y reanudar solo un recorrido, o realizar pausas masivas y reanudar operaciones en un grupo de recorridos.</p>
<p>Además, puede aplicar filtros globales a recorridos en pausa para excluir perfiles en función de sus atributos.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.</p>
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

<!--* **Channel rule sets**

  * **Custom duration window** for capping -  A new **Repeat Count** field is now available in the channel rule sets configuration screen, allowing you to apply frequency capping rules over multiple days, weeks, or months, depending on the specified duration.

  * **Hourly duration** - You can now apply capping on an hourly basis for channel rule sets.    -->

* **Experiencias basadas en código**

   * La adición de una política de decisión ya está disponible en plantillas de contenido de experiencia basadas en código, donde se puede utilizar para aprovechar ofertas en campos de formulario editables. [Más información](../code-based/code-based-form-fields.md)

   * Desde la pantalla de edición de campaña o recorrido de experiencias basado en código, ahora puede añadir directamente una política de decisión, sin abrir el editor de personalización. [Más información](../code-based/create-code-based.md#edit-code)

* **Compatibilidad con CSS personalizado en el Designer de correo electrónico**

  Journey Optimizer ahora le permite añadir CSS personalizado al contenido del correo electrónico directamente en el Designer de correo electrónico. [Más información](../email/custom-css.md)

* **Nueva navegación con pestañas para las campañas**

  Un nuevo patrón de navegación permite un acceso más rápido a la creación de contenido y admite una mayor expansión de la configuración entre campañas. [Más información](../campaigns/create-campaign.md)

* **Decisiones**, fecha de disponibilidad: 3 de junio de 2025

  Ahora, los objetos de decisiones se pueden copiar entre zonas protegidas, lo que optimiza los flujos de trabajo de prueba e implementación. [Más información](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Compatibilidad con atributos de elementos de decisión para reglas de toma de decisiones** - Fecha de disponibilidad: 4 de junio de 2025

  Ahora puede aprovechar los atributos de elementos de decisión para crear reglas de toma de decisiones. [Más información](../experience-decisioning/rules.md#create)

* **Actualización de la API de ejecución de mensajes interactivos** - Fecha de disponibilidad: 6 de junio de 2025

  La API de ejecución de mensajes interactivos ahora le permite eliminar la programación de la próxima ejecución de campañas. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
