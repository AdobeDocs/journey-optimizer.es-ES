---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 61ea0cc6c6f0dcb90944bb7af96dbd4dbaeb7ae0
workflow-type: tm+mt
source-wordcount: 1348
ht-degree: 26%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos. Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

>[!NOTE]
>
>Las funcionalidades que se enumeran en estas notas de la versión incluyen una **Fecha de disponibilidad** que indica cuándo se puede acceder a cada cambio en su entorno. Se esperan entradas en los acordeones de **Próximamente** en los próximos días o semanas. La información de estas secciones está sujeta a cambios.

## Notas de la versión de agosto de 2026 {#aug-26-updates}

<!--
### Loyalty {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Loyalty Insights skill</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer introduces <strong>Loyalty Insights</strong>, a new CX Coworker skill for asking questions about challenge performance and other loyalty program data ingested into the Loyalty field groups in Adobe Experience Platform.</p>
<p>For more information, refer to the <a href="../start/ajo-coworker-skills.md">detailed documentation</a>.</p>
<p>Availability date: August 12, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

### Administración de contenido

En esta versión se han introducido las siguientes funciones y mejoras en la Gestión de contenido.

<table>
<thead>
<tr>
<th><strong>Abastecimiento flexible de imágenes para la generación de contenido de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La generación de contenido en Journey Optimizer ahora obtiene imágenes aprobadas por la marca directamente desde Adobe Experience Manager Assets Essentials y versiones posteriores. Tres modos controlan el equilibrio: Equilibrado (primero, administración de activos digitales; IA llena los huecos, predeterminado), Assets (origen de administración de activos digitales) y Creative (IA).</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>Para obtener más información, consulte la <a href="../content-management/generative-uc.md#image-mode">documentación detallada</a>.</p>
<p> Fecha de disponibilidad: 5 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

### Recorridos {#aug-26-journeys}

* **Nuevas funciones de lista en el editor de expresiones avanzadas**: hay dos nuevas funciones disponibles en el editor de expresiones avanzadas: `mergeLists` combina dos listas, con o sin deduplicación, y `differenceLists` devuelve los elementos de una lista que no están presentes en otra. [Más información](../building-journeys/functions/list-functions.md)

  Fecha de disponibilidad: 13 de agosto de 2026

