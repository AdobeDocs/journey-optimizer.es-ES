---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campaña, cómo, inicio, optimizador
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 68%

---

# Introducción a las campañas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programación de campañas"
>abstract="De forma predeterminada, las campañas se inician tras la activación manual y finalizan inmediatamente después de enviar el mensaje una vez. Sin embargo, tiene la flexibilidad de establecer una fecha y hora específicas para que se envíe el mensaje. Además, puede especificar una fecha de finalización para las campañas de acción recurrentes. En los Activadores de acción, también puede configurar la frecuencia de envío de mensajes para adaptarla a sus preferencias."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Inicio de campaña"
>abstract="Especifique la fecha y la hora a las que se debe enviar el mensaje."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fin de campaña"
>abstract="Especifique cuándo se debe detener la ejecución de una campaña recurrente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Activadores de acciones de campaña"
>abstract="Defina una frecuencia a la que se debe enviar el mensaje de la campaña."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Control de la velocidad de limitación"
>abstract="Control de la velocidad de limitación"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Creación de campañas"
>abstract="Utilice **Adobe Journey Optimizer** para ofrecer contenido único a un público específico mediante varios canales. Cuando se utilizan recorridos, las acciones se ejecutan en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea de forma inmediata o en función de una programación especificada."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campañas"
>abstract="Cree campañas para ofrecer contenido de una sola vez a un público específico en varios canales. Antes de crear la campaña, asegúrese de que tiene una configuración de canal y un público de Adobe Experience Platform listos para usar."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campaña"
>abstract="**Campañas programadas** se ejecutan inmediatamente o en una fecha especificada y están pensadas para enviar mensajes de tipo marketing. Las campañas **activadas por API** se ejecutan mediante el uso de una llamada de API. Están destinados a enviar mensajes de marketing (mensajes promocionales que requieren el consentimiento del usuario) o mensajes transaccionales (mensajes no comerciales, que también se pueden enviar a perfiles no suscritos en contextos específicos)."

Utilice las campañas de Journey Optimizer para ofrecer contenido único a un público específico mediante varios canales. Cuando se utilizan recorridos, las acciones se ejecutan en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea de forma inmediata o en función de una programación especificada.

![](assets/gs-campaigns.png)

Puede crear diferentes tipos de campañas en Journey Optimizer:

* **Campañas de acción**

  Las campañas de acción (o campañas programadas) permiten comunicaciones por lotes ad hoc sencillas para casos de uso de marketing como ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de directivas.

* **Campañas activadas por API**

  Las campañas activadas por API permiten que las comunicaciones de marketing lleguen a una audiencia en el momento adecuado o que los mensajes transaccionales/operacionales lleguen a una persona, como un restablecimiento de contraseña, donde la necesidad puede implicar personalización no solo mediante el uso de atributos de perfil, sino también mediante los datos de contexto en tiempo real en la déclencheur, que es una carga útil de API de REST.

<!--* **Orchestrated campaigns**

    Campaign Orchestration in Adobe Journey Optimizer powers sophisticated, brand-initiated marketing campaigns across channels, helping you drive engagement, revenue, and customer loyalty at scale.

    While cross-channel marketing is essential, orchestrated campaigns make it seamless. With a visual, drag-and-drop interface, you can design and automate complex marketing workflows, from segmentation to message delivery, across multiple channels. Everything happens in one intuitive environment, built for speed, control, and efficiency.-->

## Antes de empezar {#campaign-prerequisites}

Compruebe los siguientes requisitos previos antes de empezar a crear su primera campaña en [!DNL Journey Optimizer]:

1. **Necesita los permisos adecuados**. Las campañas solo están disponibles para usuarios con acceso a un **[!UICONTROL perfil de producto]** relacionado con una campaña, como administrador de campañas, aprobador de campañas, administrador de campañas o visualizador de campañas. Si no puede acceder a las campañas, debe ampliar los permisos.

   +++Más información sobre cómo asignar una función relacionada con la campaña

   1. Para asignar una función a un usuario en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Funciones]** y seleccione una de las **[!UICONTROL Funciones]** integradas relacionadas con las campañas: Administrador de campañas, Aprobador de campañas, Gestor de campañas o Visualizador de campañas.

   1. En la pestaña **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Añadir usuario]**.

   1. Introduzca el nombre o la dirección de correo electrónico del usuario o selecciónelo de la lista y haga clic en **[!UICONTROL Guardar]**.

      Si el usuario no se ha creado previamente, consulte la [documentación de Añadir usuarios](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/users).

   El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

   +++

1. **Necesita un público**. Los públicos deben estar disponibles antes de crear la campaña. [Introducción a las audiencias](../audience/about-audiences.md).

1. **Necesita una configuración de canal**. Para poder seleccionar un canal, debe tener la configuración del canal correspondiente (es decir, preestablecida) creada y disponible. [Aprenda a configurar las configuraciones de canal](../configuration/channel-surfaces.md).

## Vamos a profundizar

Ahora que comprende las campañas de [!DNL Journey Optimizer], es hora de profundizar en estas secciones de documentación para empezar a crear sus primeras campañas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="campañas de acción" src="assets/do-not-localize/gs-action-campaign.png" width="50%"></a><br/><a href="create-campaign.md">Campañas de acción</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png" width="50%"></a><br/><a href="api-triggered-campaigns.md">Campañas activadas por API</a></td>
</tr></table>

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="action campaigns" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Action campaigns</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API triggered campaigns</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrated campaigns</a></td>
</tr></table>-->
