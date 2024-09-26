---
solution: Journey Optimizer
product: journey optimizer
title: Revisión y activación de una campaña
description: Obtenga información sobre cómo revisar y activar campañas en Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campaña, revisión, validación, activación, activación, optimizador
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 6%

---

# Revisión y activación de una campaña {#review-activate}

>[!IMPORTANT]
>
>A partir de la versión de septiembre, una nueva experiencia de activación de recorrido y campaña le permite administrar todo el proceso de aprobación, lo que garantiza que las campañas y los recorridos sean revisados y aprobados a fondo por las partes interesadas adecuadas antes de lanzarse. Esta función está disponible con disponibilidad limitada. [Más información](../test-approve/gs-approval.md)

Una vez configurada la campaña, debe revisar su parámetro y contenido antes de activarla. Para ello, siga estos pasos:

1. En la pantalla de configuración de la campaña, haga clic en **[!UICONTROL Revisar para activar]** y mostrar un resumen de la campaña.

   El resumen le permite modificar la campaña si es necesario y comprobar si algún parámetro es incorrecto o falta.

   >[!IMPORTANT]
   >
   >En caso de errores, no puede activar la campaña. Resuelva los errores antes de continuar.

   ![](assets/create-campaign-alerts.png)

1. Compruebe que la campaña esté configurada correctamente y luego haga clic en **[!UICONTROL Activar]**.

1. La campaña está ahora activada. Su estado es **[!UICONTROL Activo]** o **[!UICONTROL Programado]** si ha especificado una fecha de inicio. [Más información sobre estados de campañas](get-started-with-campaigns.md#statuses).

   El mensaje configurado en la campaña se envía inmediatamente o en la fecha especificada.

   >[!NOTE]
   >
   >El estado **[!UICONTROL Completado]** se asigna automáticamente a una campaña 3 días después de activarse o en la fecha de finalización de la campaña si tiene una ejecución recurrente.
   >
   >Si no se ha especificado una fecha de finalización, la campaña mantendrá el estado **[!UICONTROL Activo]**. Para cambiarlo, debe detener la campaña manualmente. [Aprenda a detener una campaña](modify-stop-campaign.md)

1. Una vez activada una campaña, puede comprobar en cualquier momento su información abriéndola. El resumen le permite obtener estadísticas sobre el número de perfiles objetivo y las acciones enviadas y fallidas.

   También puede obtener estadísticas adicionales en informes dedicados si hace clic en el botón **[!UICONTROL Informes]**. [Más información](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)
