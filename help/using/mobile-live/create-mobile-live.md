---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje de actividad Live
description: Obtenga información sobre cómo crear una actividad Live en Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bfd36dddb5795cd8b6eeb164f70b6cf3fdcb5750
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# Crear una actividad en directo {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Introducción a la actividad en directo](get-started-mobile-live.md)
* [Configuración de actividades activas](mobile-live-configuration.md)
* [Integración de actividades en directo con Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* **[Crear una actividad en vivo](create-mobile-live.md)**
* [Preguntas frecuentes](mobile-live-faq.md)
* [Informe de campaña de actividad en directo](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Después de configurar la configuración móvil e implementar el SDK móvil de Adobe Experience Platform, puede empezar a crear la actividad en directo en Journey Optimizer:

1. Acceda al menú **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.

1. Seleccione el tipo de campaña **API desencadenada**.

   * Seleccione **Marketing activado por API** para campañas basadas en audiencias

   * Seleccione **Transaccional activado por API** para campañas individuales.

   >[!IMPORTANT]
   >
   > Tenga en cuenta que para **Transaccional activado por API**, la opción **[!UICONTROL Alto rendimiento]** no debería estar habilitada.

   ![](assets/create-live-1.png)

1. En la sección **[!UICONTROL Propiedades]**, edite el **[!UICONTROL Título]** y la **[!UICONTROL Descripción]** de su campaña.

1. En la sección **[!UICONTROL Acciones]**, elija **[!UICONTROL Actividad en directo]** y seleccione o cree una nueva configuración.

   Obtenga más información acerca de la configuración de actividades en vivo en [esta página](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia objetivo. [Más información](../content-management/content-experiment.md)

1. En la ficha **[!UICONTROL Audiencia]**, elija su **[!UICONTROL tipo de identidad]** [Más información](../audience/about-audiences.md).

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Aprenda a configurar la **[!UICONTROL programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. Una vez configurada, haz clic en **[!UICONTROL Revisar para activar]** y luego haz clic en **[!UICONTROL Activar]**.

1. Una vez activada la campaña, usa la **solicitud cURL** proporcionada como plantilla para almacenar en déclencheur los eventos de inicio, actualización o finalización de la actividad. Actualice la carga útil de ejemplo con los datos específicos antes de la ejecución.

   Asegúrese de copiar también los identificadores de **[!UICONTROL ID de campaña]** para incluirlos en su carga útil.

   ➡️ Consulte la [Documentación de campañas activadas por API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) para conocer los requisitos de autenticación, incluidos tokens de OAuth y claves de API.

   ![](assets/create-live-3.png)

   +++ Ejemplo de una carga útil individual

   Tenga en cuenta que la mayoría de los campos del siguiente ejemplo de carga útil son obligatorios, solo `requestId`, `dismissal-date` y `alert` son opcionales.

   ```json
   {
       "requestId": "your-request-id",
       "campaignId": "your-campaign-id",
       "recipients": [
   {
       "type": "aep",
       "userId": "testemail@gmail.com",
       "namespace": "email",
       "context": {
        "requestPayload": {
       "aps": {
       "content-available": 1,
       "timestamp": 1756984054,              // current epoch time
       "dismissal-date": 1756984084,         // optional – auto remove when event="end"
       "event": "update",                    // start | update | end
   
       // Fields from FoodDeliveryLiveActivityAttributes
       "content-state": {
         "orderStatus": "Delivered"
       },
   
       "attributes-type": "FoodDeliveryLiveActivityAttributes",
       "attributes": {
         "restaurantName": "Pizza",
         "liveActivityData": {
           "liveActivityID": "orderId1"       // customer reference ID
         }
       },
   
       "alert": {
         "title": "Order Delivered!",
         "body": "Your pizza has arrived."
       }
     }
   }
   }
   }
   ]
   }
   ```

   +++

Después de diseñar la actividad en vivo, puede hacer un seguimiento para medir el impacto de su actividad en vivo con [informes integrados](../reports/campaign-global-report-cja-activity.md).
