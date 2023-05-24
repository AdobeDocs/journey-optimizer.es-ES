---
title: Creación de ofertas personalizadas
description: Obtenga información sobre cómo crear, configurar y administrar sus ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 13%

---

# Creación de ofertas personalizadas {#create-personalized-offers}

Antes de crear una oferta, asegúrese de que ha creado lo siguiente:

* A **ubicación** en el que se mostrará la oferta. Consulte [Crear ubicaciones](../offer-library/creating-placements.md)
* Si desea añadir una condición de idoneidad: a **regla de decisión** que definirá la condición bajo la cual se presentará la oferta. Consulte [Creación de reglas de decisión](../offer-library/creating-decision-rules.md).
* Uno o varios **calificadores de colección** (anteriormente conocidas como &quot;etiquetas&quot;) que puede que desee asociar a la oferta. Consulte [Crear calificadores de colección](../offer-library/creating-tags.md).

➡️ [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de ofertas personalizadas en el **[!UICONTROL Ofertas]** menú.

![](../assets/offers_list.png)

## Crear una oferta {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="Acerca de los atributos de oferta"
>abstract="Con los atributos de oferta, puede asociar pares de valores clave con la oferta para realizar informes y análisis."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="Atributos de oferta"
>abstract="Con los atributos de oferta, puede asociar pares de valores clave con la oferta para realizar informes y análisis."

Para crear un **oferta**, siga estos pasos:

1. Clic **[!UICONTROL Crear oferta]**, luego seleccione **[!UICONTROL Oferta personalizada]**.

   ![](../assets/create_offer.png)

1. Especifique el nombre de la oferta, así como su fecha y hora de inicio y finalización. Fuera de estas fechas, el motor de decisión no selecciona la oferta.

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >La actualización de las fechas de inicio y finalización puede afectar al límite. [Más información](add-constraints.md#capping-change-date)

1. También puede asociar uno o varios existentes **[!UICONTROL calificadores de colección]** a la oferta, lo que le permite buscar y organizar la Biblioteca de ofertas más fácilmente. [Más información](creating-tags.md).

1. El **[!UICONTROL Atributos de oferta]** permite asociar pares de clave-valor con la oferta para fines de informes y análisis.

1. Para asignar etiquetas de uso de datos personalizadas o principales a la oferta, seleccione **[!UICONTROL Administrar acceso]**. [Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC)](../../administration/object-based-access.md)

   ![](../assets/offer_manage-access.png)

1. Añada representaciones para definir dónde se mostrará la oferta en el mensaje. [Más información](add-representations.md)

   ![](../assets/channel-placement.png)

1. Añada restricciones para definir las condiciones en las que se mostrará la oferta. [Más información](add-constraints.md)

   >[!NOTE]
   >
   >Al seleccionar segmentos o reglas de decisión, puede ver información sobre los perfiles cualificados estimados. Clic **[!UICONTROL Actualizar]** para actualizar los datos.
   >
   >Tenga en cuenta que las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto. Por ejemplo, una regla de idoneidad que requiere que el clima actual sea de ≥80 grados.

   ![](../assets/offer-constraints-example.png)

1. Revise y guarde la oferta. [Más información](#review)

## Revisión de la oferta {#review}

Una vez definidas las reglas de idoneidad y las restricciones, se muestra un resumen de las propiedades de la oferta.

1. Asegúrese de que todo está configurado correctamente.

1. Puede mostrar información sobre los perfiles cualificados estimados. Clic **[!UICONTROL Actualizar]** para actualizar los datos.

   ![](../assets/offer-summary-estimate.png)

1. Cuando la oferta esté lista para presentarse a los usuarios, haga clic en **[!UICONTROL Finalizar]**.

1. Seleccionar **[!UICONTROL Guardar y aprobar]**.

   ![](../assets/offer_review.png)

   También puede guardar la oferta como borrador para editarla y aprobarla más adelante.

La oferta se muestra en la lista con la variable **[!UICONTROL Aprobado]** o **[!UICONTROL Borrador]** estado, en función de si lo aprobó o no en el paso anterior.

Ahora está listo para entregarse a los usuarios.

![](../assets/offer_created.png)

## Administración de ofertas {#offer-list}

En la lista de oferta, se puede seleccionar la oferta para mostrar sus propiedades. También puede editarlo y cambiar su estado (**Borrador**, **Aprobado**, **Archivado**), duplique la oferta o elimínela.

![](../assets/offer_created.png)

Seleccione el **[!UICONTROL Editar]** para volver al modo de edición de la oferta, donde puede modificar la [detalles](#create-offer), [representaciones](#representations), así como editar el [reglas de elegibilidad y restricciones](#eligibility).

Seleccione una oferta aprobada y haga clic en **[!UICONTROL Deshacer aprobación]** para volver a establecer el estado de la oferta en **[!UICONTROL Borrador]**.

Para volver a establecer el estado en **[!UICONTROL Aprobado]**, seleccione el botón correspondiente que ahora se muestra.

![](../assets/offer_approve.png)

El **[!UICONTROL Más acciones]** habilita las acciones que se describen a continuación.

![](../assets/offer_more-actions.png)

* **[!UICONTROL Duplicar]**: crea una oferta con las mismas propiedades, representaciones, reglas de elegibilidad y restricciones. De forma predeterminada, la nueva oferta tiene el **[!UICONTROL Borrador]** estado.
* **[!UICONTROL Eliminar]**: elimina la oferta de la lista.

   >[!CAUTION]
   >
   >Ya no se podrá acceder a la oferta ni a su contenido. No se puede deshacer esta acción.
   >
   >Si la oferta se utiliza en una colección o una decisión, no se puede eliminar. Primero debe eliminar la oferta de cualquier objeto.

* **[!UICONTROL Archivar]**: establece el estado de la oferta en **[!UICONTROL Archivado]**. La oferta sigue estando disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Borrador]** o **[!UICONTROL Aprobado]**. Solo puede duplicarlo o eliminarlo.

También puede eliminar o cambiar el estado de varias ofertas al mismo tiempo seleccionando las casillas de verificación correspondientes.

![](../assets/offer_multiple-selection.png)

Si desea cambiar el estado de varias ofertas con diferentes estados, solo se cambiarán los estados relevantes.

![](../assets/offer_change-status.png)

Una vez creada una oferta, se puede hacer clic en su nombre desde la lista.

![](../assets/offer_click-name.png)

Esto le permite acceder a información detallada de esa oferta. Seleccione el **[!UICONTROL Registro de cambios]** pestaña a [monitorizar todos los cambios](../get-started/user-interface.md#monitoring-changes) que se han hecho a la oferta.

![](../assets/offer_information.png)

## Tutorial en vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
