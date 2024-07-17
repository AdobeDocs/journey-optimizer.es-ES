---
solution: Journey Optimizer
product: journey optimizer
title: Creación de campañas de calentamiento de IP
description: Obtenga información sobre cómo crear una campaña de calentamiento de IP
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP, grupos, capacidad de entrega
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: c400104c86e1a9a2de819db7743b3f77153ad90b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 17%

---

# Creación de campañas de calentamiento de IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activación de la opción de plan de calentamiento de IP"
>abstract="Al seleccionar esta opción, la campaña se puede utilizar en un plan de calentamiento de IP. La programación de la campaña se regirá por el plan de calentamiento de IP con el que está asociada."

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a los planes de calentamiento de IP](ip-warmup-gs.md)
* **[Crear campañas de calentamiento de IP](ip-warmup-campaign.md)**
* [Creación de un plan de calentamiento de IP](ip-warmup-plan.md)
* [Ejecución del plan de calentamiento de IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Antes de crear el plan de calentamiento de IP en [!DNL Journey Optimizer], primero debe crear una o más campañas diseñadas específicamente para usarlas en un plan de calentamiento de IP<!--through a dedicated option-->.

Para crear una campaña de calentamiento de IP, siga los pasos a continuación.

1. Cree un [correo electrónico](../email/email-settings.md) canal [surface](channel-surfaces.md) para el dominio y las direcciones IP que identificó para su plan de calentamiento.

   >[!NOTE]
   >
   >Aprenda a seleccionar el dominio y las direcciones IP que se utilizarán en una superficie de correo electrónico en [esta sección](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Póngase en contacto con el consultor del equipo de entrega para identificar el dominio y las direcciones IP que se utilizarán para el plan de calentamiento de IP.<!--TBC-->

1. Cree una [campaña](../campaigns/create-campaign.md) de marketing programado y seleccione la acción [Correo electrónico](../email/create-email.md#create-email-journey-campaign).

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. Seleccione la superficie que ha creado para el calentamiento de IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Haga clic en **[!UICONTROL Crear]**.

1. En la sección **[!UICONTROL Programar]**, seleccione **[!UICONTROL Activación del plan de calentamiento IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La programación [schedule](../campaigns/create-campaign.md#schedule) de la campaña estará dirigida por el plan de calentamiento de IP con el que estará asociada, lo que significa que la programación ya no está definida en la propia campaña.

1. Complete los pasos para crear una campaña de correo electrónico, como definir las propiedades de la campaña, [audiencia](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?--> y [contenido](../email/get-started-email-design.md#key-steps).

   Tenga en cuenta que debe seleccionar una audiencia basada en reglas para la campaña de calentamiento de IP. [Más información](../audience/creating-a-segment-definition.md)

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

1. [Activar](../campaigns/review-activate-campaign.md) la campaña. Su estado cambia a **[!UICONTROL Activo]**.

   Tenga en cuenta que las reglas empresariales no deben utilizarse en el plan de calentamiento de IP. La aplicación de estas reglas podría dificultar el logro del número deseado de perfiles objetivo para las campañas.

   >[!NOTE]
   >
   >Para una campaña en vivo con el plan de calentamiento de IP activado, el botón **[!UICONTROL Eliminar]** está disponible hasta que se asocie con un plan de calentamiento de IP. Una vez utilizada en un plan, la campaña ya no se puede eliminar.

1. La campaña se muestra en la lista **[!UICONTROL Campañas]**. Para recuperar fácilmente todas las campañas de calentamiento de IP creadas en la zona protegida actual, puede filtrar por la opción de campaña **[!UICONTROL calentamiento de IP]**.

   ![](assets/ip-warmup-campaign-filter.png)

Una vez activa, la campaña está lista para utilizarse en un plan de calentamiento de IP. [Más información](ip-warmup-plan.md)

Una campaña de calentamiento de IP solo se puede utilizar en un plan de calentamiento de IP. Sin embargo, la misma campaña se puede utilizar en una o más fases del mismo plan de calentamiento de IP. [Más información](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>Cuando se usa una campaña activa en un plan de calentamiento de IP, después de que el plan esté [marcado como completado](ip-warmup-execution.md#mark-as-completed), el estado de esa campaña cambia a **[!UICONTROL Detenido]**.

