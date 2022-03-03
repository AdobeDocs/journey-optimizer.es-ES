---
title: Configuración de un evento empresarial
description: Learn how to create a business event
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
source-git-commit: 587ac4a17db71790ed4d9ee07214293a2882180c
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 12%

---

# Configuración de un evento empresarial {#configure-a-business-event}

Unlike unitary events, business events are not linked to a specific profile. The event ID type is always rule-based. [](../event/about-events.md)

Read segment based journeys can be triggered in one-shot, by a scheduler on a regular basis or by a business event, when the event occurs.

Business events can be &quot;a product is back in stock&quot;, &quot;the stock price of a company reaches a certain value”, etc.

>[!NOTE]
>
>[](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-business-event.html)

## Notas importantes {#important-notes}

* Only time series schemas are available. Experience Events, Decision Events and Journey Step Events schemas are not available. The event schema must contain a primary identity. `_id``timestamp`
* Business events can only be dropped as the first step of a journey.
* When dropping a business event as the first step of a journey, the scheduler type of the journey will be &quot;business event&quot;.
* Only a read segment activity can be dropped after a business event. It is automatically added as the next step.
* **[!UICONTROL Execution]**
* After a business event is triggered, there will be a delay to have the segment exported from 15 minutes to up to one hour.
* When testing a business event, you have to pass the event parameters and the identifier of the test profile that will enter the journey in test. Also, when testing a business event based journey, you can only trigger single profile entrance. Consulte [esta sección](../building-journeys/testing-the-journey.md#test-business). In test mode, there is no &quot;Code view&quot; mode available.
* What happens to individuals that are currently in the journey if a new business event arrives? It behaves the same way as when individuals are still in a recurring journey when a new recurrence happens. Their path is ended. As a result, marketers must pay attention to avoid building too long journeys if they expect frequent business events.

## Multiple business events {#multiple-business-events}

Here are a few important notes that apply when multiple business events are received in a row.

****

Business events follow re-entrance rules in the same way as for unitary events. If a journey allows re-entrance, the next business event will be processed.

****

In the case of on-shot business events, for a given journey, data pushed by the first event job is reused during a 1-hour time window. For scheduled journeys, there is no guardrail. [](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)

## Get started with business events {#gs-business-events}

Here are the first steps to configure a business event:

1. **[!UICONTROL Configurations]** **[!UICONTROL Events]****[!UICONTROL Manage]** Se muestra la lista de eventos.

   ![](assets/jo-event1.png)

1. Haga clic en **[!UICONTROL Create Event]** para crear un nuevo evento. El panel de configuración de evento se abre en el lado derecho de la pantalla.

   ![](assets/jo-event2.png)

1. Enter the name of your event. You can also add a description.

   ![](assets/jo-event3-business.png)

   >[!NOTE]
   >
   >No utilice espacios ni caracteres especiales. No utilice más de 30 caracteres.

1. **[!UICONTROL Type]******

   ![](assets/jo-event3bis-business.png)

1. El número de recorridos que utiliza este evento se muestra en el campo **[!UICONTROL Used in]**. Puede hacer clic en el icono **[!UICONTROL View journeys]** para mostrar la lista de los recorridos con este evento.

1. Define the schema and payload fields: this is where you select the event information (usually called a payload) journeys expects to receive. Podrá utilizar esta información en su recorrido. Consulte [esta sección](../event/about-creating-business.md#define-the-payload-fields).

   ![](assets/jo-event5-business.png)

   Only time series schemas are available. Experience Events, Decision Events and Journey Step Events schemas are not available. The event schema must contain a primary identity. `_id``timestamp`

   ![](assets/test-profiles-4.png)

1. **[!UICONTROL Event ID condition]** Using the simple expression editor, define the condition that will be used by the system to identify the events that will trigger your journey.
   ![](assets/jo-event6-business.png)

   In our example, we wrote a condition based on the product&#39;s id. This means that whenever the system receives an event that matches this condition, it will pass it to journeys.

   >[!NOTE]
   >
   >In the simple expression editor, not all operators are available, they depend on the data type. For example, for a string type of field, you can use &quot;contains&quot; or &quot;equal to&quot;.

1. Haga clic en **[!UICONTROL Save]**.

   ![](assets/journey7-business.png)

   El evento está ahora configurado y listo para añadirse a un recorrido. Se requieren pasos de configuración adicionales para recibir eventos. Consulte [esta página](../event/additional-steps-to-send-events-to-journey-orchestration.md).

## Define the payload fields {#define-the-payload-fields}

The payload definition allows you to choose the information the system expects to receive from the event in your journey and the key to identify which person is associated to the event. The payload is based on the Experience Cloud XDM field definition. [](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html)

1. **[!UICONTROL Fields]****[!UICONTROL Edit]**

   ![](assets/journey8-business.png)

   All the fields defined in the schema are displayed. The list of fields varies from one schema to another. You can search for a specific field or use the filters to display all nodes and fields or only the selected fields. According to the schema definition, some fields may be mandatory and pre-selected. You cannot unselect them. All fields that are mandatory for the event to be received properly by journeys are selected by default.

   ![](assets/journey9-business.png)

   >[!NOTE]
   >
   > `_id``timestamp`

1. Select the fields you expect to receive from the event. These are the fields which the business user will leverage in the journey.

1. **[!UICONTROL Save]****[!UICONTROL Enter]**

   **[!UICONTROL Fields]**

   ![](assets/journey12-business.png)

## Preview the payload {#preview-the-payload}

The payload preview allows you to validate the payload definition.

1. **[!UICONTROL View Payload]**

   ![](assets/journey13-business.png)

   You can notice that the fields selected are displayed.

   ![](assets/journey14-business.png)

1. Check the preview to validate the payload definition.

1. Then, you can share the payload preview with to the person responsible for the event sending. [!DNL Journey Optimizer] Consulte [esta página](../event/additional-steps-to-send-events-to-journey-orchestration.md).
