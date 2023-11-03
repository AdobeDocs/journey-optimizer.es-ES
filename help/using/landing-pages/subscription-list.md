---
solution: Journey Optimizer
product: journey optimizer
title: Creación de una lista de suscripción
description: Obtenga información sobre cómo configurar una lista de suscripción en Journey Optimizer
feature: Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: aterrizaje, página de aterrizaje, lista, suscripción, servicio
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: f63f9d6ffd28d276f8a3dadbf8dc6b947b8331e7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 13%

---

# Listas de suscripciones {#create-subscription-list}

## ¿Qué es una lista de suscripción?  {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="Configurar una lista de suscripción"
>abstract="Cree una lista de suscripción para recopilar perfiles que hayan optado por recibir comunicaciones sobre un asunto o evento específico. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html?lang=es#define-subscription-list" text="Creación de una lista de suscripción"

Un servicio de suscripción se refiere a los bienes y servicios de marketing proporcionados a los clientes que han elegido recibir comunicaciones sobre un tema/evento/interés/etc específico. de forma continua. Entrada [!DNL Journey Optimizer]Sin embargo, estos clientes se incluyen en una lista de suscripción.

Un servicio de suscripción puede ser:

* un boletín informativo, por ejemplo: &quot;Running series&quot;
* un evento, por ejemplo: &quot;Summit 2021&quot;
* un seminario web, por ejemplo: &quot;Más información sobre la criptografía&quot;.
* un interés en un determinado producto/deporte/servicio/etc., por ejemplo: &quot;Interesado en comprar una casa en los próximos 12 meses&quot;
* una preferencia sobre cómo recibir notificaciones, por ejemplo: &quot;Recibir notificaciones de nuevas canciones por correo electrónico&quot;

Los perfiles se pueden añadir a una lista de suscripción mediante una [página de aterrizaje](create-lp.md). Se presenta un ejemplo en [esta sección](lp-use-cases.md#subscription-to-a-service).

## Creación de una lista de suscripción {#define-subscription-list}

Para crear una lista de suscripción, siga los pasos a continuación.

1. Para acceder a las listas de suscripción, seleccione **[!UICONTROL Cliente]** > **[!UICONTROL Lista de suscripción]**.

   ![](assets/lp_subscription-lists.png)

1. Seleccione el **[!UICONTROL Crear lista de suscripción]** botón.

   ![](assets/lp_create-subscription-list.png)

1. Añada un título y una descripción. Estos campos son obligatorios.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >Actualmente no puede utilizar el espaciado ni introducir un nombre que ya exista para otra lista de suscripción en **[!UICONTROL Título]** field.

1. Puede definir una fecha de inicio y una fecha de finalización.

   ![](assets/lp_subscription-list-dates.png)

1. Seleccione o cree etiquetas de Adobe Experience Platform en **[!UICONTROL Etiquetas]** para categorizar la página de aterrizaje y mejorar la búsqueda. [Más información](../start/search-filter-categorize.md#tags)

1. Haga clic en **[!UICONTROL Guardar]**.

La lista muestra todas las listas de suscripción creadas. Puede filtrarlos en función de la fecha de creación o de modificación, y de su estado.

![](assets/lp_subscription-filters.png)

Los estados posibles son los siguientes:

* **[!UICONTROL Sin iniciar]**: Ha definido una fecha de inicio posterior al día actual. Los perfiles suscritos aún no recibirán comunicaciones relacionadas con esta lista de suscripción.
* **[!UICONTROL Activo]**: el día actual se compone entre la fecha de inicio y la fecha de finalización de la lista de suscripción o no ha definido fechas de finalización/inicio, lo que significa que la lista de suscripción siempre está activa.
* **[!UICONTROL Caducado]**: Se pasa la fecha de finalización, por lo que la lista de suscripción ya no es válida. Ningún perfil suscrito recibirá más comunicaciones relacionadas con esta lista de suscripción.

Una vez creada la lista de suscripción, puede utilizarla en una página de aterrizaje. Los perfiles que se incluyan en el formulario de página de aterrizaje se añadirán a la lista. [Más información](design-lp.md)

También puede utilizar las listas de suscripción como audiencias cuando [recorridos de construcción](../building-journeys/journey-gs.md#jo-build) y agregando personalización.

>[!NOTE]
>
>Puede monitorizar el impacto de su lista de suscripciones a través de informes específicos. [Más información](../reports/subscription-report-live.md)
