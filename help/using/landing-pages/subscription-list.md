---
solution: Journey Optimizer
product: journey optimizer
title: Crear una lista de suscripción
description: Obtenga información sobre cómo configurar una lista de suscripción en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Listas de suscripciones {#create-subscription-list}

## ¿Qué es una lista de suscripción? {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="Configuración de una lista de suscripción"
>abstract="Cree una lista de suscripción para recopilar perfiles que hayan elegido recibir comunicaciones sobre un asunto o evento específico. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html#define-subscription-list" text="Crear una lista de suscripción"

Un servicio de suscripción se refiere a los bienes y servicios de marketing proporcionados a los clientes que han elegido recibir comunicaciones sobre un asunto específico, evento, interés, etc. de forma continua. En [!DNL Journey Optimizer], estos clientes seleccionados se agrupan en una lista de suscripción.

Un servicio de suscripción puede ser:

* un boletín, por ejemplo: &quot;Serie en ejecución&quot;
* un evento, por ejemplo: Cumbre 2021
* un seminario web, por ejemplo: &quot;Más información sobre crypto&quot;
* un interés por un determinado producto, deporte, servicio, etc., por ejemplo: &quot;Interesado en comprar una casa en los próximos 12 meses&quot;
* una preferencia sobre cómo recibir notificaciones, por ejemplo: &quot;Reciba nuevas notificaciones de canciones por correo electrónico&quot;

Los perfiles se pueden agregar a una lista de suscripción mediante un [página de aterrizaje](create-lp.md). Un ejemplo se presenta en [esta sección](lp-use-cases.md#subscription-to-a-service).

## Crear una lista de suscripción {#define-subscription-list}

Para crear una lista de suscripción, siga los pasos a continuación.

1. Para acceder a las listas de suscripción, seleccione **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](assets/lp_subscription-lists.png)

1. Seleccione el **[!UICONTROL Create subscription list]** botón.

   ![](assets/lp_create-subscription-list.png)

1. Añada un título y una descripción. Estos campos son obligatorios.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >Actualmente no puede utilizar el espaciado ni especificar un nombre que ya exista para otra lista de suscripción en la **[!UICONTROL Title]** campo .

1. Puede definir una fecha de inicio y una de finalización.

   ![](assets/lp_subscription-list-dates.png)

1. Haga clic en **[!UICONTROL Save]**.

La lista muestra todas las listas de suscripción creadas. Puede filtrarlos en función de la fecha de creación o de modificación, así como de su estado.

![](assets/lp_subscription-filters.png)

Los estados posibles son los siguientes:

* **[!UICONTROL Not started]**: Se ha definido una fecha de inicio posterior al día actual. Los perfiles suscritos aún no recibirán comunicaciones relacionadas con esta lista de suscripción.
* **[!UICONTROL Live]**: El día actual está comprendido entre la fecha de inicio y la fecha de finalización de la lista de suscripción, o bien no se han definido fechas de finalización/inicio, lo que significa que la lista de suscripción siempre está activa.
* **[!UICONTROL Expired]**: Se pasa la fecha de finalización, por lo que la lista de suscripción ya no es válida. Los perfiles suscritos no recibirán más comunicaciones relacionadas con esta lista de suscripción.

Una vez creada la lista de suscripción, puede utilizarla en una página de aterrizaje. Los perfiles que acepten a través del formulario de página de aterrizaje se agregarán a la lista. [Más información](design-lp.md)

También puede utilizar listas de suscripción como segmentos cuando [creación de recorridos](../building-journeys/journey-gs.md#jo-build) y añadir personalización.

>[!NOTE]
>
>Puede controlar el impacto de su lista de suscripción a través de informes específicos. [Más información](../reports/subscription-report-live.md)
