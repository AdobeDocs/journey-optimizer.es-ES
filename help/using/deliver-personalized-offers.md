---
title: Adición de ofertas personalizadas
description: Aprenda a añadir ofertas personalizadas a los mensajes
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 695eec156c7d159d2ab10a6aeb27a35108d704c0
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 3%

---

# Adición de ofertas personalizadas {#deliver-personalized-offers}

En [!DNL Journey Optimizer] mensajes de correo electrónico, puede insertar decisiones (anteriormente conocidas como &quot;actividades de oferta&quot;) que aprovechan el motor de decisión de ofertas para elegir la mejor oferta y enviarla a sus clientes.

Por ejemplo, puede agregar una decisión que muestre en el correo electrónico una oferta de descuento especial que variará según el nivel de lealtad del destinatario.

Para obtener más información sobre cómo crear y administrar ofertas, consulte [esta sección](offers/get-started/starting-offer-decisioning.md).

Para un **ejemplo completo de extremo a extremo** mostrar cómo configurar ofertas, utilizarlas en una decisión y aprovechar esta decisión en un correo electrónico, consulte [esta sección](offers/offers-e2e.md#insert-decision-in-email).

➡️ [Aprenda a añadir ofertas como personalización en este vídeo](#video-offers)

## Insertar una decisión en un correo electrónico {#insert-offers}

>[!CAUTION]
>
>Antes de empezar, debe [definir una decisión de oferta](offers/offer-activities/create-offer-activities.md).

Para insertar una decisión en un mensaje de correo electrónico, siga los pasos a continuación:

1. Cree el correo electrónico y, a continuación, abra el Diseñador de correo electrónico para configurar su contenido.

1. Agregue un **[!UICONTROL Offer decision]** componente de contenido.

   ![](assets/deliver-offer-component.png)

   Aprenda a utilizar los componentes de contenido en [esta sección](content-components.md).

1. La variable **[!UICONTROL Offer decision]** aparece en la paleta derecha. Haga clic en **[!UICONTROL Select Offer decision]**.

   ![](assets/deliver-offer-tab.png)

1. En la ventana que se muestra, seleccione la colocación correspondiente a las ofertas que desea mostrar.

   [Ubicaciones](offers/offer-library/creating-placements.md) son contenedores que se utilizan para mostrar sus ofertas. En este ejemplo, utilizaremos la ubicación &quot;imagen superior del correo electrónico&quot;. Esta ubicación se ha creado en la Biblioteca de ofertas para mostrar las ofertas de tipo imagen situadas en la parte superior de los mensajes.

1. Seleccione la actividad de oferta que desea utilizar en el componente de contenido y haga clic en **[!UICONTROL Add]**.

   >[!NOTE]
   >
   >En la lista solo se muestran las decisiones compatibles con la colocación seleccionada. En este ejemplo, solo una actividad de oferta coincide con la ubicación &quot;imagen superior del correo electrónico&quot;.

   ![](assets/deliver-offer-placement.png)

La actividad de oferta ahora se agrega al componente.


## Vista previa de ofertas en un correo electrónico {#preview-offers-in-email}

Puede obtener una vista previa de las diferentes ofertas que forman parte de la decisión agregada al correo electrónico mediante la variable **[!UICONTROL Offers]** o las flechas de los componentes de contenido.

![](assets/deliver-offer-preview.png)

Para mostrar las diferentes ofertas que forman parte de la decisión con un perfil de cliente, siga los pasos a continuación.

1. Haga clic en **[!UICONTROL Preview]**.

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >Debe tener perfiles de prueba disponibles para poder previsualizar los mensajes. Obtenga información sobre cómo [crear perfiles de prueba](building-journeys/creating-test-profiles.md).

1. Para elegir el área de nombres que se utiliza para identificar los perfiles de prueba, seleccione **[!UICONTROL Email]** de la variable **[!UICONTROL Identity namespace]** campo .

   >[!NOTE]
   >
   >En este ejemplo, utilizaremos la variable **Correo electrónico** espacio de nombres. Obtenga más información sobre las áreas de nombres de identidad de Adobe Experience Platform [en esta sección](get-started-identity.md).

1. En la lista de áreas de nombres de identidad, seleccione **[!UICONTROL Email]** y haga clic en **[!UICONTROL Select]**.

1. En el **[!UICONTROL Identity value]** , introduzca el valor para identificar el perfil de prueba. En este ejemplo, introduzca la dirección de correo electrónico de un perfil de prueba.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. Añada otros perfiles para poder probar distintas variantes del mensaje según los datos del perfil.

   ![](assets/deliver-offer-test-profiles.png)

1. Haga clic en el **[!UICONTROL Preview]** para probar el mensaje.

1. Seleccione un perfil de prueba. Se muestra la oferta correspondiente al perfil seleccionado (una mujer).

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. Seleccione otros perfiles de prueba para previsualizar el contenido del correo electrónico de cada variante del mensaje. En el contenido del mensaje, ahora se muestra la oferta correspondiente al perfil de prueba seleccionado (ahora un hombre).

   ![](assets/deliver-offer-test-profile-male-preview.png)

Obtenga más información sobre los pasos detallados para comprobar la vista previa del mensaje en [esta sección](#preview-your-messages).

## Vídeo explicativo{#video-offers}

Aprenda a añadir un componente de Offer Decisioning a los mensajes en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)

