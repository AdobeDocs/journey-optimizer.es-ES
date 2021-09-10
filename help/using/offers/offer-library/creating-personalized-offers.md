---
title: Crear ofertas personalizadas
description: Aprenda a crear ofertas personalizadas en Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 024a450724aecfde0eab7ab97421052a0aa99f2e
workflow-type: tm+mt
source-wordcount: '1278'
ht-degree: 3%

---

# Crear ofertas personalizadas {#creating-personalized-offers}

Antes de crear una oferta, asegúrese de que ha creado:

* Una **ubicación** en la que se mostrará la oferta. Consulte [Crear ubicaciones](../offer-library/creating-placements.md)
* Una **regla de decisión** que definirá la condición bajo la cual se presentará la oferta. Consulte [Crear reglas de decisión](../offer-library/creating-decision-rules.md).
* Una o varias **etiquetas** que desea asociar a la oferta. Consulte [Crear etiquetas](../offer-library/creating-tags.md).

➡️ [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de ofertas personalizadas en el menú **[!UICONTROL Offers]** .

![](../../assets/offers_list.png)

## Creación de la oferta {#create-offer}

Para crear una **oferta**, siga estos pasos:

1. Haga clic en **[!UICONTROL Create offer]** y, a continuación, seleccione **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. Especifique el nombre de la oferta, así como su fecha y hora de inicio y finalización. También puede asociar una o varias etiquetas existentes a la oferta, lo que le permite buscar y organizar la Biblioteca de ofertas con mayor facilidad.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >La sección **[!UICONTROL Offer attributes]** permite asociar pares clave-valor con la oferta con fines de informes y análisis.

## Configuración de las representaciones de la oferta {#representations}

Una oferta se puede mostrar en diferentes lugares de un mensaje: en un banner superior con una imagen, como texto en un párrafo, como un bloque HTML, etc. Cuantas más representaciones tenga una oferta, más oportunidades habrá de utilizar la oferta en diferentes contextos de ubicación.

Para añadir una o varias representaciones a la oferta y configurarlas, siga los pasos a continuación.

1. Para la primera representación, comience por seleccionar el **[!UICONTROL Channel]** que se utilizará.

   ![](../../assets/channel-placement.png)

   En la lista desplegable **[!UICONTROL Placement]** solo se muestran las ubicaciones disponibles para el canal seleccionado.

1. Seleccione una colocación de la lista o utilice el botón situado junto a la lista desplegable **[!UICONTROL Placement]** para examinar todas las ubicaciones.

   ![](../../assets/browse-button-placements.png)

   Aquí todavía puede filtrar las ubicaciones según su canal o tipo de contenido. Elija una ubicación y haga clic en **[!UICONTROL Select]**.

   ![](../../assets/browse-placements.png)

1. Añada contenido a su representación.

   >[!NOTE]
   >
   >Solo está disponible el contenido correspondiente al tipo de contenido de la ubicación.

   * Si la ubicación seleccionada es de tipo imagen, puede añadir contenido proveniente de la biblioteca de recursos de Adobe Experience Cloud, un repositorio centralizado de recursos proporcionado por [!DNL Adobe Experience Manager Assets Essentials].

      >[!NOTE]
      >
      > Para trabajar con [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}, debe implementar [!DNL Assets Essentials] en su organización y asegurarse de que los usuarios forman parte de los **Usuarios de consumidores de Assets Essentials** o **Usuarios de Assets Essentials** perfiles de producto. Obtenga más información sobre [esta página](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

      Elija la opción **[!UICONTROL Asset library]** y seleccione **[!UICONTROL Browse]**.

      ![](../../assets/offer-browse-asset-library.png)

      Examine los recursos para seleccionar la imagen que desee y haga clic en **[!UICONTROL Select]**.

      ![](../../assets/offer-select-asset.png)

   * Para añadir contenido desde una ubicación pública externa, seleccione **[!UICONTROL URL]** e introduzca la dirección URL del contenido que desea añadir.

      ![](../../assets/offer-content-url.png)

   * También puede insertar contenido de tipo texto al seleccionar una ubicación compatible. Seleccione la opción **[!UICONTROL Custom]** y escriba el texto que aparecerá en la oferta.

      ![](../../assets/offer-text-content.png)

      >[!NOTE]
      >
      >Esta opción no está disponible para ubicaciones de tipo imagen.

1. Cuando agrega contenido, como una imagen o URL, puede especificar un **[!UICONTROL Destination link]**: los usuarios que hacen clic en la oferta se dirigen a la página correspondiente.

   ![](../../assets/offer-destination-link.png)

1. Finalmente, seleccione el idioma que desee para ayudar a identificar y administrar lo que se mostrará a los usuarios.

1. Para añadir otra representación, utilice el botón **[!UICONTROL Add representation]** y añada tantas representaciones como sea necesario.

   ![](../../assets/offer-add-representation.png)

1. Una vez agregadas todas las representaciones, seleccione **[!UICONTROL Next]**.

## Agregar reglas y restricciones de idoneidad {#eligibility}

Las reglas y restricciones de idoneidad le permiten definir las condiciones en las que se mostrará una oferta.

1. Configure el **[!UICONTROL Offer eligibility]**. De forma predeterminada, la opción **[!UICONTROL All visitors]** regla de decisión está seleccionada, lo que significa que cualquier perfil podrá presentarse en la oferta.

   Puede limitar la presentación de la oferta a los miembros de uno o varios segmentos de Adobe Experience Platform. Para ello, active la opción **[!UICONTROL Visitors who fall into one or multiple segments]**, luego agregue uno o varios segmentos del panel izquierdo y combínelos utilizando los operadores lógicos **[!UICONTROL And]** / **[!UICONTROL Or]**.

   Para obtener más información sobre cómo trabajar con segmentos, consulte [esta página](../../segment/about-segments.md).

   ![](../../assets/offer-eligibility-segment.png)

   Si desea asociar una regla de decisión específica a la oferta, seleccione **[!UICONTROL By defined decision rule]** y, a continuación, arrastre la regla que desee del panel izquierdo al área **[!UICONTROL Decision rule]**. Para obtener más información sobre cómo crear una regla de decisión, consulte [esta sección](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

   >[!CAUTION]
   >
   >Actualmente, las ofertas basadas en eventos no son compatibles con [!DNL Journey Optimizer]. Si crea una regla de decisión basada en un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, no podrá aprovecharla en una oferta.

1. Defina el **[!UICONTROL Priority]** de la oferta comparado con otros si el usuario cumple los requisitos para más de una oferta. Cuanto mayor sea la prioridad de una oferta, mayor será su prioridad en comparación con otras ofertas.

1. Especifique el **[!UICONTROL Capping]** de la oferta, lo que significa el número de veces que la oferta se presentará en total entre todos los usuarios. Si la oferta se ha enviado a todos los usuarios la cantidad de veces que ha especificado en este campo, su entrega se detendrá.

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

La oferta se muestra en la lista con los estados **[!UICONTROL Approved]** o **[!UICONTROL Draft]**, en función de si la aprobó o no en el paso anterior.

Ahora está listo para enviarse a los usuarios.

![](../../assets/offer_created.png)

## Lista de ofertas {#offer-list}

En la lista de ofertas, puede seleccionar la oferta para mostrar sus propiedades. También puede editarlo, cambiar su estado (**Borrador**, **Aprobado**, **Archivado**), duplicar la oferta o eliminarla.

![](../../assets/offer_created.png)

Seleccione el botón **[!UICONTROL Edit]** para volver al modo de edición de la oferta, donde puede modificar los [detalles](#create-offer), [representaciones](#representations) de la oferta, así como editar las [reglas de idoneidad y restricciones](#eligibility).

Seleccione una oferta aprobada y haga clic en **[!UICONTROL Undo approve]** para volver a establecer el estado de la oferta en **[!UICONTROL Draft]**.

Para volver a establecer el estado en **[!UICONTROL Approved]**, seleccione el botón correspondiente que se muestra ahora.

![](../../assets/offer_approve.png)

El botón **[!UICONTROL More actions]** habilita las acciones descritas a continuación.

![](../../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**: crea una oferta con las mismas propiedades, representaciones, reglas de idoneidad y restricciones. De forma predeterminada, la nueva oferta tiene el estado **[!UICONTROL Draft]**.
* **[!UICONTROL Delete]**: elimina la oferta de la lista.

   >[!CAUTION]
   >
   >La oferta y su contenido ya no serán accesibles. Esta acción no se puede deshacer.
   >
   >Si la oferta se utiliza en una recopilación o una decisión, no se puede eliminar. Primero debe eliminar la oferta de cualquier objeto.

* **[!UICONTROL Archive]**: establece el estado de la oferta en  **[!UICONTROL Archived]**. La oferta sigue estando disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. Solo puede duplicarlo o eliminarlo.

También puede eliminar o cambiar el estado de varias ofertas al mismo tiempo seleccionando las casillas de verificación correspondientes.

![](../../assets/offer_multiple-selection.png)

Si desea cambiar el estado de varias ofertas con estados diferentes, solo se cambiarán los estados relevantes.

![](../../assets/offer_change-status.png)

Una vez creada una oferta, puede hacer clic en su nombre desde la lista.

![](../../assets/offer_click-name.png)

Esto le permite acceder a información detallada de esa oferta. Seleccione la pestaña **[!UICONTROL Change log]** para [supervisar todos los cambios](../get-started/user-interface.md#monitoring-changes) que se han realizado en la oferta.

![](../../assets/offer_information.png)

## Tutorial en vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
