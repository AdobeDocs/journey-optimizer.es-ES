---
title: Acerca de los datos de Adobe Analytics
description: Aprenda a aprovechar los datos de Adobe Analytics
feature: Eventos
topic: Administración
role: Administrator
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# Aproveche los datos de Adobe Analytics{#analytics-data}

Puede aprovechar todos los datos de evento de comportamiento de Adobe Analytics que ya está capturando y transmitiendo a la plataforma para almacenar en déclencheur los recorridos y automatizar las experiencias para sus clientes.

>[!NOTE]
>
>Esta sección solo se aplica para eventos basados en reglas y clientes que necesitan utilizar datos de Adobe Analytics.

Para que esto funcione, debe activar en Adobe Experience Platform el grupo de informes que desea aprovechar:

1. En Adobe Experience Platform, seleccione **[!UICONTROL Sources]** y luego **[!UICONTROL Add data]** en la sección Adobe Analytics . Se muestra la lista de grupos de informes de Adobe Analytics disponibles.

1. Elija el grupo de informes que desea habilitar, haga clic en **[!UICONTROL Next]** y haga clic en **[!UICONTROL Finish]**.

1. Comparta el ID de datos de origen con el punto de contacto del programa Beta.

Esto habilita el conector de origen de Analytics para ese grupo de informes. Cada vez que entran los datos, estos se transforman en un evento de Experience y se envían a Adobe Experience Platform.

![](../assets/jo-event9.png)

Obtenga más información sobre el conector de origen de Adobe Analytics en [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) y [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html).
