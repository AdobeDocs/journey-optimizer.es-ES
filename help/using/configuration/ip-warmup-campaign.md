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
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '344'
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

Antes de crear el propio plan de calentamiento de IP en [!DNL Journey Optimizer], primero debe crear una o más campañas con la opción dedicada habilitada para que se puedan usar en un plan de calentamiento de IP.

Para crear una campaña de calentamiento de IP, siga los pasos a continuación.

1. Crear un [email](../email/email-settings.md) canal [emerger](channel-surfaces.md) para el dominio y las direcciones IP que ha identificado para su plan de calentamiento.

   >[!NOTE]
   >
   >Obtenga información sobre cómo seleccionar el dominio y las direcciones IP que se utilizarán en una superficie de correo electrónico en [esta sección](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Si es necesario, póngase en contacto con el consultor del equipo de entrega para identificar el dominio y las direcciones IP que se utilizarán para el plan de calentamiento de IP.<!--TBC-->

1. Crear un [campaña](../campaigns/create-campaign.md) y seleccione la [Correo electrónico](../email/create-email.md#create-email-journey-campaign) acción.

1. Seleccione la superficie que ha creado para el calentamiento de IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Haga clic en **[!UICONTROL Crear]**.

1. Desde el **[!UICONTROL Programación]** , seleccione **[!UICONTROL Activación del plan de calentamiento IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La campaña [programación](../campaigns/create-campaign.md#schedule) será impulsado por el plan de calentamiento de IP con el que estará asociado, lo que significa que la programación ya no está definida en la propia campaña.

1. Complete los pasos para crear una campaña de correo electrónico, como la definición de las propiedades de la campaña, [audiencia](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, y [content](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

1. [Activar](../campaigns/review-activate-campaign.md) la campaña.

   >[!NOTE]
   >
   >Para una campaña en directo con el plan de calentamiento de IP activado, la variable **[!UICONTROL Eliminar]** está disponible hasta que se asocia con un plan de calentamiento de IP. Una vez utilizada en un plan de calentamiento de IP, la campaña ya no se puede eliminar.

1. La campaña se muestra en la **[!UICONTROL Campañas]** lista. Para recuperar fácilmente todas las campañas de calentamiento de IP creadas en la zona protegida actual, puede filtrar por la opción de campaña **[!UICONTROL Preparación de IP]**.

   ![](assets/ip-warmup-campaign-filter.png)

Una vez activa, la campaña está lista para utilizarse en un plan de calentamiento de IP. [Más información](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

