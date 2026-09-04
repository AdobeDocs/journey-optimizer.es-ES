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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a3f084da6079fbdf158aeced3167fb88c695b7af
workflow-type: tm+mt
source-wordcount: 2323
ht-degree: 83%

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

## Actualizaciones de septiembre de 2026 {#sep-26-updates}

### Administración de contenido {#sep-26-content-management}

<table>
<thead>
<tr>
<th><strong>Herramientas MCP de gestión de contenido en CX Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker ahora tiene un nuevo conjunto de <strong>herramientas MCP de administración de contenido</strong>, que le permiten descubrir y administrar recursos de contenido de Journey Optimizer a través de mensajes en lenguaje natural. Pídale que enumere o recupere plantillas de contenido, fragmentos, páginas de aterrizaje y contenido de mensajes en línea de recorrido/campaña. También puede crear contenido, actualizar plantillas y crear, actualizar, clonar y publicar fragmentos, además de actualizar el contenido de acciones del canal en línea directamente en recorrido y campaña.</p>
<p>Para obtener más información, consulte la <a href="../start/ajo-coworker-skills.md#content-management">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

### Recorridos {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>Exclusión de nivel de recorrido (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar un grupo de exclusión para los recorridos directamente desde las propiedades del recorrido. Una exclusión es un porcentaje configurable del público destinatario que se excluye de la entrada al recorrido y que no recibe ninguna comunicación. Al comparar los perfiles de exclusión con los perfiles activos en los informes de Customer Journey Analytics, puede medir el alza incremental (el verdadero impacto) que ofrece su recorrido.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte <a href="releases.md">Ciclo de lanzamiento de Journey Optimizer</a>.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-properties.md#performance-management">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 1 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generación de expresiones con IA en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El editor de expresiones avanzadas de recorrido ahora integra la generación de expresiones con tecnología de IA: describa la expresión que desea crear en lenguaje natural y el editor genera código listo para usar que puede aplicar inmediatamente o refinar mediante mensajes de seguimiento.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/expression/generate-expression.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 1 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Nueva función dateDiff en el editor de expresiones de recorrido**. El editor de expresiones de recorrido ahora incluye la función `dateDiff`, que calcula la diferencia entre dos fechas en número de días. Esta función es útil para lógica basada en tiempo, como la creación de plazos, el cálculo de las duraciones del ciclo vital de los clientes o la creación de temporizadores de cuenta atrás en condiciones de recorrido.  [Más información](../building-journeys/functions/date-functions.md#dateDiff)

  Fecha de disponibilidad: 1 de septiembre de 2026

### Campañas {#sep-26-campaigns}

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Simulación de experiencia de entrada en campañas de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede simular acciones de canal de entrada en campañas de acción antes de lanzarlas. Utilice el modo de simulación para probar la configuración con usuarios simulados y previsualizar la experiencia procesada, incluida una URL y un código QR generados, para poder validar las reglas, la toma de decisiones y el renderizado de contenido de extremo a extremo.</p>
<p>Actualmente, esta funcionalidad está en versión Private Beta y está disponible para un conjunto limitado de organizaciones. Póngase en contacto con su representante de Adobe para obtener más información.</p>
<p>Fecha de disponibilidad: 4 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Carpetas para campañas de acción**: ahora puede organizar sus campañas de acción en carpetas para mejorar la navegación y la administración en la interfaz.

* **Rediseño del flujo de creación de campañas de acción**: el flujo de creación de campañas de acción de Adobe Journey Optimizer se ha rediseñado para ofrecer una experiencia del usuario significativamente más intuitiva, eficiente y fluida.

* **Anular los campos de ejecución predeterminados en las campañas de acción**. Anteriormente disponible en el nivel de recorrido, ahora puede anular los campos de ejecución predeterminados configurados globalmente para las entregas de correo electrónico, SMS y WhatsApp en los parámetros de la campaña de acción.

+++

## Notas de la versión de agosto de 2026 {#aug-26-updates}

### Gestión de contenidos

En esta versión se han añadido las siguientes funcionalidades y mejoras a la gestión de contenidos.

