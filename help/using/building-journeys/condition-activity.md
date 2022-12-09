---
solution: Journey Optimizer
product: journey optimizer
title: Actividad de condición
description: Obtenga información sobre la actividad de condición
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 0%

---

# Actividad de condición{#condition-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_condition"
>title="Actividad de condición"
>abstract="Esta actividad le permite definir cómo fluirá el individuo en el recorrido. Se crearán varias rutas basadas en distintos criterios. También puede crear una ruta alternativa en caso de tiempo de espera o error."

Estos tipos de condiciones están disponibles:

* [Condición de fuente de datos](#data_source_condition)
* [Condición horaria](#time_condition)
* [División de porcentaje](#percentage_split)
* [Condición de fecha](#date_condition)
* [Límite de perfiles](#profile_cap)

![](assets/journey49.png)

## Acerca de la actividad Condition {#about_condition}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple"
>title="Acerca del editor de expresiones simple"
>abstract="El modo de editor de expresiones simple permite realizar consultas simples basadas en una combinación de campos. Todos los campos disponibles se muestran en la parte izquierda de la pantalla. Arrastre y suelte los campos en la zona principal. Para combinar los distintos elementos, conéctelos entre sí para crear diferentes grupos o niveles de grupo. A continuación, puede seleccionar un operador lógico para combinar elementos en el mismo nivel."

Al utilizar varias condiciones en un recorrido, puede definir etiquetas para cada una de ellas para identificarlas con mayor facilidad.

Haga clic en **[!UICONTROL Add a path]** si desea definir varias condiciones. Para cada condición, se agrega una nueva ruta en el lienzo después de la actividad .

![](assets/journey47.png)

Tenga en cuenta que el diseño de los recorridos tiene un impacto funcional. Cuando se definen varias rutas después de una condición, solo se ejecuta la primera ruta elegible. Significa que puede variar la priorización de las rutas colocándolas encima o debajo de las otras.

Por ejemplo, tomemos el ejemplo de la condición de una primera ruta &quot;La persona es un VIP&quot; y la condición de una segunda ruta &quot;La persona es un hombre&quot;. Si una persona que cumple ambas condiciones (un hombre que es VIP) pasa este paso, la primera ruta se elegirá incluso si esta persona también es elegible para la segunda, porque la primera ruta es &quot;superior&quot;. Para cambiar esta prioridad, mueva las actividades en otro orden vertical.

![](assets/journey48.png)

Puede crear otra ruta para las audiencias que no cumplan los requisitos de las condiciones definidas comprobando **[!UICONTROL Show path for other cases than the one(s) above]**. Tenga en cuenta que esta opción no está disponible en condiciones de división. Consulte [División de porcentaje](#percentage_split).

El modo simple permite realizar consultas simples basadas en una combinación de campos. Todos los campos disponibles se muestran en la parte izquierda de la pantalla. Arrastre y suelte los campos en la zona principal. Para combinar los distintos elementos, conéctelos entre sí para crear diferentes grupos o niveles de grupo. A continuación, puede seleccionar un operador lógico para combinar elementos en el mismo nivel:

* Y: una intersección de dos criterios. Solo se tienen en cuenta los elementos que coinciden con todos los criterios.
* O: una unión de dos criterios. Se tienen en cuenta los elementos que coinciden con al menos uno de los dos criterios.

![](assets/journey64.png)

Si está utilizando la variable [Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;} para crear sus segmentos, puede aprovecharlos en las condiciones del recorrido. Consulte [Uso de segmentos en condiciones](../building-journeys/condition-activity.md#using-a-segment).


>[!NOTE]
>
>No puede realizar consultas en series temporales (por ejemplo, una lista de compras o clics anteriores en mensajes) con el editor simple. Para ello, debe utilizar el editor avanzado. Consulte [esta página](expression/expressionadvanced.md).

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera de continuar es marcar la casilla **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Consulte [esta sección](../building-journeys/using-the-journey-designer.md#paths).

En el editor simple, también encontrará la categoría Propiedades del recorrido , debajo de las categorías de evento y fuente de datos. Esta categoría contiene campos técnicos relacionados con el recorrido de un perfil determinado. Esta es la información que el sistema recupera de los recorridos en directo, como el ID del recorrido o los errores específicos encontrados. [Más información](expression/journey-properties.md)

## Condición de fuente de datos {#data_source_condition}

Esto le permite definir una condición basada en los campos de las fuentes de datos o en los eventos colocados previamente en el recorrido. Aprenda a utilizar el editor de expresiones en [esta sección](expression/expressionadvanced.md).

Con el editor de expresiones avanzadas, puede configurar condiciones más avanzadas para manipular colecciones o utilizar fuentes de datos que requieran el paso de parámetros. [Más información](../datasource/external-data-sources.md).

![](assets/journey50.png)

## Condición horaria{#time_condition}

Esto le permite realizar diferentes acciones según la hora del día o el día de la semana. Por ejemplo, puede decidir enviar notificaciones push durante el día y los correos electrónicos durante la noche durante la semana.

>[!NOTE]
>
>La zona horaria no es específica de una condición y se define a nivel de recorrido en las propiedades del recorrido. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey51.png)

Hay tres opciones de filtrado disponibles:

* Hora: permite configurar una condición en función de la hora del día. A continuación, defina las horas de inicio y finalización. Los individuos entrarán en la ruta solo durante el intervalo de horas definido.
* Día de la semana: permite configurar una condición en función del día de la semana. A continuación, seleccione los días en los que desea que las personas entren en la ruta.
* Día de la semana y hora: esta opción combina las dos primeras opciones.

## División de porcentaje {#percentage_split}

Esta opción le permite dividir aleatoriamente la audiencia para definir una acción diferente para cada grupo. Defina el número de divisiones y la repartición para cada ruta. El cálculo de la división es estadístico, ya que el sistema no puede anticipar cuántas personas fluirán en esta actividad del recorrido. Como resultado, la división tiene un margen de error muy bajo. Esta función se basa en un mecanismo aleatorio de Java (consulte esta [página](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html)).

En el modo de prueba, al alcanzar una división, siempre se elige la rama superior. Puede reorganizar la posición de las ramas divididas si desea que la prueba elija una ruta diferente. Consulte [esta página](../building-journeys/testing-the-journey.md)

>[!NOTE]
>
>Tenga en cuenta que no hay ningún botón para agregar una ruta en la condición de división porcentual. El número de rutas dependerá del número de divisiones. En condiciones divididas, no se puede añadir una ruta para otros casos, ya que no puede suceder. Las personas siempre irán a una de las rutas divididas.

![](assets/journey52.png)

## Condición de fecha {#date_condition}

Esto permite definir un flujo diferente en función de la fecha. Por ejemplo, si la persona introduce el paso durante el periodo de &quot;ventas&quot;, le envía un mensaje específico. El resto del año, usted enviará otro mensaje.

>[!NOTE]
>
>La zona horaria ya no es específica de una condición y ahora se define a nivel de recorrido en las propiedades del recorrido. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey53.png)

## Límite de perfiles {#profile_cap}

Utilice este tipo de condición para establecer un número máximo de perfiles para una ruta de recorrido. Cuando se alcanza este límite, los perfiles que se introducen toman una ruta alternativa. Esto garantiza que los recorridos nunca superen el límite definido.

>[!NOTE]
>
>Se recomienda definir un límite de perfil de alto valor. La precisión y la probabilidad de que una población alcance el límite exacto solo aumentan a medida que aumenta el límite máximo. Para números pequeños (por ejemplo, un límite de 50), los números no siempre coinciden, ya que es posible que no se alcance el límite antes de que los perfiles tomen una ruta alternativa.

Puede utilizar este tipo de condición para aumentar el volumen de los envíos. Consulte esta [caso de uso](ramp-up-deliveries-uc.md).

El límite predeterminado es 1000.

El contador solo se aplica a la versión del recorrido seleccionada. El contador se restablece a cero después de un mes. Después de un restablecimiento, los perfiles introducidos siguen la ruta nominal de nuevo hasta que se alcanza el límite del contador.

La ruta nominal siempre tiene prioridad sobre la ruta alternativa, incluso si se mueve la ruta alternativa por encima de la ruta nominal en el lienzo del recorrido.

Para los recorridos en directo, estos son los umbrales que se deben tener en cuenta para garantizar que se alcance el límite:

* Para un límite superior a 10000, el número de perfiles distintos que se inyectarán debe ser al menos 1,3 veces superior al límite superior.
* Para un límite inferior a 10000, el número de perfiles distintos que se inyectarán debe ser de más de 1000.

El límite del perfil no se tiene en cuenta en el modo de prueba.

![](assets/profile-cap-condition.png)

## Uso de segmentos en condiciones {#using-a-segment}

En esta sección se explica cómo utilizar un segmento en una condición de recorrido. Para obtener más información sobre los segmentos y cómo crearlos, consulte [esta sección](../segment/about-segments.md).

Para utilizar un segmento en una condición de recorrido, siga estos pasos:

1. Abra un recorrido, coloque un **[!UICONTROL Condition]** actividad y elija la **Condición de fuente de datos**.
   ![](assets/journey47.png)

1. Haga clic en **[!UICONTROL Add a path]** para cada ruta adicional necesaria. Para cada ruta, haga clic en el botón **[!UICONTROL Expression]** campo .

   ![](assets/segment3.png)

1. En el lado izquierdo, despliegue **[!UICONTROL Segments]** nodo . Arrastre y suelte el segmento que desee utilizar para su condición. De forma predeterminada, la condición del segmento es verdadera.

   ![](assets/segment4.png)

   >[!NOTE]
   >
   >Tenga en cuenta que solo las personas con la variable **Realizado** y **Existente** los estados de participación de segmentos se considerarán miembros del segmento. Para obtener más información sobre cómo evaluar un segmento, consulte la [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.
