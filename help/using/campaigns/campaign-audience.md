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
TQID: https://experienceleague.adobe.com/3lWwW0Lru2D5D83QqHl48Gsxv7JVKjX8ZBmZAiMFiB0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0c30d994a1ba0b4b5ef3ee1c34d836ce7887cc19
workflow-type: tm+mt
source-wordcount: 231
ht-degree: 6%

---

# Definición de la audiencia de la campaña de acción {#action-campaign-audience}

>[!BEGINSHADEBOX]

**En esta página:** Seleccione la audiencia y el tipo de identidad en la ficha Audiencia para que la campaña de acción se dirija a las personas adecuadas.

>[!ENDSHADEBOX]

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
