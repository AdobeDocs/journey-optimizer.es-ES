---
title: Envío de un mensaje a los suscriptores
description: Learn how to build a journey to send a message to the subscribers of a list
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# Use case: send a message to the subscribers of a list{#send-a-message-to-the-subscribers-of-a-list}

The purpose of this use case is to create a journey to send a message to the subscribers of a list.

**[!UICONTROL Consent and Preference Details]**[!DNL Adobe Experience Platform] **[!UICONTROL Data Management]****[!UICONTROL Schemas]** **[!UICONTROL Field groups]**

![](assets/consent-and-preference-details-field-group.png)

To configure this journey, follow these steps:

1. **[!UICONTROL Read]** [Más información](journey-gs.md).
1. **[!UICONTROL Message]** [Más información](journeys-message.md).
1. **[!UICONTROL Email parameters]****[!UICONTROL Message]**`PersonalEmail.adress`

   1. **[!UICONTROL Enable parameter override]****[!UICONTROL Address]****[!UICONTROL Edit]**

      ![](assets/message-to-subscribers-uc-1.png)

      To be able to modify the email address, you must have previously published the message.

   1. In the expression editor, enter the expression to retrieve the subscribers&#39; email addresses. [Más información](expression/expressionadvanced.md).

      This example shows an expression that includes references to map fields:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In this example, these functions are used:

      | Función | Descripción | Ejemplo |
      | --- | --- | --- |
      | `entry` | Refer to a map element according to the selected namespace | Refer to a specific subscription list |
      | `firstEntryKey` | Retrieve the first entry key of a map | Retrieve the first email address of subscribers |

      `daily-email` `subscribers`

      [](expression/field-references.md)

      ![](assets/message-to-subscribers-uc-2.png)

   1. **[!UICONTROL Add an expression]****[!UICONTROL Ok]**

   ![](assets/message-to-subscribers-uc-3.png)

1. **[!UICONTROL End]**
