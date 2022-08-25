---
title: Configuración de informes
description: Obtenga información sobre cómo configurar una fuente de datos de informes
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
ht-degree: 5%

---

# Configuración de informes {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configuración de conjuntos de datos para informes"
>abstract="La configuración de informes permite definir una conexión con un sistema para recuperar información personalizada adicional que se utilizará en los informes. Debe realizarlo un usuario técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Seleccionar un conjunto de datos"
>abstract="Solo puede seleccionar un conjunto de datos de tipo evento que debe contener al menos uno de los grupos de campos admitidos: experienceevent-web, experienceevent-application, experienceevent-commerce."

La configuración de la fuente de datos de informes permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los informes.

>[!NOTE]
>
>La configuración de la fuente de datos debe realizarla un usuario técnico. <!--Rights?-->

Para esta configuración, debe agregar uno o más conjuntos de datos que contengan los atributos que desee usar en los informes. Para realizar esto, siga los pasos a continuación.

>[!CAUTION]
>
>Antes de poder agregar un conjunto de datos a la configuración de informes, debe crearlo. Obtenga información sobre cómo en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.
>
>Solo puede agregar conjuntos de datos de tipo de evento que deben contener al menos uno de los [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Por ejemplo, si desea conocer el impacto de una campaña de correo electrónico en los datos de comercio, como compras o pedidos, debe crear un conjunto de datos de evento de experiencia con la variable **experienceevent-commerce** grupo de campos. Del mismo modo, si desea crear un informe sobre interacciones móviles, debe crear un conjunto de datos de evento de experiencia con la variable **experienceevent-application** grupo de campos. <!--If you want to report on web interactions then you need to include the web field group.--> Puede agregar estos grupos de campos a uno o varios esquemas que se utilizarán en un conjunto de datos o en diferentes conjuntos de datos.

>[!NOTE]
>
>Obtenga más información sobre los esquemas XDM y los grupos de campos en la [Documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.

1. En el **[!UICONTROL ADMINISTRATION]** seleccione **[!UICONTROL Configurations]**. En el  **[!UICONTROL Reporting]** , haga clic en **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   Se muestra la lista de conjuntos de datos que ya se han agregado.

1. En la pestaña **[!UICONTROL Dataset]**, haga clic en **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Si selecciona la opción **[!UICONTROL System dataset]** , solo se muestran los conjuntos de datos creados por el sistema. No podrá agregar otros conjuntos de datos.

1. En el **[!UICONTROL Dataset]** lista desplegable, seleccione el conjunto de datos que desee usar para sus informes.

   >[!CAUTION]
   >
   >Solo puede seleccionar un conjunto de datos de tipo de evento que debe contener al menos uno de los [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. Si selecciona un conjunto de datos que no coincida con esos criterios, no podrá guardar los cambios.

   ![](assets/reporting-config-datasets.png)

   Obtenga más información sobre los conjuntos de datos en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

1. En el **[!UICONTROL Profile ID]** en la lista desplegable, seleccione el atributo de campo del conjunto de datos que se utilizará para identificar cada perfil en los informes.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Solo se muestran los ID disponibles para la creación de informes.

1. La opción **[!UICONTROL Use Primary ID namespace]** está activada de forma predeterminada. Si el **[!UICONTROL Profile ID]** es **[!UICONTROL Identity Map]**, puede desactivar esta opción y elegir otro espacio de nombres en la lista desplegable que se muestra.

   ![](assets/reporting-config-namespace.png)

   Obtenga más información sobre las áreas de nombres en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=es){target=&quot;_blank&quot;}.

1. Guarde los cambios para agregar el conjunto de datos seleccionado a la lista de configuración de informes.

   >[!CAUTION]
   >
   >Si seleccionó un conjunto de datos que no es de tipo de evento, no podrá continuar.

Al crear los informes de las entregas, ahora puede utilizar los datos de este conjunto de datos para recuperar información personalizada adicional y ajustar mejor los informes. [Más información](content-experiment.md#objectives-global)

>[!NOTE]
>
>Si agrega varios conjuntos de datos, todos los datos de todos los conjuntos de datos estarán disponibles para el sistema de informes.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
