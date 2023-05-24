---
product: journey optimizer
title: inSegment
description: Obtenga información sobre la función en Segmento
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, function, expression, recorrido
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 6%

---

# inSegment {#inSegment}

Comprueba si un individuo pertenece a un segmento determinado.

>[!NOTE]
>
>Puede recuperar hasta 100 segmentos.

El nombre del segmento debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión.

Los segmentos se definen en la [Adobe Experience Platform](https://platform.adobe.com/segment/overview). El editor de expresiones proporciona una lista autocompletada de segmentos.

Los segmentos pueden tener tres estados:

* existente: la entidad sigue estando en el segmento.
* realizado: la entidad se está introduciendo en el segmento.
* saliente: la entidad sale del segmento.

Solo las personas con el **Realizado** y **Existente** los estados de participación en el segmento se considerarán miembros del mismo. Para obtener más información sobre cómo evaluar un segmento, consulte la [Documentación del Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

`IF inSegment('segmentName') == true` significa que tiene una pertenencia a segmento con el estado introducido/existente.

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

La función devolverá **[!UICONTROL true]** si el individuo dentro de la instancia de recorrido es parte del segmento de Adobe Experience Platform denominado &quot;hombres mayores de 50 años&quot;, **[!UICONTROL false]** de lo contrario.
