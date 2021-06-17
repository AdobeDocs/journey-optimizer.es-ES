---
title: Uso de ofertas personalizadas en un correo electrónico
description: Descubra un ejemplo completo que muestra todos los pasos necesarios para configurar ofertas y utilizarlas en un correo electrónico.
feature: Ofertas
topic: Integraciones
role: User
level: Intermediate
source-git-commit: a6a421fc23f4564bb24061c019c9418b491e7eee
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 4%

---

# Caso de uso: Configure ofertas personalizadas para utilizarlas en un correo electrónico {#configure-add-personalized-offers-email}

Esta sección presenta un ejemplo completo de cómo configurar ofertas y utilizarlas en un mensaje de correo electrónico, en función de una decisión que haya creado anteriormente.

## Pasos principales

A continuación se enumeran los pasos clave para configurar ofertas, incluirlas en una decisión y aprovechar esta decisión en un correo electrónico:

1. Antes de crear ofertas, [defina sus componentes](#define-components)

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

1. [Cree una ](#create-collection) colección para incluir las ofertas personalizadas que ha creado

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

## Defina los componentes {#define-components}

Antes de comenzar a crear ofertas, debe definir varios componentes que utilizará en las ofertas.

Los encontrará en **[!UICONTROL Decision Management]** > **[!UICONTROL Components menu]**.

1. Comience creando **ubicaciones** para sus ofertas.

   Se utilizan estas ubicaciones para definir dónde aparecerá la oferta resultante al definir la decisión de la oferta.

   En este ejemplo, cree tres ubicaciones con los siguientes tipos de contenido y canal:

   * *Web - Imagen*
   * *Correo electrónico: imagen*
   * *No digital: texto*

   ![](../assets/offers-e2e-placements.png)

   Los pasos detallados para crear ubicaciones se describen en [esta sección](../../using/offers/offer-library/creating-placements.md).

1. Cree **reglas de decisión**.

   Las reglas de decisión proporcionarán la mejor oferta a un perfil en Adobe Experience Platform.

   Configure dos reglas simples usando el atributo **[!UICONTROL XDM Individual Profile > Person > Gender]** :

   * *Clientes femeninos*
   * *Clientes masculinos*

   ![](../assets/offers-e2e-rules.png)

   Los pasos detallados para crear reglas se describen en [esta sección](../../using/offers/offer-library/creating-decision-rules.md).

1. También puede crear una etiqueta ****.

   A continuación, podrá asociarlo a sus ofertas y utilizar esta etiqueta para agrupar las ofertas en una colección.

   En este ejemplo, cree la etiqueta *Yoga*.

   ![](../assets/offers-e2e-tag.png)

   Los pasos detallados para crear etiquetas se describen en [esta sección](../../using/offers/offer-library/creating-tags.md).

1. Si desea definir reglas que determinen qué oferta debe presentarse primero para una ubicación determinada (en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas), puede crear una fórmula de **clasificación**.

   Los pasos detallados para crear fórmulas de clasificación se describen en [esta sección](../../using/offers/offer-library/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >En este ejemplo, solo utilizaremos las puntuaciones de prioridad. Obtenga más información sobre [reglas de idoneidad y restricciones](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).

## Configurar ofertas {#configure-offers}

Ahora puede crear y configurar sus ofertas. En este ejemplo, creará cuatro ofertas que desea mostrar según cada perfil específico.

1. Crear una oferta. Obtenga más información en [esta sección](../../using/offers/offer-library/creating-personalized-offers.md#create-offer).

1. En esta oferta, cree tres representaciones. Cada representación debe ser una combinación de una colocación que haya creado anteriormente y un recurso:

   * Uno correspondiente a la ubicación *Web - Imagen*
   * Uno correspondiente a la colocación *Email - Image*
   * Uno correspondiente a la colocación *No digital - Texto*

   >[!NOTE]
   >
   >Una oferta se puede mostrar en diferentes lugares de un mensaje para crear más oportunidades de utilizar la oferta en diferentes contextos de ubicación.

   Obtenga más información sobre las representaciones en [esta sección](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. Seleccione una imagen adecuada para las dos primeras ubicaciones. Introduzca texto personalizado para la colocación *No digital - Texto*.

   ![](../assets/offers-e2e-representations.png)

1. En la sección **[!UICONTROL Offer eligiblity]** , seleccione **[!UICONTROL By defined decision rule]** y arrastre y suelte la regla que desee.

   ![](../assets/offers-e2e-eligibility.png)

1. Complete el **[!UICONTROL Priority]**. En este ejemplo, agregue *25*.

1. Revise la oferta y haga clic en **[!UICONTROL Save and approve]**.

   ![](../assets/offers-e2e-review.png)

1. En este ejemplo, cree tres ofertas más con las mismas representaciones, pero diferentes recursos. Asignarlos con distintas reglas y prioridades, como:

   * Primera oferta: Regla de decisión: *Clientes mujeres*, Prioridad: *25*
   * Segunda oferta: Regla de decisión: *Clientes mujeres*, Prioridad: *15*
   * Tercera oferta: Regla de decisión: *Clientes masculinos*, prioridad: *25*
   * Cuarta oferta: Regla de decisión: *Clientes masculinos*, prioridad: *15*

   ![](../assets/offers-e2e-offers-created.png)

Los pasos detallados para crear y configurar ofertas se describen en [esta sección](../../using/offers/offer-library/creating-personalized-offers.md).

## Crear una oferta de reserva {#create-fallback}

1. Crear una oferta de reserva.

1. Defina las mismas representaciones que para las ofertas, con los recursos adecuados (deben ser diferentes de los utilizados en las ofertas).

   Cada representación debe ser una combinación de una colocación que haya creado anteriormente y un recurso:

   * Uno correspondiente a la ubicación *Web - Imagen*
   * Uno correspondiente a la colocación *Email - Image*
   * Uno correspondiente a la colocación *No digital - Texto*

   ![](../assets/offers-e2e-fallback-representations.png)

1. Revise la oferta de reserva y haga clic en **[!UICONTROL Save and approve]**.

![](../assets/offers-e2e-fallback.png)

La oferta de reserva ya está lista para utilizarse en una decisión.

Los pasos detallados para crear y configurar una oferta de reserva se describen en [esta sección](../../using/offers/offer-library/creating-fallback-offers.md).

## Crear una colección {#create-collection}

Al configurar la decisión, debe añadir las ofertas personalizadas como parte de una colección.

1. Para acelerar el proceso de decisión, cree una colección dinámica.

1. Utilice la etiqueta *Yoga* para seleccionar las cuatro ofertas personalizadas que creó anteriormente.

   ![](../assets/offers-e2e-collection-using-tag.png)

Los pasos detallados para crear una colección se describen en [esta sección](../../using/offers/offer-library/creating-collections.md).

## Configure la decisión {#configure-decision}

Ahora debe crear una decisión que combine ubicaciones con las ofertas personalizadas y la oferta de reserva que acaba de crear.

El motor de Offer decisioning utilizará esta combinación para encontrar la mejor oferta para un perfil específico: en este ejemplo, se basa en la regla de prioridad y decisión que asignó a cada oferta.

Para crear y configurar una decisión de oferta, siga los pasos principales a continuación:

1. Crear una decisión. Obtenga más información en [esta sección](../../using/offers/offer-activities/create-offer-activities.md#create-activity).

1. Seleccione las ubicaciones *Web - Image*, *Email - Image* y *Non-digital - Text*.

   ![](../assets/offers-e2e-decision-placements.png)

1. Para cada ubicación, agregue la colección que ha creado.

   ![](../assets/offers-e2e-decision-collection.png)

1. Si definió una clasificación al [crear los componentes](#define-components), puede asignarla a una ubicación en la decisión. Si varias ofertas son elegibles para presentarse en esta ubicación, la decisión utilizará esta fórmula para calcular qué oferta enviar primero.

   Los pasos detallados para asignar una fórmula de clasificación a una ubicación se describen en [esta sección](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. Seleccione la oferta de reserva que ha creado. Se muestra como una oferta de reserva disponible para las tres ubicaciones seleccionadas.

   ![](../assets/offers-e2e-decision-fallback.png)

1. Revise su decisión y haga clic en **[!UICONTROL Save and approve]**.

   ![](../assets/offers-e2e-review-decision.png)

Su decisión ya está lista para utilizarse para ofrecer ofertas optimizadas y personalizadas.

Los pasos detallados para crear y configurar una decisión se describen en [esta sección](../../using/offers/offer-activities/create-offer-activities.md).

## Inserte la decisión en un correo electrónico {#insert-decision-in-email}

Ahora que su decisión está activa, puede insertarla en un mensaje de correo electrónico. Para ello, siga los pasos a continuación:

1. Cree su correo electrónico y, a continuación, abra [Email Designer](../../using/design-emails.md) para configurar su contenido.

1. Añada un componente de estructura de la paleta izquierda.

1. Añada un componente de contenido **[!UICONTROL Offer decision]**. Aprenda a utilizar componentes de contenido en [esta sección](../../using/content-components.md).

   ![](../assets/offers-e2e-decision-component.png)

1. Selecciónelo. En la paleta derecha, haga clic en **[!UICONTROL Select offer decision]** para agregar una decisión.

   ![](../assets/offers-e2e-select-offer-decision.png)

1. Seleccione la colocación correspondiente a las ofertas que desee mostrar en la lista desplegable **[!UICONTROL Placements]**.

   En este caso, a partir de las ubicaciones que creó anteriormente como parte de este ejemplo, solo está disponible la ubicación **Email - Image** , ya que desea utilizar la decisión en un correo electrónico. Obtenga más información sobre la [creación de ubicaciones](../../using/offers/offer-library/creating-placements.md).

   ![](../assets/offers-e2e-select-placement-in-decision.png)

1. Se muestran las decisiones que coinciden con la colocación **Email - Image** . Seleccione la decisión que desea utilizar en el componente de contenido y haga clic en **[!UICONTROL Add]**.

   ![](../assets/offers-e2e-matching-placement-in-decision.png)

   >[!NOTE]
   >
   >En la lista solo se muestran las decisiones compatibles con la colocación seleccionada.

Ahora puede ver todas las ofertas personalizadas y la oferta de reserva visualizada en el Diseñador de correo electrónico.

![](../assets/offers-e2e-offers-displayed.png)

Utilice la sección **[!UICONTROL Offers]** o las flechas de los componentes de contenido (flechas derecha e izquierda) para examinar los datos. También puede mostrar las diferentes ofertas que forman parte de la decisión con un perfil de cliente. Obtenga más información en [esta sección](../../using/deliver-personalized-offers.md#preview-offers-in-email).

Después de guardar los cambios y una vez publicado el mensaje, las ofertas están listas para mostrarse a los perfiles relevantes al enviar el mensaje como parte de un recorrido.

**Temas relacionados:**

* Obtenga información sobre cómo comprobar la vista previa del mensaje en [esta sección](../../using/preview.md#preview-your-messages).

* Aprenda a publicar mensajes en [esta sección](../../using/publish-manage-message.md).

* Descubra cómo se activan los mensajes mediante uno o varios recorridos en [esta sección](../building-journeys/journey.md).

