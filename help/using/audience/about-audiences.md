---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de las audiencias de Adobe Experience Platform
description: Aprenda a trabajar con las audiencias de Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 298562247af79b9dd504a957c197856d702d0f6b
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 93%

---

# Introducción a las audiencias de Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audiencia "
>abstract="Al aprovechar los datos del perfil del cliente en tiempo real, Adobe Experience Platform permite generar fácilmente definiciones de segmentos para crear audiencias destinatarias que reflejen los comportamientos y preferencias únicas de sus clientes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selección de la audiencia de campaña"
>abstract="Esta lista muestra todas las audiencias de Adobe Experience Platform disponibles. Seleccione la audiencia a la que se dirige la campaña. El mensaje configurado en la campaña se envía a todas las personas que pertenecen a la audiencia seleccionada. [Más información sobre las audiencias](../audience/about-audiences.md)"

[!DNL Journey Optimizer] le permite generar y aprovechar las audiencias de Adobe Experience Platform con datos de perfil del cliente en tiempo real directamente desde el menú **[!UICONTROL audiencias]** y utilizarlos en sus recorridos o campañas.

Obtenga más información en la [documentación del Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es).

## Uso de audiencias en [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puede aprovechar las audiencias en **[!DNL Journey Optimizer]** de maneras diferentes:

* Elija una audiencia para una **campaña**, donde el mensaje se envía a todos los particulares que pertenecen a la audiencia seleccionada. [Obtenga información sobre cómo definir la audiencia de una campaña](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilice una actividad de orquestación **Leer audiencia** en un recorrido para hacer que todos los particulares de la audiencia entren en el recorrido y reciban los mensajes incluidos en el recorrido.

  Supongamos que tiene una audiencia de “clientes plata”. Con esta actividad, puede hacer que todos los “clientes plata” entren en un recorrido y se les envíe una serie de mensajes personalizados. [Obtenga información sobre cómo configurar la actividad Leer audiencia](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilice la actividad de evento **Calificación de la audiencia** en un recorrido para hacer que los particulares entren o avancen en el recorrido en función de las entradas y salidas de la audiencia de Adobe Experience Platform.

  Por ejemplo, puede hacer que todos los “clientes plata” nuevos entren en el recorrido para enviarles mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [Obtener información sobre cómo configurar una actividad Calificación de audiencia](../building-journeys/audience-qualification-events.md).

* Utilice la actividad **Condición** en un recorrido para crear condiciones basadas en el abono de la audiencia. [Aprenda a utilizar las audiencias en condiciones](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de evaluación de audiencias{#evaluation-method-in-journey-optimizer}

En Adobe Journey Optimizer, las audiencias se generan a partir de definiciones de segmentos mediante uno de los dos métodos de evaluación:

* **Segmentación de streaming**: la lista de perfiles de audiencias se mantiene actualizada en tiempo real a medida que ingresan nuevos datos al sistema.

  La segmentación de streaming es un proceso continuo de selección de datos que actualiza las audiencias en respuesta a la actividad de los usuarios. Una vez que se ha creado una definición de segmento y se ha guardado la audiencia resultante, la definición del segmento se aplica a los datos entrantes en Journey Optimizer. Esto significa que los particulares se añaden o eliminan de la audiencia a medida que cambian sus datos de perfil, lo que garantiza que el público destinatario siempre sea relevante.

* **Segmentación por lotes**: la lista de perfiles de la audiencia se evalúa cada 24 horas.

  La segmentación por lotes es una alternativa a la segmentación de streaming que procesa todos los datos de perfil a la vez mediante definiciones de segmento. Esto crea una instantánea de la audiencia que se puede guardar y exportar para su uso. Sin embargo, a diferencia de la segmentación de streaming, la segmentación por lotes no actualiza continuamente la lista de audiencias en tiempo real, y los nuevos datos que llegan después del proceso por lotes no se reflejarán en la audiencia hasta el siguiente proceso por lotes.

El sistema determina la segmentación por lotes o la segmentación de streaming para cada audiencia en función de la complejidad y el coste de evaluar la regla de definición del segmento. Puede ver el método de evaluación de cada audiencia en la columna **[!UICONTROL Método de evaluación]** de la lista de audiencias.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Si la columna **[!UICONTROL Método de evaluación]** no se muestra, debe añadirla mediante el botón de configuración en la parte superior derecha de la lista.

Una vez que haya definido una audiencia por primera vez, los perfiles se añaden cuando esta cumple los requisitos.

Rellenar la audiencia a partir de datos anteriores puede tardar hasta 24 horas. Una vez que se ha rellenado la audiencia, se mantiene actualizada continuamente y siempre está lista para la segmentación.
