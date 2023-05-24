---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de calificación de segmentos
description: Obtenga información sobre los eventos de calificación de segmentos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: calificación, eventos, segmento, recorrido, plataforma
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 10%

---

# Eventos de calificación de segmentos {#segment-qualification}

## Acerca de los eventos de calificación de segmentos{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Eventos de cualificación de segmentos"
>abstract="Esta actividad permite realizar un recorrido para escuchar las entradas y salidas de perfiles en segmentos de Adobe Experience Platform para que los particulares entren o avancen en un recorrido."

Esta actividad permite realizar un recorrido para escuchar las entradas y salidas de perfiles en segmentos de Adobe Experience Platform para que los particulares entren o avancen en un recorrido. Para obtener más información sobre la creación de segmentos, consulte [sección](../segment/about-segments.md).

Supongamos que tiene un segmento llamado &quot;cliente plata&quot;. Con esta actividad, puede hacer que todos los clientes nuevos de Silver Ingresen a un recorrido y les envíen una serie de mensajes personalizados.

Este tipo de evento se puede colocar como primer paso o más tarde en el recorrido.

>[!IMPORTANT]
>
>Tenga en cuenta que los segmentos de Adobe Experience Platform se calculan una vez al día (**lote** segmentos) o en tiempo real (**transmitido** mediante la opción Audiencias de alta frecuencia de Adobe Experience Platform).
>
>Si el segmento seleccionado se transmite, las personas que pertenecen a este segmento potencialmente ingresarán al recorrido en tiempo real. Si el segmento es por lotes, las personas recién cualificadas para este segmento potencialmente ingresarán al recorrido cuando el cálculo del segmento se ejecute en Adobe Experience Platform.
>
>Los grupos de campos de eventos de experiencia no se pueden utilizar en recorridos que comiencen por un segmento de lectura, una calificación de segmentos o una actividad de evento empresarial.


1. Despliegue el **[!UICONTROL Eventos]** categoría y soltar una **[!UICONTROL Calificación de segmentos]** actividad en el lienzo.

   ![](assets/segment5.png)

1. Añadir un **[!UICONTROL Etiqueta]** a la actividad. Este paso es opcional.

1. Haga clic en en **[!UICONTROL Segmento]** y seleccione los segmentos que desee aprovechar.

   >[!NOTE]
   >
   >Tenga en cuenta que puede personalizar las columnas mostradas en la lista y ordenarlas.

   ![](assets/segment6.png)

   Una vez agregado el segmento, la variable **[!UICONTROL Copiar]** permite copiar su nombre y su ID:

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. En el **[!UICONTROL Comportamiento]** , elija si desea escuchar las entradas del segmento, las salidas o ambos.

   >[!NOTE]
   >
   >Tenga en cuenta que **[!UICONTROL Entrar]** y **[!UICONTROL Salir]** corresponde a la **Realizado** y **cerrado** estados de participación de segmentos de Adobe Experience Platform. Para obtener más información sobre cómo evaluar un segmento, consulte la [Documentación del Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. Seleccione un área de nombres. Esto solo es necesario si el evento se coloca como el primer paso del recorrido. De forma predeterminada, el campo está rellenado previamente con el último área de nombres utilizado.

   >[!NOTE]
   >
   >Solo puede seleccionar un área de nombres de identidad basada en personas. Si ha definido un área de nombres para una tabla de búsqueda (por ejemplo: área de nombres ProductID para una búsqueda Product), no estará disponible en la **Área de nombres** lista desplegable.

   ![](assets/segment7.png)

La carga útil contiene la siguiente información de contexto, que puede utilizar en condiciones y acciones:

* el comportamiento (entrada, salida)
* la marca de tiempo de la calificación
* el id del segmento

Cuando se utiliza el editor de expresiones en una condición o acción que sigue a **[!UICONTROL Calificación de segmentos]** actividad, tiene acceso a la **[!UICONTROL Calificación de segmentos]** nodo. Puede elegir entre las **[!UICONTROL Última hora de clasificación]** y el **[!UICONTROL status]** (entrada o salida).

Consulte [Actividad de condición](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Un nuevo recorrido que incluye un evento de calificación de segmentos está en funcionamiento diez minutos después de su publicación. Este intervalo de tiempo corresponde al intervalo de actualización de caché del servicio dedicado. Por lo tanto, debe esperar diez minutos antes de utilizar este recorrido.

## Prácticas recomendadas {#best-practices-segments}

El **[!UICONTROL Calificación de segmentos]** La actividad de permite la entrada inmediata en recorridos de personas que se califican o descalifican de un segmento de Adobe Experience Platform.

La velocidad de recepción de esta información es alta. Las mediciones realizadas muestran una velocidad de 10 000 eventos recibidos por segundo. Como resultado, debe asegurarse de comprender cómo pueden producirse los picos de entrada, cómo evitarlos y cómo preparar su recorrido para ellos.

### Segmentos por lotes{#batch-speed-segment-qualification}

Cuando utilice la calificación de segmentos para un segmento de lote, tenga en cuenta que se producirá un pico de entrada en el momento del cálculo diario. El tamaño del pico dependerá del número de individuos que entren (o salgan) del segmento diariamente.

Además, si el segmento de lote se crea recientemente y se utiliza inmediatamente en un recorrido, el primer lote de cálculo puede hacer que un gran número de personas entren en el recorrido.

### Segmentos transmitidos{#streamed-speed-segment-qualification}

Cuando se utiliza la calificación de segmentos para segmentos transmitidos, hay menos riesgo de obtener grandes picos de entradas/salidas debido a la evaluación continua del segmento. Sin embargo, si la definición del segmento conduce a que un gran volumen de clientes cumpla los requisitos al mismo tiempo, puede haber un pico también.

Para obtener más información sobre la segmentación de flujo continuo, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### Cómo evitar sobrecargas{#overloads-speed-segment-qualification}

Estas son algunas prácticas recomendadas que ayudarán a evitar la sobrecarga de sistemas aprovechados en los recorridos (fuentes de datos, acciones personalizadas, actividades de acción del canal).

No use, en un **[!UICONTROL Calificación de segmentos]** actividad, un segmento por lotes inmediatamente después de su creación. Evitará el primer pico de cálculo. Tenga en cuenta que si está a punto de usar un segmento que nunca se ha calculado, aparecerá una advertencia amarilla en el lienzo de recorrido.

![](assets/segment-error.png)

Establezca una regla de límite para las fuentes de datos y las acciones utilizadas en los recorridos para evitar sobrecargarlos. Obtenga más información en [Documentación del Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. Tenga en cuenta que la regla de límite no tiene reintento. Si necesita volver a intentarlo, debe utilizar una ruta alternativa en el recorrido marcando la casilla **[!UICONTROL Añadir una ruta alternativa en caso de tiempo de espera o error]** en condiciones o acciones.

Antes de usar el segmento en un recorrido de producción, evalúe siempre primero el volumen de personas que cumplen los requisitos para este segmento todos los días. Para ello, puede consultar la **[!UICONTROL Segmentos]** , abra el segmento y observe la variable **[!UICONTROL Perfiles a lo largo del tiempo]** gráfico.

![](assets/segment-overload.png)
