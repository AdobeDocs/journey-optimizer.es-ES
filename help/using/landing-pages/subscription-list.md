---
title: Crear una lista de suscripción
description: Obtenga información sobre cómo configurar una lista de suscripción en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 2%

---

# Listas de suscripciones {#create-subscription-list}

## ¿Qué es una lista de suscripción?

Un servicio de suscripción se refiere a los bienes y servicios de marketing proporcionados a los clientes que han elegido recibir comunicaciones sobre un asunto específico, evento, interés, etc. de forma continua. En [!DNL Journey Optimizer], estos clientes seleccionados se agrupan en una lista de suscripción.

Un servicio de suscripción puede ser:

* un boletín, por ejemplo: &quot;Serie en ejecución&quot;
* un evento, por ejemplo: Cumbre 2021
* un seminario web, por ejemplo: &quot;Más información sobre crypto&quot;
* un interés por un determinado producto, deporte, servicio, etc., por ejemplo: &quot;Interesado en comprar una casa en los próximos 12 meses&quot;
* una preferencia sobre cómo recibir notificaciones, por ejemplo: &quot;Reciba nuevas notificaciones de canciones por correo electrónico&quot;

Los perfiles se pueden agregar a una lista de suscripción mediante un [página de aterrizaje](create-lp.md). Un ejemplo se presenta en [esta sección](lp-use-cases.md#subscription-to-a-service).

## Definir una lista de suscripción {#define-subscription-list}

Para crear una lista de suscripción, siga los pasos a continuación.

1. Para acceder a las listas de suscripción, seleccione **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. Seleccione el botón **[!UICONTROL Create subscription list]**.

   ![](../assets/lp_create-subscription-list.png)

1. Añada un nombre y una descripción. Estos campos son obligatorios.

1. Puede definir una fecha de inicio y una de finalización.

   ![](../assets/lp_subscription-list-dates.png)

1. Haga clic en **[!UICONTROL Save]**.

La lista muestra todas las listas de suscripción creadas. Puede filtrarlos en función de la fecha de creación o de modificación, así como de su estado.

![](../assets/lp_subscription-filters.png)

Los estados posibles son los siguientes:

* **[!UICONTROL Not started]**: Se ha definido una fecha de inicio posterior al día actual. Los perfiles suscritos aún no recibirán comunicaciones relacionadas con esta lista de suscripción.
* **[!UICONTROL Live]**: El día actual está comprendido entre la fecha de inicio y la fecha de finalización de la lista de suscripción, o bien no se han definido fechas de finalización/inicio, lo que significa que la lista de suscripción siempre está activa.
* **[!UICONTROL Expired]**: Se pasa la fecha de finalización, por lo que la lista de suscripción ya no es válida. Los perfiles suscritos no recibirán más comunicaciones relacionadas con esta lista de suscripción.

Una vez creada la lista de suscripción, puede utilizarla en una página de aterrizaje. Los perfiles que acepten a través del formulario de página de aterrizaje se agregarán a la lista. [Más información](design-lp.md)

También puede utilizar listas de suscripción como segmentos cuando [creación de recorridos](../building-journeys/journey-gs.md#jo-build) y añadir personalización.

>[!NOTE]
>
>Puede controlar el impacto de su lista de suscripción a través de informes específicos. [Más información](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
