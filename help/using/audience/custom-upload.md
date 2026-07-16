---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los públicos de Adobe Experience Platform
description: Aprenda a trabajar con los públicos de Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 71c652ba-f38f-452c-9c1b-dcd728307baf
TQID: https://experienceleague.adobe.com/HkybhydJwQDHVEXCKM5o16ZNeiBk-n9mogm-2pwFKus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 22d6cddf35fa26a5fd3f0eddc74ed15faf9d6503
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 8%

---

# Carga personalizada {#custom-upload}

>[!BEGINSHADEBOX]

**En esta página:** Obtenga información sobre cómo importar una audiencia de un archivo CSV mediante Adobe Experience Platform Audience Portal y asignar su atributo de identidad a perfiles de clientes.

>[!ENDSHADEBOX]

Adobe Experience Platform Audience Portal le permite importar una audiencia utilizando un archivo CSV.

Durante el proceso de carga personalizado, especifique el atributo CSV que se utilizará como identidad y la identidad del perfil a la que se asigna. Esto establece un vínculo entre los datos de audiencia y el perfil. Si el archivo CSV contiene un valor de identidad que no se encuentra en el perfil, se crea un nuevo perfil con ese valor de identidad.

![](assets/import-audience.png)

Encontrará información detallada sobre cómo importar audiencias en [Documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}.

>[!NOTE]
>
>Para audiencias de carga personalizadas (carga CSV) y otras audiencias externas, **[!UICONTROL Lectura incremental]** no es compatible funcionalmente hoy. En cada repetición, se recupera **toda la audiencia**, independientemente de la configuración de alternancia de lectura incremental.

Obtenga información sobre cómo cargar audiencias en formato CSV en vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3423362?captions=spa&quality=12)
