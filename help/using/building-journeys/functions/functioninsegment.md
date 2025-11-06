---
product: journey optimizer
title: inSegment
description: Obtenga información sobre la función en Segmento
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, function, expression, recorrido
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 6%

---

# inSegment {#inSegment}

Comprueba si un individuo pertenece a una audiencia determinada.

>[!NOTE]
>
>Puede recuperar hasta 100 audiencias.

El nombre de la audiencia debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión.

Las audiencias se definen en [Adobe Experience Platform](https://platform.adobe.com/audience/overview). El editor de expresiones proporciona una lista autocompletada de audiencias.

Las audiencias pueden tener dos estados:

* realizado: la entidad cumple los requisitos para la definición del segmento.
* saliente: la entidad sale de la definición del segmento.

Solo las personas con el estado de participación de audiencia **Realized** se considerarán miembros de la audiencia. Para obtener más información sobre cómo evaluar una audiencia, consulte la [documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inSegment('segmentName') == true` significa que tiene un segmentMembership con el estado introducido/existente.

`inSegment('segmentName') == false` significa que usted tiene un segmentMembership del estado saliente.

## Categoría

Adobe Experience Platform

## Sintaxis de función

`inSegment(<parameter>)`

## Parámetros

| Parámetro | Descripción | Tipo |
|--- |--- |--- |
| Segmento | El nombre de la audiencia | `<string>` |

## Firma y tipo devuelto

`inSegment(<string>)`

Devuelve un valor booleano.

## Ejemplo

`inSegment("men over 50")`

Explicación:

La función devolverá **[!UICONTROL true]** si el individuo de la instancia de recorrido es parte de la audiencia de Adobe Experience Platform denominada &quot;hombres de más de 50 años&quot;, **[!UICONTROL false]** en caso contrario.
