---
title: Crear decisiones
description: Aprenda a crear decisiones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 89e0223ebbf5015b61b55da693e0c6401307ce9f
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 3%

---

# Crear decisiones {#create-offer-activities}

Las decisiones (anteriormente conocidas como actividades de oferta) son contenedores para sus ofertas que aprovecharán el motor de decisión de ofertas para elegir la mejor oferta que se debe entregar, según el destinatario del envío.

➡️ [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de decisiones desde la pestaña **[!UICONTROL Offers]** menu > **[!UICONTROL Decisions]** . Los filtros están disponibles para ayudarle a recuperar las decisiones según su estado o las fechas de inicio y finalización.

![](../../assets/activities-list.png)

Antes de crear una decisión, asegúrese de que los componentes siguientes se hayan creado en la Biblioteca de ofertas:

* [Ubicaciones](../offer-library/creating-placements.md)
* [Colecciones](../offer-library/creating-collections.md)
* [Ofertas personalizadas](../offer-library/creating-personalized-offers.md)
* [Ofertas de reserva](../offer-library/creating-fallback-offers.md)

## Cree la decisión {#create-activity}

1. Acceda a la lista de decisiones y haga clic en **[!UICONTROL Create decision]**.

1. Especifique el nombre de la decisión.

1. Defina una fecha y hora de inicio y finalización y haga clic en **[!UICONTROL Next]**.

   ![](../../assets/activities-name.png)

## Agregar ámbitos de decisión {#add-decision-scopes}

1. Arrastre y suelte una ubicación de la lista para agregarla a la decisión y, a continuación, haga clic en **[!UICONTROL Add collection]**.

   ![](../../assets/activities-placement.png)

   >[!NOTE]
   >
   >La misma ubicación se puede seleccionar varias veces en la decisión.

1. Seleccione la colección que contiene las ofertas que desea tener en cuenta y haga clic en **[!UICONTROL Add]**.

   ![](../../assets/activities-collection.png)

1. Las ofertas seleccionadas se añaden a la ubicación.

   En este ejemplo, seleccionamos dos ofertas que se mostrarán en una ubicación de tipo JSON con el fin de presentar ofertas en una solución de centro de llamadas.

   ![](../../assets/offers-added.png)

1. De forma predeterminada, si varias ofertas son elegibles para esta ubicación, las ofertas con la puntuación de prioridad más alta se entregarán al cliente.

   Si desea utilizar una fórmula específica o una estrategia de clasificación para elegir qué oferta apta para publicar, seleccione una fórmula de clasificación en la lista desplegable **[!UICONTROL Rank offers by]**. Para obtener más información, consulte [esta sección](../offer-activities/configure-offer-selection.md).

1. El campo **[!UICONTROL Constraint]** restringe la selección de ofertas para esta ubicación. Esta restricción se puede aplicar utilizando una **regla de decisión**, o uno o varios **segmentos de Adobe Experience Platform**. Ambas se detallan en [esta sección](#segments-vs-decision-rules).

   * Para restringir la selección de ofertas a los miembros de un segmento de Adobe Experience Platform, seleccione **[!UICONTROL Segments]** y haga clic en **[!UICONTROL Add segments]**.

      ![](../../assets/activity_constraint_segment.png)

      Agregue uno o varios segmentos del panel izquierdo, combínelos con los operadores lógicos **[!UICONTROL And]** / **[!UICONTROL Or]** y haga clic en **[!UICONTROL Select]** para confirmar.

      ![](../../assets/activity_constraint_segment2.png)

      Obtenga más información sobre cómo trabajar con segmentos en [esta sección](../../segment/about-segments.md).

   * Si desea agregar una restricción de selección para esta ubicación mediante una regla de decisión, seleccione la opción **[!UICONTROL Decision rule]** y, a continuación, arrastre la regla deseada del panel izquierdo al área **[!UICONTROL Decision rule]**.

      ![](../../assets/activity_constraint_rule.png)

      Obtenga más información sobre cómo crear una regla de decisión en [esta sección](../offer-library/creating-decision-rules.md).

### Uso de segmentos frente a reglas de decisión {#segments-vs-decision-rules}

<!--to move to create-offers?-->

Para aplicar una restricción, puede restringir la selección de ofertas a los miembros de uno o varios **segmentos de Adobe Experience Platform**, o puede utilizar una **regla de decisión**, ambas soluciones correspondientes a diferentes usos.

Básicamente, el resultado de un segmento es una lista de perfiles, mientras que una regla de decisión es una función ejecutada bajo demanda contra un solo perfil durante el proceso de toma de decisiones. A continuación se detalla la diferencia entre estos dos usos.

* **Segmentos**

   Por un lado, los segmentos son un grupo de perfiles de Adobe Experience Platform que coinciden con una lógica determinada basada en atributos de perfil y eventos de experiencia. Sin embargo, Administración de ofertas no vuelve a calcular el segmento, el cual puede no estar actualizado al presentar la oferta.

   Obtenga más información sobre los segmentos en [esta sección](../../segment/about-segments.md).

* **Reglas de decisión**

   Por otro lado, una regla de decisión se basa en los datos disponibles en Adobe Experience Platform y determina a quién se puede mostrar una oferta. Una vez seleccionada en una oferta o una decisión para una ubicación determinada, la regla se ejecuta cada vez que se toma una decisión, lo que garantiza que cada perfil obtenga la oferta más reciente y la mejor.

   Obtenga más información sobre las reglas de decisión en [esta sección](../offer-library/creating-decision-rules.md).

## Añadir una oferta de reserva {#add-fallback}

Seleccione la oferta de reserva que se presentará como último recurso a los clientes que no coincidan con las reglas y restricciones de idoneidad de las ofertas y, a continuación, haga clic en **[!UICONTROL Next]**.

![](../../assets/add-fallback-offer.png)

## Revisar y guardar la decisión {#review}

Si todo está configurado correctamente, se muestra un resumen de las propiedades de decisión.

1. Asegúrese de que la decisión esté lista para utilizarse para presentar ofertas a los clientes.
1. Haga clic en **[!UICONTROL Finish]**.
1. A continuación, seleccione **[!UICONTROL Save and activate]**.

   ![](../../assets/save-activities.png)

   También puede guardar la decisión como borrador para editarla y activarla más adelante.

La decisión se muestra en la lista con los estados **[!UICONTROL Live]** o **[!UICONTROL Draft]**, dependiendo de si lo activó o no en el paso anterior.

Ahora está listo para utilizarse para ofrecer ofertas a los clientes.

## Lista de decisiones {#decision-list}

En la lista de decisión, puede seleccionar la decisión para mostrar sus propiedades. Desde allí también puede editarlo, cambiar su estado (**Borrador**, **Activo**, **Completado**, **Archivado**), duplicar la decisión o eliminarla.

![](../../assets/decision_created.png)

Seleccione el botón **[!UICONTROL Edit]** para volver al modo de edición de decisión, donde puede modificar los [detalles](#create-activity), [ámbitos de decisión](#add-decision-scopes) y [oferta de reserva](#add-fallback) de la decisión.

Seleccione una decisión activa y haga clic en **[!UICONTROL Deactivate]** para volver a establecer el estado de la decisión en **[!UICONTROL Draft]**.

Para volver a establecer el estado en **[!UICONTROL Live]**, seleccione el botón **[!UICONTROL Activate]** que se muestra ahora.

![](../../assets/decision_activate.png)

El botón **[!UICONTROL More actions]** habilita las acciones descritas a continuación.

![](../../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**: establece el estado de la decisión en  **[!UICONTROL Complete]**, lo que significa que ya no se puede llamar a la decisión. Esta acción solo está disponible para decisiones activadas. La decisión sigue estando disponible en la lista, pero no puede volver a establecerse en **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. Solo puede duplicarlo, eliminarlo o archivarlo.

* **[!UICONTROL Duplicate]**: crea una decisión con las mismas propiedades, ámbitos de decisión y oferta de reserva. De forma predeterminada, la nueva decisión tiene el estado **[!UICONTROL Draft]**.

* **[!UICONTROL Delete]**: elimina la decisión de la lista.

   >[!CAUTION]
   >
   >La decisión y su contenido ya no serán accesibles. Esta acción no se puede deshacer.
   >
   >Si la decisión se utiliza en otro objeto, no se puede eliminar.

* **[!UICONTROL Archive]**: establece el estado de decisión en  **[!UICONTROL Archived]**. La decisión sigue estando disponible en la lista, pero no puede volver a establecerse en **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. Solo puede duplicarlo o eliminarlo.

También puede eliminar o cambiar el estado de varias decisiones al mismo tiempo seleccionando las casillas de verificación correspondientes.

![](../../assets/decision_multiple-selection.png)

Si desea cambiar el estado de varias decisiones con estados diferentes, solo se cambiarán los estados relevantes.

![](../../assets/decision_change-status.png)

Una vez creada la decisión, puede hacer clic en su nombre desde la lista.

![](../../assets/decision_click-name.png)

Esto le permite acceder a información detallada para esa decisión. Seleccione la pestaña **[!UICONTROL Change log]** para [supervisar todos los cambios](../get-started/user-interface.md#changes-log) que se han realizado en la decisión.

![](../../assets/decision_information.png)

## Tutorial en vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
