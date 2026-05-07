---
title: Content cards configuration
description: Content cards channel prerequisites
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 9%

---

# Requisitos previos de tarjetas de contenido {#content-card-configuration-prereq}

For Adobe Journey Optimizer to correctly display content cards, you must configure the following Adobe Experience Platform settings:

* **Adobe Experience Platform Data Collection**

  [Create a datastream](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure){target="_blank"} and [add the Experience Platform service](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure#aep){target="_blank"}. Enable the **[!UICONTROL Edge Segmentation]** and **[!UICONTROL Adobe Journey Optimizer]** options. This ensures that Journey Optimizer events are handled by the Adobe Experience Platform Edge Network.
Add the **Experience Event – Proposition Interaction** field group to your dataset to include this data in your reports. [Learn more about datastreams](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  Ensure the default merge policy has **Active-On-Edge Merge Policy** enabled under **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es#configure){target="_blank"}

  >[!NOTE]
  >
  >When using a custom **[!UICONTROL Dataset preference]** merge policy, make sure to add the **[!UICONTROL Journey Inbound]** dataset within the specified merge policy.

* **Adobe Experience Platform Mobile or Platform Web SDK**

  For mobile and web applications, to add modifications to your web pages or mobile apps, you need to implement either the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/es/docs/platform-learn/implement-web-sdk/overview){target="_blank"} on your website or [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home){target="_blank"} on your mobile apps.

* **Journey Optimizer**

  Create a [Content card configuration](#content-card-configuration).

* **Resolución de problemas**

  Use the **Edge Delivery** view within **Adobe Experience Platform Assurance** to troubleshoot mobile experiences. It can inspect requests, verify edge calls, and examine profile data. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **Content Experiments**

  Ensure the dataset used in your app&#39;s [datastream](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/overview#_blank){target="_blank"} is also included in your content experiment reporting configuration. Los datos de la aplicación no se mostrarán en los informes si los conjuntos de datos no coinciden.

  Aprenda a agregar conjuntos de datos para los informes de experimentos de contenido en [esta sección](../reports/reporting-configuration.md).

>[!CAUTION]
>
>Al segmentar perfiles seudónimos (visitantes no autenticados) con sus tarjetas de contenido, considere la posibilidad de establecer un tiempo de vida (TTL) para la eliminación automática de perfiles a fin de administrar el recuento de perfiles atractivos y los costes asociados. [Más información](../start/guardrails.md#profile-management-inbound)