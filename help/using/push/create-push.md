---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de una notificación push
description: Obtenga información sobre cómo crear una notificación push en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 4%

---

# Crear una notificación push {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Creación de mensajes push"
>abstract="Añada el mensaje push y comience a personalizarlo con el editor de expresiones."

## Creación de la notificación push en un recorrido o campaña {#create}

Para crear una notificación push, siga los pasos a continuación:

>[!BEGINTABS]

>[!TAB Añadir una inserción a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad Push desde la sección Actions de la paleta.

   ![](assets/push_create_1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Si envía una notificación push desde un recorrido, puede aprovechar la función de optimización del tiempo de envío de Adobe Journey Optimizer para predecir el mejor momento para enviar el mensaje y maximizar la participación en función de las tasas de clics y de apertura históricas. [Aprenda a trabajar con la optimización del tiempo de envío](../building-journeys/journeys-message.md#send-time-optimization)

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

1. En la pantalla de configuración del recorrido, haga clic en el **[!UICONTROL Editar contenido]** para configurar el contenido push. [Diseño de una notificación push](design-push.md)

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo.

1. Cuando el push esté listo, complete la configuración de su [recorrido](../building-journeys/journey-gs.md) para enviarlo.

   Para realizar un seguimiento del comportamiento de los destinatarios a través de las aperturas de push o las interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento están habilitadas en la variable [actividad de correo electrónico](../building-journeys/journeys-message.md).

>[!TAB Adición de una push a una campaña]

1. Cree una nueva campaña programada o activada por la API, seleccione **[!UICONTROL Notificaciones push]** como su acción y elija el **[!UICONTROL Superficie de la aplicación]** para usar. [Más información sobre la configuración push](push-configuration.md).

   ![](assets/push_create_3.png)

1. Haga clic en **[!UICONTROL Crear]**.

1. En el **[!UICONTROL Propiedades]** , edite la **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

   ![](assets/push_create_4.png)

1. Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para definir la audiencia a la que se dirigirá desde la lista de segmentos de Adobe Experience Platform disponibles. [Más información](../segment/about-segments.md).

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información](../event/about-creating.md#select-the-namespace).

   ![](assets/push_create_5.png)

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. En el **[!UICONTROL Déclencheur de acción]** , seleccione **[!UICONTROL Frecuencia]** de la notificación push:

   * Una vez
   * Diario
   * Semanal
   * Mensual

1. En la pantalla de configuración de la campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido push. [Diseño de una notificación push](design-push.md)

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo.

1. Cuando el push esté listo, complete la configuración de su [campaign](../campaigns/create-campaign.md) para enviarlo.

   Para realizar un seguimiento del comportamiento de los destinatarios a través de las aperturas de push o las interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento están habilitadas en la variable [campaign](../campaigns/create-campaign.md).

>[!ENDTABS]

**Temas relacionados**

* [Configurar el canal push](push-gs.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)

## Modo de entrega rápido {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Modo de entrega rápido"
>abstract="El modo de entrega rápida permite realizar envíos de mensajes a alta velocidad en el canal push a un tamaño de audiencia inferior a 30 M."

El modo de entrega rápida, anteriormente conocido como modo de ráfaga en recorridos, es un [!DNL Journey Optimizer] complemento que permite enviar mensajes push muy rápidamente a grandes volúmenes mediante campañas.

La entrega rápida se utiliza cuando el retraso en la entrega de mensajes es crítico para el negocio, cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo una noticia de último minuto para los usuarios que han instalado la aplicación de canal de noticias.

Para obtener más información sobre el rendimiento al utilizar el modo de entrega rápida, consulte [Descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html).

### Requisitos previos {#prerequisites}

La mensajería de envío rápido incluye los siguientes requisitos:

* La entrega rápida está disponible para **[!UICONTROL Programado]** solo campañas y no está disponible para campañas activadas por API,
* No se permite ninguna personalización en el mensaje push,
* La audiencia de destino debe contener menos de 30 millones de perfiles,
* Puede ejecutar hasta 5 campañas simultáneamente mediante el modo de envío rápido.

### Activar el modo de entrega rápido

1. Cree una campaña de notificaciones push y active la opción **[!UICONTROL Entrega rápida]** .

![](assets/create-campaign-burst.png)

1. Configure el contenido del mensaje y seleccione la audiencia a la que desea dirigirse. [Obtenga información sobre cómo crear una campaña](#create)

   >[!IMPORTANT]
   >
   >Asegúrese de que el contenido del mensaje no incluya ninguna personalización y de que la audiencia contenga menos de 30 millones de perfiles.

1. Revise y active la campaña como de costumbre. Tenga en cuenta que, en el modo de prueba, los mensajes no se envían mediante el modo de envío rápido.