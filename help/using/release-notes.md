---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
source-git-commit: 0fb6d8f611a849696d83e0f129e6462431e5fe83
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 24%

---


# Notas de la versión {#release-notes}

Esta página lista todas las nuevas funciones y mejoras de Journey Optimizer.
También puede consultar las últimas [Actualizaciones de documentación](documentation-updates.md).

## Versión de julio de 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Aprovechar las relaciones de esquema</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform le permite definir relaciones entre esquemas para utilizar un conjunto de datos como una tabla de búsqueda para otro. Journey Optimizer ahora puede aprovechar los datos procedentes de un esquema vinculado.</p>
<p>Estos campos están disponibles en la configuración de eventos unitarios, las condiciones de recorrido, la personalización de mensajes y la personalización de acciones personalizadas.
<p>Para obtener más información, consulte la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

* La tasa de regulación general de todos los segmentos de lectura que se ejecutan simultáneamente en el mismo entorno limitado está limitada a 17.000 mensajes por segundo. [Más información](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* El campo **Cache duration** se ha eliminado del panel de configuración del origen de datos. [Más información](datasource/about-data-sources.md)
* Para las fuentes de datos externas, ahora se define automáticamente una regla de límite de 15 llamadas por segundo. [Más información](configuration/external-systems.md#capping)
* En el caso de los recorridos activos, la pantalla de propiedades de recorrido ahora muestra la fecha de publicación y el nombre del usuario que publicó el recorrido. [Más información](building-journeys/journey-gs.md#change-properties)
* En la pantalla de la lista de recorridos, se ha añadido el filtro de tipo de recorrido. [Más información](user-interface.md#section_lgm_hpz_pgb)
* El parámetro [!UICONTROL Throttling rate] se ha agregado en la actividad Leer segmento . [Más información](building-journeys/read-segment.md#configuring-segment-trigger-activity)
