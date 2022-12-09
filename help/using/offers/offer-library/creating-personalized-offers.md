---
title: Creación de ofertas personalizadas
description: Obtenga información sobre cómo crear, configurar y administrar sus ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 11596bfbe5f98e362224384d51ba32d61275bc1d
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# Creación de ofertas personalizadas {#create-personalized-offers}

Antes de crear una oferta, asegúrese de que ha creado:

* A **placement** en el que se muestra la oferta. Consulte [Creación de ubicaciones](../offer-library/creating-placements.md)
* Si desea agregar una condición de elegibilidad: a **regla de decisión** que definirá la condición bajo la cual se presentará la oferta. Consulte [Crear reglas de decisión](../offer-library/creating-decision-rules.md).
* Uno o varios **etiquetas** que puede que desee asociar a la oferta. Consulte [Creación de etiquetas](../offer-library/creating-tags.md).

➡️ [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de ofertas personalizadas en la **[!UICONTROL Offers]** para abrir el Navegador.

![](../assets/offers_list.png)

## Creación de una oferta {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="Acerca de los atributos de oferta"
>abstract="Con los atributos de oferta, puede asociar pares de valor clave con la oferta para realizar informes y análisis."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="Atributos de oferta"
>abstract="Con los atributos de oferta, puede asociar pares de valor clave con la oferta para realizar informes y análisis."

Para crear un **oferta**, siga estos pasos:

1. Haga clic en **[!UICONTROL Create offer]** y, a continuación, seleccione **[!UICONTROL Personalized offer]**.

   ![](../assets/create_offer.png)

1. Especifique el nombre de la oferta, así como su fecha y hora de inicio y finalización. Fuera de estas fechas, el motor de decisiones no selecciona la oferta.

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >La actualización de las fechas de inicio y finalización puede tener un impacto en el límite. [Más información](add-constraints.md#capping-change-date)

1. También puede asociar una o varias **[!UICONTROL tags]** a la oferta, lo que le permite buscar y organizar la biblioteca de ofertas con mayor facilidad. [Más información](creating-tags.md).

1. La variable **[!UICONTROL Offer attributes]** permite asociar pares de clave-valor con la oferta con fines de informes y análisis.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la oferta, seleccione **[!UICONTROL Manage access]**. [Más información sobre Control de acceso a nivel de objeto (OLAC)](../../administration/object-based-access.md)

   ![](../assets/offer_manage-access.png)

1. Añada representaciones para definir dónde se mostrará la oferta en el mensaje. [Más información](add-representations.md)

   ![](../assets/channel-placement.png)

1. Añada restricciones para establecer las condiciones de la oferta que se va a mostrar. [Más información](add-constraints.md)

   >[!NOTE]
   >
   >Al seleccionar segmentos o reglas de decisión, puede ver información sobre los perfiles cualificados estimados. Haga clic en **[!UICONTROL Refresh]** para actualizar los datos.
   >
   >Tenga en cuenta que las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como los datos de contexto. Por ejemplo, una regla de aceptación que requiera que el clima actual sea ≥ 80 grados.

   ![](../assets/offer-constraints-example.png)

1. Revise y guarde la oferta. [Más información](#review)

## Revisar la oferta {#review}

Una vez definidas las reglas y restricciones de idoneidad, se muestra un resumen de las propiedades de la oferta.

1. Asegúrese de que todo esté configurado correctamente.

1. Puede mostrar información sobre los perfiles cualificados estimados. Haga clic en **[!UICONTROL Refresh]** para actualizar los datos.

   ![](../assets/offer-summary-estimate.png)

1. Cuando la oferta esté lista para ser presentada a los usuarios, haga clic en **[!UICONTROL Finish]**.

1. Select **[!UICONTROL Save and approve]**.

   ![](../assets/offer_review.png)

   También puede guardar la oferta como borrador para editarla y aprobarla más adelante.

La oferta se muestra en la lista con la variable **[!UICONTROL Approved]** o **[!UICONTROL Draft]** , dependiendo de si lo aprobó o no en el paso anterior.

Ahora está listo para enviarse a los usuarios.

![](../assets/offer_created.png)

## Administrar ofertas {#offer-list}

En la lista de ofertas, puede seleccionar la oferta para mostrar sus propiedades. También puede editarlo, cambiar su estado (**Borrador**, **Aprobado**, **Archivado**), duplicar la oferta o eliminarla.

![](../assets/offer_created.png)

Seleccione el **[!UICONTROL Edit]** para volver al modo de edición de la oferta, donde puede modificar el [detalles](#create-offer), [representaciones](#representations), así como editar la variable [reglas y restricciones de elegibilidad](#eligibility).

Seleccione una oferta aprobada y haga clic en **[!UICONTROL Undo approve]** para volver a establecer el estado de la oferta en **[!UICONTROL Draft]**.

Para volver a establecer el estado en **[!UICONTROL Approved]**, seleccione el botón correspondiente que se muestra ahora.

![](../assets/offer_approve.png)

La variable **[!UICONTROL More actions]** activa las acciones que se describen a continuación.

![](../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**: crea una oferta con las mismas propiedades, representaciones, reglas de idoneidad y restricciones. De forma predeterminada, la nueva oferta tiene la variable **[!UICONTROL Draft]** estado.
* **[!UICONTROL Delete]**: elimina la oferta de la lista.

   >[!CAUTION]
   >
   >La oferta y su contenido ya no serán accesibles. Esta acción no se puede deshacer.
   >
   >Si la oferta se utiliza en una recopilación o una decisión, no se puede eliminar. Primero debe eliminar la oferta de cualquier objeto.

* **[!UICONTROL Archive]**: establece el estado de la oferta en **[!UICONTROL Archived]**. La oferta sigue estando disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. Solo puede duplicarlo o eliminarlo.

También puede eliminar o cambiar el estado de varias ofertas al mismo tiempo seleccionando las casillas de verificación correspondientes.

![](../assets/offer_multiple-selection.png)

Si desea cambiar el estado de varias ofertas con estados diferentes, solo se cambiarán los estados relevantes.

![](../assets/offer_change-status.png)

Una vez creada una oferta, puede hacer clic en su nombre desde la lista.

![](../assets/offer_click-name.png)

Esto le permite acceder a información detallada de esa oferta. Seleccione el **[!UICONTROL Change log]** para [supervisar todos los cambios](../get-started/user-interface.md#monitoring-changes) que se han realizado en la oferta.

![](../assets/offer_information.png)

## Tutorial en vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
