---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las notificaciones push
description: Obtenga información sobre cómo crear una notificación push en Journey Optimizer
feature: Overview, Push
topic: Content Management
role: User
level: Beginner
exl-id: c1f16edd-efdf-41c2-a0ad-5f55009008f5
TQID: https://experienceleague.adobe.com/S-3ZtTNfgZGEFChfjaXPihxGWpdkWacrWF9AWc-AyZY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 28eeed0d2b5dc3054c57004ead01de32151ab743
workflow-type: tm+mt
source-wordcount: 392
ht-degree: 93%

---

# Introducción a las notificaciones push {#gs-push-notification}

>[!BEGINSHADEBOX]

**En esta página:** Empiece a usar las notificaciones push en Adobe Journey Optimizer para llegar a los usuarios de su aplicación móvil y a los visitantes web a través de recorridos y campañas.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Si es la primera vez que crea una notificación push, asegúrese de que el canal push esté configurado. [Más información](push-gs.md).

Las notificaciones push le ayudan a llegar a sus usuarios de aplicaciones móviles en cualquier momento, especialmente cuando no utilizan activamente su aplicación ni exploran su sitio web. Las notificaciones push pueden ayudarle a lograr una variedad de casos de uso, como proporcionar actualizaciones sobre el servicio, solicitar al usuario que realice una acción, avisar al usuario de una nueva oferta, etc. Las plataformas de dispositivos exigen que los usuarios den su inclusión antes de que puedan recibir o ver las notificaciones. La inclusión del usuario puede recibirse tan pronto como se inicie la aplicación por primera vez después de la instalación, o en una sesión o flujo de trabajo posterior, según corresponda.

[!DNL Journey Optimizer] admite notificaciones push y le ayuda a enviar notificaciones muy relevantes a tasas de rendimiento líderes en el sector. Las notificaciones push pueden incluir personalización y contexto basado en Recorridos para aprovechar la información de datos que su marca tiene con Adobe Experience Cloud.

Se pueden crear notificaciones push:

* En un **Recorrido**: una vez que haya añadido una actividad Push en el recorrido y haya definido la configuración básica, utilice el panel derecho **[!UICONTROL Acciones: Push]** para crear el contenido de las notificaciones push. [Obtenga información sobre cómo crear un recorrido](../building-journeys/journey-gs.md)

* En una **Campaña**: una vez creada una campaña, seleccione Notificaciones push como acción y defina la configuración básica. Aprenda a crear [una campaña de acción](../campaigns/campaign-action.md#action-campaign-action) | [una campaña desencadenada por API](../campaigns/api-triggered-campaigns.md) | [una campaña orquestada](../orchestrated/create-orchestrated-campaign.md#create)

Utilice las pestañas dedicadas para definir la configuración de las notificaciones push para plataformas **iOS**, **Android** y **Web**.

>[!NOTE]
>
>Mientras **[!DNL Journey Optimizer]** proporciona formas de administrar la exclusión en correos electrónicos y mensajes SMS, las notificaciones push no requieren ninguna acción por su parte, ya que los destinatarios pueden cancelar la suscripción a través de sus propios dispositivos. Por ejemplo, al descargar o al usar la aplicación, pueden seleccionar detener las notificaciones. Del mismo modo, pueden cambiar la configuración de notificación a través del sistema operativo móvil o de los ajustes del navegador web. Para comprobar el estado de consentimiento push de un perfil en el visor de perfiles de AEP, consulte [Comprobar el estado de exclusión push](../privacy/opt-out.md#push-opt-out-status).

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-push.md">
<img alt="Posible cliente" src="../assets/do-not-localize/push-create.jpg">
</a>
<div><a href="create-push.md"><strong>Crear una notificación push</strong>
</div>
<p>
</td>
<td>
<a href="design-push.md">
<img alt="Poco frecuente" src="../assets/do-not-localize/push-design.jpg">
</a>
<div>
<a href="design-push.md"><strong>Diseño de la notificación push</strong></a>
</div>
<p></td>
<td>
<a href="send-push.md">
<img alt="Validación" src="../assets/do-not-localize/push-sending.jpg">
</a>
<div>
<a href="send-push.md"><strong>Enviar la notificación push</strong></a>
</div>
<p>
</td>
<td>
<a href="push-gs.md">
<img alt="Validación" src="../assets/do-not-localize/push-config.jpg">
</a>
<div>
<a href="push-gs.md"><strong>Configuración de notificaciones push</strong></a>
</div>
<p>
</td>
</tr></table>
