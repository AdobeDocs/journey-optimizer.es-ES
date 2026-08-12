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
source-git-commit: 27ea2cd4b19bbb796e70a2b9be8cb6c61fb949aa
workflow-type: tm+mt
source-wordcount: 3245
ht-degree: 19%

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

## Actualizaciones del 26 de agosto {#aug-26-updates}

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

### Campañas {#aug-26-campaigns}

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

### Mejoras de uso {#august-26-usability}

* **Operaciones masivas en el inventario de recorrido**: ahora puede realizar nuevas acciones masivas directamente desde la lista de inventario de recorrido, lo que permite administrar varios recorridos a la vez con mayor rapidez. Seleccione varios recorridos y aplique cualquiera de las siguientes acciones nuevas en un solo paso: **agregar al paquete**, **eliminar**, **mover a la carpeta**, **editar etiquetas** o **administrar el acceso**. Esto reduce la necesidad de repetir la misma acción un recorrido a la vez, lo que optimiza la administración de recorridos para equipos que trabajan con un gran número de recorridos. [Más información](../building-journeys/journey-ui.md)

  Fecha de disponibilidad: 12 de agosto de 2026

* **Nueva experiencia de simulación de contenido para pruebas de contenido**. El flujo de trabajo **Simular contenido** presenta una experiencia rediseñada: ahora todas las variantes se representan juntas en una sola cuadrícula desplazable (una al lado de la otra, apilada o envuelta en diseños), reemplazando la vista de variante a variante. Una sola barra de acciones inferior consolida la navegación entre las variantes de prueba, el zoom, el cambio de ventanilla (escritorio/móvil), el cambio de configuración regional, la adición de entradas de muestra, la generación de variantes con IA, la selección y el guardado de usuarios simulados y la importación o exportación de variantes. Si se elimina el carril izquierdo y se contraen las capas de encabezado adicionales, las previsualizaciones tendrán mucho más espacio. La opción **Cambiar a experiencia clásica** de la barra de acciones inferior le permite volver a la experiencia anterior en cualquier momento. [Más información](../test-approve/simulate-content-variations.md)

  Fecha de disponibilidad: 11 de agosto de 2026

## Notas de la versión de julio de 2026 {#july-26-updates}

### Desafíos de fidelización {#july-26-loyalty}

Journey Optimizer presenta Loyalty Challenges, una nueva funcionalidad de esta versión.

<table>
<thead>
<tr>
<th><strong>Desafíos de fidelización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los retos de fidelidad convierten las iniciativas de fidelidad en experiencias atractivas y entretenidas que motivan a los clientes a realizar acciones valiosas, como realizar compras, escribir críticas o cualquier comportamiento deseado.</p>
<p>Los administradores pueden utilizar el menú de configuraciones de Fidelidad para conectar Journey Optimizer con el ecosistema de fidelidad, incluidas las API de cumplimiento de recompensas, las definiciones de eventos, el inventario de productos, las exclusiones y la configuración de identidad. Los especialistas en marketing pueden diseñar desafíos estándar, de racha o secuenciales, definir tareas y recompensas, ofrecer tarjetas de contenido de marca y mensajes, y monitorizar el rendimiento con paneles de informes impulsados por IA. Journey Optimizer genera los recorridos que organizan cada desafío en segundo plano, de modo que los equipos puedan centrarse en la experiencia del cliente y los objetivos empresariales.</p>
<p>La lealtad también introduce habilidades de Coworker que permiten a los equipos realizar operaciones de desafío clave de forma más eficiente, incluida la creación de desafíos, la configuración de propiedades de desafío, la administración de audiencias y la configuración relacionada, y la revisión de perspectivas para monitorizar la participación en el desafío y recompensar el rendimiento.</p>
<p><img src="assets/do-not-localize/loyalty.png"></p>
<p>Esta funcionalidad solo está disponible para organizaciones con licencia de Lealtad de Journey Optimizer. Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../loyalty-challenges/get-started.md">documentación detallada</a>.</p>
<p> Fecha de disponibilidad: 28 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

### Canales {#july-26-channels}

En esta versión se han introducido las siguientes funciones y mejoras.

