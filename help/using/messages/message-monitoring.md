---
title: Monitor message execution
description: Learn monitoring guidelines
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 950f8186-07f6-4cc1-936c-d0984fb0f988
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Monitorización de mensajes {#monitor-message-execution}

[!DNL Journey Optimizer] <!--and APIs-->**[!UICONTROL Executions]**

**[!DNL Journey Optimizer]****[!UICONTROL Messages]****[!UICONTROL Executions]**

**[!UICONTROL Live view]****[!UICONTROL Global view]**

* **[!UICONTROL Live view]******[](../building-journeys/journey.md)****

   ![](assets/message-execution-tab-live.png)

   This list auto-refreshes every sixty seconds. If no execution occurred in the last 24 hours for a specific message, all columns will display null values (0) for that message.

* **[!UICONTROL Global view]******[](../building-journeys/journey.md)****

   ![](assets/message-execution-tab-global.png)

   This list auto-refreshes every ninety minutes. The data are aggregated over time since each message start date.

If a message is published but not triggered yet by a journey, it it not listed in any of the tabs. Only the following elements are listed:
* Messages that have been triggered, but not yet started (pending).
* Messages that have been triggered and that are currently running (in progress).

>[!NOTE]
>
>If a message has been used in several journeys, one row per journey is displayed for each execution.

By default, the messages are displayed starting from the most recent execution date. **[!UICONTROL Filters]** ****

![](assets/message-execution-tab-filters.png)

<!--**[!UICONTROL Quick action]**-->[](create-message.md)[](../reports/live-report.md)**[!UICONTROL Live view]**[](../reports/global-report.md)**[!UICONTROL Global view]**

![](assets/message-execution-open-live-report.png)

For each message execution, a number of indicators are displayed:

* **[!UICONTROL Message label]**[](create-message.md) The execution ID, which is automatically generated, is displayed in parentheses.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**

* **[!UICONTROL Status]**

* **[!UICONTROL Start date]**

* **[!UICONTROL Targeted]**

* **[!UICONTROL Excluded]**

* **[!UICONTROL Sent]**

* **[!UICONTROL Delivered]**

* **[!UICONTROL Bounces]** [](suppression-list.md)

* **[!UICONTROL Opens]**

* **[!UICONTROL Clicks]**

   >[!NOTE]
   >
   >Clicks do not exist for push notifications: when a user clicks a push notification, it opens the app, which can only be considered as an open.

* **[!UICONTROL Errors]**

* **[!UICONTROL Spam complaints]** [](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability)

You can choose which columns to display in the table. **[!UICONTROL Customize table]**

![](assets/message-execution-customize-table.png)

**** ****

![](assets/message-execution-data-format.png)

Clicking each hyperlink will open the corresponding message summary view. [](create-message.md)
