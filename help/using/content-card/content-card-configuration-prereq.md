---
title: Configuración de tarjetas de contenido
description: Requisitos previos del canal de tarjetas de contenido
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 5%

---

# Requisitos previos de tarjetas de contenido {#content-card-configuration-prereq}

Para que Adobe Journey Optimizer muestre correctamente las tarjetas de contenido, debe configurar las siguientes opciones de Adobe Experience Platform:

* **Recopilación de datos de Adobe Experience Platform**

  [Cree una secuencia de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure) y [agregue el servicio Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure#aep). Habilite las opciones **[!UICONTROL Segmentación de Edge]** y **[!UICONTROL Adobe Journey Optimizer]**. Esto garantiza que Adobe Experience Platform Edge Network gestione los eventos de Journey Optimizer.
Agregue el grupo de campos **Evento de experiencia - Interacción de propuesta** al conjunto de datos para incluir estos datos en los informes. [Más información sobre las secuencias de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure)

* **Adobe Experience Platform**

  Asegúrese de que la política de combinación predeterminada tenga habilitada la **Política de combinación activa en Edge** en **[!UICONTROL Cliente]** > **[!UICONTROL Perfiles]** > **[!UICONTROL Políticas de combinación]** en el menú de Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es#configure){target="_blank"}

  >[!NOTE]
  >
  >Cuando use una directiva de combinación personalizada de **[!UICONTROL preferencias del conjunto de datos]**, asegúrese de agregar el conjunto de datos **[!UICONTROL Recorrido entrante]** dentro de la directiva de combinación especificada.

* **Adobe Experience Platform Mobile o Platform Web SDK**

  Para aplicaciones móviles y web, para agregar modificaciones a tus páginas web o aplicaciones móviles, debes implementar [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/es/docs/platform-learn/implement-web-sdk/overview) en tu sitio web o [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/) en tus aplicaciones móviles.

* **Journey Optimizer**

  Crear una [configuración de tarjeta de contenido](#content-card-configuration).

* **Resolución de problemas**

  Use la vista de **Edge Delivery** en **Adobe Experience Platform Assurance** para solucionar problemas de experiencias móviles. Puede inspeccionar solicitudes, comprobar llamadas perimetrales y examinar datos de perfil. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/view/edge-delivery)

* **Experimentos de contenido**

  Asegúrese de que el conjunto de datos utilizado en la [secuencia de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/overview#_blank) de la aplicación también esté incluido en la configuración de informes del experimento de contenido. Los datos de la aplicación no se mostrarán en los informes si los conjuntos de datos no coinciden.

  Aprenda a agregar conjuntos de datos para los informes de experimentos de contenido en [esta sección](../reports/reporting-configuration.md).
