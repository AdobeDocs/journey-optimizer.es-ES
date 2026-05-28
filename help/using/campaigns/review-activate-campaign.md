---
solution: Journey Optimizer
product: journey optimizer
title: Revisión y activación de una campaña de acción
description: Obtenga información sobre cómo revisar y activar campañas de acción en  [!DNL Journey Optimizer].
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campaña, revisión, validación, activación, activación, optimizador
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
TQID: https://experienceleague.adobe.com/BKGXccq-kwZJA-cZ4SAyf3zJBIvyJnr5V01xmbQgwmo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 087a4bd254486a4962d8338d1d35ffb5345341af
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 4%

---

# Revisión y activación de la campaña de acción {#action-campaign-review}

Una vez configurada la campaña de acción, debe revisar su parámetro y contenido antes de activarla. Para realizar esto, siga los pasos a continuación.

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, debe solicitar la aprobación para poder enviarla. [Más información](../test-approve/gs-approval.md)

1. En la pantalla de configuración de la campaña, haga clic en **[!UICONTROL Revisar para activar]** y mostrar un resumen de la campaña.

   ![](assets/campaign-review.png)

1. Se muestra un resumen de la configuración de la campaña, que le permite comprobar si algún parámetro es incorrecto o falta y modificar la campaña si es necesario.

   En caso de errores, no puede activar la campaña. Resuelva los errores antes de continuar.

   ![](assets/create-campaign-alerts.png)

1. Cuando una campaña usa [políticas de decisión](../experience-decisioning/create-decision.md) en su contenido, puede revisar la estructura de cada política y copiar los detalles técnicos directamente desde el resumen de la campaña. [Descubra cómo](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

1. Compruebe que la campaña esté configurada correctamente y luego haga clic en **[!UICONTROL Activar]**.

1. La campaña se activa. Su estado es **[!UICONTROL Activo]** o **[!UICONTROL Programado]** si ha especificado una fecha de inicio. El mensaje configurado en la campaña se envía inmediatamente o en la fecha especificada.

   El estado **[!UICONTROL Completado]** se asigna automáticamente a la campaña 3 días después de activarse o en la fecha de finalización de la campaña si esta tiene una ejecución recurrente. [Más información sobre los estados de las campañas](manage-campaigns.md#statuses).

   Si no se ha especificado una fecha de finalización, la campaña mantiene el estado **[!UICONTROL Activo]**. Para cambiarlo, debe detener la campaña manualmente. [Aprenda a detener una campaña](manage-campaigns.md)

1. Una vez activada una campaña, puede comprobar en cualquier momento su información abriéndola. El resumen le permite obtener estadísticas sobre el número de perfiles objetivo y las acciones enviadas y fallidas.

   También puede obtener estadísticas adicionales en informes dedicados si hace clic en el botón **[!UICONTROL Informes]**. [Más información](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)
