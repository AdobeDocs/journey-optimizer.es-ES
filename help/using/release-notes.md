---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
source-git-commit: cd38b6ec9be0417f5c65e37805c0e7b072d1cb96
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 16%

---


# Notas de la versión {#release-notes}

Esta página lista todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar las últimas [Actualizaciones de documentación](documentation-updates.md).

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
<p>Adobe Experience Platform le permite definir relaciones entre esquemas para utilizar un conjunto de datos como una tabla de búsqueda para otro. [!DNL Journey Optimizer] ahora puede aprovechar los datos procedentes de un esquema vinculado.</p>
<p>Estos campos están disponibles en la configuración de eventos unitarios, las condiciones de recorrido, la personalización de mensajes y la personalización de acciones personalizadas.</p>
<p>Para obtener más información, consulte la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lista de permitidos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir una lista específica de seguridad de envío a nivel de entorno limitado para disponer de un entorno seguro para realizar pruebas. En una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a sus clientes. Esta función se habilita aprovechando las API de supresión.</p>
<p>Para obtener más información, consulte la <a href="allow-list.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

* **Journeys**
   * La tasa de regulación general de todos los segmentos de lectura que se ejecutan simultáneamente en el mismo entorno limitado está limitada a 17.000 mensajes por segundo. [Más información](building-journeys/read-segment.md#configuring-segment-trigger-activity)
   * El campo **Cache duration** se ha eliminado del panel de configuración del origen de datos. [Más información](datasource/about-data-sources.md)
   * Para las fuentes de datos externas, ahora se define automáticamente una regla de límite de 15 llamadas por segundo. [Más información](configuration/external-systems.md#capping)
   * En el caso de los recorridos activos, la pantalla de propiedades de recorrido ahora muestra la fecha de publicación y el nombre del usuario que publicó el recorrido. [Más información](building-journeys/journey-gs.md#change-properties)
   * En la pantalla de la lista de recorridos, se ha añadido el filtro de tipo de recorrido. [Más información](user-interface.md#section_lgm_hpz_pgb)
   * El parámetro **[!UICONTROL Throttling rate]** se ha agregado en la actividad Leer segmento . [Más información](building-journeys/read-segment.md#configuring-segment-trigger-activity)

* **Vista previa y prueba**
   * La identidad y el área de nombres ahora están visibles en la pantalla **[!UICONTROL Preview]**. [Más información](preview.md#preview-your-messages)
   * El número de correos electrónicos de prueba para pruebas ahora está restringido a 10.
   * Los caracteres permitidos para el **Subject line prefix** en las pruebas ahora están limitados. [Más información](preview.md#send-proofs)

* **Editor de expresiones de personalización**
   * Se ha cambiado el nombre de la lista desplegable de ayuda y se ha reorganizado.

### Correcciones

* Se ha corregido un problema que hacía que se enviaran mensajes duplicados para la entrega por lotes de correo electrónico.
* Los eventos ahora se generan de forma acorde cuando el envío de correo electrónico no se realiza una vez finalizado el periodo de reintento.
* Se ha corregido un problema por el que faltaba información de IP en la pantalla Registros de PTR .
* Ya está implementada la localización en el carril de la oferta dentro del Editor de expresiones.
* Se ha corregido un espaciado incorrecto en las ventanas emergentes de información.
