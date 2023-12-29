---
solution: Journey Optimizer
product: journey optimizer
title: Modificación o detención de una campaña
description: Aprenda a modificar, detener o duplicar campañas en directo en Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: administrar campañas, estado, programación, acceso, optimizador
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: b9630c922ff67b0a402af5f950ee4e5a442bb1b1
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 1%

---

# Administración de campañas {#modify-stop-campaign}

Una vez activada una campaña, puede modificarla o detenerla en cualquier momento. Estas operaciones están disponibles para campañas con una ejecución recurrente solamente.

Además, puede duplicar campañas en directo (ejecutadas una vez o con una ejecución recurrente) para crear otras nuevas y archivar las campañas completadas o detenidas.

## Acceso a campañas {#access}

Se puede acceder a las campañas desde **[!UICONTROL Campañas]** menú.

De forma predeterminada, la lista muestra todas las campañas con el **[!UICONTROL Borrador]**, **[!UICONTROL Programado]**, y **[!UICONTROL Activo]** estados. Para mostrar las campañas detenidas, completadas y archivadas, debe borrar el filtro.

![](assets/create-campaign-list.png)

Además, puede filtrar la lista en función del tipo de campaña y canal, o las etiquetas que se hayan asignado a las campañas al crearlas. [Obtenga información sobre cómo asignar etiquetas a una campaña](create-campaign.md#create)

## Estados de campaña y alertas {#statuses}

Las campañas pueden tener varios estados:

* **[!UICONTROL Borrador]**: la campaña se está editando y no se ha activado.
* **[!UICONTROL Activando]**: la campaña se está activando.
* **[!UICONTROL Procesando]** *(solo campañas de correo electrónico)*: la exportación de la audiencia se ha completado y la campaña se está publicando.
* **[!UICONTROL Activo]**: la campaña se ha activado.
* **[!UICONTROL Programado]**: la campaña está configurada para activarse en una fecha de inicio específica.
* **[!UICONTROL Detenido]**: la campaña se ha detenido manualmente. Ya no puede activarlo ni reutilizarlo. [Obtenga información sobre cómo detener una campaña](modify-stop-campaign.md#stop)
* **[!UICONTROL Completado]**: la campaña se ha completado. Este estado se asigna automáticamente 3 días después de activar una campaña o en la fecha de finalización de la campaña si tiene una ejecución recurrente.
* **[!UICONTROL Archivado]**: se ha archivado la campaña. [Obtenga información sobre cómo archivar campañas](modify-stop-campaign.md#archive)

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a una **[!UICONTROL Activo]** o **[!UICONTROL Programado]** El estado indica que se ha creado una nueva versión de la campaña y que aún no se ha activado. [Más información](modify-stop-campaign.md#modify).

Cuando se produce un error en una de las campañas, aparece un icono de advertencia junto al estado de la campaña. Haga clic en ella para mostrar información sobre la alerta. Estas alertas pueden producirse en varias situaciones, como cuando el mensaje de la campaña no se ha publicado o si la superficie elegida es incorrecta.

![](assets/campaign-alerts.png)

## Modificación de una campaña recurrente {#modify}

Para modificar y crear una nueva versión de una campaña recurrente, siga estos pasos:

1. Abra la campaña y haga clic en **[!UICONTROL Modificar campaña]** botón.

1. Se crea una nueva versión de la campaña. Puede comprobar la versión activa haciendo clic en **[!UICONTROL Abrir versión activa]**.

   ![](assets/create-campaign-draft.png)

   En la lista de campañas, las campañas activadas con una versión de borrador en curso se muestran con un icono específico en la **[!UICONTROL Estado]** columna. Haga clic en este icono para abrir la versión de borrador de la campaña.

   ![](assets/create-campaign-edit-list.png)

1. Una vez que los cambios estén listos, puede activar la nueva versión de la campaña (consulte [Revisión y activación de una campaña](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Al activar el borrador, se reemplazará la versión activa de la campaña.

## Detener una campaña recurrente {#stop}

Para detener una campaña recurrente, ábrala y haga clic en **[!UICONTROL Detener campaña]** botón.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Al detener una campaña, no se detendrá un envío en curso, pero se detendrá un envío programado o las siguientes incidencias si el envío ya está en marcha.

<!-- inbound campaign (inapp): can stop and resume -->

## Duplicación de una campaña {#duplicate}

Puede duplicar una campaña en directo para crear una nueva. Para ello, abra la campaña y haga clic en **[!UICONTROL Duplicar]**.

![](assets/create-campaign-duplicate.png)

## Archivado de una campaña {#archive}

Con el tiempo, la lista de campañas sigue creciendo y, finalmente, dificulta la exploración de campañas completadas y detenidas.

Para evitarlo, puede archivar las campañas completadas y detenidas que ya no necesite. Para ello, haga clic en el botón de los tres puntos y seleccione **[!UICONTROL Archivar]**.

![](assets/create-campaign-archive.png)

Las campañas archivadas se pueden recuperar utilizando el filtro dedicado de la lista. [Obtenga información sobre cómo acceder a campañas](get-started-with-campaigns.md#access)
