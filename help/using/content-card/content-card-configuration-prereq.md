---
title: Configuración de tarjetas de contenido
description: Requisitos previos del canal de tarjetas de contenido
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# Requisitos previos de tarjetas de contenido {#content-card-configuration-prereq}

Para que Adobe Journey Optimizer muestre correctamente las tarjetas de contenido, debe configurar las siguientes opciones de Adobe Experience Platform:

* **Recopilación de datos de Adobe Experience Platform**

  [Cree una secuencia de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure){target="_blank"} y [agregue el servicio Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure#aep){target="_blank"}. Habilite las opciones **[!UICONTROL Segmentación de Edge]** y **[!UICONTROL Adobe Journey Optimizer]**. Esto garantiza que Adobe Experience Platform Edge Network gestione los eventos de Journey Optimizer.
Agregue el grupo de campos **Evento de experiencia - Interacción de propuesta** al conjunto de datos para incluir estos datos en los informes. [Más información sobre las secuencias de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  Asegúrese de que la política de combinación predeterminada tenga habilitada la **Política de combinación activa en Edge** en **[!UICONTROL Cliente]** > **[!UICONTROL Perfiles]** > **[!UICONTROL Políticas de combinación]** en el menú de Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es#configure){target="_blank"}

  >[!NOTE]
  >
  >Cuando use una directiva de combinación personalizada de **[!UICONTROL preferencias del conjunto de datos]**, asegúrese de agregar el conjunto de datos **[!UICONTROL Recorrido entrante]** dentro de la directiva de combinación especificada.

* **Adobe Experience Platform Mobile o Platform Web SDK**

  Para aplicaciones móviles y web, para agregar modificaciones a tus páginas web o aplicaciones móviles, debes implementar [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/es/docs/platform-learn/implement-web-sdk/overview){target="_blank"} en tu sitio web o [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/){target="_blank"} en tus aplicaciones móviles.

* **Journey Optimizer**

  Crear una [configuración de tarjeta de contenido](#content-card-configuration).

* **Resolución de problemas**

  Use la vista de **Edge Delivery** en **Adobe Experience Platform Assurance** para solucionar problemas de experiencias móviles. Puede inspeccionar solicitudes, comprobar llamadas perimetrales y examinar datos de perfil. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **Experimentos de contenido**

  Asegúrese de que el conjunto de datos utilizado en la [secuencia de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/overview#_blank){target="_blank"} de la aplicación también esté incluido en la configuración de informes del experimento de contenido. Los datos de la aplicación no se mostrarán en los informes si los conjuntos de datos no coinciden.

  Aprenda a agregar conjuntos de datos para los informes de experimentos de contenido en [esta sección](../reports/reporting-configuration.md).

## Protección de administración de perfiles {#profile-management-guardrail}

Las tarjetas de contenido [!DNL Journey Optimizer] pueden segmentar perfiles seudónimos, es decir, perfiles que no se han autenticado o que aún no se conocen porque no se han utilizado anteriormente en otros canales. Este es el caso, por ejemplo, al dirigirse a todos los visitantes o audiencias en función de ID temporales como ECID.

Esto aumenta el recuento total de perfiles atractivos, lo que puede tener implicaciones de costes si se supera el número contractual de perfiles atractivos que ha adquirido. Las métricas de licencia de cada paquete se enumeran en la página [Descripción del producto Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Puede comprobar el número de perfiles atractivos en [tablero de uso de licencias](../audience/license-usage.md).

Para mantener los perfiles atractivos dentro de límites razonables, Adobe recomienda configurar un tiempo de vida (TTL) para eliminar automáticamente los perfiles seudónimos del perfil del cliente en tiempo real si no se han visto o no se han identificado en un intervalo de tiempo específico.

>[!NOTE]
>
>Aprenda a configurar la caducidad de los datos de los perfiles seudónimos en la [documentación de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

Adobe recomienda establecer el valor TTL en 14 días para que coincida con el TTL de perfil de Edge actual.