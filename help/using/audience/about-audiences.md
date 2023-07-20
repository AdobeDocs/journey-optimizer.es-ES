---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de las audiencias de Adobe Experience Platform
description: Aprenda a trabajar con audiencias de Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 5%

---

# Introducción a las audiencias de Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audiencia "
>abstract="Al aprovechar los datos del perfil del cliente en tiempo real, Adobe Experience Platform permite generar fácilmente definiciones de segmentos para crear públicos destinatarios que reflejen los comportamientos y las preferencias únicos de sus clientes."

[!DNL Journey Optimizer] le permite crear y aprovechar las audiencias de Adobe Experience Platform con datos de perfil del cliente en tiempo real directamente desde el **[!UICONTROL Audiencias]** y utilícelos en sus recorridos o campañas.

Obtenga más información en la [Documentación del Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Uso de audiencias en [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puede aprovechar las audiencias de en **[!DNL Journey Optimizer]** de diferentes maneras:

* Elija una audiencia para una **campaña**, donde el mensaje se envía a todas las personas que pertenecen a la audiencia seleccionada. [Obtenga información sobre cómo definir la audiencia de una campaña](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilice un **Leer audiencia** actividad de orquestación en un recorrido para hacer que todas las personas de la audiencia entren en el recorrido y reciban los mensajes incluidos en el recorrido.

  Supongamos que tiene una audiencia &quot;cliente plata&quot;. Con esta actividad, puede hacer que todos los clientes de plata entren en un recorrido y les envíen una serie de mensajes personalizados. [Obtenga información sobre cómo configurar una actividad de audiencia de lectura](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilice el **Calificación de audiencia** actividad de evento en un recorrido para hacer que los individuos entren o avancen en el recorrido en función de las entradas y salidas de audiencia de Adobe Experience Platform.

  Por ejemplo, puede hacer que todos los clientes nuevos de Silver introduzcan un recorrido y les envíen mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [Obtenga información sobre cómo configurar una actividad de calificación de audiencias](../building-journeys/audience-qualification-events.md).

* Utilice el **Condición** actividad en un recorrido para crear condiciones basadas en la pertenencia a audiencias. [Aprenda a utilizar audiencias en condiciones](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de evaluación de audiencia{#evaluation-method-in-journey-optimizer}

En Adobe Journey Optimizer, las audiencias se generan a partir de definiciones de segmentos mediante uno de los dos métodos de evaluación:

* **Segmentación de streaming**: la lista de perfiles de la audiencia se mantiene actualizada en tiempo real a medida que ingresan nuevos datos al sistema.

  La segmentación por streaming es un proceso de selección de datos continuo que actualiza las audiencias en respuesta a la actividad del usuario. Una vez que se ha creado una definición de segmento y se ha guardado la audiencia resultante, la definición del segmento se aplica a los datos entrantes en Journey Optimizer. Esto significa que las personas se añaden o eliminan de la audiencia a medida que cambian los datos de perfil, lo que garantiza que la audiencia de destino siempre sea relevante.

* **Segmentación por lotes**: la lista de perfiles de la audiencia se evalúa cada 24 horas.

  La segmentación por lotes es una alternativa a la segmentación por secuencias que procesa todos los datos de perfil a la vez mediante definiciones de segmento. Esto crea una instantánea de la audiencia que se puede guardar y exportar para su uso. Sin embargo, a diferencia de la segmentación por secuencias, la segmentación por lotes no actualiza continuamente la lista de audiencias en tiempo real, y los nuevos datos que llegan después del proceso por lotes no se reflejarán en la audiencia hasta el siguiente proceso por lotes&quot;.

El sistema determina la segmentación por lotes y la segmentación por flujo continuo para cada audiencia en función de la complejidad y el coste de evaluar la regla de definición del segmento. Puede ver el método de evaluación de cada audiencia en la **[!UICONTROL Método de evaluación]** de la lista de audiencias.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Si la variable **[!UICONTROL Método de evaluación]** no se muestra, debe añadirla mediante el botón de configuración en la parte superior derecha de la lista.

Una vez que haya definido una audiencia por primera vez, los perfiles se añaden a la audiencia cuando cumplen los requisitos.

Realizar una copia de seguridad de la audiencia a partir de datos anteriores puede tardar hasta 24 horas. Una vez que la audiencia se ha rellenado, se mantiene actualizada continuamente y siempre está lista para la segmentación.
