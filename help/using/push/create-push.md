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
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 11%

---

# Crear una notificación push {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Creación de mensajes push"
>abstract="Añada el mensaje push y comience a personalizarlo con el editor de personalización."

Puede crear notificaciones push para dispositivos móviles (iOS y Android) y navegadores web. Esta página le guía a través del proceso de configuración de una notificación push en un recorrido o una campaña.

## Creación de la notificación push en un recorrido o una campaña {#create}

Para crear una notificación push, siga los pasos a continuación:

>[!BEGINTABS]

>[!TAB Agregar una notificación push a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad **[!UICONTROL Action]** desde la sección **[!UICONTROL Actions]** de la paleta. Más información sobre la [actividad de acción](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >Dado que ahora se puede acceder a todos los canales nativos a través de la actividad de acción, las actividades de canal nativo heredadas quedarán obsoletas con la versión de marzo. Los recorridos existentes que incluyen acciones heredadas seguirán funcionando tal cual; no se requiere ninguna migración.

1. Seleccione **[!UICONTROL Push]** como tipo de acción.

   ![](assets/push_create_1.png)

1. Escriba una **[!UICONTROL etiqueta]** para identificar la acción en el lienzo de recorrido.

1. Haga clic en el botón **[!UICONTROL Configurar acción]**.

1. Se le dirigirá a la ficha **[!UICONTROL Acciones]**. A partir de ahí, seleccione o cree la configuración push que desee utilizar. [Más información](push-configuration.md)

   ![](assets/push_create_2.png)

1. Además:

   * Puede aplicar reglas de límite a la acción push seleccionando un conjunto de reglas en la lista desplegable **[!UICONTROL Reglas de negocio]**. [Más información](../conflict-prioritization/channel-capping.md)

   * Puede usar la opción **[!DNL Send time optimization]** para predecir el mejor momento para enviar el mensaje y maximizar la participación en función de la apertura histórica y las tasas de clics. [Descubra cómo](../building-journeys/send-time-optimization.md)

1. Utilice **[!UICONTROL Modo de envío rápido]** para enviar la notificación push en grandes volúmenes. [Descubra cómo](#rapid-delivery)

1. Seleccione el botón **[!UICONTROL Editar contenido]** y cree el contenido como desee. [Más información](design-push.md)

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente para previsualizar su contenido. [Descubra cómo](send-push.md)

1. Volver al lienzo de recorrido. Si es necesario, complete el flujo de recorrido arrastrando y soltando acciones o eventos adicionales. [Más información](../building-journeys/about-journey-activities.md)

   >[!NOTE]
   >
   >Para rastrear el comportamiento de sus destinatarios a través de aperturas push o interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento estén habilitadas en la [actividad de correo electrónico](../building-journeys/journey-action.md).

Para obtener más información sobre cómo crear, configurar y publicar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Agregar una notificación push a una campaña]

1. Acceda al menú **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.

1. Seleccione el tipo de campaña que desea ejecutar

   * **Programado - Marketing**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar mensajes de marketing. Se configuran y ejecutan desde la interfaz de usuario de.

   * **Activado por API - Marketing/Transaccional**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar mensajes de marketing o transaccionales, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc.

1. En la sección **[!UICONTROL Propiedades]**, edite el **[!UICONTROL Título]** y la **[!UICONTROL Descripción]** de su campaña.

1. Haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para definir la audiencia a la que se dirigirá desde la lista de audiencias de Adobe Experience Platform disponibles. [Más información](../audience/about-audiences.md).

1. En el campo **[!UICONTROL Área de nombres de identidad]**, elija el área de nombres que desea usar para identificar a los individuos de la audiencia seleccionada. [Más información](../event/about-creating.md#select-the-namespace).

1. En la sección **[!UICONTROL Acciones]**, elija la **[!UICONTROL notificación push]** y seleccione o cree una nueva configuración.

   Obtenga más información acerca de la configuración push para móviles en [esta página](push-configuration.md) y para la web en [esta página](push-configuration-web.md).

   ![](assets/push_create_3.png)

1. Haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia objetivo. [Más información](../content-management/content-experiment.md)

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Aprenda a configurar la **[!UICONTROL programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. En el menú **[!UICONTROL déclencheur de acción]**, elija la **[!UICONTROL frecuencia]** de la notificación push:

   * Una vez
   * Diaria
   * Semanal
   * Mensual

1. En la pantalla de configuración de la campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido push. [Diseñar una notificación push](design-push.md)

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente para previsualizar su contenido. [Descubra cómo](send-push.md)

1. Cuando tu notificación push esté lista, completa la configuración de tu [campaña](../campaigns/create-campaign.md) para enviarla.

   Para hacer un seguimiento del comportamiento de los destinatarios a través de las aperturas push o las interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento estén habilitadas en [campaign](../campaigns/create-campaign.md).

Para obtener más información sobre cómo crear, configurar y activar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

**Temas relacionados**

* [Configuración del canal push](push-gs.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journey-action.md)

## Modo de envío rápido {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Modo de envío rápido"
>abstract="El modo de envío rápido permite realizar envíos de mensajes a alta velocidad en el canal push a un tamaño de público inferior a 30 millones."

El modo de envío rápido es un complemento de [!DNL Journey Optimizer] que permite el envío muy rápido de mensajes push en grandes volúmenes a través de campañas.

La entrega rápida se utiliza cuando el retraso en la entrega de mensajes es crítico para la empresa, cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo, una noticia de última hora a los usuarios que han instalado su aplicación de canal de noticias.

Para obtener más información sobre el rendimiento al usar el modo de envío rápido, consulte [Descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

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