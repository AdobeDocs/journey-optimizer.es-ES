---
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: b9fa6bff926eb8cee476fa53feb38ed783e048fc
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 2%

---


# Introducción a las campañas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campañas"
>abstract="Con Campañas, puede entregar contenido de una sola vez a un segmento específico en varios canales. Antes de crear una nueva campaña, asegúrese de tener un mensaje preestablecido y un segmento de Adobe Experience Platform listos para usar."

## Acerca de las campañas {#about}

Las campañas le permiten entregar contenido único a un segmento específico mediante varios canales.

A diferencia de los recorridos, donde las acciones están diseñadas para ejecutarse en secuencia, las campañas ejecutan acciones simultáneamente, ya sea inmediatamente o en una programación especificada. Puede utilizarlos, por ejemplo, para ofrecer ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de políticas.

<!--Additionally, campaigns' content experiment feature allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.-->

Obtenga información sobre cómo administrar campañas &lt;!>—y experimentos de contenido&lt;>:
* [Creación de una campaña](create-campaign.md)
* [Modificar o detener una campaña](modify-stop-campaign.md)
<!--* [Create a content experiment](content-experiment.md)-->

## Acceso a campañas {#access}

Se puede acceder a las campañas desde la **[!UICONTROL Campaigns]** para abrir el Navegador.

De forma predeterminada, la lista muestra todas las campañas con la variable **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]** y **[!UICONTROL Live]** estados. Para mostrar las campañas detenidas, completadas y archivadas, debe borrar el filtro.

![](assets/create-campaign-list.png)

## Estados de campaña {#statuses}

Las campañas pueden tener varios estados:

* **[!UICONTROL Draft]**: La campaña se está editando y no se ha activado.
* **[!UICONTROL Activating]**: La campaña se está activando.
* **[!UICONTROL Live]**: La campaña se ha activado.
* **[!UICONTROL Scheduled]**: La campaña se ha configurado para activarse en una fecha de inicio específica.
* **[!UICONTROL Stopped]**: La campaña se ha detenido manualmente. Ya no puede activarlo ni reutilizarlo (consulte [Detener una campaña](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**: La campaña ha finalizado.
* **[!UICONTROL Archived]**: La campaña se ha archivado.

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a una **[!UICONTROL Live]** o **[!UICONTROL Scheduled]** El estado indica que se ha creado una nueva versión de la campaña y que aún no se ha activado (consulte [Modificación de una campaña](modify-stop-campaign.md#modify)).
