---
title: Añadir representaciones a una oferta
description: Obtenga información sobre cómo añadir representaciones a las ofertas
badge: label="Heredado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 96afe15b89b0a8291d5682bbfaa67404b5ebef93
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 8%

---

# Añadir representaciones a una oferta {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Representaciones"
>abstract="Añada representaciones para definir dónde se mostrará la oferta en el mensaje. Cuantas más representaciones tenga una oferta, más oportunidades habrá de utilizar la oferta en diferentes contextos de ubicación."

Una oferta se puede mostrar en diferentes lugares de un mensaje: en un banner superior con una imagen, como texto en un párrafo, como un bloque de HTML, etc. Cuantas más representaciones tenga una oferta, más oportunidades habrá de utilizar la oferta en diferentes contextos de ubicación.

## Configuración de las representaciones de la oferta {#representations}

Para añadir una o varias representaciones a la oferta y configurarlas, siga los pasos a continuación.

1. Para la primera representación, comience por seleccionar el **[!UICONTROL canal]** que se utilizará.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Solo se muestran las ubicaciones disponibles para el canal seleccionado en la lista desplegable **[!UICONTROL Ubicación]**.

1. Seleccione una ubicación de la lista.

   También puede usar el botón que se encuentra junto a la lista desplegable **[!UICONTROL Ubicación]** para examinar todas las ubicaciones.

   ![](../assets/browse-button-placements.png)

   Allí aún puede filtrar las ubicaciones según su canal o tipo de contenido. Elija una ubicación y haga clic en **[!UICONTROL Seleccionar]**.

   ![](../assets/browse-placements.png)

1. Añada contenido a su representación. Aprenda en [esta sección](#content).

1. Al agregar contenido, como una imagen o una dirección URL, puede especificar un **[!UICONTROL vínculo de destino]**: los usuarios que hagan clic en la oferta se dirigirán a la página correspondiente.

   ![](../assets/offer-destination-link.png)

1. Finalmente, seleccione el idioma de su elección para identificar y administrar qué mostrar a los usuarios.

1. Para agregar otra representación, use el botón **[!UICONTROL Agregar representación]** y agregue tantas representaciones como sea necesario.

   ![](../assets/offer-add-representation.png)

1. Una vez que hayas agregado todas tus representaciones, selecciona **[!UICONTROL Siguiente]**.

## Definición del contenido de las representaciones {#content}

Se pueden añadir distintos tipos de contenido a una representación.

>[!NOTE]
>
>Solo el contenido correspondiente al tipo de contenido de la ubicación está disponible para su uso.

### Adición de imágenes {#images}

Si la ubicación seleccionada es de tipo imagen, puede agregar contenido procedente de la biblioteca **Adobe Experience Cloud Asset**, un repositorio centralizado de recursos proporcionado por [!DNL Adobe Experience Manager Assets].

>[!NOTE]
>
> Para trabajar con [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, debes implementar [!DNL Assets Essentials] para tu organización y asegurarte de que los usuarios formen parte de los perfiles de producto de **Usuarios consumidores de Assets Essentials** o **Usuarios de Assets Essentials**. Más información sobre [esta página](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. Elija la opción **[!UICONTROL Biblioteca de recursos]**.

1. Seleccione **[!UICONTROL Examinar]**.

   ![](../assets/offer-browse-asset-library.png)

1. Examine los recursos para seleccionar la imagen que desee

1. Haga clic en **[!UICONTROL Seleccionar]**.

   ![](../assets/offer-select-asset.png)

### Añadir archivos HTML o JSON {#html-json}

Si la ubicación seleccionada es de tipo HTML, también puede agregar contenido HTML o JSON proveniente de la [biblioteca de recursos de Adobe Experience Cloud](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}).

Por ejemplo, creó una plantilla de correo electrónico de HTML en [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} y quiere usar ese archivo para el contenido de su oferta. En lugar de crear un nuevo archivo, simplemente puede cargar la plantilla en la **Biblioteca de recursos** para poder reutilizarla en las representaciones de la oferta.

Para reutilizar el contenido en una representación, examine la **Biblioteca de recursos** tal como se describe en [esta sección](#images) y seleccione el archivo HTML o JSON que elija.

![](../assets/offer-browse-asset-library-json.png)

### Añadir URL {#urls}

Para agregar contenido desde una ubicación pública externa, seleccione **[!UICONTROL URL]** y luego ingrese la dirección URL del contenido que desea agregar.

Puede personalizar las direcciones URL mediante el editor de personalización. Más información sobre [personalización](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

Por ejemplo, se desea personalizar la imagen que se muestra como oferta. Desea que los usuarios que favorecen las vacaciones en la ciudad vean el horizonte de Nueva York y los usuarios que favorecen las vacaciones en la playa vean la costa norte de Hawai.

Utilice el editor de personalización para recuperar los atributos de perfil almacenados en Adobe Experience Platform mediante esquemas de unión. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

Si especifica un **[!UICONTROL vínculo de destino]**, también puede personalizar la dirección URL a la que se dirigirán los usuarios que hagan clic en la oferta.

### Añadir texto personalizado {#custom-text}

También puede insertar contenido de tipo texto al seleccionar una ubicación compatible.

1. Seleccione la opción **[!UICONTROL Personalizado]** y haga clic en **[!UICONTROL Agregar contenido]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Esta opción no está disponible para ubicaciones de tipo imagen.

1. Escriba el texto que se mostrará en la oferta.

   ![](../assets/offer-text-content.png)

   Puede personalizar el contenido mediante el editor de personalización. Más información sobre [personalización](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Solo los orígenes de **[!UICONTROL atributos de perfil]**, **[!UICONTROL Audiencias]** y **[!UICONTROL Funciones de ayuda]** están disponibles para Administración de decisiones.

## Personalizar representaciones basadas en datos de contexto{#context-data}

Cuando se pasan datos de contexto en la llamada a [Edge Decisioning](../api-reference/offer-delivery-api/edge-decisioning-api.md), puede aprovechar estos datos para personalizar representaciones de forma dinámica. Por ejemplo, puede adaptar la representación de una oferta en función de factores en tiempo real como las condiciones meteorológicas actuales en el momento en que se toma la decisión.

Para utilizar datos de contexto en representaciones de ofertas, incorpore la variable de datos de contexto directamente dentro del contenido de representación mediante el espacio de nombres `profile.timeSeriesEvents.`.

Este es un ejemplo de sintaxis utilizado para personalizar la representación de una oferta en función de los sistemas operativos de los usuarios:

```
 {%#if profile.timeSeriesEvents.device.model = "Apple"%}ios{%else%}android{%/if%} 
```

La solicitud de Edge Decisioning correspondiente, incluidos los datos de contexto, es la siguiente:

```
{
    "body": {
        "xdm": {
            "identityMap": {
                "Email": [
                    {
                        "id": "xyz@abc.com"
                    }
                ]
            },
            "device": {
                "model": "Apple"
            }
        },
        "extra": {
            "query": {
                "decisionScopes": [
                    "eyJ4ZG06..."
                ]
            }
        }
    }
}
```
