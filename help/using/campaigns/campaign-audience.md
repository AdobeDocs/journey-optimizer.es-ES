---
solution: Journey Optimizer
product: journey optimizer
title: Definición de la audiencia de la campaña de acción
description: Obtenga información sobre cómo definir la audiencia de la campaña de acción.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: crear, optimizador, campaña, superficie, mensajes
exl-id: 5635ef04-c69d-4397-9762-7a6f1265d453
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 4%

---

# Definición de la audiencia de la campaña de acción {#action-campaign-audience}

Utilice la ficha **[!UICONTROL Audiencia]** para definir la audiencia de la campaña.

![](assets/campaign-audience.png)

1. **Selección del público**

   Para las campañas de marketing, haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. [Más información sobre las audiencias](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >El uso de audiencias y atributos de [composición de audiencias](../audience/get-started-audience-orchestration.md) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.

1. **Seleccionar el tipo de identidad**

   En el campo **[!UICONTROL Tipo de identidad]**, elija el tipo de clave que desea usar para identificar a los individuos de la audiencia seleccionada. Puede utilizar un tipo de identidad existente o crear uno nuevo mediante el servicio de identidad de Adobe Experience Platform. Las áreas de nombres de identidad estándar se enumeran en [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Solo se permite un tipo de identidad por campaña. La campaña no puede dirigirse a las personas que pertenezcan a un segmento que no tenga el tipo de identidad seleccionado entre sus diferentes identidades. Obtenga más información acerca de tipos de identidad y áreas de nombres en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=es){target="_blank"}.

## Próximos pasos {#next}

Una vez que la audiencia de la campaña de acción esté lista, puede programar la campaña. [Más información](campaign-schedule.md)
