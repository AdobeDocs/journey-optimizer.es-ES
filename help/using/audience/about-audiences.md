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
source-git-commit: be05bb72ace2e2084675f4278501a520d592e304
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 17%

---


# Introducción a los públicos {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Público"
>abstract="Al aprovechar los datos del perfil del cliente en tiempo real, Adobe Experience Platform permite generar fácilmente definiciones de segmentos para crear públicos destinatarios que reflejen los comportamientos y preferencias únicas de sus clientes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selección del público de la campaña"
>abstract="Esta lista muestra todos los públicos de Adobe Experience Platform disponibles. Seleccione el público al que se dirige la campaña. El mensaje configurado en la campaña se envía a todas las personas que pertenecen al público seleccionado. [Más información sobre los públicos](../audience/about-audiences.md)"

Las audiencias son colecciones de personas que comparten comportamientos o características similares. Se configuran y mantienen de forma centralizada en Adobe Experience Platform mediante el servicio de segmentación de Adobe Experience Platform y son fácilmente accesibles desde Journey Optimizer para su activación en recorridos y campañas.

Adobe Journey Optimizer proporciona herramientas sólidas para crear, administrar y enriquecer audiencias a fin de mejorar los esfuerzos de marketing. Cuando se combina con Adobe Real-Time Customer Data Platform, Journey Optimizer le permite crear capas de audiencias para una segmentación más compleja y compartir audiencias bidireccionalmente con otras soluciones de Adobe Experience Cloud.

A medida que se producen flujos de datos en tiempo real o cargas por lotes, los conjuntos de datos se actualizan y Journey Optimizer mueve dinámicamente a los individuos dentro y fuera de las audiencias y los recorridos en tiempo real.

>[!BEGINSHADEBOX]

Esta documentación proporciona información sobre cómo trabajar con audiencias dentro de [!DNL Adobe Journey Optimizer]. Encontrará información detallada sobre Audience Portal y las audiencias en la documentación del servicio de segmentación de Adobe Experience Platform. Consulte estas secciones para obtener más información:

* [Guía de interfaz de usuario del servicio de segmentación](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/overview){target="_blank"}

* [Servicio de segmentación - Preguntas más frecuentes](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/faq){target="_blank"}

>[!ENDSHADEBOX]

## Examinar públicos {#browse}

Las audiencias están disponibles en el menú **[!UICONTROL Cliente]** > **[!UICONTROL Audiencias]**.

Un panel muestra visualmente superposiciones entre audiencias importantes y admite la exploración de tendencias de audiencia valiosas. Por ejemplo, los cambios de tamaño de audiencia durante un periodo determinado o los picos repentinos de audiencia pueden resaltar eventos o acciones que hicieron que una audiencia se achicara o aumentara, como una oferta exitosa.

![](assets/audiences-overview.png)

Desde Audience Portal, puede administrar, buscar y explorar audiencias fácilmente con etiquetado, controles de gobernanza, carpetas en las que se pueden realizar búsquedas y etiquetas estandarizados.

Para obtener más información sobre cómo trabajar con audiencias en Audience Portal, consulte la [documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es){target="_blank"}.

## Tipos de audiencias {#types}

Las audiencias se pueden generar mediante diferentes métodos:

* **Definiciones de segmentos**: Cree una nueva definición de audiencia con el servicio de segmentación de Adobe Experience Platform. Las audiencias se generan a partir de definiciones de segmentos y se actualizan en momentos diferentes según su tipo de evaluación:

   * Segmentación de streaming: las audiencias se actualizan en tiempo real a medida que ingresan nuevos datos, lo que garantiza una relevancia continua basada en la actividad del usuario.
   * Segmentación por lotes: las audiencias se actualizan cada 24 horas y capturan una instantánea de los perfiles a un intervalo fijo. Cuando se utilizan en los recorridos, es posible que los miembros del segmento recién cualificados no aparezcan hasta la siguiente captura de pantalla. [Más información sobre la sincronización](../building-journeys/audience-qualification-events.md#timing-segment-membership).
   * Segmentación de Edge: las audiencias se evalúan instantáneamente en el perímetro, lo que permite la personalización en tiempo real.

  [Obtenga información sobre cómo generar definiciones de segmentos](creating-a-segment-definition.md)

* **Carga personalizada**: importe una audiencia con un archivo CSV. [Aprenda a crear audiencias de carga personalizadas](custom-upload.md)

* **Composición de audiencias**: cree un flujo de trabajo de composición para combinar audiencias existentes en un lienzo visual y aplicar acciones como clasificación, división o unión para crear nuevas audiencias. [Aprenda a trabajar con la composición de audiencias](get-started-audience-orchestration.md)

* **Composición de audiencias federada**: federe conjuntos de datos directamente desde el almacén de datos existente para crear y enriquecer audiencias y atributos de Adobe Experience Platform en un solo sistema. [Aprenda a trabajar con la composición de audiencias federada](federated-audience-composition.md).

## Audiencias objetivo en recorridos y campañas {#target-audiences}

Una vez que las audiencias estén listas, puede seleccionarlas al crear recorridos o campañas, lo que le permite llegar a las personas adecuadas en el momento adecuado con mensajes relevantes. [Más información acerca de la activación de audiencias en Journey Optimizer](target-audiences.md).

## Vídeo práctico {#video}

Obtenga información sobre perfiles y públicos del cliente en Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3432671?quality=12)
