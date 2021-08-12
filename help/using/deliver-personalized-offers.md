---
title: Adición de ofertas personalizadas
description: Aprenda a añadir ofertas personalizadas a los mensajes
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 1f93158f89e7e05e8e7978960f09cc7e1d4cdc7a
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 4%

---

# Adición de ofertas personalizadas {#deliver-personalized-offers}

En los mensajes de correo electrónico [!DNL Journey Optimizer], puede insertar decisiones (anteriormente conocidas como &quot;actividades de oferta&quot;) que aprovecharán el motor de decisión de oferta para elegir la mejor oferta que se debe entregar a sus clientes.

Por ejemplo, puede agregar una decisión que muestre en el correo electrónico una oferta de descuento especial que variará según el nivel de lealtad del destinatario.

Para obtener más información sobre cómo crear y administrar ofertas, consulte [esta sección](offers/get-started/starting-offer-decisioning.md).

Para ver un **ejemplo completo de extremo a extremo** que muestra cómo configurar ofertas, utilícelas en una decisión y aproveche esta decisión en un mensaje de correo electrónico, consulte [esta sección](offers/offers-e2e.md#insert-decision-in-email).

➡️ [Aprenda a añadir ofertas como personalización en este vídeo](#video-offers)

## Insertar una decisión en un correo electrónico {#insert-offers}

>[!CAUTION]
>
>Antes de comenzar, debe [definir una decisión de oferta](offers/offer-activities/create-offer-activities.md).

Para insertar una decisión en un mensaje de correo electrónico, siga los pasos a continuación:

1. Cree el correo electrónico y, a continuación, abra el Diseñador de correo electrónico para configurar su contenido.

1. Añada un componente de contenido **[!UICONTROL Offer decision]**.

   ![](assets/deliver-offer-component.png)

   Aprenda a utilizar componentes de contenido en [esta sección](content-components.md).

1. La ficha **[!UICONTROL Offer decision]** aparece en la paleta derecha. Haga clic en **[!UICONTROL Select Offer decision]**.

   ![](assets/deliver-offer-tab.png)

1. En la ventana que se muestra, seleccione la colocación correspondiente a las ofertas que desea mostrar.

   [](offers/offer-library/creating-placements.md) Las ubicaciones son contenedores que se utilizan para mostrar las ofertas. En este ejemplo, utilizaremos la ubicación &quot;imagen superior del correo electrónico&quot;. Esta ubicación se ha creado en la Biblioteca de ofertas para mostrar las ofertas de tipo imagen situadas en la parte superior de los mensajes.

1. Seleccione la actividad de oferta que desea utilizar en el componente de contenido y haga clic en **[!UICONTROL Add]**.

   >[!NOTE]
   >
   >En la lista solo se muestran las decisiones compatibles con la colocación seleccionada. En este ejemplo, solo una actividad de oferta coincide con la ubicación &quot;imagen superior del correo electrónico&quot;.

   ![](assets/deliver-offer-placement.png)

La actividad de oferta ahora se agrega al componente.


## Vista previa de ofertas en un correo electrónico {#preview-offers-in-email}

Puede obtener una vista previa de las diferentes ofertas que forman parte de la decisión añadida al correo electrónico mediante la sección **[!UICONTROL Offers]** o las flechas de los componentes de contenido.

![](assets/deliver-offer-preview.png)

Para mostrar las diferentes ofertas que forman parte de la decisión con un perfil de cliente, siga los pasos a continuación.

1. Haga clic en **[!UICONTROL Preview]**.

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >Debe tener perfiles de prueba disponibles para poder previsualizar los mensajes. Obtenga información sobre cómo [crear perfiles de prueba](building-journeys/creating-test-profiles.md).

1. Para elegir el espacio de nombres que se utiliza para identificar los perfiles de prueba, seleccione **[!UICONTROL Email]** en el campo **[!UICONTROL Identity namespace]**.

   >[!NOTE]
   >
   >En este ejemplo, utilizaremos el espacio de nombres **Email**. Obtenga más información sobre los áreas de nombres de identidad [de Adobe Experience Platform en esta sección](get-started-identity.md).

1. En la lista de áreas de nombres de identidad, seleccione **[!UICONTROL Email]** y haga clic en **[!UICONTROL Select]**.

1. En el campo **[!UICONTROL Identity value]**, introduzca el valor para identificar el perfil de prueba. En este ejemplo, introduzca la dirección de correo electrónico de un perfil de prueba.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. Añada otros perfiles para poder probar distintas variantes del mensaje según los datos del perfil.

   ![](assets/deliver-offer-test-profiles.png)

1. Haga clic en la pestaña **[!UICONTROL Preview]** para probar el mensaje.

1. Seleccione un perfil de prueba. Se muestra la oferta correspondiente al perfil seleccionado (una mujer).

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. Seleccione otros perfiles de prueba para previsualizar el contenido del correo electrónico de cada variante del mensaje. En el contenido del mensaje, ahora se muestra la oferta correspondiente al perfil de prueba seleccionado (ahora un hombre).

   ![](assets/deliver-offer-test-profile-male-preview.png)

Obtenga más información sobre los pasos detallados para comprobar la vista previa del mensaje en [esta sección](#preview-your-messages).

## Vídeo explicativo{#video-offers}

Aprenda a añadir un componente de Offer Decisioning a los mensajes en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
