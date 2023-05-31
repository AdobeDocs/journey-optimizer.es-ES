---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de informes de Journey Optimizer para experimentación
description: Obtenga información sobre cómo configurar una fuente de datos de creación de informes
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: configuración, experimentación, informes, optimizador
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: dc48cc6d95e4af288727961fd9f7761dee4f2552
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 43%

---

# Configuración de informes para experimentación {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configuración de conjuntos de datos para creación de informes"
>abstract="La configuración de la creación de informes permite recuperar métricas adicionales que se utilizarán en la pestaña Objetivos de los informes de campaña. Debe realizarla un usuario técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selección de un conjunto de datos"
>abstract="Solo puede seleccionar un conjunto de datos de tipo evento, que debe contener al menos uno de los grupos de campos admitidos: detalles de la aplicación, detalles de comercio, detalles web."

La configuración de la fuente de datos de creación de informes permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los informes.

<!--The reporting data source configuration allows you to retrieve additional metrics that will be used in the **[!UICONTROL Objectives]** tab of your campaign reports. [Learn more](content-experiment.md#objectives-global)-->

>[!NOTE]
>
>La configuración de creación de informes debe realizarla un usuario técnico. <!--Rights?-->

Para esta configuración, debe agregar uno o más conjuntos de datos que contengan los elementos adicionales que desee utilizar en los informes. Para ello, siga los pasos [abajo](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Requisitos previos


Antes de poder agregar un conjunto de datos a la configuración de creación de informes, debe crearlo. Obtenga más información en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#create){target="_blank"}.

* Solo puede añadir conjuntos de datos de tipo evento.

* Estos conjuntos de datos deben contener al menos uno de los siguientes elementos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"}: **Detalles de aplicación**, **Detalles de comercio**, **Detalles web**.

   >[!NOTE]
   >
   >Actualmente solo se admiten estos grupos de campos.

   Por ejemplo, si desea conocer el impacto de una campaña de correo electrónico en los datos de comercio, como compras o pedidos, debe crear un conjunto de datos de evento de experiencia con **Detalles de comercio** grupo de campos.

   Del mismo modo, si desea crear un informe sobre interacciones móviles, debe crear un conjunto de datos de evento de experiencia con **Detalles de aplicación** grupo de campos.

   <!--The metrics corresponding to each field group are listed [here](#objective-list).-->

* Puede añadir estos grupos de campos a uno o varios esquemas que se utilizarán en uno o varios conjuntos de datos.

>[!NOTE]
>
>Obtenga más información sobre los esquemas XDM y los grupos de campos en la [Documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

<!--
## Objectives corresponding to each field group {#objective-list}

The table below shows which metrics will be added to the **[!UICONTROL Objectives]** tab of your campaign reports for each field group.

| Field group | Objectives |
|--- |--- |
| Commerce Details | Price Total<br>Payment Amount<br>(Unique) Checkouts<br>(Unique) Product List Adds<br>(Unique) Product List Opens<br>(Unique) Product List Removal<br>(Unique) Product List Views<br>(Unique) Product Views<br>(Unique) Purchases<br>(Unique) Save For Laters<br>Product Price Total<br>Product Quantity |
| Application Details | (Unique) App Launches<br>First App Launches<br>(Unique) App Installs<br>(Unique) App Upgrades |
| Web Details | (Unique) Page Views |
-->

## Añadir conjuntos de datos {#add-datasets}

1. Desde el **[!UICONTROL ADMINISTRACIÓN]** menú, seleccione **[!UICONTROL Configuraciones]**. En el  **[!UICONTROL Informes]** , haga clic en **[!UICONTROL Administrar]**.

   ![](assets/reporting-config-menu.png)

   Se muestra la lista de conjuntos de datos que ya se han añadido.

1. Desde el **[!UICONTROL Conjunto de datos]** pestaña, haga clic en **[!UICONTROL Añadir conjunto de datos]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Si selecciona la opción **[!UICONTROL Conjunto de datos del sistema]** pestaña, solo se muestran los conjuntos de datos creados por el sistema. No podrá añadir otros.

1. Desde el **[!UICONTROL Conjunto de datos]** , seleccione el conjunto de datos que desee utilizar para sus informes.

   >[!CAUTION]
   >
   >Solo puede seleccionar un conjunto de datos de tipo evento, que debe contener al menos uno de los [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"}: **Detalles de aplicación**, **Detalles de comercio**, **Detalles web**. Si selecciona un conjunto de datos que no coincida con esos criterios, no podrá guardar los cambios.

   ![](assets/reporting-config-datasets.png)

   Obtenga más información sobre los conjuntos de datos en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=es){target="_blank"}.

1. Desde el **[!UICONTROL ID de perfil]** , seleccione el atributo de campo del conjunto de datos que se utilizará para identificar cada perfil en los informes.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Solo se muestran los ID disponibles para la creación de informes.

1. El **[!UICONTROL Usar área de nombres de ID principal]** está activada de forma predeterminada. Si el seleccionado **[!UICONTROL ID de perfil]** es **[!UICONTROL Mapa de identidad]**, puede desactivar esta opción y elegir otra área de nombres en la lista desplegable que se muestra.

   ![](assets/reporting-config-namespace.png)

   Obtenga más información acerca de las áreas de nombres en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=es){target="_blank"}.

1. Guarde los cambios para añadir el conjunto de datos seleccionado a la lista de configuración de creación de informes.

   >[!CAUTION]
   >
   >Si seleccionó un conjunto de datos que no es de tipo de evento, no podrá continuar.

<!--
When building your campaign reports, you can now see the metrics corresponding to the field groups used in the datasets you added. Go to the **[!UICONTROL Objectives]** tab and select the metrics of your choice to better fine-tune your reports. [Learn more](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>If you add several datasets, all data from all datasets will be available for reporting.


## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
