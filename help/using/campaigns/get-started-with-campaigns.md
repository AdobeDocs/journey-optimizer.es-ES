---
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: bbcafe364ca13501972b3d8e1150aa2f51ba88a0
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 5%

---

# Introducción a las campañas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campañas"
>abstract="Cree campañas para ofrecer contenido de una sola vez a un segmento específico en varios canales. Antes de crear la campaña, asegúrese de que tiene una superficie de canal (es decir, un ajuste preestablecido de mensaje) y un segmento de Adobe Experience Platform listos para usar."

Utilice campañas de Journey Optimizer para ofrecer contenido único a un segmento específico mediante varios canales. Cuando se utilizan recorridos, las acciones se ejecutan en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea inmediatamente o en función de una programación especificada.

Cree campañas para enviar comunicaciones por lotes ad-hoc sencillas para casos de uso de marketing, como ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de políticas.

➡️ [Descubra esta función en vídeo](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## Antes de empezar {#campaign-prerequisites}

Compruebe los siguientes requisitos previos antes de empezar a crear la primera campaña en Journey Optimizer:

1. **Necesita los permisos adecuados**. Las campañas solo están disponibles para los usuarios con acceso a campañas relacionadas **[!UICONTROL Product profile]** como administrador de campañas, aprobador de campañas, administrador de campañas o visualizador de campañas.

   Si no puede acceder a las campañas, sus permisos deben ampliarse. Si tiene acceso a [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} para su organización, siga los pasos a continuación. Si no es así, póngase en contacto con el administrador de Journey Optimizer.

   +++Obtenga información sobre cómo asignar permisos de campaña

   Para asignar la **[!UICONTROL Product profile]** a sus usuarios:

   1. De [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}, seleccione la opción [!DNL Adobe Experience Platform] producto.

   1. Vaya a la **[!UICONTROL Product profile]** , seleccione una de las campañas integradas relacionadas **[!UICONTROL Product profile]**: Administrador de campañas, aprobador de campañas, administrador de campañas o visualizador de campañas.

      Para obtener más información sobre la campaña de Journey Optimizer **[!UICONTROL Product profiles]** y **[!UICONTROL Permissions]**, [consulte esta página](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Haga clic en **[!UICONTROL Add user]** para asignar al usuario el **[!UICONTROL Product profile]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Escriba el nombre del usuario, el grupo o la dirección de correo electrónico y haga clic en **[!UICONTROL Save]**.
   El usuario ahora puede acceder a **[!UICONTROL Campaigns]**.

+++

1. **Necesita una audiencia**. Los segmentos de audiencia deben estar disponibles antes de crear la campaña. Más información sobre la creación de audiencias [en esta página](../segment/about-segments.md).
1. **Necesita una superficie de canal**. Para poder seleccionar un canal, debe tener la superficie del canal correspondiente (es decir, preestablecida) creada y disponible. Obtenga más información sobre las superficies de canal [en esta página](../configuration/channel-surfaces.md).

## Acceso a campañas {#access}

Se puede acceder a las campañas desde la **[!UICONTROL Campaigns]** para abrir el Navegador.

De forma predeterminada, la lista muestra todas las campañas con la variable **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]** y **[!UICONTROL Live]** estados. Para mostrar las campañas detenidas, completadas y archivadas, debe borrar el filtro.

![](assets/create-campaign-list.png)

## Estados de campaña {#statuses}

Las campañas pueden tener varios estados:

* **[!UICONTROL Draft]**: La campaña se está editando y no se ha activado.
* **[!UICONTROL Activating]**: La campaña se está activando.
* **[!UICONTROL Live]**: La campaña se ha activado.
* **[!UICONTROL Scheduled]**: La campaña está configurada para activarse en una fecha de inicio específica.
* **[!UICONTROL Stopped]**: La campaña se ha detenido manualmente. Ya no se puede activar ni volver a utilizar. [Más información](modify-stop-campaign.md#stop)
* **[!UICONTROL Completed]**: La campaña ha finalizado. Este estado se asigna automáticamente 3 días después de activar una campaña o en la fecha de finalización de la campaña si tiene una ejecución recurrente.
* **[!UICONTROL Archived]**: La campaña se ha archivado.

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a una **[!UICONTROL Live]** o **[!UICONTROL Scheduled]** indica que se ha creado una nueva versión de la campaña y que aún no se ha activado. [Más información](modify-stop-campaign.md#modify).

## Vídeo explicativo {#video}

Aprenda a crear su primera campaña.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