* **Optimización del tiempo de envío en la actividad de espera**: la optimización del tiempo de envío ya está disponible en la actividad de espera, lo que permite que la IA de Adobe determine el momento óptimo para continuar a cualquier actividad descendente. [Más información](../building-journeys/wait-activity.md#sto-wait)

  Fecha de disponibilidad: 13 de agosto de 2026

### Campañas {#aug-26-campaigns}

En esta versión se han introducido las siguientes funciones y mejoras en Campañas.

<table>
<thead>
<tr>
<th><strong>Archivos adjuntos personalizados de PDF en correos electrónicos activados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora admite hasta <b>cinco archivos adjuntos de PDF</b> en total por correo electrónico en campañas activadas por API, incluidos archivos PDF estáticos y específicos de destinatarios. Los archivos PDF específicos del destinatario se recuperan de forma segura desde la zona de aterrizaje de datos y se adjuntan en el momento de la entrega, con la ubicación de cada archivo pasada directamente en la carga útil de la API. Esto permite que los sistemas existentes de generación de documentos de subida permanezcan en su sitio, con Journey Optimizer gestionando la entrega.</p>
<p>Los casos de uso admitidos incluyen facturas, extractos, tickets, contratos, etiquetas de envío y documentos similares que varían según el destinatario. Los archivos adjuntos personalizados de PDF solo están disponibles para campañas de correo electrónico transaccionales activadas por API y no son compatibles con recorridos o campañas organizadas.</p>
<p>Los volúmenes y tamaños de archivos adjuntos más grandes son compatibles mediante el complemento de archivos adjuntos de PDF. Para obtener más información, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../email/pdf-attachments.md#personalized-attachments">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 12 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Suscripciones a la alerta de ciclo vital por campaña**: ahora puede suscribirse a alertas de ciclo vital de campaña admitidas para una sola campaña, además de la suscripción existente a nivel de zona protegida. Esto permite monitorizar campañas de alta prioridad individuales sin recibir la misma alerta para cada campaña en la zona protegida. [Más información](../reports/alerts.md#subscribe-alerts)
Fecha de disponibilidad: 13 de agosto de 2026

### Campañas orquestadas {#august-26-oc}

En esta versión se han introducido las siguientes funciones y mejoras en las campañas orquestadas.

<table>
<thead>
<tr>
<th><strong>Asistencia de Horas tranquilas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar Horas de silencio. Las horas tranquilas le permiten definir exclusiones basadas en el tiempo para evitar que los mensajes se envíen durante períodos específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento en los casos de uso de la orquestación de la campaña.</p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/quiet-hours.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envío mediante olas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede programar que los mensajes salientes se entreguen en lotes controlados a lo largo del tiempo. Ideal para campañas de gran volumen o en las que el tiempo es un factor importante, la entrega de olas también ofrece una mejor capacidad de entrega y ayuda a mantener una sólida reputación de remitente, ya que reduce el riesgo de ser marcado como correo no deseado. </p>
<p>Para obtener más información, consulte la <a href="../delivery/send-using-waves.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con el canal LINE (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede añadir acciones LINE a sus campañas orquestadas. Esta nueva actividad le permite crear y ofrecer contenido altamente personalizado, incluidos texto, pegatinas, imágenes, vídeos, datos de ubicación y mensajes Flex enriquecidos, para atraer a sus clientes sin problemas en la plataforma LINE. Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../orchestrated/activities/channels.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 12 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<!--
* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups. [Learn more](../campaigns/api-triggered-high-throughput.md)

  Availability date: August 18, 2026
-->

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña (disponibilidad limitada)**: las campañas orquestadas ahora admiten la personalización de los campos de encabezado de correo electrónico, incluidos el nombre del remitente, el prefijo del correo electrónico remitente, el nombre del remitente y el correo electrónico de respuesta, así como la dirección de ejecución, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa. Los valores del encabezado se pueden establecer a nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso. [Más información](../orchestrated/activities/channels.md#configuration)

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

  Fecha de disponibilidad: 18 de agosto de 2026

* **Simplificación de la dimensión de destino**: la dimensión de segmentación activa ahora se muestra en el lienzo del flujo de trabajo, para que pueda ver qué dimensión utiliza una actividad de canal. El flujo de segmentación de varias entidades es más sencillo, ya que ya no necesita una actividad &quot;Change dimension&quot; independiente. Además, ahora puede elegir explícitamente si los mensajes se envían en el nivel de perfil o en un nivel de dimensión secundario. [Más información](../orchestrated/activities/channels.md#add)

  Fecha de disponibilidad: 18 de agosto de 2026

### Canales {#august-26-channels}

* **Complemento de rendimiento para el rendimiento - Push** - Hay un nuevo modo de mensajería transaccional de alto rendimiento disponible en las campañas activadas por API. Este modo está diseñado para la mensajería transaccional a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Antes solo estaba disponible para el canal de correo electrónico, pero ahora también lo está para el canal push, para organizaciones que han adquirido la oferta de complementos de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información. [Más información](../campaigns/api-triggered-high-throughput.md)

  Fecha de disponibilidad: 11 de agosto de 2026

### Mejoras de uso {#august-26-usability}

* **Operaciones masivas en el inventario de recorrido**: ahora puede realizar nuevas acciones masivas directamente desde la lista de inventario de recorrido, lo que permite administrar varios recorridos a la vez con mayor rapidez. Seleccione varios recorridos y aplique cualquiera de las siguientes acciones nuevas en un solo paso: **agregar al paquete**, **eliminar**, **mover a la carpeta**, **editar etiquetas** o **administrar el acceso**. Esto reduce la necesidad de repetir la misma acción un recorrido a la vez, lo que optimiza la administración de recorridos para equipos que trabajan con un gran número de recorridos. [Más información](../building-journeys/journey-ui.md)

  Fecha de disponibilidad: 12 de agosto de 2026

* **Nueva experiencia de simulación de contenido para pruebas de contenido**. El flujo de trabajo **Simular contenido** presenta una experiencia rediseñada: ahora todas las variantes se representan juntas en una sola cuadrícula desplazable (una al lado de la otra, apilada o envuelta en diseños), reemplazando la vista de variante a variante. Una sola barra de acciones inferior consolida la navegación entre las variantes de prueba, el zoom, el cambio de ventanilla (escritorio/móvil), el cambio de configuración regional, la adición de entradas de muestra, la generación de variantes con IA, la selección y el guardado de usuarios simulados y la importación o exportación de variantes. Si se elimina el carril izquierdo y se contraen las capas de encabezado adicionales, las previsualizaciones tendrán mucho más espacio. La opción **Cambiar a experiencia clásica** de la barra de acciones inferior le permite volver a la experiencia anterior en cualquier momento. [Más información](../test-approve/simulate-content-variations.md)

  Fecha de disponibilidad: 11 de agosto de 2026

* **Selección múltiple en el nuevo lienzo de recorrido**: la nueva experiencia del lienzo de recorrido presenta la selección simplificada de varios nodos: mantenga presionada la tecla Mayús y arrastre para seleccionar varios nodos a la vez, en lugar de seleccionarlos individualmente. Esto permite realizar acciones masivas, como copiar, eliminar o guardar como un fragmento de recorrido, de forma eficaz en varios nodos. [Más información](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  Fecha de disponibilidad: 17 de agosto de 2026

### Toma de decisiones {#decisioning-august}

* **Página espejo en fragmento visual**: ahora puede insertar páginas espejo en un fragmento visual. Los atributos de toma de decisiones se representan correctamente en el vínculo de la página espejo, incluso cuando el fragmento se utiliza en una campaña de correo electrónico que aprovecha Decisioning. La página espejo debe agregarse al fragmento visual antes de publicar el fragmento para que se muestren los atributos de toma de decisiones.

  Fecha de disponibilidad: 11 de agosto de 2026

  [Más información](../email/message-tracking.md#decisioning-mirror-page)