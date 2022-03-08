---
title: Update Profile
description: Learn how to use the Update Profile activity in a journey
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Update Profile {#update-profile}

**[!UICONTROL Update Profile]**

## Notas importantes

* ****
* The action only updates existing fields, it does not create new profile fields.
* ****
* Just like any other action, you can define an alternative path in case of error or timeout and you cannot place two actions in parallel.
* The update request sent to Platform will be fast but not immediate/within a second. It will take normally a few seconds but sometimes more with no guarantee. As a result, for example, if an action is using &quot;field 1&quot; updated by an Update Profile action positioned right before, you should not expect that &quot;field 1&quot; will be updated in the action.
* ****

## Using the test mode {#using-the-test-mode}

In test mode, the profile update will not be simulated. The update will be performed on the test profile.

Only test profiles can enter a journey in test mode. You can either create a new test profile or turn an existing profile into a test profile. In Adobe Experience Platform, you can update profiles attributes via a csv file import or API calls. ****

[](../building-journeys/creating-test-profiles.md#create-test-profiles-csv)

## Using the profile update

1. Design your journey by starting with an event. [](../building-journeys/journey.md)

1. ********

   ![](assets/profileupdate0.png)

1. Select a schema from the list.

1. **** Only one field can be selected.

   ![](assets/profileupdate2.png)

1. Select a dataset from the list.

   >[!NOTE]
   >
   >**** The dataset selection is needed as the profile is a record related to a dataset.

1. ****

   * Using the simple expression editor, you can select a field from a data source or from the incoming event.

      ![](assets/profileupdate4.png)

   * ****

      ![](assets/profileupdate3.png)

****

![](assets/profileupdate1.png)
