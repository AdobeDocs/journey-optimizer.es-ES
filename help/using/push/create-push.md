---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de una notificación push
description: Obtenga información sobre cómo crear una notificación push en Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 11%

---

# Creación de una notificación push {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Creación de mensajes push"
>abstract="Añada el mensaje push y comience a personalizarlo con el editor de personalización."

## Creación de la notificación push en un recorrido o una campaña {#create}

Para crear una notificación push, siga los pasos a continuación:

>[!BEGINTABS]

>[!TAB Agregar una notificación push a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad Push desde la sección Acciones de la paleta.

   ![](assets/push_create_1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la configuración de mensaje que desea utilizar.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Si envía una notificación push desde un recorrido, puede aprovechar la función Optimización del tiempo de envío de Adobe Journey Optimizer para predecir el mejor momento para enviar el mensaje y maximizar la participación en función de la apertura histórica y las tasas de clics. [Aprenda a trabajar con la optimización del tiempo de envío](../building-journeys/send-time-optimization.md)

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

1. En la pantalla de configuración del recorrido, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido push. [Diseñar una notificación push](design-push.md)

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente para previsualizar su contenido.

1. Cuando tu notificación push esté lista, completa la configuración de tu [recorrido](../building-journeys/journey-gs.md) para enviarla.

   Para rastrear el comportamiento de sus destinatarios a través de aperturas push o interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento estén habilitadas en la [actividad de correo electrónico](../building-journeys/journeys-message.md).

>[!TAB Agregar una notificación push a una campaña]

1. Acceda al menú **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.

1. Seleccione el tipo de campaña que desea ejecutar

   * **Programado - Marketing**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar mensajes de marketing. Se configuran y ejecutan desde la interfaz de usuario de.

   * **Activado por API - Marketing/Transaccional**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar mensajes de marketing o transaccionales, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc.

1. En la sección **[!UICONTROL Propiedades]**, edite el **[!UICONTROL Título]** y la **[!UICONTROL Descripción]** de su campaña.

1. Haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para definir la audiencia a la que se dirigirá desde la lista de audiencias de Adobe Experience Platform disponibles. [Más información](../audience/about-audiences.md).

1. En el campo **[!UICONTROL Área de nombres de identidad]**, elija el área de nombres que desea usar para identificar a los individuos de la audiencia seleccionada. [Más información](../event/about-creating.md#select-the-namespace).

1. En la sección **[!UICONTROL Acciones]**, elija la **[!UICONTROL notificación push]** y seleccione o cree una nueva configuración.

   Más información acerca de la configuración push en [esta página](push-configuration.md).

   ![](assets/push_create_3.png)

1. Haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia objetivo. [Más información](../content-management/content-experiment.md)

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Aprenda a configurar la **[!UICONTROL programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. En el menú **[!UICONTROL déclencheur de acción]**, elija la **[!UICONTROL frecuencia]** de la notificación push:

   * Una vez
   * Diaria
   * Semanal
   * Mensual

1. En la pantalla de configuración de la campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido push. [Diseñar una notificación push](design-push.md)

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente para previsualizar su contenido.

1. Cuando tu notificación push esté lista, completa la configuración de tu [campaña](../campaigns/create-campaign.md) para enviarla.

   Para hacer un seguimiento del comportamiento de los destinatarios a través de las aperturas push o las interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento estén habilitadas en [campaign](../campaigns/create-campaign.md).

>[!ENDTABS]

**Temas relacionados**

* [Configuración del canal push](push-gs.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journeys-message.md)

## Modo de envío rápido {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Modo de envío rápido"
>abstract="El modo de envío rápido permite realizar envíos de mensajes a alta velocidad en el canal push a un tamaño de público inferior a 30 millones."

El modo de envío rápido es un complemento de [!DNL Journey Optimizer] que permite el envío muy rápido de mensajes push en grandes volúmenes a través de campañas.

La entrega rápida se utiliza cuando el retraso en la entrega de mensajes es crítico para la empresa, cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo, una noticia de última hora a los usuarios que han instalado su aplicación de canal de noticias.

Para obtener más información sobre el rendimiento al usar el modo de envío rápido, consulte [Descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html).

### Requisitos previos {#prerequisites}

La mensajería de envío rápido incluye los siguientes requisitos:

* La entrega rápida solo está disponible para **[!UICONTROL campañas programadas]** y no para campañas activadas por API,
* No se permite ninguna personalización en el mensaje push,
* La audiencia de destino debe contener menos de 30 millones de perfiles,
* Puede ejecutar hasta 5 campañas simultáneamente utilizando el modo de envío rápido.

### Activar modo de envío rápido

1. Cree una campaña de notificaciones push y active la opción **[!UICONTROL Envío rápido]**.

   ![](assets/create-campaign-burst.png)

1. Configure el contenido del mensaje y seleccione la audiencia a la que desee dirigirse. [Obtenga información sobre cómo crear una campaña](#create)

   >[!IMPORTANT]
   >
   >Asegúrese de que el contenido del mensaje no incluya personalización y de que la audiencia tenga menos de 30 millones de perfiles.

1. Revise y active la campaña como de costumbre. Tenga en cuenta que, en el modo de prueba, los mensajes no se envían mediante el modo de envío rápido.