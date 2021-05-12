---
title: Creación de ofertas personalizadas
description: Aprenda a crear ofertas personalizadas en Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 4%

---

# Creación de ofertas personalizadas {#creating-personalized-offers}

Antes de crear una oferta, asegúrese de que ha creado:

* Una **ubicación** en la que se mostrará la oferta. Consulte [Crear ubicaciones](../offer-library/creating-placements.md)
* Una **regla de decisión** que definirá la condición bajo la cual se presentará la oferta. Consulte [Crear reglas de decisión](../offer-library/creating-decision-rules.md).
* Una o varias **etiquetas** que desea asociar a la oferta. Consulte [Crear etiquetas](../offer-library/creating-tags.md).

![](../../assets/do-not-localize/how-to-video.png) [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de ofertas personalizadas en el menú **[!UICONTROL Offers]** .

![](../../assets/offers_list.png)

## Cree la oferta {#create-offer}

Para crear una **oferta**, siga estos pasos:

1. Haga clic en **[!UICONTROL Create offer]** y, a continuación, seleccione **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. Especifique el nombre de la oferta, así como su fecha y hora de inicio y finalización. También puede asociar una o varias etiquetas existentes a la oferta, lo que le permite buscar y organizar la Biblioteca de ofertas con mayor facilidad.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >La sección **[!UICONTROL Offer attributes]** permite asociar pares de valor clave con la oferta para fines de informes y análisis.

## Configurar las representaciones de la oferta {#representations}

1. Añada una o varias representaciones para la oferta con el botón **[!UICONTROL Add representation]** .

   >[!NOTE]
   >
   >Una oferta se puede mostrar en diferentes lugares de un mensaje: en un banner superior con una imagen, como texto en un párrafo, como un bloque html, etc. Cuantas más representaciones tenga una oferta, más oportunidades habrá de utilizar la oferta en diferentes contextos de ubicación.

1. Para cada representación, especifique **[!UICONTROL Channel]** y el **[!UICONTROL Placement]** donde se mostrará la oferta.

   ![](../../assets/channel-placement.png)

   El botón **[!UICONTROL Browse]** le permite filtrar las ubicaciones disponibles y filtrarlas según su canal o tipo de contenido.

   ![](../../assets/browse-placements.png)

1. Añada contenido a cada representación procedente de la biblioteca de Adobe Experience Cloud Assets o de una ubicación pública externa.

   * Para agregar contenido de la biblioteca de Adobe Experience Cloud Assets, arrástrelo y suéltelo desde el panel izquierdo al área de representación y, a continuación, especifique la dirección URL que desea asociar al contenido en el campo **[!UICONTROL Destination link]**.

      >[!NOTE]
      >
      >El contenido solo se puede arrastrar y soltar desde el Selector de recursos en el panel izquierdo. Solo está disponible el contenido correspondiente al tipo de contenido de la ubicación.

      ![](../../assets/offer_drag_content.png)

   * Para añadir contenido desde una ubicación pública externa, haga clic en el botón **[!UICONTROL Add content]** y, a continuación, especifique el nombre, la dirección URL y el vínculo de destino del contenido que desea añadir.

      Asegúrese de que el contenido que está agregando corresponde al tipo de contenido de la ubicación seleccionada.

      ![](../../assets/offer_add_content.png)

   * También puede insertar contenido de tipo texto. Para ello, haga clic en el botón **[!UICONTROL Add content]** y luego seleccione la opción **[!UICONTROL Custom text]**. En el campo **[!UICONTROL Text]**, escriba el texto que se mostrará en la oferta.

      >[!NOTE]
      >
      >Esta opción no está disponible para ubicaciones de tipo imagen.

      ![](../../assets/offer_text_content.png)

## Agregar reglas y restricciones de idoneidad {#eligibility}

Las reglas y restricciones de idoneidad le permiten definir las condiciones en las que se mostrará una oferta.

1. Configure el **[!UICONTROL Offer eligibility]**. De forma predeterminada, la opción **[!UICONTROL All visitors]** regla de decisión está seleccionada, lo que significa que cualquier perfil podrá presentarse en la oferta.

   Puede limitar la presentación de la oferta a los miembros de uno o varios segmentos de Adobe Experience Platform. Para ello, active la opción **[!UICONTROL Visitors who fall into one or multiple segments]**, luego agregue uno o varios segmentos del panel izquierdo y combínelos utilizando los operadores lógicos **[!UICONTROL And]** / **[!UICONTROL Or]**.

   Para obtener más información sobre cómo trabajar con segmentos, consulte la [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../../assets/offer-eligibility-segment.png)

   Si desea asociar una regla de decisión específica a la oferta, seleccione **[!UICONTROL By defined decision rule]** y, a continuación, arrastre la regla que desee del panel izquierdo al área **[!UICONTROL Decision rule]**. Para obtener más información sobre cómo crear una regla de decisión, consulte [esta sección](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

1. Defina el **[!UICONTROL Priority]** de la oferta comparado con otros si el usuario cumple los requisitos para más de una oferta. La prioridad más alta que tendrá una oferta es la que mayor será su prioridad comparada con otras ofertas

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

## Revise la oferta {#review}

Una vez definidas las reglas y restricciones de idoneidad, se muestra un resumen de las propiedades de la oferta. Si todo está configurado correctamente y la oferta está lista para presentarse a los usuarios, haga clic en **[!UICONTROL Finish]** y seleccione **[!UICONTROL Save and approve]**.

También puede guardar la oferta como borrador para editarla y aprobarla más adelante.

![](../../assets/offer_review.png)

La oferta se muestra en la lista con los estados **[!UICONTROL Live]** o **[!UICONTROL Draft]**, en función de si la aprobó o no en el paso anterior.

Ahora está listo para enviarse a los usuarios. Puede seleccionarlo para mostrar sus propiedades y editarlo o suprimirlo.

![](../../assets/offer_created.png)

Una vez creada una oferta, puede hacer clic en su nombre en la lista para acceder a información detallada y monitorizar todos los cambios realizados en ella mediante la pestaña **[!UICONTROL Change log]** (consulte [Control de cambios en ofertas y decisiones](../get-started/user-interface.md#monitoring-changes)).

## Tutorial en vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
