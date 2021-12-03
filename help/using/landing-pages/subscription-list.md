---
title: Crear una lista de suscripción
description: Obtenga información sobre cómo configurar una lista de suscripción en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Crear una lista de suscripción {#create-subscription-list}

## ¿Qué es una lista de suscripción?

Un servicio de suscripción se refiere a los bienes y servicios de marketing proporcionados a los clientes que han elegido recibir comunicaciones sobre un asunto específico, evento, interés, etc. de forma continua. En [!DNL Journey Optimizer], estos clientes seleccionados se agrupan en una lista de suscripción.

Un servicio de suscripción puede ser:

* un boletín, por ejemplo &quot;series en ejecución&quot;
* un evento, por ejemplo &quot;Summit 2021&quot;
* un seminario web, por ejemplo &quot;Más información sobre crypto&quot;
* un interés por un determinado producto/deporte/servicio/etc., por ejemplo, &quot;Interesado en comprar una casa en los próximos 12 meses&quot;
* una preferencia sobre cómo recibir notificaciones, por ejemplo &quot;Recibir nuevas notificaciones de canciones por correo electrónico&quot;

Los perfiles se pueden agregar a una lista de suscripción mediante un [página de aterrizaje](create-lp.md). Un ejemplo se presenta en [esta sección](get-started-lp.md#subscription-to-a-service).

## Definir una lista de suscripción {#define-subscription-list}

Para crear una lista de suscripción, siga los pasos a continuación.

1. Para acceder a las listas de suscripción, seleccione **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. En la lista de suscripción, haga clic en **[!UICONTROL Create subscription]** lista.

   ![](../assets/lp_create-subscription-list.png)

1. Añada un nombre y una descripción. Estos campos son obligatorios.

1. Puede definir una fecha de inicio y una de finalización.

   ![](../assets/lp_subscription-list-dates.png)

1. Haga clic en **[!UICONTROL Save]**.

La lista muestra todas las listas de suscripción creadas. Puede filtrarlos en función de la fecha de creación o de modificación.

![](../assets/lp_subscription-filters.png)

Los estados posibles son los siguientes:

* **[!UICONTROL Not started]**: Se ha definido una fecha de inicio posterior al día actual. Los perfiles suscritos a esta lista aún no recibirán comunicaciones relacionadas con esta lista de suscripción.
* **[!UICONTROL Live]**: El día actual está comprendido entre la fecha de inicio y la fecha de finalización de la lista de suscripción, o bien no se han definido fechas de finalización/inicio, lo que significa que la lista de suscripción siempre está activa.
* **[!UICONTROL Expired]**: Se pasa la fecha de finalización, la lista de suscripción ya no es válida. Cualquier perfil suscrito a esta lista no recibirá más comunicaciones relacionadas con esta lista de suscripción.

Una vez creada la lista de suscripción, puede utilizarla en una página de aterrizaje para que los perfiles puedan incluirse en un formulario y añadirse a la lista. [Más información](design-lp.md)

También puede utilizar listas de suscripción como segmentos al crear recorridos y personalizaciones.

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->