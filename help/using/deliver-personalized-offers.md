---
title: Añadir ofertas personalizadas
description: Aprenda a añadir ofertas personalizadas a los mensajes
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Añadir ofertas personalizadas {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## Acerca de la Administración de decisiones {#about-offer-decisioning}

Con [!DNL Journey Optimizer], puede insertar en sus mensajes de correo electrónico decisiones (anteriormente conocidas como actividades de oferta) que aprovecharán el motor de decisión de ofertas para elegir la mejor oferta que se debe entregar a sus clientes.

Por ejemplo, puede agregar una decisión que muestre en el correo electrónico una oferta de descuento especial que variará según el nivel de lealtad del destinatario.

Para obtener más información sobre cómo crear y administrar ofertas, consulte [esta sección](offers/get-started/starting-offer-decisioning.md).

## Inserte una decisión en un correo electrónico {#insert-offers}

Para insertar una decisión en un mensaje de correo electrónico, siga los pasos a continuación:

1. Cree el correo electrónico y, a continuación, abra el Diseñador de correo electrónico para configurar su contenido.

1. Añada un componente de contenido **[!UICONTROL Offer decision]** (consulte [Uso de componentes de contenido](content-components.md)).

   ![](assets/deliver-offer-component.png)

1. Se añade una pestaña **[!UICONTROL Offer decision]** al componente. Haga clic en **[!UICONTROL Add personalization - Offer decision]** para añadir una actividad de oferta.

   ![](assets/deliver-offer-tab.png)

1. Seleccione la colocación correspondiente a las ofertas que desee mostrar.

   Las ubicaciones son contenedores que se utilizan para mostrar las ofertas. En este ejemplo, utilizaremos la ubicación &quot;imagen superior del correo electrónico&quot;. Esta ubicación se ha creado en la Biblioteca de ofertas para mostrar las ofertas de tipo imagen situadas en la parte superior de los mensajes.

1. Seleccione la actividad de oferta que desea utilizar en el componente de contenido y haga clic en **[!UICONTROL Add]**.

   >[!NOTE]
   >
   >Tenga en cuenta que solo las decisiones compatibles con la colocación seleccionada se muestran en la lista. En este ejemplo, solo una actividad de oferta coincide con la ubicación &quot;imagen superior del correo electrónico&quot;.

   ![](assets/deliver-offer-placement.png)

1. La actividad de oferta ahora se agrega al componente. Puede obtener una vista previa de las diferentes ofertas que forman parte de la decisión mediante la sección **[!UICONTROL Offers]** o las flechas de los componentes de contenido.

   ![](assets/deliver-offer-preview.png)
