---
title: Reactions events
description: Learn about reaction events
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---

# Eventos de reacción {#reaction-events}

**[!UICONTROL Reactions]** This activity allows you to react to tracking data related to a message sent within the same journey. We capture this information in real-time at the moment it is shared with Adobe Experience Platform. For push notifications, you can react to clicked, sent or failed messages. For SMS messages, you can react to sent or failed messages. For emails, you can react to clicked, sent, opened or failed messages.

You can also use this mechanism to perform an action when there is no reaction to your messages. To do this, create a second path parallel to the reaction activity and add a wait activity. If there is no reaction during the period defined in the wait activity, the second path will be chosen. You can choose to send, for example, a follow-up message.

****

[](../building-journeys/about-journey-activities.md#action-activities)

![](assets/journey45.png)

Here are the different steps to configure the reaction events:

1. **[!UICONTROL Label]** Este paso es opcional.
1. From the drop-down list, select the action activity you want to react to. You can select any action activity positioned in the previous steps of the path.
1. Depending on the action you selected, choose what you want to react to.
1. You can define an event timeout (between 40 seconds and 30 days) and a timeout path. This will create a second path for individuals who did not react within the defined duration. **[!UICONTROL Wait time]** Consulte [esta sección](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Reaction events cannot track messages that take place in a different journey.
>
>Reaction events track clicks on links of the type &quot;tracked&quot;. Unsubscription and mirror page links are not taken into account.

>[!IMPORTANT]
>
>Email clients such as Gmail allow image blocking. Emails opens are tracked using a 0-pixel image included in the email. If images are blocked, email opens will not be taken into account.
