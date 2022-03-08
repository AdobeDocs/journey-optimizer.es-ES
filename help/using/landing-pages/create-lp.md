---
title: Creación de una página de destino
description: Learn how to configure and publish a landing page in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 4%

---

# Create and publish landing pages {#create-lp}

>[!CAUTION]
>
>The use of landing pages is currently available in early access to select users only. If you want to leverage this feature, contact your Adobe account executive.

## Access landing pages {#access-landing-pages}

**[!UICONTROL Journey Management]****[!UICONTROL Landing pages]**

![](assets/lp_access-list.png)

**[!UICONTROL Landing Pages]** You can filter them based on their status or modification date.

![](assets/lp_access-list-filter.png)

## Creación de una página de destino {#create-landing-page}

The steps to create a landing page are as follows.

1. **[!UICONTROL Create landing page]**

   ![](assets/lp_create-lp.png)

1. Add a title. You can add a description if needed.

   ![](assets/lp_create-lp-details.png)

1. Select a preset.

   ![](assets/lp_create-lp-presets.png)

   >[!NOTE]
   >
   >[](https://helpx.adobe.com/es/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html)

1. Haga clic en **[!UICONTROL Create]**.

1. The primary page and its properties display. [](#configure-primary-page)

   ![](assets/lp_primary-page.png)

1. Click the + icon to add a subpage. [](#configure-subpages)

   ![](assets/lp_add-subpage.png)

[](#configure-primary-page)[](#configure-subpages)[](#test-landing-page)[](#publish-landing-page)

## Configure the primary page {#configure-primary-page}

The primary page is the page that is immediately displayed to the users after they click the link to your landing page, such as from an email or a website.

To define the primary page settings, follow the steps below.

1. **[!UICONTROL Primary page]**

1. Edit the content of your page using the content designer. [](design-lp.md)

   ![](assets/lp_open-designer.png)

1. Define your landing page URL. The first part of the URL requires the domain delegation to be performed. It is pre-filled and cannot be edited through the user interface. [](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html)

   >[!CAUTION]
   >
   >The landing page URL must be unique.

   ![](assets/lp_access-url.png)

1. You can define an expiry date for your page. In that case, you must select an action upon page expiry:

   * **[!UICONTROL Redirect URL]**
   * **[!UICONTROL Custom page]**[](#configure-subpages)
   * **[!UICONTROL Browser error]**

   ![](assets/lp_expiry-date.png)

   <!--1. In the **[!UICONTROL Additional data]** section, define a **[!UICONTROL Key]** and the corresponding **[!UICONTROL Parameter value]**. // you can define how the data entered in the landing page is managed once it has been submitted by a user??-->

1. [](design-lp.md)**[!UICONTROL Subscription list]**

   ![](assets/lp_subscription-list.png)

1. [](../building-journeys/journey-gs.md#jo-build) [](lp-use-cases.md#subscription-to-a-service)

   ![](assets/lp_create-journey.png)

   **[!UICONTROL Create journey]****[!UICONTROL Journey Management]****[!UICONTROL Journeys]**

## Configure subpages {#configure-subpages}

You can add up to 2 subpages. For example, you can create a &#39;thank you&#39; page that will display once the users submit the form, and you can define an error page that will be called if a problem occurs with the landing page.

To define the subpage settings, follow the steps below.

1. **[!UICONTROL Subpage 1]**

1. Edit the content of your page using the content designer. [](design-lp.md)

1. Define your landing page URL. The first part of the URL requires the domain delegation to be performed. It is pre-filled and cannot be edited through the user interface. [](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html)

   >[!CAUTION]
   >
   >The landing page URL must be unique.

![](assets/lp_subpage-settings.png)

## Test the landing page {#test-landing-page}

Once your landing page settings and content have been defined, you can use test profiles to preview it. [](../personalization/personalize.md)

>[!CAUTION]
>
>You need to have test profiles available to be able to preview your messages and send proofs. [](../building-journeys/creating-test-profiles.md)

1. **[!UICONTROL Preview & test]**

   ![](assets/lp_preview-button.png)

   >[!NOTE]
   >
   >**[!UICONTROL Preview]**

1. **[!UICONTROL Preview & test]**

   ![](assets/lp_test-profiles.png)

   The steps to select test profiles are the same as when testing a message. Se detallan en [esta sección](../messages/preview.md#select-test-profiles).

1. **[!UICONTROL Preview]****[!UICONTROL Open preview]**

   ![](assets/lp_open-preview.png)

1. The preview of your landing page opens in a new tab. Personalized elements are replaced by the selected test profile data.

   ![](assets/lp_preview.png)

1. Select other test profiles to preview the rendering for each variant of your landing page.

## Comprobación de alertas {#check-alerts}

While you are creating your landing page, alerts warn you when you need to take important actions before publishing.

Alerts are displayed on top right of the screen, as shown below:

![](assets/lp_alerts.png)

>[!NOTE]
>
>If you do not see this button, no alert has been detected.

Two types of alerts can happen:

* ****<!--For example, a message will display if -->

* **** For example, you will get a warning if the primary page URL is missing.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> ****

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you need to resolve all **error** alerts.
-->

## Publish the landing page {#publish-landing-page}

Once your landing page is ready, you can publish it to make it available for use in a message.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Before publishing, check and resolve alerts. [Más información](#check-alerts)

**[!UICONTROL Published]**

[!DNL Journey Optimizer][](../messages/create-message.md)[](../building-journeys/journey.md)

>[!NOTE]
>
>You can monitor your landing page impacts through specific reports. [Más información](lp-report.md)

