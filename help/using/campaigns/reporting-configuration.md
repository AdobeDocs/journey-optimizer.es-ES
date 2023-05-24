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
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 38%

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

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* [Introducción al experimento de contenido](get-started-experiment.md)
* [Creación de un experimento de contenido](content-experiment.md)
* [Comprensión de los cálculos estadísticos](experiment-calculations.md)
* **[Configurar informes de experimentación](reporting-configuration.md)**
* [Cálculos estadísticos en el informe de experimentación](experiment-report-calculations.md)

>[!ENDSHADEBOX]

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

La configuración de la fuente de datos de creación de informes permite recuperar métricas adicionales que se utilizarán en la **[!UICONTROL Objetivos]** de los informes de campaña. [Más información](content-experiment.md#objectives-global)

>[!NOTE]
>
>La configuración de creación de informes debe realizarla un usuario técnico. <!--Rights?-->

Para esta configuración, debe agregar uno o más conjuntos de datos que contengan los elementos adicionales que desee utilizar en los informes. Para ello, siga los pasos [abajo](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Requisitos previos


Antes de poder agregar un conjunto de datos a la configuración de creación de informes, debe crearlo. Obtenga más información en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=es#create){target="_blank"}.

* Solo puede añadir conjuntos de datos de tipo evento.

* Estos conjuntos de datos deben contener al menos uno de los siguientes elementos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"}: **Detalles de aplicación**, **Detalles de comercio**, **Detalles web**.

   >[!NOTE]
   >
   >Actualmente solo se admiten estos grupos de campos.

   Por ejemplo, si desea conocer el impacto de una campaña de correo electrónico en los datos de comercio, como compras o pedidos, debe crear un conjunto de datos de evento de experiencia con **Detalles de comercio** grupo de campos.

   Del mismo modo, si desea crear un informe sobre interacciones móviles, debe crear un conjunto de datos de evento de experiencia con **Detalles de aplicación** grupo de campos.

   Se muestran las métricas correspondientes a cada grupo de campos [aquí](#objective-list).

* Puede añadir estos grupos de campos a uno o varios esquemas que se utilizarán en uno o varios conjuntos de datos.

>[!NOTE]
>
>Obtenga más información sobre los esquemas XDM y los grupos de campos en la [Documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

## Objetivos correspondientes a cada grupo de campos {#objective-list}

La tabla siguiente muestra qué métricas se agregarán al **[!UICONTROL Objetivos]** de los informes de campaña para cada grupo de campos.

| Grupo de campos | Objetivos |
|--- |--- |
| Detalles de comercio | Precio total<br>Importe de pago<br>Cierres de compra (únicos)<br>Adiciones de lista de productos (únicas)<br>Aperturas de lista de productos (únicas)<br>Eliminación de la lista de productos (única)<br>Vistas de lista de productos (únicas)<br>Vistas del producto (únicas)<br>Compras (únicas)<br>(Único) Guardar Para Más Tarde<br>Precio total del producto<br>Cantidad de productos |
| Detalles de aplicación | Lanzamientos de aplicaciones (únicos)<br>Primeros inicios de la aplicación<br>Instalaciones de la aplicación (únicas)<br>Actualizaciones de aplicaciones (únicas) |
| Detalles web | Vistas de página (únicas) |

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

Al crear los informes de campaña, ahora puede ver las métricas correspondientes a los grupos de campos utilizados en los conjuntos de datos agregados. Vaya a la **[!UICONTROL Objetivos]** y seleccione las métricas que desee para ajustar mejor los informes. [Más información](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Si añade varios conjuntos de datos, los datos de todos ellos estarán disponibles para la creación de informes.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
