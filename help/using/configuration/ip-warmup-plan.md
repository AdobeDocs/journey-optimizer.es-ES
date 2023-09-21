---
solution: Journey Optimizer
product: journey optimizer
title: Crear un plan de calentamiento de IP
description: Obtenga información sobre cómo crear un plan de calentamiento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupos, grupo, subdominios, capacidad de entrega
hide: true
hidefromtoc: true
source-git-commit: 53be033ff0474cbafff71ed36194c18627234fd4
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 5%

---

# Crear un plan de calentamiento de IP {#ip-warmup}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción al calentamiento de IP](ip-warmup-gs.md)
* [Creación de campañas de calentamiento de IP](ip-warmup-campaign.md)
* **[Crear un plan de calentamiento de IP](ip-warmup-plan.md)**
* [Ejecutar el plan de calentamiento de IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

Una vez que [ha creado una o más campañas](ip-warmup-campaign.md) con una superficie dedicada y la opción calentamiento de IP habilitada, puede empezar a crear su plan de calentamiento de IP.

## Acceso y administración de planes de calentamiento de IP {#manage-ip-warmup-plans}

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL planes de calentamiento de IP]** menú. Se muestran todos los planes de calentamiento de IP creados hasta el momento.

   ![](assets/ip-warmup-filter-list.png)

1. Puede filtrar por el estado. Los diferentes estados son:

   * **Sin iniciar**: no se ha producido ninguna ejecución
   * **En curso**: tan pronto como se ha iniciado una ejecución <!--or is done?-->
   * **En pausa**
   * **Completado**: todas las ejecuciones del plan han finalizado

1. Para eliminar un plan de calentamiento de IP, seleccione la **[!UICONTROL Eliminar]** junto a un elemento de la lista y confirme la eliminación.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >El plan de calentamiento de IP seleccionado se eliminará de forma permanente.

## Crear un plan de calentamiento de IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Especifique el plan de calentamiento de IP"
>abstract="Descargue la plantilla CSV y rellénela con datos de las fases de calentamiento de la IP y el número de destinatarios de los perfiles."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Selección de una superficie de marketing"
>abstract="Debe seleccionar la misma superficie que la seleccionada en la campaña que desea asociar con su plan de calentamiento de IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=es" text="Configuración de superficies de canal"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=es" text="Creación de campañas de calentamiento de IP"

>[!CAUTION]
>
>Para crear, editar y eliminar los planes de calentamiento de IP, debe tener **[!UICONTROL Consultor de capacidad de entrega]** permiso.
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

Cuando una o más campañas en directo con **[!UICONTROL Activación del plan de calentamiento IP]** activada, puede asociarlas a un plan de calentamiento de IP.

>[!CAUTION]
>
>Póngase en contacto con el consultor del equipo de entrega para asegurarse de que la plantilla del plan de calentamiento de IP esté correctamente configurada. <!--TBC-->

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL planes de calentamiento de IP]** y haga clic en **[!UICONTROL Crear plan de calentamiento de IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Complete los detalles del plan de calentamiento de IP: asígnele un nombre y una descripción.

   ![](assets/ip-warmup-plan-details.png)

1. Seleccione una [emerger](channel-surfaces.md). Solo las superficies de marketing están disponibles para su selección. [Más información sobre el tipo de correo electrónico](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >Debe seleccionar la misma superficie que la seleccionada en la campaña que desea asociar con su plan de calentamiento de IP. [Obtenga información sobre cómo crear una campaña de calentamiento de IP](#create-ip-warmup-campaign)

1. Cargue el archivo de Excel que contiene el plan de calentamiento de IP<!--which formats are allowed?-->. Puede utilizar la plantilla proporcionada por el equipo de entrega.<!--TBC?--> [Más información](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Haga clic en **[!UICONTROL Crear]**. El número de fases definidas en el archivo que ha cargado se muestra automáticamente en todas las ejecuciones de cada fase. [Más información](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

### Volver a cargar un plan de calentamiento de IP {#re-upload-plan}

Puede volver a cargar otro plan de calentamiento de IP con el botón correspondiente.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>Los detalles del plan de calentamiento de IP cambiarán según el archivo recién cargado. Las ejecuciones completas y las ejecuciones activadas no se ven afectadas.

### Cargue el archivo que contiene el plan {#upload-plan}

A continuación se muestra un ejemplo de un archivo que contiene un plan de calentamiento de IP.

![](assets/ip-warmup-sample-file.png)

Cada fase corresponde a un periodo compuesto por varias ejecuciones, a las que se asigna una sola campaña.

Para cada ejecución, tiene un determinado número de destinatarios y definirá una fecha en la que se ejecutará.

Puede tener tantas columnas como desee para los dominios a los que desee enviar. En este ejemplo, tiene tres columnas: Gmail, Adobe y Otros, lo que significa que

La idea es tener más ejecuciones en las primeras fases y aumentar progresivamente el número de direcciones objetivo al mismo tiempo que se reduce el número de ejecuciones.
