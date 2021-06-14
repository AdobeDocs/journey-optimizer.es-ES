---
title: Crear decisiones
description: Aprenda a crear decisiones
feature: Ofertas
topic: Integraciones
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 4%

---

# Crear decisiones {#create-offer-activities}

Las decisiones (anteriormente conocidas como actividades de oferta) son contenedores para sus ofertas que aprovecharán el motor de decisión de ofertas para elegir la mejor oferta que se debe entregar, según el destinatario del envío.

![](../../assets/do-not-localize/how-to-video.png) [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de decisiones desde la pestaña **[!UICONTROL Offers]** menu / **[!UICONTROL Decisions]** . Los filtros están disponibles para ayudarle a recuperar las decisiones según su estado o las fechas de inicio y finalización.

![](../../assets/activities-list.png)

Antes de crear una decisión, asegúrese de que los componentes siguientes se hayan creado en la Biblioteca de ofertas:

* [Ubicaciones](../offer-library/creating-placements.md),
* [Colecciones](../offer-library/creating-collections.md),
* [Ofertas personalizadas](../offer-library/creating-personalized-offers.md),
* [Ofertas de reserva](../offer-library/creating-fallback-offers.md).

## Cree la decisión {#create-activity}

1. Acceda a la lista de decisiones y haga clic en **[!UICONTROL Create activity]**.

1. Especifique el nombre de la decisión, así como su fecha y hora de inicio y finalización y, a continuación, haga clic en **[!UICONTROL Next]**.

   ![](../../assets/activities-name.png)

## Agregar decisiones {#add-decisions}

1. Arrastre y suelte una ubicación de la lista para agregarla a la decisión y, a continuación, haga clic en **[!UICONTROL Add collection]**.

   ![](../../assets/activities-placement.png)

1. Seleccione la colección que contiene las ofertas que desea tener en cuenta y haga clic en **[!UICONTROL Add]**.

   ![](../../assets/activities-collection.png)

1. Las ofertas seleccionadas se añaden a la ubicación. En este ejemplo, seleccionamos dos ofertas que se mostrarán en una ubicación de tipo JSON con el fin de presentar ofertas en una solución de centro de llamadas.

   ![](../../assets/offers-added.png)

1. De forma predeterminada, si varias ofertas son elegibles para esta ubicación, las ofertas con la puntuación de prioridad más alta se entregarán al cliente.

   Si desea utilizar una fórmula específica para elegir qué oferta apta para entregar, seleccione una fórmula de clasificación en la lista desplegable **[!UICONTROL Rank offers by]**. Para obtener más información, consulte [esta sección](../offer-activities/configure-offer-selection.md).

1. El campo **[!UICONTROL Constraint]** restringe la selección de ofertas para esta ubicación. Esta restricción se puede aplicar utilizando una regla de decisión o uno o varios segmentos de Adobe Experience Platform.

   Para restringir la selección de ofertas a los miembros de un segmento de Adobe Experience Platform, seleccione **[!UICONTROL Segments]** y haga clic en **[!UICONTROL Add segments]**.

   ![](../../assets/activity_constraint_segment.png)

   Agregue uno o varios segmentos del panel izquierdo, combínelos con los operadores lógicos **[!UICONTROL And]** / **[!UICONTROL Or]** y haga clic en **[!UICONTROL Select]** para confirmar.

   Para obtener más información sobre cómo trabajar con segmentos, consulte la [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../../assets/activity_constraint_segment2.png)

   Si desea agregar una restricción de selección para esta ubicación mediante una regla de decisión, seleccione la opción **[!UICONTROL Decision rule]** y, a continuación, arrastre la regla deseada del panel izquierdo al área **[!UICONTROL Decision rule]**. Para obtener más información sobre cómo crear una regla de decisión, consulte [esta sección](../offer-library/creating-decision-rules.md).

   ![](../../assets/activity_constraint_rule.png)

## Agregar una oferta de reserva {#add-fallback}

Seleccione la oferta de reserva que se presentará como último recurso a los clientes que no coincidan con las reglas y restricciones de idoneidad de las ofertas y, a continuación, haga clic en **[!UICONTROL Next]**.

![](../../assets/add-fallback-offer.png)

## Revisar y guardar la decisión {#review}

Si todo está configurado correctamente y su decisión está lista para utilizarse para presentar ofertas a los clientes, haga clic en **[!UICONTROL Finish]** y seleccione **[!UICONTROL Save and activate]**.

También puede guardar la decisión como borrador para editarla y activarla más adelante.

![](../../assets/save-activities.png)

La decisión se muestra en la lista con los estados **[!UICONTROL Live]** o **[!UICONTROL Draft]**, dependiendo de si lo activó o no en el paso anterior.

Ahora está listo para utilizarse para ofrecer ofertas a los clientes. Puede seleccionarlo para mostrar sus propiedades y editarlo o suprimirlo.

Para obtener más información sobre la entrega de ofertas, consulte estas secciones:

* [Añadir ofertas personalizadas en mensajes](../../deliver-personalized-offers.md)
* [Enviar ofertas mediante API](../api-reference/decisions-api/deliver-offers.md)

![](../../assets/activities-created.png)

>[!NOTE]
>
>Una vez que se ha creado una decisión, puede hacer clic en su nombre en la lista para acceder a información detallada y visualizar todos los cambios que se le han realizado mediante la pestaña **[!UICONTROL Change log]** (consulte [Registro de cambios de ofertas y decisiones](../get-started/user-interface.md#changes-log)).

## Tutorial en vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
