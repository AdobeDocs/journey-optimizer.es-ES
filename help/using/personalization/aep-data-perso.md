---
solution: Journey Optimizer
product: journey optimizer
title: Uso de datos de Adobe Experience Platform para la personalización (Beta)
description: Aprenda a utilizar los datos de Adobe Experience Platform para la personalización.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: 07e855b1a334a226c34223e5dd034f88733d6e2e
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 3%

---

# Uso de datos de Adobe Experience Platform para la personalización{#aep-data}

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible para todos los clientes como una versión beta pública.
>
>Para utilizar esta capacidad, primero debe aceptar los términos beta para su organización que se muestran al agregar las nuevas funciones de ayuda &quot;datasetLookup&quot; en el editor de personalización.

Journey Optimizer permite aprovechar datos de Adobe Experience Platform en el editor de personalización para [personalizar el contenido](../personalization/personalize.md). Para ello, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero mediante una llamada de API como se describe a continuación. Cuando haya terminado, puede usar sus datos para personalizar su contenido en [!DNL Journey Optimizer].

## Restricciones y directrices de Beta {#guidelines}

Antes de empezar, revise las siguientes restricciones y directrices:

* **Canales compatibles**: Por ahora, esta capacidad solo está disponible para su uso en canales de correo electrónico, SMS y correo directo.
* **Fragmentos**: la personalización de la búsqueda de conjuntos de datos no se puede colocar en fragmentos visuales o de expresión en este momento.

## Habilitar un conjunto de datos para la búsqueda de datos {#enable}

Para aprovechar los datos del conjunto de datos para la personalización, debe utilizar una llamada de API para recuperar su estado y habilitar el servicio de búsqueda. Encontrará información detallada en esta sección: [Aprovechar conjuntos de datos de Adobe Experience Platform en [!DNL Journey Optimizer]](../data/lookup-aep-data.md)

## Aprovechamiento de un conjunto de datos para la personalización {#leverage}

Una vez que se ha habilitado un conjunto de datos para la personalización de búsquedas mediante una llamada de API, puede utilizar sus datos para personalizar el contenido en [!DNL Journey Optimizer].

1. Abra el editor de personalización, que está disponible en todos los contextos en los que puede definir la personalización, como los mensajes. [Aprenda a trabajar con el editor de personalización](../personalization/personalization-build-expressions.md)

1. Vaya a la lista de funciones de ayuda y agregue la función de ayuda **datasetLookup** al panel de código.

   ![](assets/aep-data-helper.png)

1. Esta función proporciona una sintaxis predefinida que le permite llamar a campos de sus conjuntos de datos de Adobe Experience Platform. La sintaxis es la siguiente:

   ```
   {{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
   ```

   * **datasetId** es el ID del conjunto de datos con el que está trabajando.
   * **id** es el ID de la columna de origen que debe unirse con la identidad principal del conjunto de datos de búsqueda.

     >[!NOTE]
     >
     >El valor especificado para este campo puede ser un identificador de campo (*profile.packages.packageSKU*), un campo pasado en un evento de recorrido (*context.recorrido.events.event_ID.productSKU*) o un valor estático (*sku007653*). En cualquier caso, el sistema utilizará el valor y buscará en el conjunto de datos para comprobar si coincide con una clave.
     >
     >Si utiliza un valor de cadena literal para la clave, mantenga el texto entre comillas. P. Ej.: `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}`. Si utiliza un valor de atributo como clave dinámica, elimine las comillas. P. ej.: `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **result** es un nombre arbitrario que debe proporcionar para hacer referencia a todos los valores de campo que va a recuperar del conjunto de datos. Este valor se utiliza en el código para llamar a cada campo.

   * **required=false**: si se requiere se establece en TRUE, el mensaje solo se enviará si se encuentra una clave coincidente. Si se establece en false, no se requiere una clave coincidente y el mensaje se puede enviar de todos modos. Tenga en cuenta que, si se establece en false, se recomienda tener en cuenta los valores de reserva o predeterminados en el contenido del mensaje.

   +++¿Dónde recuperar un ID de conjunto de datos?

   Los ID de conjuntos de datos se pueden recuperar en la interfaz de usuario de Adobe Experience Platform. Aprenda a trabajar con conjuntos de datos en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

   +++

1. Adapte la sintaxis para adaptarla a sus necesidades. En este ejemplo, queremos recuperar datos relacionados con los vuelos de los pasajeros. La sintaxis es la siguiente:

   ```
   {{datasetLookup datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * Estamos trabajando en el conjunto de datos cuyo ID es &quot;1234567890abcdtId&quot;,
   * El campo que queremos usar para unir con el conjunto de datos de búsqueda es *profile.nextFlightId*,
   * Queremos incluir todos los valores de campo en la referencia &quot;vuelo&quot;.

1. Una vez configurada la sintaxis a la que se va a llamar en el conjunto de datos de Adobe Experience Platform, puede especificar qué campos desea recuperar. La sintaxis es la siguiente:

   ```
   {{result.fieldId}}
   ```

   >[!NOTE]
   >
   >Al hacer referencia a un campo del conjunto de datos, asegúrese de hacer coincidir la ruta del campo completo tal como se define dentro del esquema.

   * **result** es el valor que ha asignado al parámetro **result** en la función de ayuda de **MultiEntity**. En este ejemplo, &quot;vuelo&quot;.
   * **fieldID** es el identificador del campo que desea recuperar. Este identificador es visible en la interfaz de usuario [!DNL Adobe Experience Platform] al examinar el esquema de registros relacionado con el conjunto de datos:

     +++¿Dónde se recupera un ID de campo?

     Los ID de campos se pueden recuperar al previsualizar un conjunto de datos en la interfaz de usuario de Adobe Experience Platform. Obtenga información sobre cómo obtener una vista previa de los conjuntos de datos en [Adobe Experience Platform documentation](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

     +++

   En este ejemplo, queremos utilizar información relacionada con la hora de embarque y la puerta de embarque de los pasajeros. Por lo tanto, añadimos estas dos líneas:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Ahora que el código está listo, puede completar el contenido como de costumbre y probarlo con el botón **Simular contenido** para comprobar la personalización. [Obtenga información sobre cómo obtener una vista previa y probar contenido](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
