---
title: Actividad de condición
description: Learn about condition activity
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 7%

---

# Actividad de condición{#condition-activity}

Estos tipos de condiciones están disponibles:

* [Condición de fuente de datos](#data_source_condition)
* [Condición horaria](#time_condition)
* [Percentage split](#percentage_split)
* [Date condition](#date_condition)
* [Límite de perfiles](#profile_cap)

![](assets/journey49.png)

## About the Condition activity {#about_condition}

When using several conditions in a journey, you can define labels for each of them to identify them more easily.

Haga clic en **[!UICONTROL Add a path]** si desea definir varias condiciones. Para cada condición, se agrega una nueva ruta en el lienzo después de la actividad .

![](assets/journey47.png)

Tenga en cuenta que el diseño de los recorridos tiene un impacto funcional. When several paths are defined after a condition, only the first eligible path will be executed. It means that you can vary the prioritization of paths by placing them above or below one another.

For example, let&#39;s take the example of a first path&#39;s condition &quot;The person is a VIP&quot; and a second path&#39;s condition &quot;The person is a male&quot;. Si una persona que cumple ambas condiciones (un hombre que es un VIP) supera este paso, se elegirá la primera ruta aunque esta persona también sea elegible para la segunda, ya que la primera ruta es &quot;superior&quot;. Para cambiar esta prioridad, mueva las actividades en otro orden vertical.

![](assets/journey48.png)

Puede crear otra ruta para las audiencias que no cumplan los requisitos de las condiciones definidas comprobando **[!UICONTROL Show path for other cases than the one(s) above]**. Note that this option is not available in split conditions. Consulte [División de porcentaje](#percentage_split).

The simple mode allows you to perform simple queries based on a combination of fields. Todos los campos disponibles se muestran en la parte izquierda de la pantalla. Arrastre y suelte los campos en la zona principal. Para combinar los distintos elementos, conéctelos entre sí para crear diferentes grupos o niveles de grupo. A continuación, puede seleccionar un operador lógico para combinar elementos en el mismo nivel:

* Y: una intersección de dos criterios. Solo se tienen en cuenta los elementos que coinciden con todos los criterios.
* O: una unión de dos criterios. Se tienen en cuenta los elementos que coinciden con al menos uno de los dos criterios.

![](assets/journey64.png)

If you&#39;re using the [Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;} to create your segments, you can leverage them in your journey conditions. Consulte [Uso de segmentos en condiciones](../building-journeys/condition-activity.md#using-a-segment).


>[!NOTE]
>
>No puede realizar consultas en series temporales (por ejemplo, una lista de compras o clics anteriores en mensajes) con el editor simple. For this you’ll need to use the advanced editor. Consulte [documentación del Journey Orchestration de Adobe](expression/expressionadvanced.md).

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera para continuar es marcar la casilla **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Consulte [esta sección](../building-journeys/using-the-journey-designer.md#paths).

En el editor simple, también encontrará la categoría Propiedades del Recorrido, debajo de las categorías de evento y fuente de datos. Esta categoría contiene campos técnicos relacionados con el recorrido de un perfil determinado. Esta es la información recuperada por el sistema de los recorridos activos, como el ID de recorrido o los errores específicos encontrados. Para obtener más información, consulte [documentación del Journey Orchestration de Adobe](expression/journey-properties.md)

## Condición de fuente de datos {#data_source_condition}

Esto le permite definir una condición basada en los campos de las fuentes de datos o en los eventos colocados previamente en el recorrido. Para aprender a utilizar el editor de expresiones, consulte [documentación del Journey Orchestration de Adobe](expression/expressionadvanced.md). Using the advanced expression editor, you can setup more advanced conditions manipulating collections or using data sources requiring the passing of parameters. Consulte [esta página](../datasource/external-data-sources.md).

![](assets/journey50.png)

## Condición horaria{#time_condition}

This allows you to perform different actions according to the hour of the day and/or the day of the week. For example, you can decide to send SMS messages during daytime and emails at night during weekdays.

>[!NOTE]
>
>La zona horaria ya no es específica de una condición y ahora se define a nivel de recorrido en las propiedades de recorrido. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey51.png)

## División de porcentaje {#percentage_split}

Esta opción le permite dividir aleatoriamente la audiencia para definir una acción diferente para cada grupo. Defina el número de divisiones y la repartición para cada ruta. El cálculo de la división es estadístico, ya que el sistema no puede anticipar cuántas personas fluirán en esta actividad del recorrido. Como resultado, la división tiene un margen de error muy bajo. This function is based on a Java random mechanism (see this [page](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html)).

In test mode, when reaching a split, the top branch is always chosen. Puede reorganizar la posición de las ramas divididas si desea que la prueba elija una ruta diferente. Consulte [esta página](../building-journeys/testing-the-journey.md)

>[!NOTE]
>
>Tenga en cuenta que no hay ningún botón para agregar una ruta en la condición de división porcentual. El número de rutas dependerá del número de divisiones. En condiciones divididas, no se puede añadir una ruta para otros casos, ya que no puede suceder. People will always go into one of the split paths.

![](assets/journey52.png)

## Condición de fecha {#date_condition}

This allows you to define a different flow based on the date. Por ejemplo, si la persona introduce el paso durante el periodo de &quot;ventas&quot;, le envía un mensaje específico. El resto del año, usted enviará otro mensaje.

>[!NOTE]
>
>La zona horaria ya no es específica de una condición y ahora se define a nivel de recorrido en las propiedades de recorrido. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey53.png)

## Límite de perfiles {#profile_cap}

Utilice este tipo de condición para establecer un número máximo de perfiles para una ruta de recorrido. Cuando se alcanza este límite, los perfiles que se introducen toman una ruta alternativa. This ensures that your journeys will never exceed the limit defined.

Puede utilizar este tipo de condición para aumentar el volumen de los envíos. Consulte esta [caso de uso](ramp-up-deliveries-uc.md).

The default cap is 1000.

El contador solo se aplica a la versión de recorrido seleccionada. El contador se restablece a cero después de un mes. Después de un restablecimiento, los perfiles introducidos siguen la ruta nominal de nuevo hasta que se alcanza el límite del contador.

La ruta nominal siempre tiene prioridad sobre la ruta alternativa, incluso si se mueve la ruta alternativa por encima de la ruta nominal en el lienzo de recorrido.

Para los recorridos activos, estos son los umbrales que se deben tener en cuenta para garantizar que se alcance el límite:

* Para un máximo bueno a 10000, el número de perfiles diferentes que se inyectarán debe ser al menos 1,3 veces superior al límite máximo.
* Para un límite inferior a 10000, el número de perfiles distintos que se inyectarán debe ser de 1000 más el límite.

El límite del perfil no se tiene en cuenta en el modo de prueba.

![](assets/profile-cap-condition.png)

## Uso de segmentos en condiciones {#using-a-segment}

En esta sección se explica cómo utilizar un segmento en una condición de recorrido. For more on segments and how to build them, refer to [this section](../segment/about-segments.md).

Para utilizar un segmento en una condición de recorrido, siga estos pasos:

1. Abra un recorrido y suelte un **[!UICONTROL Condition]** actividad y elija la **Condición de fuente de datos**.
   ![](assets/journey47.png)

1. Haga clic en **[!UICONTROL Add a path]** para cada ruta adicional necesaria. Para cada ruta, haga clic en el botón **[!UICONTROL Expression]** campo .

   ![](assets/segment3.png)

1. En el lado izquierdo, despliegue **[!UICONTROL Segments]** nodo . Arrastre y suelte el segmento que desee utilizar para su condición. De forma predeterminada, la condición del segmento es verdadera.

   ![](assets/segment4.png)

   >[!NOTE]
   >
   >Note that only the individuals with the **Realized** and **Existing** segment participation statuses will be considered as members of the segment. Para obtener más información sobre cómo evaluar un segmento, consulte la [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.
