---
title: Acerca de los segmentos de Adobe Experience Platform
description: Obtenga información sobre cómo configurar un segmento de Adobe Experience Platform
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 2d882b8d10cc642b04705dd924fd2b129f4f78ac
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 3%

---

# Introducción a los segmentos {#about-segments}

[!DNL Journey Optimizer] le permite crear segmentos de Adobe Experience Platform utilizando datos de perfil de cliente en tiempo real directamente desde el  **[!UICONTROL Segments]** menú y aprovecharlos en sus recorridos.

Tenga en cuenta que los segmentos también se pueden crear desde el propio servicio de Segmentación. Obtenga más información en la [documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.

Puede aprovechar los segmentos en los recorridos de diferentes maneras:

* Utilice una actividad de organización **Read segment** para hacer que todas las personas que pertenecen al segmento especificado entren en el recorrido. Los mensajes incluidos en el recorrido se envían a las personas pertenecientes al segmento. Supongamos que tiene un segmento &quot;cliente plata&quot;. Con esta actividad, puede hacer que todos los clientes plata introduzcan un recorrido y envíen una serie de mensajes personalizados.

   Para obtener más información sobre cómo utilizar la actividad **[!UICONTROL Read segment]**, consulte [esta sección](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilice la actividad de evento **Segment qualification** para que los individuos entren o avancen en un recorrido en función de las entradas y salidas de segmentos de Adobe Experience Platform. Por ejemplo, puede hacer que todos los clientes nuevos de plata introduzcan un recorrido y envíen mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [esta sección](../building-journeys/segment-qualification-events.md).

* Cree **condiciones complejas** en sus recorridos con el editor de expresiones simple o avanzado. Obtenga más información en [esta sección](../building-journeys/condition-activity.md#using-a-segment).
