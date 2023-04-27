---
solution: Journey Optimizer
product: journey optimizer
title: Adición de ofertas personalizadas
description: Aprenda a añadir ofertas personalizadas a los mensajes
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: ofertas, decisión, correos electrónicos, personalización, decisión
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Adición de ofertas personalizadas {#deliver-personalized-offers}

En [!DNL Journey Optimizer] correos electrónicos, puede insertar decisiones que aprovechen el motor de administración de decisiones para elegir la mejor oferta y enviarla a sus clientes.

Por ejemplo, puede agregar una decisión que muestre en el correo electrónico una oferta de descuento especial que variará según el nivel de lealtad del destinatario.

>[!IMPORTANT]
>
>Si se realizan cambios en una decisión de oferta que se está utilizando en el mensaje de un recorrido, debe cancelar la publicación del recorrido y volver a publicarlo.  Esto garantizará que los cambios se incorporen al mensaje del recorrido y que el mensaje sea coherente con las últimas actualizaciones.

* Para obtener más información sobre cómo crear y administrar ofertas, consulte [esta sección](../offers/get-started/starting-offer-decisioning.md).
* Para un **ejemplo completo de extremo a extremo** mostrar cómo configurar ofertas, utilizarlas en una decisión y aprovechar esta decisión en un correo electrónico, consulte [esta sección](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [Aprenda a añadir ofertas como personalización en este vídeo](#video-offers)

## Insertar una decisión en un correo electrónico {#insert-offers}

>[!CAUTION]
>
>Antes de empezar, debe [definir una decisión de oferta](../offers/offer-activities/create-offer-activities.md).

Para insertar una decisión en un mensaje de correo electrónico, siga los pasos a continuación:

1. Cree el correo electrónico y, a continuación, abra el Diseñador de correo electrónico para configurar su contenido.

1. Agregue un **[!UICONTROL Decisión de oferta]** componente de contenido.

   ![](assets/deliver-offer-component.png)

   Aprenda a utilizar los componentes de contenido en [esta sección](content-components.md).

1. La variable **[!UICONTROL Decisión de oferta]** aparece en la paleta derecha. Haga clic en **[!UICONTROL Seleccionar decisión de oferta]**:

   1. En la ventana que se muestra, seleccione la colocación correspondiente a las ofertas que desea mostrar.

      [Ubicaciones](../offers/offer-library/creating-placements.md) son contenedores que se utilizan para mostrar sus ofertas. En este ejemplo, utilizaremos la ubicación &quot;imagen superior del correo electrónico&quot;. Esta ubicación se ha creado en la Biblioteca de ofertas para mostrar las ofertas de tipo imagen situadas en la parte superior de los mensajes.

   1. Se muestran las decisiones que coinciden con la colocación seleccionada. Seleccione la decisión que desea utilizar en el componente de contenido y haga clic en **[!UICONTROL Agregar]**.

      >[!NOTE]
      >
      >En la lista solo se muestran las decisiones compatibles con la colocación seleccionada. En este ejemplo, solo una actividad de oferta coincide con la ubicación &quot;imagen superior del correo electrónico&quot;.

      ![](assets/deliver-offer-placement.png)

La decisión ahora se añade al componente. Después de guardar los cambios, las ofertas están listas para mostrarse en los perfiles relevantes al enviar el mensaje como parte de un recorrido.

>[!NOTE]
>
>Cuando se actualiza una oferta, una oferta de reserva, una recopilación de ofertas o una decisión de oferta a la que se hace referencia directa o indirectamente en el mensaje, las actualizaciones se reflejan automáticamente en el mensaje correspondiente.

## Vista previa de ofertas en un correo electrónico {#preview-offers-in-email}

Puede obtener una vista previa de las diferentes ofertas que forman parte de la decisión agregada al correo electrónico mediante la variable **[!UICONTROL Oferta]** o las flechas de los componentes de contenido.

![](assets/deliver-offer-preview.png)

Para mostrar las diferentes ofertas que forman parte de la decisión con un perfil de cliente, siga los pasos a continuación.

>[!NOTE]
>
>Debe tener perfiles de prueba disponibles para poder previsualizar los mensajes. Obtenga información sobre cómo [crear perfiles de prueba](../segment/creating-test-profiles.md).

1. Seleccione los perfiles de prueba que desea utilizar para obtener una vista previa de la oferta:

   1. Haga clic en el **[!UICONTROL Botón Simular contenido]** a continuación, elija el espacio de nombres que se utilizará para identificar los perfiles de prueba de la variable **[!UICONTROL Área de nombres de identidad]** campo .

      >[!NOTE]
      >
      >En este ejemplo, utilizamos la variable **Correo electrónico** espacio de nombres. Obtenga más información sobre las áreas de nombres de identidad de Adobe Experience Platform [en esta sección](../segment/get-started-identity.md).

   1. En el **[!UICONTROL Valor de identidad]** , introduzca el valor para identificar el perfil de prueba. En este ejemplo, introduzca la dirección de correo electrónico de un perfil de prueba.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. Añada otros perfiles para poder probar distintas variantes del mensaje según los datos del perfil.

      ![](assets/deliver-offer-test-profiles.png)


1. Haga clic en el **[!UICONTROL Vista previa]** para probar el mensaje y, a continuación, seleccione un perfil de prueba. Se muestra la oferta correspondiente al perfil seleccionado (una mujer).

   ![](assets/deliver-offer-test-profile-female-preview.png)

   Puede seleccionar otros perfiles de prueba para previsualizar el contenido del correo electrónico de cada variante del mensaje. En el contenido del mensaje, ahora se muestra la oferta correspondiente al perfil de prueba seleccionado (ahora un hombre).

Obtenga más información sobre los pasos detallados para comprobar la vista previa de los mensajes en [esta sección](#preview-your-messages).

## Vídeo explicativo{#video-offers}

Aprenda a añadir un componente de gestión de decisiones a los mensajes en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
