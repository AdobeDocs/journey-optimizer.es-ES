---
product: journey optimizer
title: inAudience
description: Obtenga información sobre la función en Audience Manager
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, función, expresión, recorrido
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 85a8d0713f87a8b3505a2294402156ba6598c8bb
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 6%

---

# inAudience {#inAudience}

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

`inAudience('audienceName') == true` significa que tiene un segmentMembership con el estado introducido.

`inAudience('audienceName') == false` significa que usted tiene un segmentMembership del estado saliente.

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

La función devolverá **[!UICONTROL true]** si el individuo de la instancia de recorrido es parte de la audiencia de Adobe Experience Platform denominada &quot;hombres de más de 50 años&quot;, **[!UICONTROL false]** en caso contrario.
