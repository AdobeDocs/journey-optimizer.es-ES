---
solution: Journey Optimizer
product: journey optimizer
title: Creación de webhooks de comentarios para campañas activadas por API en Journey Optimizer
description: Aprenda a crear webhooks de comentarios para campañas activadas por API en Journey Optimizer.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
exl-id: a46f29a4-5115-4feb-8b2c-751765be2b36
TQID: https://experienceleague.adobe.com/RPopgwZfOcaw-uHvqVnforixMTAH57urwF2ViaZQemQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: f3781010d99a2993f88fd4907a94278c610cb4cb
workflow-type: tm+mt
source-wordcount: 473
ht-degree: 24%

---

# Creación de webhooks de comentarios para campañas activadas por API {#webhooks}

>[!CONTEXTUALHELP]
>id="ajo_channels_feedback_webhook_settings_configuration"
>title="Configuración básica"
>abstract="En esta sección, introduzca un nombre descriptivo para identificar el webhook y seleccione los canales para los que este webhook debe recibir comentarios (correo electrónico o SMS). En el campo URL del webhook, indique el punto final de HTTPS en el que deben entregarse los eventos de comentarios."

>[!CONTEXTUALHELP]
>id="ajo_channels_feedback_webhook_settings_create"
>title="Webhooks de comentarios"
>abstract="Los webhooks de comentarios le permiten recibir comentarios en tiempo real sobre el estado de ejecución de los mensajes enviados con campañas transaccionales activadas por API. Solo se permite una configuración de webhook por organización + combinación de zona protegida."

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a crear y configurar enlaces web de comentarios que proporcionen actualizaciones del estado de los mensajes en tiempo real a sus sistemas para campañas transaccionales activadas por API en Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Los enlaces web de comentarios le permiten recibir actualizaciones de estado en tiempo real de los mensajes enviados a través de campañas transaccionales activadas por API. Al configurar un gancho web, puede recibir automáticamente los resultados de la entrega directamente en sus sistemas, lo que permite la monitorización, el registro y el procesamiento automatizado.

Puede administrar las configuraciones del webhook desde el menú **[!UICONTROL Administración]** / **[!UICONTROL Canales]** / **[!UICONTROL Configuración del webhook de comentarios]**.

![](assets/webhook-list.png)

>[!NOTE]
>Solo se permite una configuración de webhook por cada combinación de **Organización + zona protegida**.

## Crear un webhook de comentarios {#feedback-webhook}

>[!CONTEXTUALHELP]
>id="ajo_channels_feedback_webhook_settings_authentication"
>title="Autenticación"
>abstract="Si el punto final requiere autenticación JWT, seleccione **Autenticación JWT** de la lista y proporcione los detalles necesarios."

>[!CONTEXTUALHELP]
>id="ajo_channels_feedback_webhook_settings_header_parameters"
>title="Parámetros de encabezado"
>abstract="En esta sección, puede configurar encabezados personalizados adicionales para que se envíen con cada solicitud de webhook."

>[!CONTEXTUALHELP]
>id="ajo_channels_feedback_webhook_relay_url"
>title="URL de retransmisión"
>abstract="El extremo HTTPS al que Journey Optimizer llama para ofrecer eventos para este webhook, incluidas las actualizaciones de estado de entrega y, cuando está activado, los mensajes SMS/RCS entrantes se retransmiten tal cual."

Para crear un webhook, siga estos pasos:

1. Vaya a **[!UICONTROL Administración]** / **[!UICONTROL Canales]** / **[!UICONTROL Configuración del enlace web de comentarios]**.

1. Haga clic en **Crear webhook de comentarios**.

1. En la sección **[!UICONTROL Configuración básica]**, proporcione los siguientes detalles:

   ![](assets/webhook-config.png)

   * **Nombre del webhook**: escriba un nombre descriptivo para identificar el webhook.
   * **Canales**: seleccione los canales para los cuales este webhook debe recibir comentarios (correo electrónico o SMS).
   * **URL de webhook**: proporcione el extremo HTTPS donde se deben entregar los eventos de comentarios.

1. En la sección **[!UICONTROL Authentication]**, seleccione el método de autenticación:

   ![](assets/webhook-authentication.png)

   * **Sin autenticación**: no se agregan encabezados de autenticación.
   * **Autenticación JWT**: proporcione los detalles necesarios si el extremo requiere autenticación JWT.

1. En la sección **[!UICONTROL Parámetros de encabezado]**, configure encabezados personalizados adicionales para enviarlos con cada solicitud de webhook.

   ![](assets/webhook-header.png)

1. Haga clic en **[!UICONTROL Enviar]** para guardar la configuración.

>[!NOTE]
>
>Puede editar un webhook en cualquier momento. Para ello, ábralo desde el inventario y haga clic en el botón **[!UICONTROL Editar]**.

## Estructura de carga útil de webhook

Después de la ejecución de un mensaje, **[!DNL Journey Optimizer]** envía la siguiente carga útil al extremo configurado.

```
{
  "requestId": "8NoByJneShCdCGRnrGS1t1m3CdA73dhR",
  "imsOrg": "myImsOrg",
  "sandbox": {
    "id": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "name": "prod"
  },
  "channel": "email",
  "eventType": "message.feedback",
  "messageExecution": {
    "messageExecutionID": "HUMA-26362805",
    "messageType": "transactional",
    "campaignID": "16f24a15-7e21-477c-848a-d5695ca7f137",
    "campaignVersionID": "2ca10c10-56dd-4505-87cd-fa5da84e7a5d"
  },
  "messageDeliveryFeedback": {
    "feedbackStatus": {
      "value": "bounce"
    },
    "offers": null,
    "messageExclusion": null,
    "messageFailure": {
      "category": "sync",
      "type": "Ignored",
      "code": "25",
      "reason": "Admin Failure"
    },
    "retryCount": 0
  },
  "identityMap": {
    "email": [
      {
        "id": "john.doe@luma.com",
        "primary": true
      }
    ]
  }
}
```

El webhook puede capturar los siguientes eventos:

* Enviados
* Entregados
* Devolución (consulte el ejemplo anterior)
* Errores

Cada solicitud entrante también incluye un requestId único que se devuelve al webhook.

## Próximos pasos {#next}

Una vez que se haya creado un webhook de comentarios, puedes habilitarlo al configurar una audiencia de **campaña desencadenada por API transaccional**. Obtenga más información en esta sección: [Habilitar webhooks](../campaigns/api-triggered-campaign-audience.md#webhook)
