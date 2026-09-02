---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de contenido de AEM
description: Obtenga información sobre cómo acceder y administrar fragmentos de contenido de AEM
topic: Content Management
role: User
level: Beginner
exl-id: c36a53a4-c324-4082-838e-ed27bd3b2e90
TQID: https://experienceleague.adobe.com/GRQ3Wz7Y4YJ3545mTtju0R8en9BYiejyo8UoMx558nM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 28395abcdcba6ed8fd02f252a57022aa473f3d3b
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 0%

---

# Introducción a los fragmentos de contenido de Adobe Experience Manager {#aem-fragments}

>[!BEGINSHADEBOX]

**En esta página:** Empiece a usar los fragmentos de contenido de Adobe Experience Manager y comprenda cómo el ciclo de vida de creación y publicación determina qué fragmentos están disponibles en Journey Optimizer.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Para los clientes del sector sanitario, la integración solo se activa tras obtener la licencia de las ofertas adicionales de Journey Optimizer Healthcare Shield y Adobe Experience Manager Enhanced Security.

Al integrar **[!DNL Adobe Experience Manager as a Cloud Service]** y **[!DNL Adobe Experience Manager Managed Service]** con Adobe Journey Optimizer, puede utilizar fragmentos de contenido de AEM en recorridos y campañas. Para **[!DNL Adobe Experience Manager Managed Service]**, la integración admite los niveles de **Author** y **Publish** en el SP2 **de** Soporte a largo plazo de AEM (LTS); las actualizaciones en tiempo real de Adobe Experience Manager no están disponibles en esta versión. Póngase en contacto con su representante de Adobe Managed Services para configurar la instancia y [configurar el acceso al repositorio de Adobe Experience Manager](aem-admin-settings.md) para agregar su repositorio de Managed Services.

Para obtener más información sobre los fragmentos de contenido de AEM, consulte [Trabajar con fragmentos de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} en la documentación de Experience Manager.

## Ciclo de fragmento de contenido

![](assets/do-not-localize/AEM_CF.png)

Los fragmentos de contenido siguen diferentes etapas del ciclo vital según el nivel de Adobe Experience Manager en el que existan. [Obtenga más información en la documentación de Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

El contenido se crea y administra en el **nivel de creación**, donde los fragmentos pueden tener estados como Nuevo, Borrador, Publicado, Modificado o No publicado. Estos estados se aplican solamente en el **nivel de creación** y admiten la creación y revisión de contenido.

Cuando se publica un fragmento de contenido, se crea una copia en el **nivel de publicación** y se expone a través de un extremo público no autenticado. Para **[!DNL Adobe Experience Manager as a Cloud Service]**, Journey Optimizer admite la integración con **Author tier** y **Publish tier**.

Como resultado, Journey Optimizer muestra solo fragmentos de contenido publicados o modificados y siempre utiliza la última versión publicada. Los cambios realizados después de la publicación no se reflejarán en Journey Optimizer hasta que se vuelva a publicar el fragmento de contenido.
