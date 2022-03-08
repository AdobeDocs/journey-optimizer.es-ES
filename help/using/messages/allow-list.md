---
title: Allow list
description: Learn how to use the allowed list.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 5%

---

# Lista de permitidos {#allow-list}

[](../administration/sandboxes.md) En una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a sus clientes.

The allowed list enables you to specify individual email addresses or domains that will be the only recipients or domains authorized to receive the emails you are sending from a specific sandbox. This can prevent you from sending emails accidentally to real customer addresses when you are in a testing environment.

>[!CAUTION]
>
>**** It only applies to the email channel.

## Enable the allowed list {#enable-allow-list}

To enable the allowed list on a non-production sandbox, you need to update the general settings using the corresponding API end point in the Message Presets Service.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* ******** Obtenga más información en [esta sección](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>[](preview.md#send-proofs)[](../building-journeys/testing-the-journey.md)

## Add entities to the allowed list {#add-entities}

`ALLOWED``listType` Por ejemplo:

![](assets/allow-list-api.png)

************

>[!NOTE]
>
>The allowed list can contain up to 1,000 entries.

[](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html)

## Allowed list logic {#logic}

**** [](suppression-list.md)

****

* ******[!UICONTROL Not allowed]**

* **** [](suppression-list.md)**[!UICONTROL Suppressed]**

>[!NOTE]
>
>**[!UICONTROL Not allowed]** ****[](../building-journeys/read-segment.md)[](../building-journeys/journeys-message.md)******[!UICONTROL Sent]**
>
>[](../reports/live-report.md)[](../reports/global-report.md)

## Exclusion reporting {#reporting}

When this feature is enabled on a non-production sandbox, you can retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html)

****

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

****

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
