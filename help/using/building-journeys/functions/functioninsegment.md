---
product: adobe campaign
title: inSegment
description: Obtenga información sobre la función en Segment
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 6%

---

# inSegment {#inSegment}

Comprueba si una persona pertenece a un segmento determinado.

>[!NOTE]
>
>Puede recuperar hasta 100 segmentos.

El nombre del segmento debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión.

Los segmentos se definen en la [Adobe Experience Platform](https://platform.adobe.com/segment/overview). El editor de expresiones proporciona una lista de segmentos autocompletada.

Los segmentos pueden tener tres estados:

* existente: la entidad sigue estando en el segmento.
* realizado: La entidad está introduciendo el segmento.
* salida: la entidad sale del segmento.

Solo las personas con la variable **Realizado** y **Existente** los estados de participación de segmentos se considerarán miembros del segmento. Para obtener más información sobre cómo evaluar un segmento, consulte la [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

`IF inSegment('segmentName') == true` significa que tiene un segmentMembership con el estado introducido/existente.

`ELSE inSegment('segmentName') == false` significa que tiene un segmentMembership del estado de salida.

## Categoría

Adobe Experience Platform

## Sintaxis de función

`inSegment(<parameter>)`

## Parámetros

| Parámetro | Descripción | Tipo |
|--- |--- |--- |
| Segmento | El nombre del segmento | `<string>` |

## Firma y tipo devuelto

`inSegment(<string>)`

Devuelve un valor booleano.

## Ejemplo

`inSegment("men over 50")`

Explicación:

La función devolverá **[!UICONTROL true]** si la persona dentro de la instancia de recorrido forma parte del segmento de Adobe Experience Platform denominado &quot;hombres mayores de 50&quot;, **[!UICONTROL false]** en caso contrario.
