---
title: Configuración de la creación de informes
description: Obtenga información sobre cómo configurar una fuente de datos de creación de informes
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---

# Configuración de la creación de informes {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configuración de conjuntos de datos para creación de informes"
>abstract="La configuración de creación de informes permite definir una conexión con un sistema para recuperar información personalizada adicional que se utilizará en los informes. Debe realizarla un usuario técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selección de un conjunto de datos"
>abstract="Solo puede seleccionar un conjunto de datos de tipo evento que debe contener al menos uno de los grupos de campos admitidos: experienceevent-web, experienceevent-application, experienceevent-commerce."

La configuración de la fuente de datos de creación de informes permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los informes.

>[!NOTE]
>
>La configuración de la fuente de datos la debe realizar un usuario técnico. <!--Rights?-->

Para esta configuración, debe agregar uno o más conjuntos de datos que contengan los atributos que desee usar en los informes. Para realizar esto, siga los pasos a continuación.

>[!CAUTION]
>
>Antes de poder añadir un conjunto de datos a la configuración de creación de informes, debe crearlo. Obtenga más información en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=es#create){target=&quot;_blank&quot;}.
>
>Solo puede añadir conjuntos de datos de tipo de evento, que deben contener al menos uno de los [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target=&quot;_blank&quot;} admitidos: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Por ejemplo, si desea conocer el impacto de una campaña de correo electrónico en los datos de comercio, como compras o pedidos, debe crear un conjunto de datos de evento de experiencia con el grupo de campos **experienceevent-commerce**. Del mismo modo, si desea crear un informe sobre interacciones móviles, debe generar un conjunto de datos de evento de experiencia con el grupo de campos **experienceevent-application**. <!--If you want to report on web interactions then you need to include the web field group.--> Puede añadir estos grupos de campos a uno o varios esquemas que se utilizarán en un conjunto de datos o en varios.

>[!NOTE]
>
>Obtenga más información sobre los esquemas XDM y los grupos de campos en la [Documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.

1. Del menú **[!UICONTROL ADMINISTRATION]**, seleccione **[!UICONTROL Configurations]**. En la sección **[!UICONTROL Reporting]**, haga clic en **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   Se muestra la lista de conjuntos de datos que ya se han añadido.

1. En la pestaña **[!UICONTROL Dataset]**, haga clic en **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Si selecciona la pestaña **[!UICONTROL System dataset]**, solo se muestran los conjuntos de datos creados por el sistema. No podrá añadir otros.

1. En la lista desplegable **[!UICONTROL Dataset]**, seleccione el conjunto de datos que desee usar para sus informes.

   >[!CAUTION]
   >
   >Solo puede seleccionar un conjunto de datos de tipo de evento, que debe contener al menos uno de los [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} admitidos: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. Si selecciona un conjunto de datos que no coincida con esos criterios, no podrá guardar los cambios.

   ![](assets/reporting-config-datasets.png)

   Obtenga más información sobre los conjuntos de datos en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=es){target=&quot;_blank&quot;}.

1. En la lista desplegable **[!UICONTROL Profile ID]**, seleccione el atributo de campo del conjunto de datos que se utilizará para identificar cada perfil en los informes.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Solo se muestran los ID disponibles para la creación de informes.

1. La opción **[!UICONTROL Use Primary ID namespace]** está activada de forma predeterminada. Si la **[!UICONTROL Profile ID]** seleccionada es **[!UICONTROL Identity Map]**, puede desactivar esta opción y elegir otra área de nombres en la lista desplegable que se muestra.

   ![](assets/reporting-config-namespace.png)

   Obtenga más información acerca de las áreas de nombres en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=es){target=&quot;_blank&quot;}.

1. Guarde los cambios para añadir el conjunto de datos seleccionado a la lista de configuración de creación de informes.

   >[!CAUTION]
   >
   >Si seleccionó un conjunto de datos que no es de tipo de evento, no podrá continuar.

Al crear los informes de las entregas, ahora puede utilizar los datos de este conjunto de datos para recuperar información personalizada adicional y refinar los informes. [Más información](content-experiment.md#objectives-global)

>[!NOTE]
>
>Si añade varios conjuntos de datos, los datos de todos ellos estarán disponibles para la creación de informes.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