<table>
<thead>
<tr>
<th><strong>Canal saliente personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora presenta Canales personalizados, una nueva funcionalidad que permite a los administradores introducir cualquier canal de mensajería saliente basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor propietario, directamente en Journey Optimizer a través de un Generador de canales sin código.</p >
<p>Una vez configurados, los canales personalizados están disponibles en todas las campañas, recorridos y campañas orquestadas, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, creación de informes predeterminada y aplicación de consentimiento y gobernanza.</p>
<p>Esto llena un hueco que anteriormente se solucionaba con las acciones personalizadas, que se limitan únicamente a los recorridos y carecen de funcionalidades de canal dedicadas.</p>
<p>Actualmente, los canales salientes personalizados están disponibles como disponibilidad limitada. Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p><img src="assets/do-not-localize/custom-channel.gif"></p>
<p>Para obtener más información, consulte la <a href="../custom-channel/get-started-custom-channel.md">documentación detallada</a>.</p>
<p> Fecha de disponibilidad: 31 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimización de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar un recorrido o una acción de campaña para incluir varios canales salientes (correo electrónico, push, SMS) y permitir que Journey Optimizer realice envíos automáticamente a través del mejor canal para cada cliente. Hay tres modos de optimización disponibles:</p>
<ul>
<li>Clasificación manual: especifique el orden de canal preferido.</li>
<li>Preferencia del cliente: utilice el canal preferido del cliente desde su perfil (atributo Consentimientos y preferencias del modelo de datos de experiencia ).</li>
<li>Clasificación basada en modelos de IA: utilice puntuaciones de tendencia de aprendizaje automático para deducir el canal más efectivo por cliente.</li>
</ul>
<p>Cuando el canal de mayor clasificación no está disponible (no está incluido, limitado por frecuencia o no está configurado), el sistema vuelve al siguiente canal disponible.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p><img src="assets/do-not-localize/channel-optimization.gif"></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/channel-optimization.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 22 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Canal de WhatsApp: admite plantillas de flujo de WhatsApp**. Ahora puedes enviar plantillas de flujo de WhatsApp en Adobe Journey Optimizer para ofrecer experiencias interactivas en varias pantallas, como encuestas y captura de posibles clientes. Las respuestas se capturan al enviarlas y se almacenan como cargas JSON sin procesar en el nuevo conjunto de datos de evento de seguimiento de canal de Journey Optimizer. [Más información](../data/get-started-datasets.md)

* **Integraciones mejoradas de proveedores personalizados - Móvil** - Las integraciones de proveedores personalizados ahora ofrecen una mayor flexibilidad con mensajes clave y actualizaciones de encabezados:

  * Personalización del encabezado: ahora puede editar el valor predeterminado del encabezado Content-Type y añadir hasta 10 parámetros de encabezado personalizados.

  * Compatibilidad con carga útil SMS: se ha agregado compatibilidad con las funciones de ayuda de Adobe Journey Optimizer en la carga útil SMS, incluida encode64.

### Administración {#july-26-administration}

En esta versión se han agregado las siguientes funcionalidades y mejoras a la administración y a la administración de datos.

<table>
<thead>
<tr>
<th><strong>Inclusión en la lista de permitidos IP del cortafuegos de aplicaciones web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora admite la inclusión en la lista de permitidos IP del cortafuegos de aplicaciones web para páginas de destino, lo que permite a las organizaciones exigir que todas las solicitudes entrantes se enruten exclusivamente a través de la infraestructura configurada del cortafuegos de aplicaciones web. Con esta mejora, los clientes pueden configurar Journey Optimizer para que rechace cualquier solicitud directa que omita el nivel del cortafuegos de aplicaciones web, asegurándose de que las políticas de seguridad definidas en herramientas como Imperva se apliquen de forma coherente.</p>
<p>Esta capacidad refuerza la postura de seguridad de las empresas con requisitos estrictos de acceso a la red, lo que les permite un control total del flujo de tráfico a sus páginas de aterrizaje alojadas en Journey Optimizer.</p>
<p><img src="assets/do-not-localize/allowed-ips.gif"></p>
<p>Para obtener más información, consulte la <a href="../configuration/waf-ip-allowlist.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 30 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Administrar dominios para personalización completa/base de URL**: ahora puede crear y administrar dominios aprobados para personalización completa y base de URL directamente desde la configuración de administración en Adobe Journey Optimizer, sin tener que ponerse en contacto con el soporte de Adobe. [Más información](../email/url-personalization.md#personalize-complete-base-url)

  Fecha de disponibilidad: 30 de julio de 2026

