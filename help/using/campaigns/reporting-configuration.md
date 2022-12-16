---
solution: Journey Optimizer
product: journey optimizer
title: Configurar los informes de Journey Optimizer para la experimentación
description: Obtenga información sobre cómo configurar una fuente de datos de creación de informes
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 29%

---

# Configurar la creación de informes para la experimentación {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configuración de conjuntos de datos para creación de informes"
>abstract="La configuración de informes permite recuperar métricas adicionales que se utilizarán en la pestaña Objetivos de los informes de campaña. Debe realizarla un usuario técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selección de un conjunto de datos"
>abstract="Solo puede seleccionar un conjunto de datos de tipo evento, que debe contener al menos uno de los grupos de campos admitidos: Detalles De La Aplicación, Detalles De Comercio, Detalles Web."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

La configuración de la fuente de datos de informes permite recuperar métricas adicionales que se utilizarán en la variable **[!UICONTROL Objetivos]** de los informes de campaña. [Más información](content-experiment.md#objectives-global)

>[!NOTE]
>
>La configuración de informes debe realizarla un usuario técnico. <!--Rights?-->

Para esta configuración, debe agregar uno o más conjuntos de datos que contengan los elementos adicionales que desee utilizar para los informes. Para ello, siga los pasos [below](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Requisitos previos


Antes de poder agregar un conjunto de datos a la configuración de informes, debe crear ese conjunto de datos. Obtenga más información en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=es#create){target=&quot;_blank&quot;}.

* Solo puede agregar conjuntos de datos de tipo de evento.

* Estos conjuntos de datos deben contener al menos uno de los siguientes [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target=&quot;_blank&quot;}: **Detalles de la aplicación**, **Detalles del comercio**, **Detalles web**.

   >[!NOTE]
   >
   >Actualmente solo se admiten estos grupos de campos.

   Por ejemplo, si desea conocer el impacto de una campaña de correo electrónico en los datos de comercio, como compras o pedidos, debe crear un conjunto de datos de evento de experiencia con la variable **Detalles del comercio** grupo de campos.

   Del mismo modo, si desea crear un informe sobre interacciones móviles, debe crear un conjunto de datos de evento de experiencia con la variable **Detalles de la aplicación** grupo de campos.

   Se muestran las métricas correspondientes a cada grupo de campos [here](#objective-list).

* Puede agregar estos grupos de campos a uno o varios esquemas que se utilizarán en uno o varios conjuntos de datos.

>[!NOTE]
>
>Obtenga más información sobre los esquemas XDM y los grupos de campos en la [Documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.

## Objetivos correspondientes a cada grupo de campos {#objective-list}

La tabla siguiente muestra qué métricas se agregarán al **[!UICONTROL Objetivos]** de los informes de campaña para cada grupo de campos.

| Grupo de campos | Objetivos |
|--- |--- |
| Detalles del comercio | Precio total<br>Importe de pago<br>(Único) Cierres de compra<br>(Único) Adiciones a la lista de productos<br>Aperturas (únicas) de la lista de productos<br>Eliminación de lista de productos (única)<br>Vistas de lista de productos (únicas)<br>Vistas del producto (únicas)<br>(Único) Compras<br>(Único) Guardar para versiones más recientes<br>Precio total del producto<br>Cantidad de productos |
| Detalles de la aplicación | (Único) Lanzamientos de aplicaciones<br>Primeros lanzamientos de la aplicación<br>(Único) Instalaciones de aplicaciones<br>Actualizaciones de aplicaciones (únicas) |
| Detalles web | Vistas de página (únicas) |

## Agregar conjuntos de datos {#add-datasets}

1. En el **[!UICONTROL ADMINISTRACIÓN]** seleccione **[!UICONTROL Configuraciones]**. En el  **[!UICONTROL Informes]** , haga clic en **[!UICONTROL Administrar]**.

   ![](assets/reporting-config-menu.png)

   Se muestra la lista de conjuntos de datos que ya se han añadido.

1. En el **[!UICONTROL Conjunto de datos]** , haga clic en **[!UICONTROL Agregar conjunto de datos]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Si selecciona la opción **[!UICONTROL Conjunto de datos del sistema]** , solo se muestran los conjuntos de datos creados por el sistema. No podrá añadir otros.

1. En el **[!UICONTROL Conjunto de datos]** lista desplegable, seleccione el conjunto de datos que desee usar para sus informes.

   >[!CAUTION]
   >
   >Solo puede seleccionar un conjunto de datos de tipo de evento que debe contener al menos uno de los [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target=&quot;_blank&quot;}: **Detalles de la aplicación**, **Detalles del comercio**, **Detalles web**. Si selecciona un conjunto de datos que no coincida con esos criterios, no podrá guardar los cambios.

   ![](assets/reporting-config-datasets.png)

   Obtenga más información sobre los conjuntos de datos en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=es){target=&quot;_blank&quot;}.

1. En el **[!UICONTROL ID de perfil]** en la lista desplegable, seleccione el atributo de campo del conjunto de datos que se utilizará para identificar cada perfil en los informes.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Solo se muestran los ID disponibles para la creación de informes.

1. La variable **[!UICONTROL Usar área de nombres de ID principal]** está activada de forma predeterminada. Si el **[!UICONTROL ID de perfil]** es **[!UICONTROL Mapa de identidad]**, puede desactivar esta opción y elegir otro espacio de nombres en la lista desplegable que se muestra.

   ![](assets/reporting-config-namespace.png)

   Obtenga más información acerca de las áreas de nombres en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=es){target=&quot;_blank&quot;}.

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
