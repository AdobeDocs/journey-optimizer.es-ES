---
title: Añadir representaciones a una oferta
description: Aprenda a añadir representaciones a las ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: 0fa8ba1dc16062ea1553f9978752f3c018cec4c6
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 2%

---

# Añadir representaciones a una oferta {#add-representations}

Una oferta se puede mostrar en diferentes lugares de un mensaje: en un banner superior con una imagen, como texto en un párrafo, como bloque de HTML, etc. Cuantas más representaciones tenga una oferta, más oportunidades habrá de utilizar la oferta en diferentes contextos de ubicación.

## Configuración de las representaciones de la oferta {#representations}

Para añadir una o varias representaciones a la oferta y configurarlas, siga los pasos a continuación.

1. Para la primera representación, comience por seleccionar la variable **[!UICONTROL Channel]** que se utilizará.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Solo se muestran las ubicaciones disponibles para el canal seleccionado en la **[!UICONTROL Placement]** lista desplegable.

1. Seleccione una colocación de la lista.

   También puede utilizar el botón situado junto al **[!UICONTROL Placement]** lista desplegable para examinar todas las ubicaciones.

   ![](../assets/browse-button-placements.png)

   Aquí todavía puede filtrar las ubicaciones según su canal o tipo de contenido. Elija una ubicación y haga clic en **[!UICONTROL Select]**.

   ![](../assets/browse-placements.png)

1. Añada contenido a su representación. Obtenga información sobre cómo [esta sección](#content).

1. Al añadir contenido, como una imagen o una dirección URL, puede especificar un **[!UICONTROL Destination link]**: los usuarios que hacen clic en la oferta se dirigen a la página correspondiente.

   ![](../assets/offer-destination-link.png)

1. Finalmente, seleccione el idioma que desee para ayudar a identificar y administrar lo que se mostrará a los usuarios.

1. Para añadir otra representación, utilice el **[!UICONTROL Add representation]** y añada tantas representaciones como sea necesario.

   ![](../assets/offer-add-representation.png)

1. Una vez que haya añadido todas las representaciones, seleccione **[!UICONTROL Next]**.

## Definir contenido para las representaciones {#content}

Puede añadir diferentes tipos de contenido a una representación.

>[!NOTE]
>
>Solo está disponible el contenido correspondiente al tipo de contenido de la ubicación.

### Adición de imágenes {#images}

Si la ubicación seleccionada es de tipo imagen, puede añadir contenido proveniente del **Adobe Experience Cloud Asset** biblioteca, un repositorio centralizado de recursos proporcionado por [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Para trabajar con [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}, debe implementar [!DNL Assets Essentials] para su organización y asegúrese de que los usuarios forman parte de la **Usuarios consumidores de Assets Essentials** o/y **Usuarios de Assets Essentials** Perfiles de producto. Más información sobre [esta página](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

1. Elija la opción **[!UICONTROL Asset library]**.

1. Seleccione **[!UICONTROL Browse]**.

   ![](../assets/offer-browse-asset-library.png)

1. Examine los recursos para seleccionar la imagen que desee

1. Haga clic en **[!UICONTROL Select]**.

   ![](../assets/offer-select-asset.png)

### Agregar direcciones URL {#urls}

Para añadir contenido desde una ubicación pública externa, seleccione **[!UICONTROL URL]** y, a continuación, introduzca la dirección URL del contenido que desea añadir.

![](../assets/offer-content-url.png)

### Agregar texto personalizado {#custom-text}

También puede insertar contenido de tipo texto al seleccionar una ubicación compatible.

1. Seleccione la opción **[!UICONTROL Custom]** y haga clic en **[!UICONTROL Add content]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Esta opción no está disponible para ubicaciones de tipo imagen.

1. Escriba el texto que se mostrará en la oferta.

   ![](../assets/offer-text-content.png)

   Puede personalizar el contenido mediante el Editor de expresiones. Más información sobre [personalización](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Solo el **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** y **[!UICONTROL Helper functions]** las fuentes están disponibles para la gestión de decisiones.
