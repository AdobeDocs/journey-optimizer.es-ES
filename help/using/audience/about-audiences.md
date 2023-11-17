---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los públicos de Adobe Experience Platform
description: Aprenda a trabajar con los públicos de Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: d3aecaefb0b356eb1d25b151e8d210620b51ea5f
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 93%

---

# Introducción a los públicos de Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Público"
>abstract="Al aprovechar los datos del perfil del cliente en tiempo real, Adobe Experience Platform permite generar fácilmente definiciones de segmentos para crear públicos destinatarios que reflejen los comportamientos y preferencias únicas de sus clientes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selección del público de la campaña"
>abstract="Esta lista muestra todos los públicos de Adobe Experience Platform disponibles. Seleccione el público al que se dirige la campaña. El mensaje configurado en la campaña se envía a todas las personas que pertenecen al público seleccionado. [Más información sobre los públicos](../audience/about-audiences.md)"

[!DNL Journey Optimizer] le permite generar y aprovechar los públicos de Adobe Experience Platform con datos de perfil del cliente en tiempo real directamente desde el menú **[!UICONTROL Públicos]** y utilizarlos en sus recorridos o campañas. Obtenga más información en la [documentación del Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es).

## Uso de públicos en [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puede seleccionar en campañas y recorridos cualquier audiencia de Adobe Experience Platform generada mediante [definiciones de segmentos](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>Además, también puede segmentar audiencias de Adobe Experience Platform creadas con [composiciones de audiencia](../audience/get-started-audience-orchestration.md) o [cargado desde un archivo CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}. Estas funcionalidades están disponibles actualmente como una versión Private Beta.

Puede aprovechar los públicos en **[!DNL Journey Optimizer]** de maneras diferentes:

* Elija un público para una **campaña**, donde el mensaje se envía a todos los particulares que pertenecen al público seleccionado. [Obtenga información sobre cómo definir el público de una campaña](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilice una actividad de orquestación **Leer público** en un recorrido para hacer que todos los particulares del público entren en el recorrido y reciban los mensajes incluidos en el recorrido.

  Supongamos que tiene un público de “clientes plata”. Con esta actividad, puede hacer que todos los “clientes plata” entren en un recorrido y se les envíe una serie de mensajes personalizados. [Obtenga información sobre cómo configurar la actividad Leer público](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilice la actividad de evento **Calificación del público** en un recorrido para hacer que los particulares entren o avancen en el recorrido en función de las entradas y salidas del público de Adobe Experience Platform.

  Por ejemplo, puede hacer que todos los “clientes plata” nuevos entren en el recorrido para enviarles mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [Obtener información sobre cómo configurar una actividad Calificación de público](../building-journeys/audience-qualification-events.md).

* Utilice la actividad **Condición** en un recorrido para crear condiciones basadas en el abono del público. [Aprenda a utilizar los públicos en condiciones](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de evaluación de públicos{#evaluation-method-in-journey-optimizer}

En Adobe Journey Optimizer, los públicos se generan a partir de definiciones de segmentos mediante uno de los dos métodos de evaluación:

* **Segmentación de streaming**: la lista de perfiles de públicos se mantiene actualizada en tiempo real a medida que ingresan nuevos datos al sistema.

  La segmentación de streaming es un proceso continuo de selección de datos que actualiza los públicos en respuesta a la actividad de los usuarios. Una vez que se ha creado una definición de segmento y se ha guardado el público resultante, la definición del segmento se aplica a los datos entrantes en Journey Optimizer. Esto significa que los particulares se añaden o eliminan del público a medida que cambian sus datos de perfil, lo que garantiza que el público destinatario siempre sea relevante.

* **Segmentación por lotes**: la lista de perfiles del público se evalúa cada 24 horas.

  La segmentación por lotes es una alternativa a la segmentación de streaming que procesa todos los datos de perfil a la vez mediante definiciones de segmento. Esto crea una instantánea del público que se puede guardar y exportar para su uso. Sin embargo, a diferencia de la segmentación de streaming, la segmentación por lotes no actualiza continuamente la lista de públicos en tiempo real, y los nuevos datos que llegan después del proceso por lotes no se reflejarán en el público hasta el siguiente proceso por lotes.

El sistema determina la segmentación por lotes o la segmentación de streaming para cada público en función de la complejidad y el coste de evaluar la regla de definición del segmento. Puede ver el método de evaluación de cada público en la columna **[!UICONTROL Método de evaluación]** de la lista de públicos.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Si la columna **[!UICONTROL Método de evaluación]** no se muestra, debe añadirla mediante el botón de configuración en la parte superior derecha de la lista.

Una vez que haya definido un público por primera vez, los perfiles se añaden cuando este cumple los requisitos.

Rellenar el público a partir de datos anteriores puede tardar hasta 24 horas. Una vez que se ha rellenado el público, se mantiene actualizado continuamente y siempre está listo para la segmentación.
