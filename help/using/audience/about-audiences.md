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
source-git-commit: cdcce470481393c821d1c5df95639602510a690a
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 43%

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

Una audiencia es un conjunto de personas que comparten comportamientos o características similares. Obtenga más información sobre las audiencias en [Documentación del Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es){target="_blank"}.

[!DNL Journey Optimizer] le permite crear audiencias de Adobe Experience Platform directamente desde el **[!UICONTROL Audiencias]** y aprovecharlos en sus recorridos o campañas.

Las audiencias se pueden generar mediante diferentes métodos:

* **Definiciones de segmentos**: cree una nueva definición de audiencia con el servicio de segmentación de Adobe Experience Platform. [Obtenga información sobre cómo crear definiciones de segmentos](creating-a-segment-definition.md)
* **Importación de archivo CSV**: importe una audiencia mediante un archivo CSV. Obtenga información sobre cómo importar audiencias en Adobe Experience Platform [Documentación del Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.
* **Composición de audiencia**: Cree un flujo de trabajo de composición para combinar las audiencias de Adobe Experience Platform existentes en un lienzo visual y aprovechar varias actividades (dividir, excluir...) para crear nuevas audiencias. [Introducción a Composición de públicos](get-started-audience-orchestration.md)

## Audiencias de Target en [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puede seleccionar en campañas y recorridos cualquier audiencia de Adobe Experience Platform generada mediante [definiciones de segmentos](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>Por ahora, las audiencias resultantes de [composiciones de audiencia](../audience/get-started-audience-orchestration.md) solo se puede segmentar en campañas de. Esta capacidad está disponible como una versión beta privada para recorridos.
>
>El uso de audiencias [cargado desde un archivo CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"} en campañas y recorridos está disponible actualmente como una versión beta privada.
>
>Para obtener más información, contacte con su representante de Adobe.

Puede aprovechar los públicos en **[!DNL Journey Optimizer]** de maneras diferentes:

* Elija un público para una **campaña**, donde el mensaje se envía a todos los particulares que pertenecen al público seleccionado. [Obtenga información sobre cómo definir el público de una campaña](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilice una actividad de orquestación **Leer público** en un recorrido para hacer que todos los particulares del público entren en el recorrido y reciban los mensajes incluidos en el recorrido.

  Supongamos que tiene un público de “clientes plata”. Con esta actividad, puede hacer que todos los “clientes plata” entren en un recorrido y se les envíe una serie de mensajes personalizados. [Obtenga información sobre cómo configurar la actividad Leer público](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilice la actividad de evento **Calificación del público** en un recorrido para hacer que los particulares entren o avancen en el recorrido en función de las entradas y salidas del público de Adobe Experience Platform.

  Por ejemplo, puede hacer que todos los “clientes plata” nuevos entren en el recorrido para enviarles mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [Obtener información sobre cómo configurar una actividad Calificación de público](../building-journeys/audience-qualification-events.md).

* Utilice la actividad **Condición** en un recorrido para crear condiciones basadas en el abono del público. [Aprenda a utilizar los públicos en condiciones](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de evaluación de públicos {#evaluation-method-in-journey-optimizer}

En Adobe Journey Optimizer, las audiencias se generan a partir de las definiciones de segmentos mediante uno de los tres métodos de evaluación siguientes.

+++ Segmentación de streaming

La lista de perfiles de la audiencia se mantiene actualizada en tiempo real a medida que ingresan nuevos datos al sistema.

La segmentación de streaming es un proceso continuo de selección de datos que actualiza los públicos en respuesta a la actividad de los usuarios. Una vez que se ha creado una definición de segmento y se ha guardado el público resultante, la definición del segmento se aplica a los datos entrantes en Journey Optimizer. Esto significa que las personas se añaden o eliminan de la audiencia a medida que cambian los datos de perfil, lo que garantiza que la audiencia de destino siempre sea relevante. [Más información](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"}

>[!NOTE]
>
>Asegúrese de utilizar los eventos adecuados como criterios de segmentación de flujo continuo. [Más información](#streaming-segmentation-events-guardrails)

+++

+++ Segmentación por lotes

La lista de perfiles de la audiencia se evalúa cada 24 horas.

La segmentación por lotes es una alternativa a la segmentación de streaming que procesa todos los datos de perfil a la vez mediante definiciones de segmento. Esto crea una instantánea del público que se puede guardar y exportar para su uso. Sin embargo, a diferencia de la segmentación por secuencias, la segmentación por lotes no actualiza continuamente la lista de audiencias en tiempo real, y los nuevos datos que llegan después del proceso por lotes no se reflejarán en la audiencia hasta el siguiente proceso por lotes. [Más información](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}

+++

+++ Segmentación de Edge

La segmentación de Edge es la capacidad de evaluar segmentos en Adobe Experience Platform de forma instantánea [en el borde](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

Si sabe qué método de evaluación desea utilizar, selecciónelo en la lista desplegable. También puede hacer clic en el icono de examinar icono de la carpeta con una lupa para ver una lista de los métodos de evaluación de definición de segmentos disponibles. [Más información](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Una vez que haya definido un público por primera vez, los perfiles se añaden cuando este cumple los requisitos.

Rellenar el público a partir de datos anteriores puede tardar hasta 24 horas. Una vez que se ha rellenado el público, se mantiene actualizado continuamente y siempre está listo para la segmentación.

### Uso de eventos con segmentación de streaming {#streaming-segmentation-events-guardrails}

La segmentación por streaming es útil para la personalización en tiempo real con casos de uso de alto valor. Sin embargo, es importante elegir la opción correcta [eventos](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"} para usar como criterios de segmentación.

Por lo tanto, para un rendimiento óptimo de la segmentación de streaming, evite utilizar los siguientes eventos:

* **Mensaje abierto** Evento de tipo de interacción

  Al crear la audiencia, el uso de **Mensaje abierto** los eventos de interacción pasaron a ser poco fiables, ya que no son indicadores reales de la actividad del usuario y pueden afectar negativamente al rendimiento de la segmentación. Descubra por qué en esto [Publicación de blog de Adobe](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  Por lo tanto, el Adobe recomienda no utilizar **Mensaje abierto** eventos de interacción con segmentación de flujo continuo. En su lugar, utilice señales reales de actividad del usuario como clics, compras o datos de señalizaciones.

* **Mensaje enviado** Evento de estado de comentarios

  El **Mensaje enviado** el evento de comentarios se utiliza a menudo para comprobar la frecuencia o la supresión antes de enviar un correo electrónico. El Adobe recomienda evitarlo, ya que ejerce presión sobre el rendimiento y puede causar una degradación del sistema.

  Por lo tanto, para la frecuencia o la lógica de supresión, utilice reglas empresariales en lugar de **Mensaje enviado** eventos de comentarios. Tenga en cuenta que pronto estarán disponibles los límites de frecuencia diarios para perfiles individuales, lo que complementa la cadencia mensual existente para reglas comerciales.

>[!NOTE]
>
>Puede utilizar **Mensaje abierto** y **Mensaje enviado** eventos en la segmentación por lotes sin problemas de rendimiento.
