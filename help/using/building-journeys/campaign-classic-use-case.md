---
title: Envío de un mensaje mediante Campaign v7/v8
description: Obtenga información sobre cómo enviar un mensaje mediante Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 2%

---

# Use case: send a message using Campaign v7/v8 {#campaign-classic-use-case}

Este caso de uso presenta todos los pasos necesarios para enviar un correo electrónico mediante la integración con Adobe Campaign Classic v7 y Adobe Campaign v8.

We will first create a transactional email template in Campaign. Then, in Journey Optimizer, we&#39;ll create the event, action and design the journey.

Para obtener más información sobre la integración de Campaign, consulte estas páginas:

* [Creación de una acción de campaña](../action/acc-action.md)
* [Uso de la acción en un recorrido](../building-journeys/using-adobe-campaign-classic.md).

**Adobe Campaign**

La instancia de Campaign debe aprovisionarse para esta integración. La función Mensajería transaccional debe configurarse.

1. Inicie sesión en la instancia de control de Campaign.

1. En **Administración** > **Plataforma** > **Enumeraciones**, seleccione **Tipo de evento** enumeración (eventType). Cree un nuevo tipo de evento (&quot;recorrido-evento&quot;, en nuestro ejemplo). You will have to use the internal name of the event type when writing the JSON file later.

   ![](assets/accintegration-uc-1.png)

1. Disconnect and reconnect to the instance for the creation to be effective.

1. En **Centro de mensajes** > **Plantillas de mensajes transaccionales**, cree una nueva plantilla de correo electrónico basada en el tipo de evento creado anteriormente.

   ![](assets/accintegration-uc-2.png)

1. Diseñe la plantilla. En este ejemplo, se utiliza la personalización en el nombre del perfil y el número de pedido. The first name is in the Adobe Experience Platform data source, and the order number is a field from our Journey Optimizer event. Asegúrese de utilizar los nombres de campo correctos en Campaign.

   ![](assets/accintegration-uc-3.png)

1. Publique la plantilla transaccional.

   ![](assets/accintegration-uc-4.png)

1. Now you need to write the JSON payload corresponding the template.

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* Para el canal, debe escribir &quot;correo electrónico&quot;.
* Para eventType, utilice el nombre interno del tipo de evento creado anteriormente.
* La dirección de correo electrónico será una variable, por lo que puede escribir cualquier etiqueta.
* En ctx, los campos de personalización también son variables.

**Journey Optimizer**

1. En primer lugar, debe crear un evento. Asegúrese de incluir el campo &quot;purchaseOrderNumber&quot;.

   ![](assets/accintegration-uc-5.png)

1. You then need to create, in Journey Optimizer, an action corresponding to your Campaign template. En el **Tipo de acción** desplegable, seleccione **Adobe Campaign Classic**.

   ![](assets/accintegration-uc-6.png)

1. Haga clic en el **Campo de carga útil** y pegue el JSON creado anteriormente.

   ![](assets/accintegration-uc-7.png)

1. For the email address and the two personalization fields, change **Constant** to **Variable**.

   ![](assets/accintegration-uc-8.png)

1. Now create a new journey and start with the event previously created.

   ![](assets/accintegration-uc-9.png)

1. Añada la acción y asigne cada campo al campo correcto en Journey Optimizer.

   ![](assets/accintegration-uc-10.png)

1. Agregue un **Fin** y pruebe el recorrido.

   ![](assets/accintegration-uc-11.png)

1. You can now publish your journey.
