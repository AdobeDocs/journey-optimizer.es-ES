---
solution: Journey Optimizer
product: journey optimizer
title: Creación de campañas de calentamiento de IP
description: Obtenga información sobre cómo crear una campaña de calentamiento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupos, grupo, subdominios, capacidad de entrega
hide: true
hidefromtoc: true
source-git-commit: 53be033ff0474cbafff71ed36194c18627234fd4
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 3%

---

# Creación de campañas de calentamiento de IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activar la opción de plan de calentamiento IP"
>abstract="Seleccione la opción de activación del plan de calentamiento IP. Una vez que la campaña está activa, puede asociarse con un plan de calentamiento de IP."

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción al calentamiento de IP](ip-warmup-gs.md)
* **[Creación de campañas de calentamiento de IP](ip-warmup-campaign.md)**
* [Crear un plan de calentamiento de IP](ip-warmup-plan.md)
* [Ejecutar el plan de calentamiento de IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

Debe crear una o más campañas con una opción específica habilitada para que se puedan usar en un plan de calentamiento de IP.

Para crear una campaña de calentamiento de IP, siga los pasos a continuación.

1. Creación de un correo electrónico [emerger](channel-surfaces.md) para el dominio y las direcciones IP que ha identificado para su plan de calentamiento.<!--how do you identify these or who does it at the customer level?-->

   >[!NOTE]
   >
   >Obtenga información sobre cómo seleccionar el dominio y las direcciones IP que se utilizarán en una superficie de correo electrónico en [esta sección](using/email/email-settings.md#subdomains-and-ip-pools).

1. Crear un [campaña](../campaigns/create-campaign.md) y seleccione la [Correo electrónico](../email/create-email.md#create-email-journey-campaign) acción.

1. Seleccione la superficie que ha creado para el calentamiento de IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Haga clic en **[!UICONTROL Crear]**.

1. Desde el **[!UICONTROL Programación]** , seleccione **[!UICONTROL Activación del plan de calentamiento IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La campaña [programación](../campaigns/create-campaign.md#schedule) será impulsado por el [plan de calentamiento de IP](ip-warmup-plan.md) se asocia con, lo que significa que la programación ya no se define en la propia campaña.

1. [Activar](../campaigns/review-activate-campaign.md) la campaña. Una vez activa, está lista para utilizarse en un plan de calentamiento de IP.

>[!NOTE]
>
>Para una campaña en directo con el plan de calentamiento de IP activado, la variable **[!UICONTROL Eliminar]** está disponible hasta que se asocia con un plan de calentamiento de IP.

Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

