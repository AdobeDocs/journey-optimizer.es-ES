---
solution: Journey Optimizer
product: journey optimizer
title: Modificación o detención de una campaña
description: Obtenga información sobre cómo modificar, detener o duplicar campañas en directo en [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 0433e312db84ee16a076c183a82345de372c6ae7
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 2%

---

# Administración de campañas {#modify-stop-campaign}

Una vez activada una campaña, puede modificarla o detenerla en cualquier momento. Estas operaciones están disponibles para campañas con una ejecución recurrente solamente.

Además, puede duplicar las campañas en vivo (ejecutadas una vez o con una ejecución recurrente) para crear otras nuevas y archivar las campañas completadas o detenidas.

## Modificación de una campaña recurrente {#modify}

Para modificar y crear una nueva versión de una campaña recurrente, siga estos pasos:

1. Abra la campaña y haga clic en el botón **[!UICONTROL Modificar campaña]** botón.

1. Se crea una nueva versión de la campaña. Puede comprobar la versión activa haciendo clic en **[!UICONTROL Abrir versión en directo]**.

   ![](assets/create-campaign-draft.png)

   En la lista de campañas, las campañas activadas con una versión de borrador en curso se muestran con un icono específico en la variable **[!UICONTROL Estado]** para abrir el Navegador. Haga clic en este icono para abrir la versión de borrador de la campaña.

   ![](assets/create-campaign-edit-list.png)

1. Una vez que los cambios estén listos, puede activar la nueva versión de la campaña (consulte [Revisar y activar una campaña](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Al activar el borrador, se reemplaza la versión activa de la campaña.

## Detener una campaña recurrente {#stop}

Para detener una campaña recurrente, ábrala y haga clic en el botón **[!UICONTROL Detener campaña]** botón.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Detener una campaña no detendrá un envío en curso, pero detendrá un envío programado o los siguientes sucesos si el envío ya está en curso.

<!-- inbound campaign (inapp): can stop and resume -->

## Duplicar una campaña {#duplicate}

Puede duplicar una campaña activa para crear una nueva. Para ello, abra la campaña y haga clic en **[!UICONTROL Duplicar]**.

![](assets/create-campaign-duplicate.png)

## Archivar una campaña {#archive}

Con el tiempo, la lista de campañas sigue creciendo y, finalmente, dificulta el examen de las campañas completadas y detenidas.

Para evitarlo, puede archivar campañas completadas y detenidas que ya no necesite. Para ello, haga clic en el botón elipse y seleccione **[!UICONTROL Archivo]**.

![](assets/create-campaign-archive.png)

Las campañas archivadas se pueden recuperar utilizando el filtro dedicado de la lista. [Obtenga información sobre cómo acceder a campañas](get-started-with-campaigns.md#access)
