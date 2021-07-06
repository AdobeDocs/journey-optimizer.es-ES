---
title: Acerca de los segmentos de Adobe Experience Platform
description: Obtenga información sobre cómo configurar un segmento de Adobe Experience Platform
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 9e93a97ff793fec9fdf4aecd645f1df95b65b31a
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 2%

---

# Acerca de los segmentos de Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  le permite crear segmentos de Adobe Experience Platform utilizando datos de perfil de cliente en tiempo real directamente desde el  **[!UICONTROL Segments]** menú y aprovecharlos en sus recorridos.

Tenga en cuenta que los segmentos también se pueden crear desde el propio servicio de Segmentación. Obtenga más información en la [documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Puede aprovechar los segmentos en los recorridos de diferentes maneras:

* Utilice una actividad de organización **Read segment** para hacer que todas las personas que pertenecen al segmento especificado entren en el recorrido. Los mensajes incluidos en el recorrido se envían a las personas pertenecientes al segmento. Supongamos que tiene un segmento &quot;cliente plata&quot;. Con esta actividad, puede hacer que todos los clientes plata introduzcan un recorrido y envíen una serie de mensajes personalizados.

   Para obtener más información sobre cómo utilizar la actividad **[!UICONTROL Read segment]**, consulte [esta sección](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilice la actividad de evento **Segment qualification** para que los individuos entren o avancen en un recorrido en función de las entradas y salidas de segmentos de Adobe Experience Platform. Por ejemplo, puede hacer que todos los clientes nuevos de plata introduzcan un recorrido y envíen mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [esta sección](../building-journeys/segment-qualification-events.md).

* Cree **condiciones complejas** en sus recorridos con el editor de expresiones simple o avanzado. Obtenga más información en [esta sección](../building-journeys/condition-activity.md#using-a-segment).

## Método de evaluación en Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

En Adobe Journey Optimizer, las audiencias se generan a partir de definiciones de segmentos mediante uno de estos métodos de evaluación:

* Segmentación por transmisión: la lista de audiencia del segmento se mantiene actualizada en tiempo real mientras los nuevos datos fluyen al sistema.
* Segmentación por lotes: la lista de audiencia del segmento se actualiza cada hora, según los datos que hayan llegado en la hora anterior.

El sistema determina la segmentación por lotes y la segmentación de flujo continuo para cada definición de segmento, en función de la complejidad y el coste de la evaluación de la regla de segmento.

Puede ver el método de evaluación para cada segmento en la columna **[!UICONTROL Evaluation method]** de la lista de segmentos.

Después de haber definido un segmento por primera vez, los perfiles se añaden a la audiencia cuando cumplen los requisitos.

Rellenar la audiencia a partir de datos anteriores puede tardar hasta 24 horas. Una vez que la audiencia se ha rellenado, se mantiene actualizada de forma continua y siempre está lista para la segmentación.
