---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: bfd0c7c976146c0cccdb51a720c27653b3e5a7b4
workflow-type: tm+mt
source-wordcount: '3104'
ht-degree: 55%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Notas de la versión de octubre de 2024 {#24-10-rn}

>[!CAUTION]
>
>**Las notas de la versión preliminar que se indican a continuación están sujetas a cambios sin previo aviso hasta la fecha del lanzamiento de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en la fecha de la versión.

**Fecha de la versión**: 29 y 30 de octubre de 2024

### Nuevas funciones {#24-10-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<table>
<thead>
<tr>
<th><strong>Bloqueo de contenido de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora permite bloquear contenido en plantillas de correo electrónico, ya sea bloqueando la plantilla completa o estructuras y componentes específicos. Esto le permite evitar ediciones o eliminaciones no intencionadas, lo que le proporciona un mayor control sobre la personalización de las plantillas y mejora la eficacia y fiabilidad de sus campañas de correo electrónico.</p>
<p>Para obtener más información, consulte la <a href="../content-management/content-locking.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalización de la configuración de correo electrónico (disponibilidad general) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para obtener una mayor flexibilidad y control sobre la configuración de correo electrónico, puede definir subdominios dinámicos y parámetros de encabezado personalizados al crear configuraciones de canal de correo electrónico.
</p>
<p>Anteriormente disponible para un conjunto de organizaciones (LA), la personalización de la configuración de correo electrónico ya está disponible para todos los usuarios (GA).</p>
<p>Para obtener más información, consulte la <a href="../email/surface-personalization.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Fecha de disponibilidad: 23 de octubre de 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aprobaciones en recorridos y campañas (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con las políticas de aprobación, ahora puede configurar un proceso de aprobación dentro de Journey Optimizer que permita a los equipos de marketing asegurarse de que las campañas y los recorridos sean revisados y firmados por las partes interesadas correspondientes antes de que se activen.</p>
<p>Antes disponibles para un conjunto de organizaciones (LA), las políticas de aprobación ya están disponibles para todos los usuarios (GA).</p>
<p>Para obtener más información, consulte la <a href="../test-approve/gs-approval.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalización de la configuración de correo electrónico (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir subdominios dinámicos y parámetros de encabezado personalizados al crear configuraciones de canal de correo electrónico para disponer de mayor flexibilidad y control sobre la configuración del correo electrónico.</p><p>El uso de una configuración personalizada en una campaña o un recorrido le permite previsualizar el contenido del correo electrónico para comprobar posibles errores con la configuración dinámica definida.</p>
<p>Anteriormente disponible para un conjunto de organizaciones (LA), la personalización de la configuración de correo electrónico ya está disponible para todos los usuarios (GA).</p>
<p>Para obtener más información, consulte la <a href="../email/surface-personalization.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Prueba del contenido con datos de entrada de ejemplo (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Recorrido Optimizer ahora le permite probar diferentes variantes del contenido del correo electrónico previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo o añadidos manualmente. El sistema detecta automáticamente todos los atributos de perfiles utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.</p>
<p>Actualmente, todos los clientes tienen esta capacidad como una versión beta pública.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Administración de conflictos y prioridades (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En Journey Optimizer, administrar el volumen y el tiempo de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ahora ofrece varias herramientas para la administración de conflictos y la priorización.</p><p><ul><li><b>Límite de frecuencia de Recorrido</b>: Ahora puede crear conjuntos de reglas para aplicarlos a sus recorridos, lo que le permite limitar el número de recorridos para un perfil por día, semana o mes, así como controlar el número de recorridos simultáneos que se ejecutan simultáneamente.</li>
<li><b>Puntuación de prioridad</b>: ahora puede asignar una puntuación de prioridad a una campaña o a un recorrido, de 0 a 100. Un número mayor indica una prioridad mayor. Cuando dos campañas o acciones de recorrido utilizan la misma configuración de canal, Journey Optimizer selecciona la que tiene la puntuación de prioridad más alta. Si las campañas tienen la misma puntuación, se elige la campaña que se haya modificado menos recientemente.</li>
<li><b>Ver conflictos potenciales</b>: El nuevo botón "Ver conflictos potenciales" en recorridos y campañas ahora le permite identificar la superposición con otros recorridos o campañas, como la fecha de inicio, la audiencia de destino o la configuración del canal seleccionado.</li>
<li><b>Arbitraje de Recorridos</b>: esta nueva funcionalidad le permite priorizar los recorridos más importantes para sus clientes. Puede crear una regla para suprimir la entrada en un recorrido de prioridad inferior cuando un cliente cumpla los requisitos para un próximo recorrido de prioridad superior.</li>
<li><b>Límite de frecuencia por tipo de comunicación: </b>Con los conjuntos de reglas, ahora puede establecer reglas granulares por tipo de comunicación (por ejemplo, Ventas, Promocional) para evitar sobrecargar a los clientes con mensajes similares. Puede controlar la frecuencia en varios canales, excluyendo automáticamente los perfiles saturados para garantizar una mejor experiencia del cliente.</li></ul>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Las funciones de administración de conflictos y prioridades están disponibles en Disponibilidad limitada para un grupo selecto de clientes. Tenga en cuenta que estas funciones se implementarán gradualmente para más usuarios en el futuro. Póngase en contacto con el equipo de la cuenta si está interesado en que se le añada a la lista de espera de estas funciones.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modo de edición no visual para el diseñador web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como alternativa al diseñador web de Journey Optimizer, ahora puede agregar modificaciones al sitio web mediante un editor no visual. Permite introducir los cambios manualmente sin abrir las páginas en el editor visual.
Este modo de edición no visual resulta útil si no puede instalar extensiones de explorador como el Asistente visual de Adobe Experience Cloud, necesario para cargar las páginas en el diseñador web.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentación de contenido en recorrido (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer, que ya estaba disponible en las campañas, ahora admite experimentos en los recorridos. Los experimentos son ensayos aleatorios, lo que en el contexto de las pruebas en línea significa que expone a algunos usuarios seleccionados aleatoriamente a una variación determinada de un mensaje y a otro conjunto de usuarios seleccionados aleatoriamente a otra variación o tratamiento. Después de la exposición, puede medir las métricas de resultado que le interesan, como aperturas de correos electrónicos, suscripciones o compras.</p>
<p>Anteriormente disponible para un conjunto de organizaciones (LA), los experimentos en recorridos ya están disponibles para todos los usuarios (GA).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Toma de decisiones (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, disponible anteriormente para un conjunto de organizaciones (LA) y conocida como Experience Decisioning, ya está disponible para todos los usuarios (GA), incluidas las organizaciones que han adquirido las ofertas adicionales de Adobe Healthcare Shield o Privacy and Security Shield.</p><p>Decisioning simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como "elementos de decisión" y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar los elementos de decisión más relevantes a cada individuo. Estos elementos de decisión se integran perfectamente en una amplia gama de superficies entrantes a través del canal de experiencia basado en código.</p>

<p>Para obtener más información, consulte la <a href="../experience-decisioning/gs-experience-decisioning.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mensajes multilingües en recorridos y campañas (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear contenido sin esfuerzo en varios idiomas dentro de una sola campaña o recorrido. Con esta función, puede cambiar entre idiomas al editar su campaña o su recorrido, lo que optimiza todo el proceso de edición y mejora su capacidad para administrar de forma eficaz el contenido multilingüe.</p>
<p>Anteriormente disponibles para un conjunto de organizaciones (LA), los mensajes multilingües ya están disponibles para todos los usuarios (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de Adobe Journey Optimizer y tinta móvil</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede integrar Movable Ink Da Vinci y Adobe Journey Optimizer. Con esta nueva integración puede: </p>
<p><ul><li>Aproveche las potentes capacidades del producto Da Vinci de Movable Ink para ensamblar y personalizar las variaciones de correo electrónico para las campañas por lotes</li>
<li>Acelere los flujos de trabajo de los profesionales para los clientes de Journey Optimizer que utilizan Da Vinci para la creación y AJO para la optimización y el envío</li>
<li>Optimizar los modelos Da Vinci con datos de Adobe.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencia actualizada de creación de informes (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponible desde el 16 de octubre de 2024</p>
<p>La creación de informes de Journey Optimizer ya está disponible de forma general (GA) y ofrece una interoperabilidad mejorada con funciones de Customer Journey Analytics, estandarización de los informes en ambas plataformas y mejora de la coherencia y fiabilidad de los datos. Esta integración perfecta entre Journey Optimizer y Customer Journey Analytics proporciona una visión más clara de las métricas de rendimiento, lo que permite a los usuarios tomar decisiones más informadas.</p>
<p>Con la disponibilidad general, se introducen cuatro nuevas funciones: la capacidad de crear métricas sencillas, crear y publicar audiencias, hacer preguntas específicas mediante Insight Builder y programar informes para que se envíen automáticamente por correo electrónico a los destinatarios clave.</p>
<p>Para obtener más información, consulte la <a href="../reports/report-cja-manage.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: La experiencia actual de creación de informes se eliminará a partir de enero de 2025. Después de esta fecha, la nueva experiencia de creación de informes pasará a ser el estándar. Recomendamos que se familiarice con las nuevas funciones y características para garantizar una transición sin problemas. <a href="../reports/report-gs-cja.md">Aprenda a empezar con la nueva interfaz de creación de informes de Journey Optimizer</a></p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencias basadas en código en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponible desde el 1 de octubre de 2024</p>
<p>Con el canal de experiencia basado en código, Adobe Journey Optimizer le permite realizar personalizaciones y pruebas avanzadas para cualquiera de sus propiedades de entrada, lo que permite ofrecer experiencias adaptadas en diversos puntos de contacto, como aplicaciones web, aplicaciones móviles, aplicaciones de escritorio, consolas de vídeo, servicios conectados a TV, televisores inteligentes, quioscos, cajeros automáticos, dispositivos IoT y mucho más. El canal de experiencia basado en código ya está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../code-based/create-code-based.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencias web en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponible desde el 1 de octubre de 2024</p>
<p>Con el canal web, Adobe Journey Optimizer permite personalizar la experiencia web que ofrece a sus clientes a través de recorridos web entrantes. El canal web ahora está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../web/create-web.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Mejoras {#24-10-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Canal de SMS**

Se han introducido mejoras en los SMS para mejorar sus funciones de mensajería:

* Puede definir y administrar palabras clave únicas para sus campañas y recorridos de SMS, lo que permite una comunicación más personalizada y eficaz.

* Puede crear y enviar un mensaje SMS predeterminado cuando no se reconozca una palabra clave.

* Ahora puede editar o eliminar una configuración de canal de API de SMS.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Número máximo de recorridos activos**: Journey Optimizer ahora tiene una protección de 500 recorridos activos en zonas protegidas de producción, en lugar de 100. El número de recorridos activos es visible en el lienzo de recorrido. <!-- DOCAC-10977-->

**Conjuntos de datos**

* **Enviar y abrir eventos**: a partir del 1 de noviembre de 2024, la segmentación de transmisión ya no admitirá el uso de eventos de envío y apertura de conjuntos de datos de seguimiento y comentarios de Journey Optimizer. Este cambio se aplicará a todas las zonas protegidas y organizaciones de clientes. [Más información](../data/datasets-ttl.md#segmentation-update)

* **Tiempo de vida del conjunto de datos (TTL)**: a partir de febrero de 2025, se implementará una protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en los nuevos entornos limitados y organizaciones de la siguiente manera:

   * 90 días para los datos en el almacén de perfiles
   * 13 meses para los datos en el lago de datos

  Este cambio se implementará en las zonas protegidas de clientes existentes en una fase posterior. [Más información](../data/datasets-ttl.md#ttl)

* **Parámetros en acciones personalizadas** (Fecha de disponibilidad: 3 de octubre de 2024): ahora se admiten parámetros nulos y opcionales en las acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Creación de informes**

* Ya está disponible la creación de informes de **Experience Decisioning**, que ofrecen información esencial sobre cómo los visitantes interactúan con las experiencias.

**Gobernanza de datos y políticas de consentimiento**: fecha de disponibilidad: 7 de octubre de 2024

* La aplicación de las **políticas de control de datos** ahora se aplica en todos los canales de Journey Optimizer. Para los clientes que han creado políticas en Adobe Experience Platform, estas se aplican a las acciones de marketing como parte de la configuración de canales. Al crear contenido con una configuración, el sistema comprueba todos los campos de personalización para detectar cualquier infracción de la gobernanza de datos. Si se encuentra una infracción, no será posible publicar un recorrido o una campaña. [Más información](../action/action-privacy.md)

* Las **políticas de consentimiento personalizado** ahora se aplican a todos los canales de Journey Optimizer. Al aplicar la ley antes de enviar un mensaje o de entregar una experiencia entrante, el sistema comprueba que el usuario haya dado su consentimiento para utilizar campos de personalización en el contenido que va a recibir. Si no se da ningún consentimiento, la experiencia no se muestra. [Más información](../action/consent.md)

  >[!NOTE]
  >
  >Actualmente, las políticas de consentimiento solo están disponibles para las organizaciones que han adquirido las ofertas sobre el programa **Healthcare Shield** y el programa **Privacy and Security Shield**.

**Públicos**: fecha de disponibilidad: 8 de octubre de 2024

* Al segmentar el público de un archivo CSV, ahora puede utilizar atributos del archivo en el editor de personalización y en el generador de reglas de recorridos y campañas. [Más información](../audience/about-audiences.md)

* El uso de públicos y atributos de cargas personalizadas (archivos CSV) no está disponible en la actualidad para su uso con el programa Healthcare Shield ni Privacy and Security Shield.

**Configuración** - Fecha de disponibilidad: 23 de octubre de 2024

* Al utilizar una configuración personalizada en una campaña o un recorrido, ahora puede obtener una vista previa del contenido del correo electrónico para comprobar posibles errores con la configuración dinámica definida. [Más información](../email/surface-personalization.md#check-configuration)

**Canal basado en código**

* Ya están disponibles las plantillas de contenido. Puede acelerar la creación de experiencias basadas en código a partir de una plantilla de contenido creada por los desarrolladores. El uso de una plantilla de contenido permite al experto en marketing modificar algunos valores o campos, en lugar de crear todo el HTML o la carga útil de contenido JSON.

**Toma de decisiones**

* Los usuarios de [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=es) ahora pueden elegir modelos personalizados para optimizarlos al configurar un modelo de IA en Decisioning (anteriormente conocido como Experience Decisioning). Esto le permite, por ejemplo, optimizar en una tabla &quot;compras&quot; personalizada en lugar de restricciones definidas como la tasa de clics.&quot;

* Al agregar una política de decisión a una campaña basada en código con Decisioning (anteriormente conocida como Experience Decisioning), ahora puede seleccionar manualmente elementos de decisión únicos, además de estrategias de selección. Además, ahora puede seleccionar más de una oferta de reserva. Esto garantiza que se devuelva un determinado número de elementos de decisión. [Más información](../experience-decisioning/create-decision.md)

## Versión de septiembre de 2024 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**Fecha de la versión**: 24-26 de septiembre de 2024

### Nuevas funciones {#24-9-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<table>
<thead>
<tr>
<th><strong>Tarjetas de contenido para aplicaciones móviles y sitios web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las tarjetas de contenido son una nueva función de mensajería digital de Adobe Journey Optimizer que ofrece contenido personalizado y atractivo directamente en aplicaciones móviles y sitios web. A diferencia de las notificaciones push tradicionales, las tarjetas de contenido se integran perfectamente en la interfaz de usuario y ofrecen actualizaciones persistentes y no intrusivas que mejoran la interacción y experiencia del usuario.</p>
<p>Esta función permite a los especialistas en marketing presentar a los usuarios contenido con medios enriquecidos y relevantes, para aumentar la participación y garantizar que se vean mensajes importantes sin distraer al usuario del recorrido.</p>
<p>Para obtener más información, consulte la <a href="../content-card/get-started-content-card.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aprobaciones en recorridos y campañas (LA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con las políticas de aprobación, ahora puede configurar un proceso de aprobación dentro de Journey Optimizer que permita a los equipos de marketing asegurarse de que las campañas y los recorridos sean revisados y firmados por las partes interesadas correspondientes antes de que se activen.</p>
<p>Ahora mismo, las políticas de aprobación solo están disponibles para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../test-approve/gs-approval.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Criterios de salida globales en los recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir los criterios de salida en el nivel de recorrido. Al añadir criterios de salida, hace que los perfiles salgan del recorrido en cuanto se produce un evento (p. ej.: compra) o cumplen los requisitos para un público. Esto evitará que el usuario reciba más comunicaciones del recorrido.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-properties.md#exit-criteria">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Acelerador de contenido del Asistente de IA </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una vez creado y personalizado el mensaje, lleve el contenido al siguiente nivel con el acelerador de contenido del asistente de IA en Journey Optimizer. Ahora puede utilizar el asistente de IA para optimizar el impacto de su mensaje experimentando con diferentes títulos e imágenes principales. Cada variante se gestiona como un tratamiento único para medir y comparar qué título genera más clics de forma efectiva.</p>
<p>Láncese a una experiencia práctica inmersiva con <a href="https://experienceleague.adobe.com/es/apps/journey-optimizer/ai-assistant-content-accelerator">nuestra vista previa en directo</a>, diseñada para permitirle explorar sus funciones en primera persona y comprender plenamente sus capacidades.</a></p>
<p>Para obtener más información, consulte la <a href="../content-management/gs-generative.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>Fecha de disponibilidad: 12 de septiembre de 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configuración de canales guiada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuración de canales guiada le permite automatizar y validar la configuración del canal en una experiencia unificada, lo que acelera el proceso de introducción a Journey Optimizer. Esta nueva configuración guiada optimiza la configuración de canal rápida, lo que garantiza que todos los recursos necesarios se instalen y funcionen fácilmente en Experience Platform, Journey Optimizer y recopilación de datos. Esto permite a los equipos de marketing, productos e ingeniería de datos empezar rápidamente en la creación de campañas y recorridos.</p>
<p>Para obtener más información, consulte la <a href="../configuration/set-mobile-config.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>Fecha de disponibilidad: 3 de septiembre de 2024</p>
</br>
</td>
</tr>
</tbody>
</table>


### Mejoras {#24-9-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Públicos**: fecha de disponibilidad: 17 de septiembre de 2024

**Uso de licencias**: el panel Uso de licencias ahora muestra perfiles interesados, en lugar de públicos interesados. [Más información](../audience/license-usage.md)

**Administración de contenido**

Ahora puede exportar plantillas de contenido y fragmentos entre zonas protegidas. [Más información](../configuration/copy-objects-to-sandbox.md)

**Recorridos**

* **Mejoras en la creación de informes en directo**: la creación de informes en directo proporciona información sobre el rendimiento de sus recorridos en las últimas 24 horas. La hemos mejorado añadiendo nuevas métricas (perfiles de entrada, salida y descartados y perfiles erróneos), lo que le permite comprender mejor el comportamiento y el rendimiento del usuario directamente desde el lienzo de recorrido. [Más información](../building-journeys/report-journey.md)


* (Fecha de disponibilidad: 10 de septiembre) **Reintentos automáticos de Leer público**: los reintentos ahora se aplican de forma predeterminada a los recorridos activados por públicos (empezando con una actividad **Leer público** o **Evento empresarial**) cuando se recupera el trabajo de exportación. Si se produce un error durante la creación del trabajo de exportación, se realizarán reintentos cada 10 minutos, hasta un máximo de 1 hora. Después de esto, se considerará como un error. Por lo tanto, estos tipos de recorridos se pueden ejecutar hasta una hora después de la hora programada. [Más información](../building-journeys/read-audience.md#retries)

**Canal de correo electrónico**

* **Encabezado de mensaje en el correo electrónico enviado y copia CCO**: se ha añadido un nuevo encabezado a todos los mensajes de correo electrónico. El valor de este encabezado es único para cada correo electrónico enviado y para su copia de correo electrónico CCO correspondiente. Este encabezado también se almacena en los conjuntos de datos del mensaje y en los comentarios CCO, lo que permite reconciliar la copia CCO y la información de correo electrónico enviado correspondiente. [Más información](../configuration/archiving-support.md#bcc-header)

* **Puntuación de correo no deseado** (GA): ahora puede comprobar la puntuación de correo no deseado de su contenido en un **informe específico**. Utilizando SpamAssassin, Adobe Journey Optimizer ahora puede probar el contenido de su correo electrónico y darle una puntuación para indicar si los ISP o los proveedores de buzones lo considerarán correo no deseado o no. [Más información](../content-management/spam-report.md)

**Canal de SMS**

* **Editar credenciales de API**: ahora puede editar la configuración en las credenciales de API de SMS, incluidas las actualizaciones de las palabras clave de inclusión/exclusión y las respuestas.

**API**

* **API de simulación de campaña**: use esta API para activar el trabajo de prueba de una campaña. El envío de la prueba de una campaña es un proceso asincrónico, la API devuelve un proofJobId que se puede utilizar para comprobar el estado de la prueba. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* (Fecha de disponibilidad: 10 de septiembre) La [documentación de la API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} ahora es interactiva. Explore los extremos de la API directamente desde las páginas de documentación para obtener comentarios inmediatos y acelerar la implementación técnica. 


  Todas las páginas de referencia de la API ahora tienen una funcionalidad **Probar** que puede usar para probar las llamadas de la API directamente en la página del sitio web de documentación. [Obtenga las credenciales de autenticación requeridas](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} y empiece a usar la funcionalidad para explorar los extremos de la API.

  Utilice esta nueva funcionalidad para explorar las solicitudes y las respuestas de los extremos de la API, obtener comentarios inmediatos y acelerar la implementación técnica. 

  >[!CAUTION]
  >
  >Tenga en cuenta que, al utilizar la funcionalidad de API interactiva en las páginas de documentación, está realizando llamadas de API reales a los puntos finales. Tenga esto en cuenta al experimentar con zonas protegidas de producción.

Configuración de ****

* **Planes de calentamiento de IP**: esta capacidad ya está disponible para todos los clientes, incluidas las organizaciones que han adquirido las ofertas complementarias **Healthcare Shield** o **Privacy and Security Shield** de Adobe. [Más información](../configuration/ip-warmup-gs.md)


![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.