<table>
<thead>
<tr>
<th><strong>Abastecimiento flexible de imágenes para la generación de contenido de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La generación de contenido en Journey Optimizer ahora obtiene imágenes aprobadas por la marca directamente desde Adobe Experience Manager Assets Essentials y versiones posteriores. Tres modos controlan el equilibrio: Equilibrado (primero, administración de activos digitales; IA llena los huecos, predeterminado), Assets (origen de administración de recursos digitales) y Creative (IA).</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>Para obtener más información, consulte la <a href="../content-management/generative-uc.md#image-mode">documentación detallada</a>.</p>
<p> Fecha de disponibilidad: 5 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Advertencia de tamaño de variante de contenido**: Journey Optimizer ahora muestra una advertencia de límite suave cuando una variante de contenido supera su umbral de tamaño recomendado: 1200 KB para plantillas y mensajes, 700 KB para fragmentos y 1000 KB para páginas de destino. Guardar y publicar no están bloqueados. [Más información](../start/guardrails.md#content-authoring)

  Fecha de disponibilidad: 25 de agosto de 2026

* **Límites de recuento de fragmentos en el contenido**: Journey Optimizer ahora valida el número de fragmentos únicos utilizados dentro de un fragmento de contenido: hasta 60 por variante y hasta 120 en todas las variantes de un solo mensaje. Las advertencias aparecen en el 75 % de cada límite; la publicación se bloquea cuando se alcanza el límite estricto. [Más información](../start/guardrails.md#fragments-guardrails)

  Fecha de disponibilidad: 25 de agosto de 2026

### Recorridos {#aug-26-journeys}


* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido, ahora aparecen en el encabezado del recorrido junto al distintivo del estado. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado. [Más información](../building-journeys/journey-properties.md#dates)

  Fecha de disponibilidad: 20 de agosto de 2026

* **Nuevas funciones de lista en el editor de expresiones avanzadas**: hay dos nuevas funciones disponibles en el editor de expresiones avanzadas: `mergeLists` combina dos listas, con o sin deduplicación, y `differenceLists` devuelve los elementos de una lista que no están presentes en otra. [Más información](../building-journeys/functions/list-functions.md)

  Fecha de disponibilidad: 13 de agosto de 2026

* **Optimización del tiempo de envío en la actividad de espera**: la optimización del tiempo de envío ya está disponible en la actividad de espera, lo que permite que la IA de Adobe determine el momento óptimo para continuar a cualquier actividad descendente. [Más información](../building-journeys/wait-activity.md#sto-wait)

  Fecha de disponibilidad: 13 de agosto de 2026

### Campañas {#aug-26-campaigns}

En esta versión se han añadido las siguientes funcionalidades y mejoras a las campañas.

<table>
<thead>
<tr>
<th><strong>Archivos PDF adjuntos personalizados en correos electrónicos activados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora admite hasta <b>cinco archivos PDF adjuntos</b> en total por correo electrónico en campañas activadas por API, incluidos archivos PDF estáticos y específicos del destinatario. Los archivos PDF específicos del destinatario se recuperan de forma segura desde la zona de aterrizaje de datos y se adjuntan en el momento del envío, con la ubicación de cada archivo pasada directamente en la carga útil de la API. Esto permite que los sistemas existentes de generación de documentos de subida permanezcan en su sitio y Journey Optimizer gestiona el envío.</p>
<p>Los casos de uso admitidos incluyen facturas, extractos, tickets, contratos, etiquetas de envío y documentos similares que varían según el destinatario. Los archivos PDF adjuntos personalizados solo están disponibles para campañas de correo electrónico transaccionales activadas por API y no son compatibles con recorridos o campañas orquestadas.</p>
<p>Los volúmenes y tamaños de archivos adjuntos más grandes son compatibles mediante el complemento de archivos PDF adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../email/pdf-attachments.md#personalized-attachments">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 12 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Suscripciones a la alerta de ciclo de vida por campaña**: ahora puede suscribirse a alertas de ciclo de vida de campaña admitidas para una sola campaña, además de la suscripción existente a nivel de zona protegida. Esto permite monitorizar campañas de alta prioridad individuales sin recibir la misma alerta para cada campaña en la zona protegida. [Más información](../reports/alerts.md#subscribe-alerts)

  Fecha de disponibilidad: 13 de agosto de 2026

### Campañas orquestadas {#august-26-oc}

En esta versión se han añadido las siguientes funcionalidades y mejoras a las campañas orquestadas.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con Horas de inactividad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar Horas de inactividad. Horas de inactividad le permite definir exclusiones basadas en el tiempo para evitar que los mensajes se envíen durante períodos específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento en los casos de uso de orquestación de campañas.</p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/quiet-hours.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envío por oleadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede programar mensajes de salida para que se entreguen en lotes controlados a lo largo del tiempo. Ideal para campañas de gran volumen o urgentes, el envío por oleadas también ofrece una mejor entregabilidad y ayuda a mantener una sólida reputación de remitente, ya que reduce el riesgo de marcarse como spam. </p>
<p>Para obtener más información, consulte la <a href="../delivery/send-using-waves.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Disponibilidad del canal LINE (disponibilidad limitada)</strong><br/></th>
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

* **Capacidad para administrar dimensiones de destino de perfil**: ahora puede eliminar una dimensión de destino de perfil o editar e intercambiar su espacio de nombres de identidad configurado, lo que proporciona mayor control y flexibilidad sobre las configuraciones de datos. [Más información](../orchestrated/target-dimension.md)

  Fecha de disponibilidad: 18 de agosto de 2026

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña (disponibilidad limitada)**: las campañas orquestadas ahora admiten la personalización de los campos de encabezado de correo electrónico, incluidos De nombre, Prefijo desde correo electrónico, Nombre de la dirección de respuesta y Dirección de correo electrónico de respuesta, así como la dirección de ejecución, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa. Los valores del encabezado se pueden establecer a nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso. [Más información](../orchestrated/activities/channels.md#configuration)

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

  Fecha de disponibilidad: 18 de agosto de 2026

* **Simplificación de la dimensión de destino**: la dimensión de segmentación activa ahora se muestra en el lienzo del flujo de trabajo, para que pueda ver qué dimensión utiliza una actividad de canal. El flujo de segmentación de varias entidades es más sencillo, ya que ya no necesita una actividad Cambiar dimensión independiente. Además, ahora puede elegir explícitamente si los mensajes se envían en el nivel de perfil o en un nivel de dimensión secundario. [Más información](../orchestrated/activities/channels.md#add)

  Fecha de disponibilidad: 18 de agosto de 2026

### Lealtad {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Aptitud de Loyalty Insights</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer presenta <strong>Loyalty Insights</strong>, una nueva habilidad de los compañeros de CX para hacer preguntas acerca del rendimiento de desafíos y otros datos del programa de fidelización incorporados en los grupos de campo Lealtad en Adobe Experience Platform.</p>
<p>Para obtener más información, consulte la <a href="../start/ajo-coworker-skills.md#loyalty-skills">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 31 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

### Canales {#august-26-channels}

* **Metadatos de ejecución de actividades activas (executionMetadata)**: las campañas de actividades activas activadas por API (transaccionales y de marketing) ahora admiten el campo executionMetadata opcional en cada destinatario. Esto permite adjuntar datos de clave/valor personalizados, como un ID de pedido, un nivel de lealtad o un código de región, a una ejecución. [Más información](../mobile-live/create-mobile-live.md#metadata)

  Fecha de disponibilidad: 19 de agosto de 2026

* **Complemento de rendimiento, push**: ahora hay disponible un nuevo modo de mensajería transaccional de alto rendimiento en las campañas activadas por API. Este modo está diseñado para la mensajería transaccional a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Antes solo disponible para el canal de correo electrónico, esta funcionalidad ahora está disponible en el canal push para organizaciones que han adquirido la oferta de complemento de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información. [Más información](../campaigns/api-triggered-high-throughput.md)

  Fecha de disponibilidad: 11 de agosto de 2026

### Configuración {#august-26-configuration}

* **Compatibilidad con varias SAN en la generación de CSR para la configuración personalizada de subdominios**: al configurar o migrar un subdominio personalizado mediante el método de delegación personalizado, la solicitud de firma de certificado (CSR) ahora se genera automáticamente con `data.{subdomain}` y `cdn.{subdomain}` como nombres alternativos del sujeto (SAN). Anteriormente, el CSR generado solo incluía `data.{subdomain}`, lo que requería la adición manual de `cdn.{subdomain}` antes de enviarlo a la entidad emisora de certificados. [Más información](../configuration/custom-subdomain-migration.md#send-csr-to-ca)

  Fecha de disponibilidad: 20 de agosto de 2026

### Toma de decisiones {#decisioning-august}

* **Límite de frecuencia de nivel de ubicación en la toma de decisiones**: las reglas de restricción de frecuencia en la toma de decisiones ahora se pueden vincular a ubicaciones individuales, lo que le proporciona un control más preciso sobre la frecuencia con la que se muestra una oferta en una superficie determinada. Hay dos modos disponibles: **límite específico de la ubicación**, que define un límite que se aplica solo cuando la oferta se muestra en una ubicación seleccionada, y **límite por ubicación**, que aplica un límite de forma independiente en cada ubicación donde aparece la oferta, de modo que cada ubicación mantiene su propio contador de límite. Tenga en cuenta que el límite relacionado con la ubicación no se aplica a las ofertas restringidas mediante reglas basadas en datos de Adobe Experience Platform. [Más información](../experience-decisioning/items.md#capping)

  Fecha de disponibilidad: 24 de agosto de 2026

* **Páginas espejo en fragmentos visuales**: ahora puede insertar páginas espejo en un fragmento visual. Los atributos de toma de decisiones se representan correctamente en el vínculo de la página espejo, incluso cuando el fragmento se utiliza en una campaña de correo electrónico que aprovecha la toma de decisiones. La página espejo debe añadirse al fragmento visual antes de publicar el fragmento para que se muestren los atributos de toma de decisiones. [Más información](../email/message-tracking.md#decisioning-mirror-page)

  Fecha de disponibilidad: 11 de agosto de 2026

### Mejoras de uso {#august-26-usability}

* **Selección múltiple en el nuevo lienzo del recorrido**: la nueva experiencia del lienzo del recorrido presenta la selección simplificada de varios nodos; mantenga presionada la tecla Mayús y arrastre para seleccionar varios nodos a la vez, en lugar de seleccionarlos individualmente. Esto permite realizar acciones masivas, como copiar, eliminar o guardar como un fragmento de recorrido, de forma eficaz en varios nodos. [Más información](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  Fecha de disponibilidad: 17 de agosto de 2026

* **Operaciones masivas en el inventario de recorrido**: ahora puede realizar nuevas acciones masivas directamente desde la lista de inventario de recorrido, lo que permite administrar varios recorridos a la vez con mayor rapidez. Seleccione varios recorridos y aplique cualquiera de las siguientes acciones nuevas en un solo paso: **añadir al paquete**, **eliminar**, **mover a la carpeta**, **editar etiquetas** o **administrar el acceso**. Esto reduce la necesidad de repetir la misma acción cada vez con un recorrido, lo que optimiza la administración de recorrido para equipos que trabajan con un gran número de recorridos. [Más información](../building-journeys/journey-ui.md)

  Fecha de disponibilidad: 12 de agosto de 2026

* **Nueva experiencia de simulación de contenido para pruebas de contenido**: el flujo de trabajo **Simular contenido** presenta una experiencia rediseñada; ahora todas las variantes se representan juntas en una sola cuadrícula desplazable (con diseños en paralelo, apilados o ajustados), lo que reemplaza la vista de variante a variante. Una sola barra de acciones inferior consolida la navegación entre las variantes de prueba, el zoom, el cambio de ventanilla (escritorio/móvil), el cambio de configuración regional, la adición de entradas de muestra, la generación de variantes con IA, la selección y el guardado de usuarios simulados y la importación o exportación de variantes. Si se elimina el carril izquierdo y se contraen las capas de encabezado adicionales, las previsualizaciones tendrán mucho más espacio. La opción **Cambiar a la experiencia clásica** de la barra de acciones inferior le permite volver a la experiencia anterior en cualquier momento. [Más información](../test-approve/simulate-content-variations.md)

  Fecha de disponibilidad: 11 de agosto de 2026


