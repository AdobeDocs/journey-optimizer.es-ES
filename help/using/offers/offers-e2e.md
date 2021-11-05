---
title: Uso de ofertas personalizadas en un correo electrónico
description: Descubra un ejemplo completo que muestra todos los pasos necesarios para configurar ofertas y utilizarlas en un correo electrónico.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 851d988a-2582-4c30-80f3-b881d90771be
source-git-commit: 8cb36038b2aeddd1662dcb7c84b36d9bc1265982
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 5%

---

# Caso de uso: Configurar ofertas personalizadas para utilizarlas en un correo electrónico {#configure-add-personalized-offers-email}

Esta sección presenta un ejemplo completo de cómo configurar ofertas y utilizarlas en un mensaje de correo electrónico, en función de una decisión que haya creado anteriormente.

## Pasos principales

A continuación se enumeran los pasos clave para configurar ofertas, incluirlas en una decisión y aprovechar esta decisión en un correo electrónico:

1. Antes de crear ofertas, [definir sus componentes](#define-components)

   * Crear ubicaciones
   * Crear reglas de decisión
   * Crear etiquetas
   * Crear clasificaciones (opcional)

1. [Configuración de las ofertas](#configure-offers)

   * Cree ofertas
   * Para cada oferta:

      * Cree representaciones y seleccione una colocación y un recurso para cada representación
      * Agregar una regla para cada oferta
      * Definir una prioridad para cada oferta

1. [Crear una oferta de reserva](#create-fallback)

1. [Crear una colección](#create-collection) para incluir las ofertas personalizadas que ha creado

1. [Configurar la decisión](#configure-decision)

   * Crear una decisión
   * Seleccione las ubicaciones que ha creado
   * Para cada ubicación, seleccione la colección
   * Para cada ubicación, seleccione una clasificación (opcional)
   * Seleccione la reserva

1. [Inserte la decisión en un correo electrónico](#insert-decision-in-email)

   * Seleccione una colocación que coincida con las ofertas que desee mostrar
   * Seleccione la decisión entre los elementos compatibles con la colocación seleccionada
   * Previsualizar las ofertas

El proceso general de gestión de decisiones para utilizar ofertas en un correo electrónico se puede describir de la siguiente manera:

![](../assets/offers-e2e-process.png)

## Definir los componentes {#define-components}

Antes de comenzar a crear ofertas, debe definir varios componentes que utilizará en las ofertas.

You will find them under the **[!UICONTROL Decision Management]** > **[!UICONTROL Components menu]**.

1. Start by creating **placements** for your offers.

   Se utilizan estas ubicaciones para definir dónde aparecerá la oferta resultante al definir la decisión de la oferta.

   En este ejemplo, cree tres ubicaciones con los siguientes tipos de contenido y canal:

   * *Web - Imagen*
   * *Correo electrónico: imagen*
   * *No digital: texto*

   ![](../assets/offers-e2e-placements.png)

   The detailed steps to create placements are described in [this section](../../using/offers/offer-library/creating-placements.md).

1. Crear **reglas de decisión**.

   Las reglas de decisión proporcionarán la mejor oferta a un perfil en Adobe Experience Platform.

   Configure dos reglas sencillas usando la variable **[!UICONTROL XDM Individual Profile > Person > Gender]** atributo:

   * *Clientes femeninos*
   * *Clientes masculinos*

   ![](../assets/offers-e2e-rules.png)

   Los pasos detallados para crear reglas se describen en [esta sección](../../using/offers/offer-library/creating-decision-rules.md).

1. También puede crear un **etiqueta**.

   A continuación, podrá asociarlo a sus ofertas y utilizar esta etiqueta para agrupar las ofertas en una colección.

   En este ejemplo, cree la variable *Yoga* etiqueta.

   ![](../assets/offers-e2e-tag.png)

   Los pasos detallados para crear etiquetas se describen en [esta sección](../../using/offers/offer-library/creating-tags.md).

1. Si desea definir reglas que determinen qué oferta debe presentarse primero para una ubicación determinada (en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas), puede crear una **fórmula de clasificación**.

   Los pasos detallados para crear fórmulas de clasificación se describen en [esta sección](../../using/offers/offer-library/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >En este ejemplo, solo utilizaremos las puntuaciones de prioridad. Más información sobre [reglas y restricciones de elegibilidad](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).

## Configurar ofertas {#configure-offers}

Ahora puede crear y configurar sus ofertas. In this example, you will create four offers that you want to display according to each specific profile.

1. Crear una oferta. Obtenga más información en [esta sección](../../using/offers/offer-library/creating-personalized-offers.md#create-offer).

1. In this offer, create three representations. Cada representación debe ser una combinación de una colocación que haya creado anteriormente y un recurso:

   * Uno correspondiente a la variable *Web - Imagen* placement
   * Uno correspondiente a la variable *Correo electrónico: imagen* placement
   * Uno correspondiente a la variable *No digital: texto* placement

   >[!NOTE]
   >
   >Una oferta se puede mostrar en diferentes lugares de un mensaje para crear más oportunidades de utilizar la oferta en diferentes contextos de ubicación.

   Obtenga más información sobre las representaciones en [esta sección](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. Seleccione una imagen adecuada para las dos primeras ubicaciones. Escriba texto personalizado para el *No digital: texto* ubicación.

   ![](../assets/offers-e2e-representations.png)

1. En el **[!UICONTROL Offer eligibility]** , seleccione **[!UICONTROL By defined decision rule]** y arrastre y suelte la regla que desee.

   ![](../assets/offers-e2e-eligibility.png)

1. Complete el **[!UICONTROL Priority]**. En este ejemplo, agregue *25*.

1. Revise la oferta y haga clic en **[!UICONTROL Save and approve]**.

   ![](../assets/offers-e2e-review.png)

1. En este ejemplo, cree tres ofertas más con las mismas representaciones, pero diferentes recursos. Asignarlos con distintas reglas y prioridades, como:

   * Primera oferta: Regla de decisión: *Clientes femeninos*, Prioridad: *25*
   * Segunda oferta: Regla de decisión: *Clientes femeninos*, Prioridad: *15*
   * Tercera oferta: Regla de decisión: *Clientes masculinos*, Prioridad: *25*
   * Cuarta oferta: Regla de decisión: *Clientes masculinos*, Prioridad: *15*

   ![](../assets/offers-e2e-offers-created.png)

Los pasos detallados para crear y configurar ofertas se describen en [esta sección](../../using/offers/offer-library/creating-personalized-offers.md).

## Crear una oferta de reserva {#create-fallback}

1. Crear una oferta de reserva.

1. Defina las mismas representaciones que para las ofertas, con los recursos adecuados (deben ser diferentes de los utilizados en las ofertas).

   Cada representación debe ser una combinación de una colocación que haya creado anteriormente y un recurso:

   * Uno correspondiente a la variable *Web - Imagen* placement
   * Uno correspondiente a la variable *Correo electrónico: imagen* placement
   * Uno correspondiente a la variable *No digital: texto* placement

   ![](../assets/offers-e2e-fallback-representations.png)

1. Revise la oferta de reserva y haga clic en **[!UICONTROL Save and approve]**.

![](../assets/offers-e2e-fallback.png)

La oferta de reserva ya está lista para utilizarse en una decisión.

Los pasos detallados para crear y configurar una oferta de reserva se describen en [esta sección](../../using/offers/offer-library/creating-fallback-offers.md).

## Crear una colección {#create-collection}

Al configurar la decisión, debe añadir las ofertas personalizadas como parte de una colección.

1. Para acelerar el proceso de decisión, cree una colección dinámica.

1. Utilice la variable *Yoga* para seleccionar las cuatro ofertas personalizadas que ha creado anteriormente.

   ![](../assets/offers-e2e-collection-using-tag.png)

Los pasos detallados para crear una colección se describen en [esta sección](../../using/offers/offer-library/creating-collections.md).

## Configurar la decisión {#configure-decision}

Ahora debe crear una decisión que combine ubicaciones con las ofertas personalizadas y la oferta de reserva que acaba de crear.

This combination will be used by the Offer Decisioning engine to find the best offer for a specific profile: in this example, it will be based on the priority and decision rule you assigned to each offer.

To create and configure an offer decision, follow the main steps below:

1. Crear una decisión. Obtenga más información en [esta sección](../../using/offers/offer-activities/create-offer-activities.md#create-activity).

1. Seleccione el *Web - Imagen*, *Correo electrónico: imagen* y *No digital: texto* ubicaciones.

   ![](../assets/offers-e2e-decision-placements.png)

1. For each placement, add the collection you created.

   ![](../assets/offers-e2e-decision-collection.png)

1. Si ha definido una clasificación cuando [creación de componentes](#define-components), puede asignarlo a una colocación en la decisión. Si se pueden presentar varias ofertas en esta ubicación, la decisión utilizará esta fórmula para calcular qué oferta enviar primero.

   Los pasos detallados para asignar una fórmula de clasificación a una ubicación se describen en [esta sección](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. Seleccione la oferta de reserva que ha creado. Se muestra como una oferta de reserva disponible para las tres ubicaciones seleccionadas.

   ![](../assets/offers-e2e-decision-fallback.png)

1. Revise su decisión y haga clic en **[!UICONTROL Save and approve]**.

   ![](../assets/offers-e2e-review-decision.png)

Su decisión ya está lista para utilizarse para ofrecer ofertas optimizadas y personalizadas.

Los pasos detallados para crear y configurar una decisión se describen en [esta sección](../../using/offers/offer-activities/create-offer-activities.md).

## Inserte la decisión en un correo electrónico {#insert-decision-in-email}

Ahora que su decisión está activa, puede insertarla en un mensaje de correo electrónico. Para ello, siga los pasos a continuación:

1. Cree su correo electrónico y, a continuación, abra el [Diseñador de correo electrónico](../../using/design-emails.md) para configurar su contenido.

1. Añada un componente de estructura de la paleta izquierda.

1. Agregue un **[!UICONTROL Offer decision]** componente de contenido. Learn how to use content components in [this section](../../using/content-components.md).

   ![](../assets/offers-e2e-decision-component.png)

1. Selecciónelo. En la paleta derecha, haga clic en **[!UICONTROL Select offer decision]** para agregar una decisión.

   ![](../assets/offers-e2e-select-offer-decision.png)

1. Select the placement corresponding to the offers that you want to display from the **[!UICONTROL Placements]** dropdown list.

   En este caso, a partir de las ubicaciones que creó anteriormente como parte de este ejemplo, solo la variable **Correo electrónico: imagen** la ubicación está disponible ya que desea utilizar la decisión en un mensaje de correo electrónico. Learn more on [creating placements](../../using/offers/offer-library/creating-placements.md).

   ![](../assets/offers-e2e-select-placement-in-decision.png)

1. Las decisiones que coinciden con la variable **Correo electrónico: imagen** se muestran. Seleccione la decisión que desea utilizar en el componente de contenido y haga clic en **[!UICONTROL Add]**.

   ![](../assets/offers-e2e-matching-placement-in-decision.png)

   >[!NOTE]
   >
   >Only decisions that are compatible with the selected placement display in the list.

Ahora puede ver todas las ofertas personalizadas y la oferta de reserva visualizada en el Diseñador de correo electrónico.

![](../assets/offers-e2e-offers-displayed.png)

Utilice la variable **[!UICONTROL Offers]** o las flechas de los componentes de contenido (flechas derecha e izquierda) para examinar los datos. También puede mostrar las diferentes ofertas que forman parte de la decisión con un perfil de cliente. Obtenga más información en [esta sección](../../using/deliver-personalized-offers.md#preview-offers-in-email).

Después de guardar los cambios y una vez publicado el mensaje, las ofertas están listas para mostrarse a los perfiles relevantes al enviar el mensaje como parte de un recorrido.

**Temas relacionados:**

* Obtenga información sobre cómo comprobar la vista previa del mensaje en [esta sección](../../using/preview.md#preview-your-messages).

* Obtenga información sobre cómo publicar mensajes en [esta sección](../../using/publish-manage-message.md).

* Obtenga información sobre cómo activan los mensajes uno o varios recorridos en [esta sección](../building-journeys/journey.md).

<!--
* Learn how to measure your offer's success and impact on your targeted audience with reports in [this section](../reports/journey-global-report.md).
-->


