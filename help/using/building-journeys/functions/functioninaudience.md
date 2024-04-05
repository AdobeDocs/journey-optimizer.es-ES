---
product: journey optimizer
title: inAudience
description: Obtenga información sobre la función en Audience Manager
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, función, expresión, recorrido
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---

# inAudience {#inAudience}

Comprueba si un individuo pertenece a una audiencia determinada.

>[!NOTE]
>
>Puede recuperar hasta 100 audiencias.

El nombre de la audiencia debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión.

Las audiencias se definen en la variable [Adobe Experience Platform](https://platform.adobe.com/audience/overview). El editor de expresiones proporciona una lista autocompletada de audiencias.

Las audiencias pueden tener tres estados:

* existente: la entidad sigue estando en la audiencia.
* realizado: la entidad se introduce en la audiencia.
* saliente: la entidad sale de la audiencia.

Solo las personas con el **Realizado** y **Existente** los estados de participación de la audiencia se considerarán miembros de la audiencia. Para obtener más información sobre cómo evaluar una audiencia, consulte la [Documentación del Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inAudience('audienceName') == true` significa que tiene un segmentMembership con el estado introducido/existente.

`inAudience('audienceName') == false` significa que tiene un segmentMembership del estado de salida.

## Categoría

Adobe Experience Platform

## Sintaxis de función

`inAudience(<parameter>)`

## Parámetros

| Parámetro | Descripción | Tipo |
|--- |--- |--- |
| Público | El nombre de la audiencia | `<string>` |

## Firma y tipo devuelto

`inAudience(<string>)`

Devuelve un valor booleano.

## Ejemplo

`inAudience("men over 50")`

Explicación:

La función devolverá **[!UICONTROL true]** si el individuo dentro de la instancia de recorrido es parte de la audiencia de Adobe Experience Platform denominada &quot;hombres mayores de 50 años&quot;, **[!UICONTROL false]** de lo contrario.
