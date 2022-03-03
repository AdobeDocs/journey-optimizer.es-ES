---
title: Integración con Adobe Campaign v7/v8
description: Learn how to integrate with Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 51c63b196b11905289c3c0c450c1976eb551bbc8
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 7%

---

# Integración con Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

This integration is available for Adobe Campaign Classic v7 starting 21.1 release, and Adobe Campaign v8. It allows you to send emails, push notifications and SMS using Adobe Campaign Transactional Messaging capabilities.

The connection between the Journey Optimizer and Campaign instances is setup by Adobe at provisioning time.

[](../building-journeys/campaign-classic-use-case.md)

For each action configured, an action activity is available in the journey designer palette. Consulte esta [sección](../building-journeys/using-adobe-campaign-classic.md).

## Notas importantes {#important-notes}

* There is no throttling of messages. The system caps the number of messages that can be sent over to 4000 per 5 minutes, based on the current Campaign SLA. For this reason, Journey Optimizer should only be used in unitary use cases (individual events, not segments).

* You need to configure one action on the canvas per template you wish to use. You need to configure one action in Journey Optimizer for each template you wish to use from Adobe Campaign.

* We recommend that you use a dedicated Message Center instance that is hosted for this integration to avoid impacting any other Campaign operations that you may have going on. The marketing server can be hosted or on-premise. The build required is 21.1 Release Candidate or greater.

* There is no validation that the payload or Campaign message is correct.

* You cannot use a Campaign action with a segment qualification event.

## Requisitos previos {#prerequisites}

In Campaign, you need to create and publish a transactional message and its associated event. [](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging)

You can build your JSON payload corresponding to each message following the pattern below. You will then paste this payload when configuring the action in Journey Orchestration (see below)

Vea el siguiente ejemplo:

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* ****
* ****
* ****

## Configuring the action {#configure-action}

In Journey Optimizer, you need to configure one action per transactional message. Siga estos pasos:

1. Create a new action. Consulte esta [sección](../action/action.md).
1. Enter a name and description.
1. ********
1. **** Contact Adobe to get this payload.
1. Adjust the different fields to be static or variable depending on if you want to map them on the Journey canvas. Certain fields, such as channel parameters for email address and personalization fields (ctx), you likely want defined as variables for mapping in context of the journey.
1. Haga clic en **Guardar**.

![](assets/accintegration1.png)
