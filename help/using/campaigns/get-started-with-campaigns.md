---
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---

# Introducción a las campañas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campañas"
>abstract="Con Campañas, puede entregar contenido de una sola vez a un segmento específico en varios canales. Antes de crear una nueva campaña, asegúrese de que tiene una superficie de canal (es decir, un mensaje preestablecido) y un segmento de Adobe Experience Platform listos para usar."

## Acerca de las campañas {#about}

>[!IMPORTANT]
>
>Esta función solo está disponible para usuarios con acceso a un perfil de producto relacionado con Campaign, como administrador de Campaign, aprobador de campañas, administrador de campañas o visualizador de campañas. Para obtener más información sobre cómo asignar perfiles de producto, consulte [esta página](../administration/permissions.md).

Las campañas le permiten entregar contenido único a un segmento específico mediante varios canales. A diferencia de los recorridos, donde las acciones están diseñadas para ejecutarse en secuencia, las campañas ejecutan acciones simultáneamente, ya sea inmediatamente o en una programación especificada.

Esto le permite enviar comunicaciones por lotes ad-hoc sencillas para casos de uso de marketing, como ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de políticas.

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

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
* **[!UICONTROL Completed]**: La campaña ha finalizado. Este estado se asigna automáticamente 3 días después de activar una campaña o en la fecha de finalización de la campaña si tiene una ejecución recurrente.
* **[!UICONTROL Archived]**: La campaña se ha archivado.

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a una **[!UICONTROL Live]** o **[!UICONTROL Scheduled]** El estado indica que se ha creado una nueva versión de la campaña y que aún no se ha activado (consulte [Modificación de una campaña](modify-stop-campaign.md#modify)).
