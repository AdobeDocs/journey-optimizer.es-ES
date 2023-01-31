---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los segmentos de Adobe Experience Platform
description: Obtenga información sobre cómo configurar un segmento de Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Introducción a los segmentos de Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  le permite crear segmentos de Adobe Experience Platform utilizando datos de perfil de cliente en tiempo real directamente desde el **[!UICONTROL Segmentos]** y utilícelos en sus recorridos o campañas.

Además, los segmentos también se pueden crear desde el propio servicio de Segmentación. Obtenga más información en la [Documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Usar segmentos en [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puede aprovechar los segmentos en **[!DNL Journey Optimizer]** de diferentes maneras:

* Elija un segmento como el **audiencia para una campaña**, donde el mensaje se envía a todas las personas que pertenecen al segmento seleccionado. [Aprenda a definir la audiencia de una campaña](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilice un **Leer segmento** actividad de organización en un recorrido para que todas las personas del segmento entren en el recorrido y reciban los mensajes incluidos en el recorrido.

   Supongamos que tiene un segmento &quot;cliente plata&quot;. Con esta actividad, puede hacer que todos los clientes plata introduzcan un recorrido y envíen una serie de mensajes personalizados. [Obtenga información sobre cómo configurar una actividad de segmento de lectura](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilice la variable **Clasificación del segmento** actividad de evento en un recorrido para hacer que las personas entren o avancen en el recorrido en función de las entradas y salidas de segmentos de Adobe Experience Platform.

   Por ejemplo, puede hacer que todos los clientes nuevos de plata introduzcan un recorrido y envíen mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [Obtenga información sobre cómo configurar una actividad de calificación de segmentos](../building-journeys/segment-qualification-events.md).

* Utilice la variable **Condición** actividad en un recorrido para crear condiciones basadas en la pertenencia a un segmento. [Aprenda a utilizar segmentos en condiciones](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de evaluación de audiencia{#evaluation-method-in-journey-optimizer}

En Adobe Journey Optimizer, las audiencias se generan a partir de definiciones de segmentos mediante uno de los dos métodos de evaluación siguientes:

* **Segmentación por transmisión**: La lista de audiencia del segmento se mantiene actualizada en tiempo real a medida que los nuevos datos entran en el sistema.

   La segmentación por transmisión es un proceso continuo de selección de datos que actualiza los segmentos en respuesta a la actividad del usuario. Una vez que se ha creado y guardado un segmento, la definición del segmento se aplica a los datos entrantes en Journey Optimizer. Esto significa que se agregan o eliminan personas del segmento a medida que cambian los datos de perfil, lo que garantiza que la audiencia de destino siempre sea relevante.

* **Segmentación por lotes**: La lista de audiencia del segmento se evalúa cada 24 horas.

   La segmentación por lotes es una alternativa a la segmentación por flujo continuo que procesa todos los datos de perfil a la vez mediante definiciones de segmentos. Esto crea una instantánea de la audiencia que se puede guardar y exportar para su uso. Sin embargo, a diferencia de la segmentación de flujo continuo, la segmentación por lotes no actualiza continuamente la lista de audiencias en tiempo real, y los nuevos datos que llegan después del proceso por lotes no se reflejarán en el segmento hasta el siguiente proceso por lotes&quot;.

El sistema determina la segmentación por lotes y la segmentación de flujo continuo para cada definición de segmento, en función de la complejidad y el coste de la evaluación de la regla de segmento. Puede ver el método de evaluación para cada segmento en la **[!UICONTROL Método de evaluación]** de la lista de segmentos.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Si la variable **[!UICONTROL Método de evaluación]** no se muestra, debe agregarla con el botón de configuración en la parte superior derecha de la lista.

Después de haber definido un segmento por primera vez, los perfiles se añaden a la audiencia cuando cumplen los requisitos.

Rellenar la audiencia a partir de datos anteriores puede tardar hasta 24 horas. Una vez que la audiencia se ha rellenado, se mantiene actualizada de forma continua y siempre está lista para la segmentación.
