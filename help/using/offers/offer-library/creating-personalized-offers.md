---
title: Creación de ofertas personalizadas
description: Obtenga información sobre cómo crear, configurar y administrar sus ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 83bb29b7026c90560ffdb961b03944d8f94c8a8c
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 5%

---

# Creación de ofertas personalizadas {#create-personalized-offers}

Antes de crear una oferta, asegúrese de que ha creado:

* A **placement** en el que se muestra la oferta. Consulte [Creación de ubicaciones](../offer-library/creating-placements.md)
* Si desea agregar una condición de elegibilidad: a **regla de decisión** que definirá la condición bajo la cual se presentará la oferta. Consulte [Crear reglas de decisión](../offer-library/creating-decision-rules.md).
* Uno o varios **etiquetas** que puede que desee asociar a la oferta. Consulte [Creación de etiquetas](../offer-library/creating-tags.md).

➡️ [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de ofertas personalizadas en la **[!UICONTROL Offers]** para abrir el Navegador.

![](../../assets/offers_list.png)

## Creación de la oferta {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="Acerca de los atributos de oferta"
>abstract="Con los atributos de oferta, puede asociar pares de valor clave con la oferta para realizar informes y análisis."
>additional-url="https://video.tv.adobe.com/v/329375" text="Ver vídeo de demostración"

Para crear un **oferta**, siga estos pasos:

1. Haga clic en **[!UICONTROL Create offer]** y, a continuación, seleccione **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. Especifique el nombre de la oferta, así como su fecha y hora de inicio y finalización. También puede asociar una o varias etiquetas existentes a la oferta, lo que le permite buscar y organizar la Biblioteca de ofertas con mayor facilidad.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >La variable **[!UICONTROL Offer attributes]** permite asociar pares de clave-valor con la oferta con fines de informes y análisis.

## Configuración de las representaciones de la oferta {#representations}

Una oferta se puede mostrar en diferentes lugares de un mensaje: en un banner superior con una imagen, como texto en un párrafo, como bloque de HTML, etc. Cuantas más representaciones tenga una oferta, más oportunidades habrá de utilizar la oferta en diferentes contextos de ubicación.

Para añadir una o varias representaciones a la oferta y configurarlas, siga los pasos a continuación.

1. Para la primera representación, comience por seleccionar la variable **[!UICONTROL Channel]** que se utilizará.

   ![](../../assets/channel-placement.png)

   >[!NOTE]
   >
   >Solo se muestran las ubicaciones disponibles para el canal seleccionado en la **[!UICONTROL Placement]** lista desplegable.


1. Seleccione una colocación de la lista.

   También puede utilizar el botón situado junto al **[!UICONTROL Placement]** lista desplegable para examinar todas las ubicaciones.

   ![](../../assets/browse-button-placements.png)

   Aquí todavía puede filtrar las ubicaciones según su canal o tipo de contenido. Elija una ubicación y haga clic en **[!UICONTROL Select]**.

   ![](../../assets/browse-placements.png)

1. Añada contenido a su representación. Obtenga información sobre cómo [esta sección](#content).

1. Al añadir contenido, como una imagen o una dirección URL, puede especificar un **[!UICONTROL Destination link]**: los usuarios que hacen clic en la oferta se dirigen a la página correspondiente.

   ![](../../assets/offer-destination-link.png)

1. Finalmente, seleccione el idioma que desee para ayudar a identificar y administrar lo que se mostrará a los usuarios.

1. Para añadir otra representación, utilice el **[!UICONTROL Add representation]** y añada tantas representaciones como sea necesario.

   ![](../../assets/offer-add-representation.png)

1. Una vez que haya añadido todas las representaciones, seleccione **[!UICONTROL Next]**.

## Definir contenido para las representaciones {#content}

Puede añadir diferentes tipos de contenido a una representación.

>[!NOTE]
>
>Solo está disponible el contenido correspondiente al tipo de contenido de la ubicación.

### Adición de imágenes {#images}

Si la ubicación seleccionada es de tipo imagen, puede añadir contenido proveniente del **Adobe Experience Cloud Asset** biblioteca, un repositorio centralizado de recursos proporcionado por [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Para trabajar con [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}, debe implementar [!DNL Assets Essentials] para su organización y asegúrese de que los usuarios forman parte de la **Usuarios consumidores de Assets Essentials** o/y **Usuarios de Assets Essentials** Perfiles de producto. Más información sobre [esta página](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

1. Elija la opción **[!UICONTROL Asset library]**.

1. Seleccione **[!UICONTROL Browse]**.

   ![](../../assets/offer-browse-asset-library.png)

1. Examine los recursos para seleccionar la imagen que desee

1. Haga clic en **[!UICONTROL Select]**.

   ![](../../assets/offer-select-asset.png)

### Agregar direcciones URL {#urls}

Para añadir contenido desde una ubicación pública externa, seleccione **[!UICONTROL URL]** y, a continuación, introduzca la dirección URL del contenido que desea añadir.

![](../../assets/offer-content-url.png)

### Agregar texto personalizado {#custom-text}

También puede insertar contenido de tipo texto al seleccionar una ubicación compatible.

1. Seleccione la opción **[!UICONTROL Custom]** y haga clic en **[!UICONTROL Add content]**.

   ![](../../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Esta opción no está disponible para ubicaciones de tipo imagen.

1. Escriba el texto que se mostrará en la oferta.

   ![](../../assets/offer-text-content.png)

   Puede personalizar el contenido mediante el Editor de expresiones. Más información sobre [personalización](../../personalization/personalize.md#use-expression-editor).

   ![](../../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Solo el **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** y **[!UICONTROL Helper functions]** las fuentes están disponibles para la gestión de decisiones.

## Agregar reglas y restricciones de idoneidad {#eligibility}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Acerca de las restricciones de oferta"
>abstract="Con las restricciones, se puede especificar cómo se prioriza la oferta y cómo se presenta al usuario en comparación con otras ofertas."
>additional-url="https://video.tv.adobe.com/v/329375" text="Ver vídeo de demostración"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Acerca de la idoneidad de la oferta"
>abstract="En esta sección, puede utilizar reglas de decisión para determinar qué usuarios son elegibles para la oferta."
>additional-url="https://video.tv.adobe.com/v/329373" text="Ver vídeo de demostración"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Acerca de la prioridad de las ofertas"
>abstract="En este campo, se puede especificar la configuración de prioridad de la oferta. Priority es un número que se usa para clasificar ofertas que cumplen con todas las restricciones, como elegibilidad, fechas y restricciones."
>additional-url="https://video.tv.adobe.com/v/329375" text="Ver vídeo de demostración"

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Acerca de la restricción de ofertas"
>abstract="En este campo, se puede especificar cuántas veces se puede presentar la oferta entre todos los usuarios."
>additional-url="https://video.tv.adobe.com/v/329375" text="Ver vídeo de demostración"

Las reglas y restricciones de idoneidad le permiten definir las condiciones en las que se mostrará una oferta.

1. Configure las variables **[!UICONTROL Offer eligibility]**.

   * De forma predeterminada, la variable **[!UICONTROL All visitors]** la opción de regla de decisión está seleccionada, lo que significa que cualquier perfil puede presentarse como oferta.

   * Puede limitar la presentación de la oferta a los miembros de uno o varios segmentos de Adobe Experience Platform. Para ello, active la variable **[!UICONTROL Visitors who fall into one or multiple segments]** , luego agregue uno o varios segmentos del panel izquierdo y combínelos usando la opción **[!UICONTROL And]** / **[!UICONTROL Or]** operadores lógicos.

      Para obtener más información sobre cómo trabajar con segmentos, consulte [esta página](../../segment/about-segments.md).

      ![](../../assets/offer-eligibility-segment.png)

   * Si desea asociar una regla de decisión específica a la oferta, seleccione **[!UICONTROL By defined decision rule]** y, a continuación, arrastre la regla que desee desde el panel izquierdo hasta la **[!UICONTROL Decision rule]** . Para obtener más información sobre cómo crear una regla de decisión, consulte [esta sección](../offer-library/creating-decision-rules.md).

      ![](../../assets/offer_rule.png)

      >[!CAUTION]
      >
      >Actualmente, las ofertas basadas en eventos no son compatibles con [!DNL Journey Optimizer]. Si crea una regla de decisión basada en un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, no podrá aprovecharlo en una oferta.
   Obtenga más información sobre el uso de segmentos frente a reglas de decisión en [esta sección](../offer-activities/create-offer-activities.md#segments-vs-decision-rules).

1. Defina el **[!UICONTROL Priority]** de la oferta comparada con otras si el usuario cumple los requisitos para más de una oferta. Cuanto mayor sea la prioridad de una oferta, mayor será su prioridad en comparación con otras ofertas.

1. Especifique los **[!UICONTROL Capping]**, es decir, el número de veces que la oferta se presentará en total entre todos los usuarios. Si la oferta se ha enviado a todos los usuarios la cantidad de veces que ha especificado en este campo, su entrega se detendrá.

   >[!NOTE]
   >
   >El número de veces que se propone una oferta se calcula en el momento de la preparación del correo electrónico. Por ejemplo, si prepara un mensaje de correo electrónico con una serie de ofertas, esos números se cuentan hasta el límite máximo, independientemente de si se envía o no el correo electrónico.
   >
   >Si se elimina una entrega por correo electrónico o si la preparación se realiza de nuevo antes de enviarse, el valor de límite de la oferta se actualiza automáticamente.

   ![](../../assets/offer_capping.png)

   En el ejemplo anterior:

   * La prioridad de la oferta se establece en &quot;50&quot;, lo que significa que la oferta se presentará antes que las ofertas con una prioridad entre 1 y 49, y después las que tengan una prioridad de al menos 51.
   * La oferta se tendrá en cuenta para los usuarios que coincidan únicamente con la regla de decisión &quot;Clientes de Lealtad Dorada&quot;.
   * La oferta se presenta solo una vez por usuario.

## Revisar la oferta {#review}

Una vez definidas las reglas y restricciones de idoneidad, se muestra un resumen de las propiedades de la oferta.

1. Asegúrese de que todo esté configurado correctamente.

1. Cuando la oferta esté lista para ser presentada a los usuarios, haga clic en **[!UICONTROL Finish]**.

1. Seleccione **[!UICONTROL Save and approve]**.

   ![](../../assets/offer_review.png)

   También puede guardar la oferta como borrador para editarla y aprobarla más adelante.

La oferta se muestra en la lista con la variable **[!UICONTROL Approved]** o **[!UICONTROL Draft]** , dependiendo de si lo aprobó o no en el paso anterior.

Ahora está listo para enviarse a los usuarios.

![](../../assets/offer_created.png)

## Lista de ofertas {#offer-list}

En la lista de ofertas, puede seleccionar la oferta para mostrar sus propiedades. También puede editarlo, cambiar su estado (**Borrador**, **Aprobado**, **Archivado**), duplicar la oferta o eliminarla.

![](../../assets/offer_created.png)

Seleccione el **[!UICONTROL Edit]** para volver al modo de edición de la oferta, donde puede modificar el [detalles](#create-offer), [representaciones](#representations), así como editar la variable [reglas y restricciones de elegibilidad](#eligibility).

Seleccione una oferta aprobada y haga clic en **[!UICONTROL Undo approve]** para volver a establecer el estado de la oferta en **[!UICONTROL Draft]**.

Para volver a establecer el estado en **[!UICONTROL Approved]**, seleccione el botón correspondiente que se muestra ahora.

![](../../assets/offer_approve.png)

La variable **[!UICONTROL More actions]** activa las acciones que se describen a continuación.

![](../../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**: crea una oferta con las mismas propiedades, representaciones, reglas de idoneidad y restricciones. De forma predeterminada, la nueva oferta tiene la variable **[!UICONTROL Draft]** estado.
* **[!UICONTROL Delete]**: elimina la oferta de la lista.

   >[!CAUTION]
   >
   >La oferta y su contenido ya no serán accesibles. Esta acción no se puede deshacer.
   >
   >Si la oferta se utiliza en una recopilación o una decisión, no se puede eliminar. Primero debe eliminar la oferta de cualquier objeto.

* **[!UICONTROL Archive]**: establece el estado de la oferta en **[!UICONTROL Archived]**. La oferta sigue estando disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. Solo puede duplicarlo o eliminarlo.

También puede eliminar o cambiar el estado de varias ofertas al mismo tiempo seleccionando las casillas de verificación correspondientes.

![](../../assets/offer_multiple-selection.png)

Si desea cambiar el estado de varias ofertas con estados diferentes, solo se cambiarán los estados relevantes.

![](../../assets/offer_change-status.png)

Una vez creada una oferta, puede hacer clic en su nombre desde la lista.

![](../../assets/offer_click-name.png)

Esto le permite acceder a información detallada de esa oferta. Seleccione el **[!UICONTROL Change log]** para [supervisar todos los cambios](../get-started/user-interface.md#monitoring-changes) que se han realizado en la oferta.

![](../../assets/offer_information.png)

## Tutorial en vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
