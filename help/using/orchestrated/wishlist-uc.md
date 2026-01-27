---
solution: Journey Optimizer
product: journey optimizer
title: Enviar actualizaciones de artículos de lista de deseos
description: Enviar actualizaciones de artículos de lista de deseos
feature: Use Cases
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 4%

---

# Enviar actualizaciones de artículos de lista de deseos {#wishist-uc}

>[!BEGINSHADEBOX]

Aunque este ejemplo usa un esquema **Wishlist**, el mismo método se aplica a cualquier entidad con una relación &quot;uno a varios&quot; con **Destinatarios**, como **Compras**, **Suscripciones** o cualquier esquema personalizado en el que cada destinatario pueda tener varios registros asociados.

**Esquemas necesarios para este caso de uso:**

* **Destinatarios**: utilizados como dimensión de segmentación
* **WishlistItems**: con campos: `creationDate`, `product`, `Wishlistid`
* **Producto**: con campos: `description`, `priceref`, `imageurl`
* **CarrosAbandonados** (opcional): con campo: `lastmodified`

➡️ [Aprenda a configurar esquemas relacionales](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

Esta campaña orquestada se centra en volver a atraer visitantes recordándoles los productos guardados en su Lista de deseos. Con Campaign Orchestration, defina la audiencia con condiciones basadas en la actividad de la lista de deseos, lo que ayuda a los visitantes a volver a la conversión.

1. Comience creando una nueva campaña específicamente dirigida a la renovación de la participación en la lista de deseos. Esto ayudará a enfocar la mensajería en los clientes que han mostrado intención de compra al guardar artículos.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Rellene la **configuración de Campaign**.

1. Agregue una actividad **[!UICONTROL Generar audiencia]** para identificar el grupo de clientes que se dirigirá en función del comportamiento de la lista de deseos.

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. Establezca una **[!UICONTROL Etiqueta]** descriptiva para esta audiencia y elija **[!UICONTROL Destinatarios]** como **[!UICONTROL Dimensión de segmentación]**. A continuación, haga clic en **[!UICONTROL Continuar]** para configurar la audiencia.

1. Haga clic en **[!UICONTROL Agregar condición]** para restringir la audiencia al crear la siguiente condición:

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
O
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   Esta audiencia se basa en destinatarios que tienen una lista de deseos, contienen elementos con imágenes de productos o tienen un carro de compras abandonado dentro del periodo de tiempo definido.

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Calcular]** para ver el número de perfiles afectados por estas condiciones y en **[!UICONTROL Ver resultados]** para inspeccionar los detalles de cada condición y confirmar que la audiencia coincide con el segmento de destino.

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Confirmar]**.

1. Agregue una actividad **[!UICONTROL Enrichment]** para personalizar la campaña con **Lista de deseos** e **información del producto**.

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Añadir datos de enriquecimiento]**.

1. Acceso `Targeting dimension > Wishlistitems > Wishlistid`.

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. Seleccione cómo se recopilan los datos, en este caso **[!UICONTROL Recopilar datos]** para recopilar los detalles de la lista de deseos de su audiencia.

1. Seleccione el número de líneas que desea recuperar. De forma predeterminada, se recuperan tres elementos por lista de deseos, pero esto se puede ajustar según la campaña necesite resaltar más o menos productos.

1. Haga clic en **[!UICONTROL Agregar atributo]** para crear los tres atributos siguientes:

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   Esto enriquece el mensaje con información detallada del producto para impulsar las conversiones.

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. Añada una actividad de correo electrónico para crear un mensaje de renovación de la participación personalizado individualmente para cada cliente. Haz clic en **[!UICONTROL Editar contenido]** para empezar a diseñar tu contenido.

   ➡️ [Más información sobre la personalización de correo electrónico](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. Después de finalizar el correo electrónico, guarda y ejecuta la campaña en modo de borrador al hacer clic en **[!UICONTROL Iniciar]** desde la campaña orquestada.

1. Después de iniciar el modo de borrador, previsualice la audiencia con detalles de la lista de deseos.

   Para obtener información más detallada, haga clic en un resultado de salida y seleccione **[!UICONTROL Previsualizar resultados]**.

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

Una vez ejecutada la campaña, podemos explorar nuestros informes, lo que nos proporciona un conjunto sólido de datos y KPI sobre el rendimiento de nuestra campaña.

➡️ [Más información sobre los informes](../reports/campaign-global-report-cja.md)
