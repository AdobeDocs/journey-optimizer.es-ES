---
solution: Journey Optimizer
product: journey optimizer
title: Envío de un mensaje mediante Campaign v7/v8
description: Obtenga información sobre cómo enviar un mensaje mediante Campaign v7/v8
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Data Engineer, User
level: Intermediate, Experienced
keywords: recorrido, mensaje, campaña, integración
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
source-git-commit: 824cbf12502f0a52e27636dddee38cb7dee94bf4
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 2%

---

# Envío de un mensaje con Campaign v7/v8 {#campaign-v7-v8-use-case}

Este caso de uso explica todos los pasos necesarios para enviar un correo electrónico mediante la integración con Adobe Campaign v7 y Adobe Campaign v8.

>[!NOTE]
>
>Para utilizar esta integración, debe tener Campaign v7/v8 compilación 9125 o superior.

En primer lugar, cree una plantilla de correo electrónico transaccional en Campaign. A continuación, en Journey Optimizer, cree el evento, la acción y diseñe el recorrido.

Para obtener más información sobre la integración de Campaign, consulte estas páginas:

* [Creación de una acción de campaña](../action/acc-action.md)
* [Usando la acción en un recorrido](../building-journeys/using-adobe-campaign-v7-v8.md).

**Adobe Campaign**

La instancia de Campaign debe estar aprovisionada para esta integración. Se debe configurar la función Mensajería transaccional.

1. Inicie sesión en la instancia de control de Campaign.

1. En **Administración** > **Plataforma** > **Enumeraciones**, seleccione la enumeración **Tipo de evento** (eventType). Cree un nuevo tipo de evento (&quot;evento de recorrido&quot;, en nuestro ejemplo). Utilice el nombre interno del tipo de evento al escribir el archivo JSON más adelante.

   ![](assets/accintegration-uc-1.png)

1. Desconecte y vuelva a conectarse a la instancia para que la creación surta efecto.

1. En **Centro de mensajes** > **Plantillas de mensajes transaccionales**, cree una nueva plantilla de correo electrónico basada en el tipo de evento creado anteriormente.

   ![](assets/accintegration-uc-2.png)

1. Diseñe la plantilla. En este ejemplo, la personalización se aplica al nombre del perfil y al número de pedido. El nombre se encuentra en la fuente de datos de Adobe Experience Platform y el número de pedido es un campo del evento de Journey Optimizer. Asegúrese de utilizar los nombres de campo correctos en Campaign.

   ![](assets/accintegration-uc-3.png)

1. Publique la plantilla transaccional.

   ![](assets/accintegration-uc-4.png)

1. Escriba la carga útil JSON correspondiente a la plantilla.

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
* La dirección de correo electrónico es una variable, por lo que puede escribir cualquier etiqueta.
* En ctx, los campos de personalización también son variables.

**Journey Optimizer**

1. Cree un evento. Incluya el campo purchaseOrderNumber.

   ![](assets/accintegration-uc-5.png)

1. Cree una acción en Journey Optimizer correspondiente a la plantilla de Campaign. En la lista desplegable **Tipo de acción**, seleccione **Adobe Campaign Classic**.

   ![](assets/accintegration-uc-6.png)

1. Haga clic en **Campo de carga útil** y pegue el JSON creado anteriormente.

   ![](assets/accintegration-uc-7.png)

1. Para la dirección de correo electrónico y los dos campos personalizados, cambie **Constant** a **Variable**.

   ![](assets/accintegration-uc-8.png)

1. Ahora cree un nuevo recorrido e inicie con el evento creado anteriormente.

   ![](assets/accintegration-uc-9.png)

1. Añada la acción y asigne cada campo al campo correcto en Journey Optimizer.

   ![](assets/accintegration-uc-10.png)

1. Pruebe el recorrido.

   ![](assets/accintegration-uc-11.png)

1. Ahora puede publicar el recorrido.
