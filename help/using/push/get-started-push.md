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
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 0%

---

# Introducción a las notificaciones push {#gs-push-notification}

>[!IMPORTANT]
>
>Si es la primera vez que crea una notificación push, asegúrese de que se ha configurado el canal push. [Más información](push-gs.md).

Las notificaciones push le ayudan a llegar a los usuarios de su aplicación móvil y a los visitantes web en cualquier momento, especialmente cuando no utilizan activamente su aplicación ni exploran el sitio web. Las notificaciones push pueden ayudarle a lograr una variedad de casos de uso, como proporcionar actualizaciones sobre su servicio, pedir a un usuario que realice una acción, alertar al usuario sobre una nueva oferta, etc. Las plataformas de dispositivos requieren la inclusión antes de que los usuarios finales puedan recibir o ver sus notificaciones. La inclusión del usuario puede recibirse tan pronto como se inicie la aplicación por primera vez después de la instalación o en una sesión o flujo de trabajo posterior, según corresponda.

[!DNL Journey Optimizer] admite notificaciones push y le ayuda a enviar notificaciones muy relevantes a tasas de rendimiento líderes en la industria. Las notificaciones push pueden incluir personalización y contexto basado en Recorridos para aprovechar la información de datos que su marca tiene con Adobe Experience Cloud.

Se pueden crear notificaciones push:

* En un **Recorrido**: Una vez que hayas agregado una actividad push al recorrido y hayas definido la configuración básica, usa el panel derecho **[!UICONTROL Acciones: push]** para crear el contenido de las notificaciones push. [Aprenda a crear un recorrido](../building-journeys/journey-gs.md)

* En una **campaña**: Una vez que hayas creado una campaña, selecciona Notificación push como acción y define la configuración básica. Aprenda a crear [una campaña de acción](../campaigns/campaign-action.md#action-campaign-action) | [una campaña activada por API](../campaigns/api-triggered-campaigns.md) | [una campaña orquestada](../orchestrated/create-orchestrated-campaign.md#create)

Use las fichas específicas para definir la configuración de notificaciones push para las plataformas **iOS**, **Android** y **Web**.

>[!NOTE]
>
>Aunque **[!DNL Journey Optimizer]** proporciona formas de administrar la exclusión en correos electrónicos y mensajes SMS, las notificaciones push no requieren ninguna acción por su parte, ya que los destinatarios pueden cancelar la suscripción a través de sus propios dispositivos. Por ejemplo, al descargar o al usar la aplicación, pueden seleccionar detener las notificaciones. Del mismo modo, pueden cambiar la configuración de las notificaciones a través del sistema operativo móvil o de la configuración del explorador web. Para comprobar el estado de consentimiento push de un perfil en el visor de perfiles de AEP, consulte [Comprobar el estado de exclusión push](../privacy/opt-out.md#push-opt-out-status).

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
<img alt="Poco Frecuente" src="../assets/do-not-localize/push-design.jpg">
</a>
<div>
<a href="design-push.md"><strong>Diseñe su notificación push</strong></a>
</div>
<p></td>
<td>
<a href="send-push.md">
<img alt="Validación" src="../assets/do-not-localize/push-sending.jpg">
</a>
<div>
<a href="send-push.md"><strong>Envíe su notificación push</strong></a>
</div>
<p>
</td>
<td>
<a href="push-gs.md">
<img alt="Validación" src="../assets/do-not-localize/push-config.jpg">
</a>
<div>
<a href="push-gs.md"><strong>Configurar notificaciones push</strong></a>
</div>
<p>
</td>
</tr></table>
