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
source-git-commit: 0ccd65f3e2f37c7893e81ab0a94ee4842cd4565d
workflow-type: tm+mt
source-wordcount: 1045
ht-degree: 38%

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

## Notas de la versión de julio de 2026 {#july-26-updates}

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

* [!BADGE Desaprobación]{type=Negative} audiencias por lotes ya no se admiten en el nodo Calificación de audiencias: a partir del 3 de agosto de 2026, Journey Optimizer bloqueará la publicación de cualquier recorrido que utilice una audiencia por lotes en un nodo Calificación de audiencias. Esta aplicación reemplaza la advertencia de lienzo introducida en la versión de junio. Los recorridos en directo existentes no se ven afectados. Utilice una audiencia de flujo continuo en el nodo Calificación de audiencias o cambie a una actividad Leer audiencia. [Aprenda a migrar sus recorridos](../building-journeys/aq-batch-audiences-migration.md)

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

### Gestión de contenidos {#july-26-content}

En esta versión se han añadido las siguientes funcionalidades y mejoras a la administración de contenido.

* **Métodos abreviados de inicio rápido en el inventario de fragmentos**: ahora puede acceder rápidamente a las acciones comunes desde la lista de fragmentos con el botón **[!UICONTROL Más acciones]**. Los métodos abreviados disponibles incluyen editar el fragmento, abrir sus detalles y descartar la versión de borrador. [Más información](../content-management/manage-fragments.md#quick-launch-fragments)

  ![](../content-management/assets/fragment-quick-launch.png)

* **Métodos abreviados de inicio rápido en el inventario de plantillas** - El botón **[!UICONTROL Más acciones]** de la lista Plantillas de contenido ahora proporciona acceso rápido a acciones comunes: editar detalles de plantilla, simular contenido y eliminar una plantilla. En el caso de las plantillas de correo electrónico, los métodos abreviados adicionales permiten editar la línea de asunto y el cuerpo del correo electrónico, ver o enviar una prueba, ejecutar un informe de correo no deseado y procesar el correo electrónico. [Más información](../content-management/access-content-templates.md#quick-launch-templates)

  ![](../content-management/assets/content-template-quick-launch.png)

### Canal de correo electrónico {#july-26-email}

En esta versión se han añadido las siguientes mejoras al canal de correo electrónico.

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

### Contenido e integraciones {#july-26-integration}

Las siguientes funcionalidades y mejoras estarán disponibles en la gestión de contenidos e integraciones en esta versión.

* Atributos personalizados dinámicos de **elementos de decisión**: los atributos personalizados de elementos de decisión ahora se pueden personalizar en el momento de la entrega mediante datos de perfil, contextuales y de audiencia. Esto elimina la necesidad de mantener ofertas duplicadas para variaciones de contenido menores, lo que permite a los especialistas en marketing administrar menos elementos de decisión más flexibles. [Más información](../experience-decisioning/items.md#attributes)

  Fecha de disponibilidad: 27 de julio de 2026

* **Nuevas herramientas del servidor MCP de AJO**: el servidor MCP de [!DNL Adobe Journey Optimizer] ahora expone cinco **herramientas de configuración de canal** de solo lectura adicionales, lo que le permite consultar las configuraciones de canal, los recursos de soporte y las acciones de marketing directamente desde su asistente de IA. Ahora puede usar **Configuraciones de canal de lista** (en todos los canales de AJO), **Obtener configuración de canal**, **Enumerar recursos de configuración**, **Obtener recurso de configuración** y **Enumerar acciones de marketing**. [Más información](../integrations/ajo-mcp.md#mcp-tools)

  Fecha de disponibilidad: 9 de julio de 2026

### Administración {#july-26-administration}

En esta versión se han añadido las siguientes mejoras a la administración y la gestión de datos.

* **Protección de tiempo de vida de conjunto de datos (TTL) — zonas protegidas existentes** - La protección de tiempo de vida (TTL) para conjuntos de datos generados por el sistema de Journey Optimizer (90 días en el almacén de perfiles, 13 meses en el lago de datos) se aplicará en **zonas protegidas y organizaciones de clientes existentes** a partir del **1 de octubre de 2026**. [Más información](../data/datasets-ttl.md#ttl-guardrail)


