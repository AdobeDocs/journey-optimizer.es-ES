---
title: Monitorización de sus experiencias web
description: Obtenga información sobre cómo monitorizar las experiencias web en Journey Optimizer
feature: Web Channel, Reporting, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: d89795bb-c51d-4d1f-b7ed-2b2c5d278922
TQID: https://experienceleague.adobe.com/CEjKwnKx1ixUKA-mO7FfWGXaW9FyO-I-ZYyYm0scs88
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c618a0dc-1818-4c6d-9916-0d92e6796f24id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 288
ht-degree: 3%

---

# Monitorización de sus experiencias web {#monitor-web-experiences}

## Consulte los informes web {#check-web-reports}

Una vez que la experiencia web esté activa, puede consultar la pestaña **[!UICONTROL Web]** del [informe de Recorrido](../reports/journey-global-report-cja-web.md) y el [informe de campaña](../reports/campaign-global-report-cja-web.md) para comparar elementos como el número de impresiones, la tasa de clics y el número de interacciones con la página web.

<!--You can check the **[!UICONTROL Web]** tab of the campaign reports. Learn more about the campaign web [live report](../reports/campaign-live-report.md#web-tab) and [global report](../reports/campaign-global-report-cja.md#web).-->

Para mejorar aún más la monitorización de la experiencia web, también puede rastrear los clics en cualquier elemento específico del sitio web. Esto le permite mostrar el número de clics en ese elemento en los informes web. [Descubra cómo](#use-click-tracing)

## Uso del rastreo de clics {#use-click-tracking}

El diseñador web le permite seleccionar cualquier elemento del sitio web y rastrear los clics en ese elemento.

Esta información puede ser útil para mejorar la experiencia de los usuarios del sitio web. Por ejemplo, si los [informes web](../reports/campaign-global-report-cja-web.md) muestran que muchos usuarios hacen clic en un elemento en el que no se puede hacer clic, es posible que desee agregar un vínculo a ese elemento.

1. Seleccione un elemento en su página y elija **[!UICONTROL Haga clic en rastrear elemento]** en el menú contextual.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >Se puede seleccionar cualquier elemento, activo o no.

1. La acción rastreada correspondiente se mostrará automáticamente en el panel **[!UICONTROL Hacer clic en rastrear]** de la izquierda.

   ![](assets/web-designer-click-track-pane.png)

1. Añada una etiqueta significativa para administrar todos los elementos rastreados y encontrarlos fácilmente en los informes. El campo **[!UICONTROL Selector de CSS]** muestra información para localizar el elemento seleccionado.

1. Repita los pasos anteriores para seleccionar tantos otros elementos como necesite para el rastreo de clics. Las acciones correspondientes se enumeran todas en el panel izquierdo.

   ![](assets/web-designer-click-tracking-actions.png)

1. Para eliminar el rastreo de clics en un elemento, seleccione el icono de eliminación correspondiente.

Una vez que la campaña esté activa, puede comprobar el número de clics de cada elemento en los [informes activos](../reports/campaign-live-report.md#web-tab) y [informes de Customer Journey Analytics](../reports/campaign-global-report-cja-web.md) de la web de la campaña.