* **Protección de tiempo de vida de conjunto de datos (TTL) — zonas protegidas existentes** - La protección de tiempo de vida (TTL) para conjuntos de datos generados por el sistema de Journey Optimizer (90 días en el almacén de perfiles, 13 meses en el lago de datos) se aplicará en **zonas protegidas y organizaciones de clientes existentes** a partir del **1 de octubre de 2026**. [Más información](../data/datasets-ttl.md#ttl-guardrail)

### Diseño de correo electrónico {#july-26-email}

En esta versión se han añadido las siguientes funcionalidades y mejoras al diseño de correo electrónico.

<table>
<thead>
<tr>
<th><strong>Módulos en el diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El diseñador de correo electrónico ahora incluye una biblioteca de módulos de diseño listos para usar, como encabezados, tarjetas de producto, bloques de información y pies de página, que puede arrastrar y soltar directamente en el lienzo del correo electrónico.</p>
<p>Cada módulo viene preconfigurado con propiedades editables (imagen, título, texto, botón, vínculos) y se puede personalizar completamente a través de la interfaz de WYSIWYG, lo que acelera la creación de correos electrónicos sin necesidad de crear estructuras desde cero.</p>
<p><img src="assets/do-not-localize/email-modules.gif"></p>
<p>Para obtener más información, consulte la <a href="../email/email-modules.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 29 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Comprobación de contenido en el Designer de correo electrónico (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora incluye validación técnica automatizada directamente en el diseñador de correo electrónico, lo que le ayuda a detectar problemas de HTML y CSS antes de enviarlos.</p>
<p>Las comprobaciones cubren elementos no admitidos, como etiquetas <code>&lt;script&gt;</code> y <code>&lt;base&gt;</code>, divs vacíos que pueden romper el diseño en Microsoft Outlook, metaetiquetas de actualización HTML y umbrales de tamaño de CSS o HTML que activan los errores de procesamiento en Gmail.</p>
<p>Los resultados aparecen como errores, advertencias o avisos informativos directamente en el panel de creación, con detalles contextuales y correcciones con un solo clic cuando están disponibles, de modo que los problemas se pueden resolver sin salir del editor.</p>
<p>Esta funcionalidad, que antes estaba disponible en disponibilidad limitada, ya está disponible para todos los clientes.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>Para obtener más información, consulte la <a href="../email/content-check.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 16 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Compatibilidad con fragmentos de expresión en`<head>`**: ahora los fragmentos de expresión se pueden usar en `<head>` de las plantillas de correo electrónico. Esto le permite centralizar el estilo de cualquier código personalizado en un solo fragmento y reutilizarlo en varias plantillas. Cuando se actualiza y vuelve a publicar un fragmento, todos los correos electrónicos creados a partir de plantillas que hacen referencia a él heredan automáticamente el código más reciente, lo que elimina la necesidad de actualizar manualmente cada correo electrónico de forma individual. [Más información](../personalization/use-expression-fragments.md)

  Fecha de disponibilidad: 29 de julio de 2026

### Recorridos {#july-26-journeys}

En esta versión se han añadido las siguientes funciones y mejoras a los recorridos.
<table>
<thead>
<tr>
<th><strong>Nueva interfaz de usuario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se ha presentado una <b>nueva interfaz de usuario</b> para el lienzo de recorrido, que ofrece un rendimiento mejorado para recorridos grandes, un diseño automático para una mejor legibilidad y una experiencia de creación guiada.</p>
<p><img src="../building-journeys/assets/journey-new-canvas.png"></p>
<p>Para cambiar a la nueva interfaz de usuario, haga clic en el botón <b>Nueva experiencia</b>. Esta configuración se guarda en el nivel de recorrido, por lo que el recorrido se vuelve a abrir en la nueva experiencia de forma predeterminada. Para volver, haz clic en <b>Experiencia anterior</b>. <a href="../building-journeys/using-the-journey-designer.md#canvas-capabilities">Más información</a>.</p>
<p><img src="../building-journeys/assets/journey-new-experience-switch.png"></p>
<p> Fecha de disponibilidad: 16 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

* [!BADGE Desaprobación]{type=Negative} **Las audiencias por lotes ya no son compatibles con el nodo de calificación de audiencias y los criterios de salida**. A partir de septiembre de 2026, Journey Optimizer bloqueará la publicación de cualquier recorrido que utilice una audiencia por lotes en un nodo de calificación de audiencias o en criterios de salida. Ya aparece una advertencia de validación en el lienzo de recorrido.  Los recorridos en directo existentes no se ven afectados. Los recorridos nuevos, borradores y duplicados que incluyen esta configuración deben actualizarse antes de septiembre de 2026. Utilice una audiencia de flujo continuo en el nodo Calificación de audiencias o cambie a una actividad Leer audiencia. Para Criterios de salida, utilice una audiencia de flujo continuo. [Aprenda a migrar sus recorridos](../building-journeys/aq-batch-audiences-migration.md)

* **Audiencias externas en la simulación de Recorrido**: la simulación de Recorrido ahora admite audiencias externas. Al simular recorridos dirigidos a audiencias CSV o Composición de audiencia federada, puede burlar los atributos de enriquecimiento de esas audiencias directamente a través del formulario de la interfaz de usuario o una importación JSON. La interfaz de usuario muestra dinámicamente solo los atributos de enriquecimiento específicos utilizados en la lógica de recorrido, lo que permite la validación precisa de las ramas de decisión y las reglas de personalización antes de su lanzamiento. [Más información](../building-journeys/simulate-journey.md)

  Fecha de disponibilidad: 29 de julio de 2026

* **Protección de disyuntor para extremos de acción personalizados lentos**: Para los extremos enrutados a través del servicio de acción personalizada lenta, Journey Optimizer ahora limita temporalmente todas las llamadas durante un máximo de 5 minutos cuando más del 20 % de las llamadas en una ventana de 120 segundos exceden los 10 segundos, si hay al menos 200 llamadas en la ventana de observación de 120 segundos. Esto ayuda a evitar sobrecargar puntos finales que ya son lentos. [Más información](../configuration/external-systems.md#response-time)

  Fecha de disponibilidad: 29 de julio de 2026. Esta capacidad se está implantando gradualmente en todas las regiones.

### Campañas orquestadas {#july-26-oc}

Las siguientes funcionalidades y mejoras estarán disponibles en las campañas orquestadas en esta versión.

<table>
<thead>
<tr>
<th><strong>Direccionamiento basado en archivos en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas ahora admiten la carga de un <strong>archivo CSV o TXT</strong> directamente en el lienzo de campaña como audiencia de segmentación, sin ingerir primero el archivo en Adobe Experience Platform. Los datos del archivo se consumen en el momento de la ejecución y no persisten como un conjunto de datos de Adobe Experience Platform. Durante la configuración del archivo, puede definir asignaciones de columnas, tipos de datos, control de valores NULL y directivas de error por columna. Las filas que no superan la validación se rechazan y registran antes de que se ejecute la campaña, lo que mantiene la audiencia limpia sin preprocesamiento manual. Esto es especialmente adecuado para envíos específicos o campañas de listas de socios en las que no es práctico crear una canalización de ingesta completa.</p>
<p>Para obtener más información, consulte la <a href="../orchestrated/activities/load-file.md">documentación detallada</a>.</p>
<p> Fecha de disponibilidad: 6 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Ver transiciones de campaña orquestadas permiso** - Se ha agregado un nuevo permiso **Ver transiciones de campaña orquestadas** para reemplazar la opción **Ver archivo en campañas orquestadas** heredada. Este cambio le permite ocultar los resultados de la vista previa en las transiciones de campaña para cumplir con la información de identificación personal.

  Fecha de disponibilidad: 29 de julio de 2026

  [Más información](../administration/ootb-permissions.md)

### Toma de decisiones {#decisioning}

* **Creación de reglas de toma de decisiones a partir de la expresión de lenguaje natural**: ahora puede describir la regla de toma de decisiones que desea crear en lenguaje sin formato y permitir que la inteligencia artificial la genere por usted. Esta funcionalidad está disponible para los clientes con acceso a las funcionalidades de Adobe AI.

  Esta funcionalidad está disponible para las organizaciones con acceso a las funcionalidades de Adobe AI. Solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

  Fecha de disponibilidad: 29 de julio de 2026

  [Más información](../experience-decisioning/rules.md#build-rule-with-ai)

* Atributos personalizados dinámicos de **elementos de decisión**: los atributos personalizados de elementos de decisión ahora se pueden personalizar en el momento de la entrega mediante datos de perfil, contextuales y de audiencia. Esto elimina la necesidad de mantener ofertas duplicadas para variaciones de contenido menores, lo que permite a los especialistas en marketing administrar menos elementos de decisión más flexibles. [Más información](../experience-decisioning/items.md#attributes)

  Fecha de disponibilidad: 27 de julio de 2026

* **Simulación de reglas de decisión y fórmulas de clasificación**: ahora puede simular las reglas de decisión y las fórmulas de clasificación directamente desde el editor de reglas o fórmulas. Agregue variantes de prueba manuales o genérelas mediante IA y, a continuación, ejecute la expresión con los datos de prueba para validar la idoneidad y revisar los resultados de clasificación, todo antes de implementarlos en producción. La generación de variantes está disponible para los clientes con acceso a las funciones de Adobe AI.

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

  Fecha de disponibilidad: 29 de julio de 2026

  [Más información acerca de la simulación de reglas](../experience-decisioning/rules.md) | [Más información sobre la simulación de fórmulas de clasificación](../experience-decisioning/ranking/ranking-formulas.md)

### Gestión de contenidos {#july-26-content}

En esta versión se han añadido las siguientes funcionalidades y mejoras a la administración de contenido.

<table>
<thead>
<tr>
<th><strong>Funciones de adopción guiada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transición a Adobe Journey Optimizer desde otra plataforma de marketing es más sencilla gracias a las funciones guiadas que le ayudan a trasladar el contenido y los recorridos de correo electrónico existentes a Journey Optimizer. Un espacio de trabajo dedicado le permite reutilizar lo que tiene en lugar de reconstruir desde cero.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p><img src="assets/do-not-localize/guided-adoption.gif"></p>
<p>Para obtener más información, consulte la <a href="../start/migrate-content-and-journeys.md">documentación detallada</a>.</p>
<p> Fecha de disponibilidad: 30 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Nuevas funciones de ayuda en las expresiones de personalización**. Las nuevas funciones de ayuda ya están disponibles en las expresiones de personalización:

  * `appendQueryParams`: anexa un parámetro de consulta a una dirección URL o lo reemplaza si la clave ya existe.
  * `dateBetween`: comprueba si una fecha se encuentra dentro de un intervalo de fechas de inicio y finalización (incluido).
  * `equalsAnyIgnoreCase`: devuelve el valor &quot;True&quot; cuando una cadena coincide con cualquier valor proporcionado, omitiendo mayúsculas y minúsculas.
  * `getUrlFragment`: extrae la parte de fragmento de una dirección URL (la parte posterior a #).
  * `join`: concatena elementos de matriz en una sola cadena utilizando un separador.
  * `decode64`: descodifica una cadena codificada en Base64. Si la entrada no es Base64 válida, la cadena de entrada original se devuelve sin cambiar.
  * `parseJson`: analiza una cadena JSON en una variable estructurada que se puede utilizar en la plantilla.
  * `valueAtPath`: asigna un valor de una ruta de datos a una variable de plantilla, con indexación opcional para extraer un elemento específico de matrices o colecciones.
  * `abort`: detiene el envío del mensaje cuando se alcanza durante el procesamiento.

  La función `concat` también se ha mejorado y ahora admite dos o más argumentos.

  Además, las siguientes funciones de migración de plantillas ya están disponibles para ayudarle a migrar plantillas existentes a Journey Optimizer:

  * `ampCompare`: compara dos valores utilizando el operador de comparación especificado.
  * `ampSubstr`: devuelve una parte de una cadena entre los índices de inicio y fin especificados.
  * `compareTo`: compara dos cadenas lexicográficamente.

  [Más información sobre las funciones de ayuda](../personalization/functions/functions.md)

  Fecha de disponibilidad: 28 de julio de 2026

* Se cambió el nombre de **&quot;Asistente de IA&quot; a &quot;Generar contenido&quot;**. Se cambió el nombre del Asistente de IA a Generar contenido en Adobe Journey Optimizer. Esta actualización se limita a los nombres y la terminología; no se han introducido cambios funcionales. Se ha cambiado el nombre de las etiquetas de navegación, los botones, los menús y los cuadros de diálogo para la generación de contenido, la generación de imágenes, las expresiones de personalización y la experimentación de contenido de &quot;Asistente de IA&quot; a &quot;Generar contenido&quot;.

  Fecha de disponibilidad: 30 de julio de 2026

* **Mejoras multilingües**: ahora se puede duplicar la configuración de idioma a partir de una configuración activa existente, por lo que ya no es necesario reconstruir completamente una configuración para realizar cambios. También puede copiar una condición de una configuración regional a otra durante la creación de la Configuración de idioma, lo que optimiza la configuración para sitios con muchos idiomas.

  Fecha de disponibilidad: 30 de julio de 2026

### Contenido e integraciones {#july-26-integration}

Las siguientes mejoras se incluyen en la administración de contenido y en las integraciones de esta versión.

<table>
<thead>
<tr>
<th><strong>Temporizador de cuenta atrás con Dynamic Media</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Integración de Dynamic Media de Journey Optimizer y Adobe Experience Manager</strong> permite la personalización en tiempo abierto para plantillas de Dynamic Media, lo que desbloquea casos de uso hiperpersonalizados. Los clientes pueden crear y publicar plantillas personalizadas en Adobe Experience Manager y utilizarlas en Journey Optimizer, con datos procesados en el momento de la apertura.</p>
<p>Para obtener más información, consulte la <a href="../integrations/aem-dynamic.md#countdown">documentación detallada</a>.</p>
<p> Fecha de disponibilidad: 30 de julio de 2026</p>
</td>
</tr>
</tbody>
</table>



* **Nuevas herramientas del servidor MCP de AJO**: el servidor MCP de [!DNL Adobe Journey Optimizer] ahora expone cinco **herramientas de configuración de canal** de solo lectura adicionales, lo que le permite consultar las configuraciones de canal, los recursos de soporte y las acciones de marketing directamente desde su asistente de IA. Ahora puede usar **Configuraciones de canal de lista** (en todos los canales de AJO), **Obtener configuración de canal**, **Enumerar recursos de configuración**, **Obtener recurso de configuración** y **Enumerar acciones de marketing**. [Más información](../integrations/ajo-mcp.md#mcp-tools)

  Fecha de disponibilidad: 9 de julio de 2026

### Creación de informes {#july-26-reporting}

En esta versión se incluyen las siguientes mejoras en los informes.

* **Nuevas métricas estimadas de clics para los informes de correo electrónico**: para proporcionar una vista más precisa de la participación real de los clientes, ahora hay disponibles nuevas métricas estimadas en los informes Recorridos, Campañas y Canal en vivo.

  * Estimated CTR (tasa de pulsaciones): se calcula como una estimación de clics en relación con la cantidad total de mensajes enviados.

  * Estimated CTOR (tasa de clics hasta la apertura): se calcula como una estimación de clics en relación con el número total de aperturas estimadas.

    Fecha de disponibilidad: 29 de julio de 2026

### Campañas {#campaigns}

+++ Próximamente

* **Complemento de rendimiento para el rendimiento en campañas activadas por API - Push** - Hay un nuevo modo de mensajería transaccional de alto rendimiento disponible en campañas activadas por API. Este modo está diseñado para la mensajería transaccional a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Antes solo estaba disponible para el canal de correo electrónico, pero ahora también lo está para el canal push, para organizaciones que han adquirido la oferta de complementos de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información. <!-- Documentation link: TBD -->

+++

### Mejoras de uso {#july-26-usability}

* **Métodos abreviados de inicio rápido en el inventario de fragmentos**: ahora puede acceder rápidamente a las acciones comunes desde la lista de fragmentos con el botón **[!UICONTROL Más acciones]**. Los métodos abreviados disponibles incluyen editar el fragmento, abrir sus detalles y descartar la versión de borrador. [Más información](../content-management/manage-fragments.md#quick-launch-fragments)

  ![](../content-management/assets/fragment-quick-launch.png)

* **Métodos abreviados de inicio rápido en el inventario de plantillas** - El botón **[!UICONTROL Más acciones]** de la lista Plantillas de contenido ahora proporciona acceso rápido a acciones comunes: editar detalles de plantilla, simular contenido y eliminar una plantilla. También hay disponibles métodos abreviados adicionales específicos del canal: para plantillas de correo electrónico, edite el cuerpo del correo electrónico, vea o envíe una prueba, ejecute un informe de correo no deseado y procese el correo electrónico; para plantillas de SMS, compruebe el recuento de caracteres y el número de segmentos. [Más información](../content-management/access-content-templates.md#edit)

  ![](../content-management/assets/content-template-quick-launch-email.png)

