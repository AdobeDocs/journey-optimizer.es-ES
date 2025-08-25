---
solution: Journey Optimizer
product: journey optimizer
title: Añadir ofertas personalizadas
description: Aprenda a añadir ofertas personalizadas a los mensajes
feature: Email Design, Offers
topic: Content Management
role: User
level: Intermediate
keywords: ofertas, decisión, correos electrónicos, personalización, decisión
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# Añadir ofertas personalizadas {#deliver-personalized-offers}

En [!DNL Journey Optimizer] correos electrónicos, puede insertar decisiones que aprovecharán el motor de administración de decisiones para elegir la mejor oferta que se ofrezca a sus clientes.

Por ejemplo, puede añadir una decisión que muestre en el correo electrónico una oferta de descuento especial que variará según el nivel de lealtad del destinatario.

>[!IMPORTANT]
>
>Si se realizan cambios en una decisión de oferta que se utiliza en el mensaje de un recorrido, se debe cancelar la publicación del recorrido y volver a publicarlo.  Esto garantizará que los cambios se incorporen al mensaje del recorrido y que el mensaje sea coherente con las últimas actualizaciones.

* Para obtener más información sobre cómo crear y administrar ofertas, consulte [esta sección](../offers/get-started/starting-offer-decisioning.md).
* Para ver un **ejemplo completo de extremo a extremo** que muestra cómo configurar ofertas, utilícelas en una decisión y aproveche esta decisión en un correo electrónico, consulte [esta sección](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [Aprenda a agregar ofertas como personalización en este vídeo](#video-offers)

## Inserción de una decisión en un correo electrónico {#insert-offers}

>[!CAUTION]
>
>Antes de empezar, debe [definir una decisión de oferta](../offers/offer-activities/create-offer-activities.md).

Para insertar una decisión en un mensaje de correo electrónico, siga los pasos a continuación:

1. Cree su correo electrónico y, a continuación, abra la Designer de correo electrónico para configurar su contenido.

1. Agregar un componente de contenido **[!UICONTROL Offer decision]**.

   ![](assets/deliver-offer-component.png)

   Aprenda a utilizar los componentes de contenido en [esta sección](content-components.md).

1. La ficha **[!UICONTROL Decisión de oferta]** se muestra en la paleta derecha. Haga clic en **[!UICONTROL Seleccionar decisión de oferta]**:

   1. En la ventana que se muestra, seleccione la ubicación correspondiente a las ofertas que desea mostrar.

      [Las ubicaciones](../offers/offer-library/creating-placements.md) son contenedores que se usan para mostrar sus ofertas. En este ejemplo, utilizaremos la ubicación &quot;imagen superior de correo electrónico&quot;. Esta ubicación se ha creado en la Biblioteca de ofertas para mostrar las ofertas de tipo imagen situadas en la parte superior de los mensajes.

   1. Se muestran las decisiones que coinciden con la ubicación seleccionada. Seleccione la decisión que desea usar en el componente de contenido y haga clic en **[!UICONTROL Agregar]**.

      >[!NOTE]
      >
      >Solo se muestran en la lista las decisiones compatibles con la ubicación seleccionada. En este ejemplo, solo una actividad de oferta coincide con la ubicación &quot;imagen superior de correo electrónico&quot;.

      ![](assets/deliver-offer-placement.png)

La decisión se agrega ahora al componente. Después de guardar los cambios, las ofertas están listas para mostrarse en los perfiles relevantes al enviar el mensaje como parte de un recorrido.

>[!NOTE]
>
>Al actualizar una oferta, una oferta de reserva, una colección de ofertas o una decisión de oferta a la que se hace referencia directa o indirectamente en un mensaje, las actualizaciones se reflejan automáticamente en el mensaje correspondiente.

## Previsualización de ofertas en un correo electrónico {#preview-offers-in-email}

Puede obtener una vista previa de las diferentes ofertas que forman parte de la decisión agregada al correo electrónico mediante la sección **[!UICONTROL Oferta]** o las flechas de los componentes de contenido.

![](assets/deliver-offer-preview.png)

Para mostrar las diferentes ofertas que forman parte de la decisión con un perfil de cliente, siga los pasos a continuación.

1. Seleccione los perfiles de prueba que se utilizarán para previsualizar la oferta:

   1. Haga clic en el botón **[!UICONTROL Simular contenido]** y, a continuación, elija el área de nombres que se utilizará para identificar los perfiles de prueba del campo **[!UICONTROL Área de nombres de identidad]**.

      >[!NOTE]
      >
      >En este ejemplo, utilizamos el área de nombres **Email**. Obtenga más información acerca de las áreas de nombres de identidad de Adobe Experience Platform [en esta sección](../audience/get-started-identity.md).

   1. En el campo **[!UICONTROL Valor de identidad]**, ingrese el valor para identificar el perfil de prueba. En este ejemplo, introduzca la dirección de correo electrónico de un perfil de prueba.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. Añada otros perfiles para poder probar distintas variantes del mensaje según los datos del perfil.

      ![](assets/deliver-offer-test-profiles.png)

1. Haga clic en la ficha **[!UICONTROL Vista previa]** para probar el mensaje y, a continuación, seleccione un perfil de prueba. Se muestra la oferta correspondiente al perfil seleccionado (una mujer).

   ![](assets/deliver-offer-test-profile-female-preview.png)

   Puede seleccionar otros perfiles de prueba para previsualizar el contenido de correo electrónico de cada variante del mensaje. En el contenido del mensaje, ahora se muestra la oferta correspondiente al perfil de prueba seleccionado (ahora un hombre).

Obtenga más información acerca de los pasos detallados para comprobar la vista previa del mensaje en [esta sección](#preview-your-messages).

## Vídeo práctico{#video-offers}

Aprenda a agregar un componente de administración de decisiones a los mensajes de [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
