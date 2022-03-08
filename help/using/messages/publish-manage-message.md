---
title: Publish and modify a message
description: Learn how to publish and update your messages
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 116e2223-a806-4f68-9a8c-c0bde6008010
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 17%

---

# Publish your messages {#publish-manage-messages}

## Publish a message {#publish-message}

Once your message has been created, you can publish it to make it available for execution.

>[!CAUTION]
>
>Before publishing, check and resolve alerts. [Más información](alerts.md)

![](assets/publish-message.png)

**[!UICONTROL Published]**

[](../building-journeys/journey.md)

>[!NOTE]
>
>Al actualizar una oferta, una oferta de reserva, una colección de ofertas o una decisión de oferta a la que se hace referencia directa o indirectamente en un mensaje publicado, las actualizaciones ahora se reflejan automáticamente en el mensaje correspondiente, sin necesidad de volver a publicarlas. [](../offers/get-started/starting-offer-decisioning.md)

## Update a read-only message {#modify-message}

After publication, a message is in read-only mode. You can still update it by creating a new draft of that message.

This enables you to update content or fix an issue for example, without republishing the whole journey where your message is used.

>[!NOTE]
>
>The draft version can be edited while the published version is still published and active.

To update a published message:

1. From the message list, select your message to open it.

1. Haga clic en **[!UICONTROL Modify]**.

   ![](assets/message-modify.png)

1. Confirme la elección. A draft version of the message is created.

   ![](assets/message-modify-v2.png)

1. Edit the content or change the settings as desired.
1. Haga clic en **[!UICONTROL Publish]**. This action will publish the new version of the message that will be used for the next executions.

As soon as the new version is published, upon the next API call, a new message execution will be generated. The next incoming profile will receive the new version.

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version. -->
