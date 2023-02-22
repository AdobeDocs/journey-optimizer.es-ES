---
solution: Journey Optimizer
product: journey optimizer
title: Modificación o detención de una campaña
description: Obtenga información sobre cómo modificar, detener o duplicar campañas en directo en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: administrar campañas, estado, programación, acceso, optimizador
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 2%

---

# Administración de campañas {#modify-stop-campaign}

Una vez activada una campaña, puede modificarla o detenerla en cualquier momento. Estas operaciones están disponibles para campañas con una ejecución recurrente solamente.

Además, puede duplicar las campañas en vivo (ejecutadas una vez o con una ejecución recurrente) para crear otras nuevas y archivar las campañas completadas o detenidas.

## Acceso a campañas {#access}

Se puede acceder a las campañas desde la **[!UICONTROL Campañas]** para abrir el Navegador.

De forma predeterminada, la lista muestra todas las campañas con la variable **[!UICONTROL Borrador]**, **[!UICONTROL Programado]** y **[!UICONTROL Activo]** estados.

Para mostrar las campañas detenidas, completadas y archivadas, debe borrar el filtro.

![](assets/create-campaign-list.png)

## Estados de campaña {#statuses}

Las campañas pueden tener varios estados:

* **[!UICONTROL Borrador]**: La campaña se está editando y no se ha activado.
* **[!UICONTROL Activación]**: La campaña se está activando.
* **[!UICONTROL Activo]**: La campaña se ha activado.
* **[!UICONTROL Programado]**: La campaña está configurada para activarse en una fecha de inicio específica.
* **[!UICONTROL Detenido]**: La campaña se ha detenido manualmente. Ya no se puede activar ni volver a utilizar. [Obtenga información sobre cómo detener una campaña](modify-stop-campaign.md#stop)
* **[!UICONTROL Completado]**: La campaña ha finalizado. Este estado se asigna automáticamente 3 días después de activar una campaña o en la fecha de finalización de la campaña si tiene una ejecución recurrente.
* **[!UICONTROL Archivado]**: La campaña se ha archivado. [Aprenda a archivar campañas](modify-stop-campaign.md#archive)

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a una **[!UICONTROL Activo]** o **[!UICONTROL Programado]** indica que se ha creado una nueva versión de la campaña y que aún no se ha activado. [Más información](modify-stop-campaign.md#modify).

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

Para evitarlo, puede archivar campañas completadas y detenidas que ya no necesite. Para ello, haga clic en el botón de puntos suspensivos y seleccione **[!UICONTROL Archivo]**.

![](assets/create-campaign-archive.png)

Las campañas archivadas se pueden recuperar utilizando el filtro dedicado de la lista. [Obtenga información sobre cómo acceder a campañas](get-started-with-campaigns.md#access)
