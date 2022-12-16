---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 12%

---

# Introducción a las campañas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campañas"
>abstract="Cree campañas para ofrecer contenido de una sola vez a un segmento específico en varios canales. Antes de crear la campaña, asegúrese de que tiene una superficie de canal (es decir, un ajuste preestablecido de mensaje) y un segmento de Adobe Experience Platform listos para usar."

Utilice campañas de Journey Optimizer para ofrecer contenido único a un segmento específico mediante varios canales. Cuando se utilizan recorridos, las acciones se ejecutan en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea de forma inmediata o en función de una programación especificada.

Puede crear dos tipos de campañas:

* **Campañas programadas** permite comunicaciones por lotes ad-hoc sencillas para casos de uso de marketing, como ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de políticas.
* **Campañas de API activadas** permiten mensajes transaccionales/operativos simples con las API de REST (restablecimiento de contraseña, abandono de tarjeta, etc.), donde la necesidad puede implicar personalización mediante atributos de perfil y datos contextuales de carga útil.

Los pasos principales para crear una campaña son los siguientes:

![](assets/create-campaign-process.png)

➡️ [Descubra esta función en vídeo](#video)

## Antes de empezar {#campaign-prerequisites}

Compruebe los siguientes requisitos previos antes de empezar a crear la primera campaña en Journey Optimizer:

1. **Necesita los permisos adecuados**. Las campañas solo están disponibles para los usuarios con acceso a campañas relacionadas **[!UICONTROL Perfil del producto]** como administrador de campañas, aprobador de campañas, administrador de campañas o visualizador de campañas.

   Si no puede acceder a las campañas, sus permisos deben ampliarse. Si tiene acceso a [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} para su organización, siga los pasos a continuación. Si no es así, póngase en contacto con el administrador de Journey Optimizer.

   +++Obtenga información sobre cómo asignar permisos de campaña

   Para asignar la **[!UICONTROL Perfil del producto]** a sus usuarios:

   1. De [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}, seleccione la opción [!DNL Adobe Experience Platform] producto.

   1. Vaya a la **[!UICONTROL Perfil del producto]** , seleccione una de las campañas integradas relacionadas **[!UICONTROL Perfil del producto]**: Administrador de campañas, aprobador de campañas, administrador de campañas o visualizador de campañas.

      Para obtener más información sobre la campaña de Journey Optimizer **[!UICONTROL Perfiles de producto]** y **[!UICONTROL Permisos]**, [consulte esta página](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Haga clic en **[!UICONTROL Agregar usuario]** para asignar al usuario el **[!UICONTROL Perfil del producto]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Escriba el nombre del usuario, el grupo o la dirección de correo electrónico y haga clic en **[!UICONTROL Guardar]**.
   El usuario ahora puede acceder a **[!UICONTROL Campañas]**.

+++

1. **Necesita una audiencia**. Los segmentos de audiencia deben estar disponibles antes de crear la campaña. Más información sobre la creación de audiencias [en esta página](../segment/about-segments.md).
1. **Necesita una superficie de canal**. Para poder seleccionar un canal, debe tener la superficie del canal correspondiente (es decir, preestablecida) creada y disponible. Obtenga más información sobre las superficies de canal [en esta página](../configuration/channel-surfaces.md).

## Vídeo explicativo {#video}

Aprenda a crear su primera campaña.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
