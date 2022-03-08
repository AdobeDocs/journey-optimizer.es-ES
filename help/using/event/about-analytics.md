---
title: Acerca de los datos de Adobe Analytics
description: Aprenda a aprovechar los datos de Adobe Analytics
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 8%

---

# Aprovechar los datos de Adobe Analytics{#analytics-data}

Puede aprovechar todos los datos de evento de comportamiento de Adobe Analytics que ya está capturando y transmitiendo a la plataforma para almacenar en déclencheur los recorridos y automatizar las experiencias para sus clientes.

>[!NOTE]
>
>Esta sección solo se aplica para eventos basados en reglas y clientes que necesitan utilizar datos de Adobe Analytics.

Para que esto funcione, debe activar en Adobe Experience Platform el grupo de informes que desea aprovechar:

1. En Adobe Experience Platform, seleccione **[!UICONTROL Sources]** then **[!UICONTROL Add data]** en la sección Adobe Analytics . Se muestra la lista de los grupos de informes de Adobe Analytics disponibles.

1. Elija el grupo de informes que desea habilitar y haga clic en **[!UICONTROL Next]** y haga clic en **[!UICONTROL Finish]**.

1. Comparta el ID de datos de origen con el punto de contacto del programa Beta.

Esto habilita el conector de origen de Analytics para ese grupo de informes. Cada vez que entran los datos, estos se transforman en un evento de Experience y se envían a Adobe Experience Platform.

![](../assets/jo-event9.png)

Obtenga más información sobre el conector de origen de Adobe Analytics en  [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=es){target=&quot;_blank&quot;} y [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=es){target=&quot;_blank&quot;}.
