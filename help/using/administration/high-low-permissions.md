---
title: Niveles de permisos
description: Learn about high and low level permissions
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: db6e970230b4d22b50c2035ecf5e7307e66feb2d
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Niveles de permisos {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Each product profile is composed of permissions allowing users to access the different features.
They can be divided into two types:

* ******[!UICONTROL Product profile]**[!DNL Admin console]**[!DNL Publish journeys]****[!DNL Manage subdomains delegation]** High level permissions encompass low level permissions.

* ****

**[!DNL Journey administrator]****[!DNL Manage journeys]** From this permission results the low-level permissions which will allow the Journey administrator to write, read and delete journeys.

## Journey capability {#journey-capability}

### [!DNL Manage journeys] {#manage-journeys}

**[!DNL Manage journeys]**

It includes the following low-level permissions:

* Journey Optimizer specific:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Adobe Experience Platform specific:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### [!DNL Publish journeys] {#publish-journeys}

**[!DNL Publish journeys]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] {#view-journeys}

**[!DNL View journeys]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * journeys.read

* Adobe Experience Platform specific:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] {#manage-journeys-events}

**[!DNL Manage journeys events, data sources and actions]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * journeys_events.read
   * journeys_events.write
   * journeys_events.delete
   * journeys_data_sources.read
   * journeys_data_sources.write
   * journeys_data_sources.delete
   * journeys_actions.read
   * journeys_actions.write
   * journeys_actions.delete

* Adobe Experience Platform specific:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys events, data sources and actions] {#view-journeys-event}

**[!DNL View journeys events, data sources and actions]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Adobe Experience Platform specific:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] {#view-journeys-report}

**[!DNL View journeys report]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * journeys_report.read
   * messages_report.read

* Adobe Experience Platform specific:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Message capability {#message-capability}

### [!DNL Manage messages] {#manage-messages}

**[!DNL Manage messages]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform specific:
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] {#mange-messages-preview}

**[!DNL Manage messages preview and test]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Adobe Experience Platform specific:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### [!DNL Publish messages] {#publish-messages}

**[!DNL Publish messages]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages.publish

* Adobe Experience Platform specific:
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] {#view-messages}

**[!DNL View messages]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages.read
   * messages_presets.read

* Adobe Experience Platform specific:
   * schemas.read
   * segments.read

### [!DNL View messages report] {#view-message-reports}

**[!DNL View messages report]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Decision management capability {#decisions-permissions}

### [!DNL Manage decisions] {#manage-decisioning}

**[!DNL Manage decisions]****[!DNL Activity entities]**

It includes the following low-level permissions:

* Decision management specific:
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform specific:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### [!DNL View decisions] {#view-decisions}

**[!DNL View decisions]**

It includes the following low-level permissions:

* Decision management specific:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Adobe Experience Platform specific:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] {#publish-decisions}

**[!DNL Publish offers decisioning]**

It includes the following low-level permissions:

* Decision management specific:
   * offers_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform specific:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] {#manage-decisions}

**[!DNL Manage ranking strategies]**

It includes the following low-level permissions:

* Decision management specific:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Administration capability {#administration-permissions}

### [!DNL Manage subdomains delegation] {#manage-subdomain}

**[!DNL Manage subdomains delegation]**

It includes the following low-level permissions:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] {#manage-ptr}

**[!DNL Manage PTR records]**

It includes the following low-level permissions:

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] {#view-ptr}

**[!DNL View PTR records]**

It includes the following low-level permissions:

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] {#manage-ip-pools}

**[!DNL Manage IP pools]**

It includes the following low-level permissions:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### [!DNL Manage messages general settings] {#manage-message-settings}

**[!DNL Manage messages general settings]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform specific:
   * schemas.read

### [!DNL View messages general settings] {#view-message-settings}

**[!DNL View messages general settings]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages_general_settings.read
* Adobe Experience Platform specific:
   * schemas.read

### [!DNL Manage messages presets] {#manage-message-presets}

**[!DNL Manage messages presets]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (from Adobe Experience Platform Launch)

### [!DNL View messages presets] {#view-message-presets}

**[!DNL View messages presets]**

It includes the following low-level permissions:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)

### [!DNL Manage suppression] {#manage-suppression}

**[!DNL Manage suppression]**

It includes the following low-level permissions:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] {#view-suppression-list}

**[!DNL View suppression list]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * suppression_list.view

* Adobe Experience Platform specific:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] {#export-suppression-list}

**[!DNL Export suppression list]**

It includes the following low-level permissions:

* Journey Optimizer specific:
   * suppression_list.export

* Adobe Experience Platform specific:
   * profiles.read
   * datasets.read

## Journey Optimizer Library capability {library-permissions}

### Manage Library Items {#library-items}

**[!DNL Manage Library Items]**[!DNL Journey Optimizer]

It includes the following low-level permissions:

* library_item.create
* ibrary_item.delete
