---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los datos de Adobe Analytics
description: Aprenda a aprovechar los datos de Adobe Analytics
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: a6735063ec68b40b1441b379a20cba8953b59447
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Aprovechar los datos de Adobe Analytics{#analytics-data}

Puede aprovechar todos los datos de evento de comportamiento de Adobe Analytics que ya está capturando y transmitiendo a Adobe Experience Platform para activar recorridos y automatizar experiencias para sus clientes.

>[!NOTE]
>
>Esta sección solo se aplica para eventos basados en reglas y clientes que necesitan utilizar datos de Adobe Analytics.

Para que esto funcione, debe activar en Adobe Experience Platform el grupo de informes que desee utilizar. Para ello, siga los pasos a continuación:

1. Conéctese a Adobe Experience Platform y vaya a **[!UICONTROL Sources]**.
1. En la sección Adobe Analytics , seleccione **[!UICONTROL Add data]**: se muestra la lista de los grupos de informes disponibles de Adobe Analytics.

1. Seleccione el grupo de informes que desea habilitar y haga clic en **[!UICONTROL Next]** y **[!UICONTROL Finish]**.

1. Comparta el ID de datos de origen con el punto de contacto del programa Beta.

Esto habilita el conector de origen de Analytics para ese grupo de informes. Siempre que entran los datos, estos se transforman en un evento de Experience y se envían a Adobe Experience Platform.

![](assets/jo-event9.png)

Obtenga más información sobre el conector de origen de Adobe Analytics en  [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html){target=&quot;_blank&quot;} y [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target=&quot;_blank&quot;}.
