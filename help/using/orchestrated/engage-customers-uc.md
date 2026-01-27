---
solution: Journey Optimizer
product: journey optimizer
title: Captar clientes mediante la actividad de navegación
description: Captar clientes mediante la actividad de navegación
feature: Use Cases
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 4%

---

# Captar clientes mediante la actividad de navegación {#engage-customers-uc}

>[!BEGINSHADEBOX]

Tenga en cuenta que este caso de uso comienza con una audiencia que ya existe en Experience Platform, específicamente, una audiencia de comportamiento web en tiempo real que recopila la actividad de navegación a medida que se produce. [Más información en Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**Esquemas necesarios para este caso de uso:**

* **Destinatarios**: utilizados como dimensión de segmentación, con campos: `email`, `churnprop`
* **Lista de deseos**: con campos: `description`, `priceref`, `imageurl`

➡️ [Aprenda a configurar esquemas relacionales](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

Esta campaña está dirigida a los clientes que han explorado la categoría de equipos de ejercicio. La audiencia se deduplica y segmenta según el riesgo de pérdida, la probabilidad de que alguien deje de participar o comprar.

Los clientes de alto riesgo se reúnen en una nueva audiencia independiente que más adelante se utilizará para una comunicación específica, mientras que los clientes de riesgo bajo y medio pasan por un recorrido de varios pasos con correos electrónicos personalizados y seguimientos.

1. Comience por configurar una nueva campaña específicamente dirigida a **renovar la participación en la lista de deseos**. Esto garantiza que su mensaje se centre en los clientes que ya han mostrado intención de compra al guardar productos en su lista de deseos.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Complete **[!UICONTROL Configuración de campaña]**, como el nombre de la campaña, la descripción, las fechas de inicio y finalización y las etiquetas relevantes.

1. Agregue una actividad **[!UICONTROL Leer audiencia]** para seleccionar una audiencia predefinida de los clientes de Adobe Experience Platform que han buscado en la categoría de equipos para ejercicios en su sitio web.

   Los destinatarios se identifican con sus direcciones de correo electrónico seleccionadas del campo **[!UICONTROL Entidad]**.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. Agregue una actividad **[!UICONTROL Deduplication]** para eliminar las direcciones de correo electrónico duplicadas de la audiencia, asegurándose de que cada cliente reciba un solo mensaje.

1. Haga clic en **[!UICONTROL Agregar atributo]** y seleccione el correo electrónico como atributo para la anulación de duplicación.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. A continuación, agregue una actividad **[!UICONTROL Split]** para segmentar a los clientes según la probabilidad de pérdida, lo que le permitirá ofrecer experiencias personalizadas adaptadas a cada grupo de clientes.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Agregar segmento]** para crear tres grupos:

   * Riesgo bajo

   * Riesgo de Medium

   * Alto riesgo

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Crear filtro]** para definir la probabilidad de pérdida de cada grupo.

   Use **Editor de condiciones** para establecer los valores específicos que determinan el riesgo de pérdida de cada cliente.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. Cada segmento se gestiona de forma diferente:

   * [Riesgo bajo/medio](#low-medium-risk)
   * [Alto riesgo](#high-risk)

1. Una vez que la campaña se haya probado y esté lista, haga clic en **[!UICONTROL Publicar]** para activarla.

Una vez ejecutada la campaña, explore el panel de informes para revisar las métricas de rendimiento y las perspectivas clave.

➡️ [Más información sobre los informes](../reports/campaign-global-report-cja.md)

## Segmentos de alto riesgo {#high-risk}

Para los clientes identificados como con un alto riesgo de pérdida, cree un segmento de audiencia dedicado. Posteriormente, esta audiencia se utiliza para una comunicación separada y con objetivo.

1. Agregar **[!UICONTROL Guardar audiencia]**.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. Agregue una **[!UICONTROL Etiqueta]** a su audiencia y elija el **[!UICONTROL Campo de asignación de perfil]**, aquí **destinatarios-correo electrónico**.

   ![](assets/uc-interest-8.png){zoomable="yes"}

A continuación, esta audiencia se guarda en Experience Cloud, donde más adelante se puede utilizar para una campaña de destino específica.

## Segmentos de riesgo bajo/medio {#low-medium-risk}

Para los clientes con un riesgo bajo y medio de pérdida, configure una campaña de varios pasos destinada a reforzar la participación:

1. Combine riesgos bajos y de Medium con una actividad **[!UICONTROL Union]**.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. Agregue una actividad **[!UICONTROL Enrichment]** para personalizar la campaña con información de productos y listas de deseos.

1. Haga clic en **[!UICONTROL Agregar atributo]** para crear los tres atributos siguientes:

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   Esto enriquece el mensaje con información detallada sobre la lista de deseos.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. Cree una nueva audiencia para el retargeting en función de la participación con correos electrónicos.

   Aquí creamos una audiencia basada en eventos de clic en correos electrónicos, para redireccionar a todas las personas que interactuaron con un correo electrónico enviado anteriormente y, más específicamente, hicieron clic en un vínculo dentro de ese mensaje.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. Divida la participación de forma uniforme para enviar un seguimiento a través de SMS o notificaciones push para fomentar las conversiones.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. Cree el contenido del mensaje para cada canal, incluidos los atributos de perfil, como el nombre del destinatario, junto con datos de enriquecimiento como los elementos de la Lista de deseos, para personalizar cada mensaje.

   ![](assets/uc-interest-13.png){zoomable="yes"}
