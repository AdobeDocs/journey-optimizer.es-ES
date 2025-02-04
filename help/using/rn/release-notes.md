---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 98%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Actualizaciones de enero de 2025 {#25-01-rn}

<table>
<thead>
<tr>
<th><strong>Plantillas de Customer Journey Analytics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora tiene la opción de mejorar los informes de Journey Optimizer mediante plantillas de Customer Journey Analytics. Esta nueva función le permite optimizar el proceso de creación de informes con plantillas prediseñadas adaptadas a sus necesidades de análisis.
</p>
<p>Para obtener más información, consulte la <a href="../reports/report-cja-manage.md#cja-template">documentación detallada</a>.</p>
<p> La funcionalidad <b>Plantilla</b> se está implementando progresivamente por fases, con previsión de una disponibilidad generalizada global a finales de enero</p>
</tr>
</tbody>
</table>

### Mejoras {#25-01-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Decisioning**

* La toma de decisiones ahora admite tipos de datos de objeto al editar el esquema del catálogo de elementos. [Más información](../experience-decisioning/catalogs.md)

**Personalización**

* Hay nuevas funciones de ayuda de fecha y hora disponibles para su uso en el editor de personalización. [Más información](../personalization/functions/dates.md)

## Versión de octubre de 2024 {#24-10-rn}

**Fecha de lanzamiento**: 29-30 de octubre de 2024

### Nuevas funciones {#24-10-features}

Esta versión incorpora las nuevas funciones que se indican a continuación:

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
<p>Disponible desde el 24 de octubre de 2024</p>
</td>
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
<p>Con el canal de experiencia basado en código, Adobe Journey Optimizer le permite realizar personalizaciones y pruebas avanzadas para cualquiera de sus propiedades de entrada, lo que permite ofrecer experiencias adaptadas en diversos puntos de contacto, como aplicaciones web, aplicaciones móviles, aplicaciones de escritorio, consolas de vídeo, servicios conectados a TV, televisores inteligentes, quioscos, cajeros automáticos, dispositivos IoT y mucho más. El canal de experiencia basado en código ya está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../code-based/create-code-based.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Disponible desde el 1 de octubre de 2024</p>
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
<p>Con el canal web, Adobe Journey Optimizer permite personalizar la experiencia web que ofrece a sus clientes a través de recorridos web entrantes. El canal web ahora está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../web/create-web.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Disponible desde el 1 de octubre de 2024</p>
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
<p>En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ahora ofrece varias herramientas para la administración de conflictos y la priorización. <p>Para obtener más información, consulte la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentación detallada</a>.</p></p><p><ul><li><b>Restricción de frecuencia de recorrido</b>: ahora puede crear conjuntos de reglas para aplicarlos a sus recorridos, lo que le permite limitar el número de recorridos para un perfil por día, semana o mes, así como controlar el número de recorridos simultáneos que se ejecutan simultáneamente.</li>
<li><b>Puntuación de prioridad</b>: ahora puede asignar una puntuación de prioridad a una campaña o a un recorrido, de 0 a 100. Un número mayor indica una prioridad mayor. Cuando dos campañas o acciones de viaje utilicen la misma configuración de canal, Journey Optimizer seleccionará la que tenga la puntuación de prioridad más alta. Si las campañas tienen la misma puntuación, se elegirá la campaña que se haya modificado en fecha menos reciente.</li>
<li><b>Ver conflictos potenciales</b>: el nuevo botón “Ver conflictos potenciales” en recorridos y campañas ahora permite identificar la superposición con otros recorridos o campañas, como la fecha de inicio, el público de destino o la configuración del canal seleccionado.</li>
<li><b>Arbitraje de recorridos</b>: esta nueva funcionalidad le permite priorizar los recorridos más importantes para sus clientes. Puede crear una regla para suprimir la entrada en un recorrido de prioridad inferior cuando un cliente cumpla los requisitos para un próximo recorrido de prioridad superior.</li>
<li><b>Restricción de frecuencia por tipo de comunicación: </b>con los conjuntos de reglas, ahora puede establecer reglas granulares por tipo de comunicación (por ejemplo, Ventas, Promocional) para evitar sobrecargar a los clientes con mensajes similares. Puede controlar la frecuencia en varios canales, excluyendo automáticamente los perfiles saturados para garantizar una mejor experiencia del cliente.</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>Las funciones de administración de conflictos y prioridades están disponibles en Disponibilidad limitada para un grupo selecto de clientes. Tenga en cuenta que estas funciones se implementarán gradualmente para más usuarios en el futuro. Póngase en contacto con el equipo de la cuenta si está interesado en que se le añada a la lista de espera de estas funciones.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Integración de Adobe Journey Optimizer y Movable Ink</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puedes integrar Movable Ink Da Vinci y Adobe Journey Optimizer. Con esta actividad puedes: </p>
<p><ul><li>Aprovechar las potentes funciones del producto Da Vinci de Movable Ink para combinar y personalizar las variaciones de correo electrónico para las campañas por lotes</li>
<li>Acelerar los flujos de trabajo de los profesionales para los clientes de Journey Optimizer que utilizan Da Vinci para la creación y Adobe Journey Optimizer para la optimización y el envío</li>
<li>Optimizar los modelos Da Vinci con datos de Adobe.</li></ul></p>
<p>Para obtener más información, consulte la <a href="https://movableink.com/adobe-and-movable-ink">documentación sobre Movable Ink Da Vinci</a>.</p>
</tr>
</tbody>
</table>

Anteriormente disponibles para un conjunto de organizaciones (LA), los experimentos en recorridos ya están disponibles para todos los usuarios (GA):

<table>
<thead>
<tr>
<th><strong>Personalización de la configuración del correo electrónico (Disponibilidad general) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para obtener una mayor flexibilidad y control sobre la configuración de correo electrónico, puede definir subdominios dinámicos y parámetros de encabezado personalizados al crear configuraciones de canal de correo electrónico.
</p>
<p>Para obtener más información, consulte la <a href="../email/surface-personalization.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Disponible desde el 23 de octubre de 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Aprobaciones en recorridos y campañas (Disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con las políticas de aprobación, ahora puede configurar un proceso de aprobación dentro de Journey Optimizer que permita a los equipos de marketing asegurarse de que las campañas y los recorridos sean revisados y firmados por las partes interesadas correspondientes antes de que se activen.</p>
<p>Para obtener más información, consulte la <a href="../test-approve/gs-approval.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Disponible desde el 22 de octubre de 2024</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Experimentación de contenido en recorridos (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer, que ya estaba disponible en las campañas, ahora admite experimentos en los recorridos. Los experimentos son ensayos aleatorios, lo que en el contexto de las pruebas en línea significa que expone a algunos usuarios seleccionados aleatoriamente a una variación determinada de un mensaje y a otro conjunto de usuarios seleccionados aleatoriamente a otra variación o tratamiento. Después de la exposición, puede medir las métricas de resultado que le interesan, como aperturas de correos electrónicos, suscripciones o compras.</p>
<p>Para obtener más información, consulte la <a href="../content-management/content-experiment.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Decisioning (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, disponible anteriormente para un conjunto de organizaciones (LA) y conocida como Decisiones sobre experiencias, ya está disponible para todos los usuarios (GA), incluidas las organizaciones que han adquirido las ofertas adicionales de Adobe Healthcare Shield o Privacy and Security Shield.</p><p>Decisioning simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como “elementos de decisión” y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar a cada persona los elementos de decisión más relevantes. Estos elementos de decisión se integran perfectamente en una amplia gama de superficies entrantes a través del canal de experiencia basado en código.</p>
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
<p>Para obtener más información, consulte la <a href="../content-management/multilingual-gs.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
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
<p>La creación de informes en Journey Optimizer ahora está disponible de manera general (GA) y cuenta con una interoperabilidad mejorada con las funciones de Customer Journey Analytics, estandarizando la creación de informes en ambas plataformas y mejorando la coherencia y fiabilidad de los datos. Esta integración perfecta entre Journey Optimizer y Customer Journey Analytics proporciona una visión más clara de las métricas de rendimiento, lo que permite a los usuarios tomar decisiones más informadas.</p>
<p>Con la disponibilidad general, se introducen cuatro nuevas funciones: la posibilidad de crear métricas sencillas, crear y publicar públicos, hacer preguntas específicas mediante Insight Builder y programar informes para que se envíen automáticamente por correo electrónico a los destinatarios clave.</p>
<p>Para obtener más información, consulte la <a href="../reports/report-cja-manage.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: la experiencia actual de creación de informes se retirará a partir de enero de 2025. Después de esta fecha, la nueva experiencia de creación de informes pasará a ser el estándar. Le recomendamos que se familiarice con las nuevas características y funcionalidades para garantizar una transición sin problemas. <a href="../reports/report-gs-cja.md">Aprenda a empezar con la nueva interfaz de creación de informes de Journey Optimizer</a></p>
<p>Disponible desde el 16 de octubre de 2024</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>Prueba del contenido con datos de entrada de muestra (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le permite probar diferentes variantes del contenido previsualizándolo y enviando pruebas por correo electrónico utilizando datos de entrada de muestra cargados desde un archivo o añadidos manualmente. El sistema detecta automáticamente todos los atributos de perfiles utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.</p>
<p>Actualmente, todos los clientes tienen esta posibilidad disponible como una versión Beta pública, para los canales de correo electrónico, SMS y notificaciones push.</p>
<p>Para obtener más información, consulte la <a href="../test-approve/simulate-sample-input.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Uso de datos de Adobe Experience Platform para la personalización (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveche los datos de Adobe Experience Platform en el editor de personalización para personalizar su contenido. Para ello, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero mediante una llamada de la API. Cuando haya terminado, puede usar sus datos para personalizar su contenido en [!DNL Journey Optimizer].</p>
<p>Esta funcionalidad está actualmente disponible para todos los clientes como beta pública.</p>
<p>Para obtener más información, consulte la <a href="../personalization/lookup-aep-data.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#24-10-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Canal de SMS**

* Ahora puede editar o eliminar una configuración de canal de API por SMS. [Más información](../sms/sms-configuration.md)

* Se han introducido las siguientes mejoras para optimizar las funciones de mensajería SMS con Infobip y Sinch:

   * Puede definir y administrar palabras clave únicas para sus campañas y recorridos de SMS, lo que permite una comunicación más personalizada y eficaz.

   * Puede crear y enviar un mensaje SMS predeterminado cuando no se reconozca una palabra clave.

  Obtenga más información sobre estas mejoras en la documentación de configuración de SMS para [Infobip](../sms/sms-configuration-infobip.md) y [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Canal web**

* **Modo de edición no visual para el diseñador web**: como alternativa al diseñador web de Journey Optimizer, ahora puede añadir modificaciones al sitio web mediante un editor no visual. Le permite introducir los cambios manualmente sin abrir las páginas en el editor visual. Este modo de edición no visual resulta útil si no puede instalar extensiones de explorador como el asistente visual de Adobe Experience Cloud, necesario para cargar las páginas en el diseñador web. [Más información](../web/web-non-visual-editor.md)


**Conjuntos de datos**

* **Enviar y abrir eventos**: a partir del 1 de noviembre de 2024, la segmentación de streaming ya no admitirá el uso de eventos de envío y apertura de conjuntos de datos de seguimiento y comentarios de Journey Optimizer. Este cambio se aplicará a todas las zonas protegidas y organizaciones de clientes. [Más información](../data/datasets-ttl.md#segmentation-update)

* **Tiempo de vida del conjunto de datos (TTL)**: a partir de febrero de 2025, se implementará una protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en las nuevas zona protegidas y organizaciones de la siguiente manera:

   * 90 días para los datos en el almacén de perfiles
   * 13 meses para los datos en el lago de datos

  Este cambio se implementará en las zonas protegidas de clientes existentes en una fase posterior. [Más información](../data/datasets-ttl.md#ttl)

* **Parámetros en acciones personalizadas**: fecha de disponibilidad: 3 de octubre de 2024. Ahora se admiten parámetros NULL y opcionales en las acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Creación de informes**

* Ya está disponible la **creación de informes de Decisioning**, que ofrece información esencial sobre cómo los visitantes interactúan con las experiencias. [Más información](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

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

* Al utilizar una configuración personalizada en una campaña o un recorrido, ahora puedes obtener una vista previa del contenido del correo electrónico para comprobar posibles errores con la configuración dinámica definida. [Más información](../email/surface-personalization.md#check-configuration)

**Canal basado en código**

* Ya están disponibles las plantillas de contenido. Puede acelerar la creación de experiencias basadas en código a partir de una plantilla de contenido creada por los desarrolladores. El uso de una plantilla de contenido permitirá al experto en marketing modificar tan solo algunos valores o campos, en lugar de crear todo el HTML o la carga útil de contenido JSON. [Más información](../content-management/content-templates.md)

**Decisioning**

* Los usuarios de [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=es) ahora pueden elegir modelos personalizados para optimizarlos al configurar un modelo de IA en Decisioning (anteriormente conocido como Decisiones sobre experiencias). Esto le permite, por ejemplo, optimizar en una tabla de “compras” personalizada en lugar de restricciones definidas como la tasa de clics. [Más información](../experience-decisioning/ranking.md)

* Al añadir una política de decisión a una campaña basada en código con Decisioning, ahora puede seleccionar manualmente elementos de decisión únicos, además de las estrategias de selección. Además, ahora puede seleccionar más de una oferta de reserva. Esto garantiza que se devuelva un determinado número de elementos de decisión. [Más información](../experience-decisioning/create-decision.md)
