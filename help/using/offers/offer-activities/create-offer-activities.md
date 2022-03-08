---
title: Crear decisiones
description: Aprenda a crear decisiones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 1%

---

# Crear decisiones {#create-offer-activities}

Las decisiones (anteriormente conocidas como actividades de oferta) son contenedores para sus ofertas que aprovecharán el motor de decisión de ofertas para elegir la mejor oferta que se debe entregar, según el destinatario del envío.

➡️ [Descubra esta función en vídeo](#video)

La lista de decisiones puede consultarse en la **[!UICONTROL Offers]** menú > **[!UICONTROL Decisions]** pestaña . Los filtros están disponibles para ayudarle a recuperar las decisiones según su estado o las fechas de inicio y finalización.

![](../assets/activities-list.png)

Antes de crear una decisión, asegúrese de que los componentes siguientes se hayan creado en la Biblioteca de ofertas:

* [Ubicaciones](../offer-library/creating-placements.md)
* [Colecciones](../offer-library/creating-collections.md)
* [Ofertas personalizadas](../offer-library/creating-personalized-offers.md)
* [Ofertas de reserva](../offer-library/creating-fallback-offers.md)

## Cree la decisión {#create-activity}

1. Acceda a la lista de decisiones y haga clic en **[!UICONTROL Create decision]**.

1. Especifique el nombre de la decisión.

1. Defina una fecha y hora de inicio y de finalización si es necesario y haga clic en **[!UICONTROL Next]**.

   ![](../assets/activities-name.png)

## Definir ámbitos de decisión {#add-decision-scopes}

1. Seleccione una colocación en la lista desplegable. Se agregará al ámbito de la primera decisión en su decisión.

   ![](../assets/activities-placement.png)

1. Haga clic en **[!UICONTROL Add]** para seleccionar criterios de evaluación para esta ubicación.

   ![](../assets/activities-evaluation-criteria.png)

   Cada criterio consiste en una colección de ofertas asociada con una restricción de elegibilidad y un método de clasificación para determinar las ofertas que se mostrarán en la colocación.

   >[!NOTE]
   >
   >Se requiere al menos un criterio de evaluación.

1. Seleccione la colección de ofertas que contiene las ofertas que se deben tener en cuenta y haga clic en **[!UICONTROL Add]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >Puede hacer clic en el botón **[!UICONTROL Open offer collections]** vínculo para mostrar la lista de colecciones en una nueva pestaña, que le permite examinar las colecciones y las ofertas que contienen.

   La colección seleccionada se agrega al criterio.

   ![](../assets/activities-collection-added.png)

1. Utilice la variable **[!UICONTROL Eligibility]** para restringir la selección de ofertas para esta ubicación.

   Esta restricción se puede aplicar utilizando una **regla de decisión**, o una o varias **Segmentos de Adobe Experience Platform**. Ambas se detallan en [esta sección](#segments-vs-decision-rules).

   * Para restringir la selección de ofertas a los miembros de un segmento de Experience Platform, seleccione **[!UICONTROL Segments]** y haga clic en **[!UICONTROL Add segments]**.

      ![](../assets/activity_constraint_segment.png)

      Añada uno o varios segmentos del panel izquierdo y combínelos utilizando la variable **[!UICONTROL And]** / **[!UICONTROL Or]** operadores lógicos.

      ![](../assets/activity_constraint_segment2.png)

      Aprenda a trabajar con segmentos en [esta sección](../../segment/about-segments.md).

   * Si desea agregar una restricción de selección con una regla de decisión, utilice la variable **[!UICONTROL Decision rule]** y seleccione la regla que desee.

      ![](../assets/activity_constraint_rule.png)

      Obtenga información sobre cómo crear una regla de decisión en [esta sección](../offer-library/creating-decision-rules.md).

1. Defina el método de clasificación que desea utilizar para seleccionar la mejor oferta para cada perfil.

   ![](../assets/activity_ranking-method.png)

   * De forma predeterminada, si se cumplen los criterios de varias ofertas para esta ubicación, la oferta con la puntuación de prioridad más alta se envía al cliente.

   * Si desea utilizar una fórmula específica para elegir qué oferta apta para entregar, seleccione **[!UICONTROL Ranking formula]**. Aprenda a clasificar ofertas en [esta sección](../offer-activities/configure-offer-selection.md).

1. Haga clic en **[!UICONTROL Add]** para definir más criterios para la misma ubicación.

   ![](../assets/activity_add-collection.png)

1. Cuando agregue varios criterios, se evaluarán en un orden específico. La primera colección agregada a la secuencia se evaluará primero, y así sucesivamente.

   Para cambiar la secuencia predeterminada, puede arrastrar y soltar las colecciones para reordenarlas como desee.

   ![](../assets/activity_reorder-collections.png)

1. También puede evaluar varios criterios al mismo tiempo. Para ello, arrastre y suelte la colección sobre otra.

   ![](../assets/activity_move-collection.png)

   Ahora tienen la misma clasificación y, por lo tanto, se evaluarán al mismo tiempo.

   ![](../assets/activity_same-rank-collections.png)

1. Para añadir otra ubicación a las ofertas como parte de esta decisión, use el **[!UICONTROL New scope]** botón. Repita los pasos anteriores para cada ámbito de decisión.

   ![](../assets/activity_new-scope.png)

### Uso de segmentos frente a reglas de decisión {#segments-vs-decision-rules}

<!--to move to create-offers?-->

Para aplicar una restricción, puede restringir la selección de ofertas a los miembros de una o varias **Segmentos de Adobe Experience Platform** o puede usar un **regla de decisión**, ambas soluciones corresponden a diferentes usos.

Básicamente, el resultado de un segmento es una lista de perfiles, mientras que una regla de decisión es una función ejecutada bajo demanda contra un solo perfil durante el proceso de toma de decisiones. A continuación se detalla la diferencia entre estos dos usos.

* **Segmentos**

   Por un lado, los segmentos son un grupo de perfiles de Adobe Experience Platform que coinciden con una lógica determinada basada en atributos de perfil y eventos de experiencia. Sin embargo, Administración de ofertas no vuelve a calcular el segmento, el cual puede no estar actualizado al presentar la oferta.

   Obtenga más información sobre los segmentos en [esta sección](../../segment/about-segments.md).

* **Reglas de decisión**

   Por otro lado, una regla de decisión se basa en los datos disponibles en Adobe Experience Platform y determina a quién se puede mostrar una oferta. Una vez seleccionada en una oferta o una decisión para una ubicación determinada, la regla se ejecuta cada vez que se toma una decisión, lo que garantiza que cada perfil obtenga la oferta más reciente y la mejor.

   Obtenga más información sobre las reglas de decisión en [esta sección](../offer-library/creating-decision-rules.md).

## Añadir una oferta de reserva {#add-fallback}

Una vez definidos los ámbitos de decisión, defina la oferta de reserva que se presentará como último recurso a los clientes que no coincidan con las reglas y restricciones de idoneidad de las ofertas.

Para ello, selecciónela en la lista de ofertas de reserva disponibles para las ubicaciones definidas en la decisión y, a continuación, haga clic en **[!UICONTROL Next]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>Puede hacer clic en el botón **[!UICONTROL Open offer library]** para mostrar la lista de ofertas en una nueva pestaña.

## Revisar y guardar la decisión {#review}

Si todo está configurado correctamente, se muestra un resumen de las propiedades de decisión.

1. Asegúrese de que la decisión esté lista para utilizarse para presentar ofertas a los clientes. Se muestran todos los ámbitos de decisión y la oferta de reserva que contiene.

   ![](../assets/review-decision.png)

   Puede expandir o contraer cada ubicación. También puede obtener una vista previa de las ofertas disponibles, los requisitos y los detalles de clasificación de cada ubicación.

   ![](../assets/review-decision-details.png)

1. Haga clic en **[!UICONTROL Finish]**.
1. Seleccione **[!UICONTROL Save and activate]**.

   ![](../assets/save-activities.png)

   También puede guardar la decisión como borrador para editarla y activarla más adelante.

La decisión se muestra en la lista con la variable **[!UICONTROL Live]** o **[!UICONTROL Draft]** , dependiendo de si lo activó o no en el paso anterior.

Ahora está listo para utilizarse para ofrecer ofertas a los clientes.

## Lista de decisiones {#decision-list}

En la lista de decisión, puede seleccionar la decisión para mostrar sus propiedades. Desde allí también puede editarlo, cambiar su estado (**Borrador**, **Activo**, **Completar**, **Archivado**), duplicar la decisión o eliminarla.

![](../assets/decision_created.png)

Seleccione el **[!UICONTROL Edit]** para volver al modo de edición de decisiones, donde puede modificar el [detalles](#create-activity), [ámbitos de decisión](#add-decision-scopes) y [oferta de reserva](#add-fallback).

Seleccione una decisión activa y haga clic en **[!UICONTROL Deactivate]** para volver a establecer el estado de decisión en **[!UICONTROL Draft]**.

Para volver a establecer el estado en **[!UICONTROL Live]**, seleccione **[!UICONTROL Activate]** que se muestra ahora.

![](../assets/decision_activate.png)

La variable **[!UICONTROL More actions]** activa las acciones que se describen a continuación.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**: establece el estado de la decisión en **[!UICONTROL Complete]**, lo que significa que la decisión ya no se puede invocar. Esta acción solo está disponible para decisiones activadas. La decisión sigue estando disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. Solo puede duplicarlo, eliminarlo o archivarlo.

* **[!UICONTROL Duplicate]**: crea una decisión con las mismas propiedades, ámbitos de decisión y oferta de reserva. De forma predeterminada, la nueva decisión tiene la variable **[!UICONTROL Draft]** estado.

* **[!UICONTROL Delete]**: elimina la decisión de la lista.

   >[!CAUTION]
   >
   >La decisión y su contenido ya no serán accesibles. Esta acción no se puede deshacer.
   >
   >Si la decisión se utiliza en otro objeto, no se puede eliminar.

* **[!UICONTROL Archive]**: establece el estado de decisión en **[!UICONTROL Archived]**. La decisión sigue estando disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. Solo puede duplicarlo o eliminarlo.

También puede eliminar o cambiar el estado de varias decisiones al mismo tiempo seleccionando las casillas de verificación correspondientes.

![](../assets/decision_multiple-selection.png)

Si desea cambiar el estado de varias decisiones con estados diferentes, solo se cambiarán los estados relevantes.

![](../assets/decision_change-status.png)

Una vez creada la decisión, puede hacer clic en su nombre desde la lista.

![](../assets/decision_click-name.png)

Esto le permite acceder a información detallada para esa decisión. Seleccione el **[!UICONTROL Change log]** para [supervisar todos los cambios](../get-started/user-interface.md#changes-log) que se hayan adoptado en la decisión.

![](../assets/decision_information.png)

## Tutorial en vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
