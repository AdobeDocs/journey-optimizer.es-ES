---
solution: Journey Optimizer
product: journey optimizer
title: Usar  [!DNL Adobe Experience Platform] datos en recorridos
description: Aprenda a utilizar la actividad de búsqueda de conjuntos de datos en  [!DNL Adobe Journey Optimizer]  para enriquecer los recorridos de los clientes con datos externos de  [!DNL Adobe Experience Platform].
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilidad limitada" type="Informative"
exl-id: b6f54a79-b9e7-4b3a-9a6f-72d5282c01d3
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 10%

---

# Usar datos de [!DNL Adobe Experience Platform] en recorridos {#datalookup}

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="Actividad de búsqueda de conjuntos de datos"
>abstract="La actividad **[!UICONTROL Búsqueda de conjuntos de datos]** le permite recuperar dinámicamente datos de [!DNL Adobe Experience Platform] conjuntos de datos de registros durante el tiempo de ejecución. Al aprovechar esta capacidad, puede acceder a datos que pueden no residir en el perfil o en la carga útil del evento, lo que garantiza que las interacciones de los clientes sean relevantes y oportunas."

La actividad **[!UICONTROL Búsqueda de conjuntos de datos]** le permite recuperar dinámicamente datos de [!DNL Adobe Experience Platform] conjuntos de datos de registros durante el tiempo de ejecución. Al aprovechar esta capacidad, puede acceder a datos que pueden no residir en el perfil o en la carga útil del evento, lo que garantiza que las interacciones de los clientes sean relevantes y oportunas.

Ventajas principales:

* **Personalización en tiempo real**: adapte las experiencias de los clientes con datos enriquecidos.
* **Toma de decisiones dinámica**: use datos externos para controlar la lógica y las acciones del recorrido.
* **Acceso mejorado a datos**: Recupere metadatos de productos, tablas de precios o datos relacionales vinculados a claves específicas.

>[!AVAILABILITY]
>
>Esta actividad solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

## Lectura obligatoria {#must-read}

Revise estos requisitos antes de configurar las búsquedas de conjuntos de datos.

### Habilitación de conjuntos de datos

El conjunto de datos debe estar habilitado para la búsqueda en [!DNL Adobe Experience Platform]. Encontrará información detallada en esta sección: [Usar [!DNL Adobe Experience Platform] datos](../data/lookup-aep-data.md).

### Límites y restricciones

* Máximo de 10 actividades de búsqueda de conjuntos de datos por recorrido.
* Máximo de 20 campos seleccionados.
* Máximo de 50 claves en la matriz de claves de búsqueda.
* El tamaño de los datos enriquecidos está limitado a 10 KB.

### Consideraciones de rendimiento adicionales

Las siguientes recomendaciones son instrucciones para evitar retrasos en la entrega:

| Consideración | Límite recomendado | Descripción |
| ------- | ------- | ------- |
| Atributos por búsqueda | Hasta 20 | Número de campos de datos recuperados por registro en una sola actividad de búsqueda. |
| Actividades de búsqueda | Hasta 5 por recorrido | Cada recorrido puede contener hasta 5 actividades de búsqueda independientes. Cada búsqueda puede dirigirse a un conjunto de datos diferente. |

## Configurar la actividad de búsqueda de conjuntos de datos {#configure}

Para configurar la actividad **[!UICONTROL Búsqueda de conjuntos de datos]**, siga estos pasos:

1. Despliegue la categoría **[!UICONTROL Orchestration]** y suelte una actividad **[!UICONTROL Consulta de conjuntos de datos]** en el lienzo.

   ![[!DNL Adobe Experience Platform] actividad de búsqueda del conjunto de datos en el recorrido ](assets/aep-data-activity.png)

1. Añada una etiqueta y una descripción.

1. En el campo **[!UICONTROL Conjunto de datos]**, seleccione el conjunto de datos con los atributos que necesite.

   >[!NOTE]
   >
   >Si el conjunto de datos que busca no se muestra en la lista, asegúrese de que lo ha habilitado para la búsqueda. Para obtener más información, consulte la sección [Debe leer](#must-read).

1. Seleccione los campos específicos que desea recuperar del conjunto de datos.

   * Solo puede seleccionar nodos de hoja (campos en el nivel inferior del esquema). El campo debe ser un valor primitivo (cadena, número, booleano, fecha, etc.).

   * No se pueden seleccionar listas (matrices) y mapas (objetos clave-valor).

   +++Ejemplo

   ![Selección de campo de conjunto de datos que muestra tipos y estructura de datos primitivos](assets/aep-data-leaf-primitive.png)

   +++

1. En el campo **[!UICONTROL Claves de búsqueda]**, elija una clave de unión que exista tanto en los atributos del elemento de decisión como en el conjunto de datos. El sistema utiliza esta clave para buscar en el conjunto de datos seleccionado.

   * Las claves pueden ser expresiones derivadas del contexto de recorrido, como SKU, ID de correo electrónico u otros identificadores. Ejemplo: `@profile.email` o `list(@event{purchase_event.products.sku})`.

   * Solo se admiten **cadenas** o **listas de cadenas**.

   +++Ejemplo

   ![Editor de expresiones con búsqueda de campos de conjunto de datos y funciones de cadena](assets/aep-data-strings.png)

   +++

## Uso de datos enriquecidos en el recorrido

Los datos recuperados por la actividad **[!UICONTROL Búsqueda de conjuntos de datos]** se almacenan en el contexto de Recorrido como una matriz de objetos. Está disponible en el editor de expresiones de recorrido y en el editor de personalización, lo que permite la lógica condicional y la mensajería personalizada basada en datos enriquecidos.

* **Editor de expresiones de Recorrido**:

  Acceda al editor de **[!UICONTROL Modo avanzado]** y use la sintaxis: `@datasetLookup{MyDatasetLookUpActivity1.entities}`. [Aprenda a trabajar con el editor de expresiones avanzadas](../building-journeys/expression/expressionadvanced.md)

* **Editor de Personalization**:

  Utilice la sintaxis: `{{context.journey.datasetLookup.1482319411.entities}}`.

>[!NOTE]
>
>Los datos enriquecidos son transitorios y están disponibles solo durante el tiempo de ejecución del recorrido y en la personalización de actividades salientes (correo electrónico, push, SMS, etc.)

## Ejemplos de casos de uso

+++Filtrado basado en categorías de productos

**Escenario**:Send es un cupón para los usuarios que gastan más de 40 dólares en productos del hogar.

**Flujo de Recorrido**:

1. **Evento de compra**: Capture SKU del carro de compras del usuario.

1. **Actividad de búsqueda de conjuntos de datos**:

   * Conjunto de datos: `products-dataset` (SKU como clave principal).
   * Claves de búsqueda: `list(@event{purchase_event.products.sku})`.
   * Campos que se van a devolver: `["SKU", "category", "price"]`.

1. **Actividad de condición**:

   * Filtrar SKU donde la categoría sea &quot;doméstica&quot;.

     ```
     @event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookupActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )} 
     ```

   O BIEN

   * Sume el gasto total en productos para el hogar y compárelo con el umbral de 40 dólares.

     ```
     sum(@event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookUpActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )}.price}, ',', true ) > 40
     ```

1. **Editor de Personalization**:

   Utilice los datos enriquecidos para personalizar el contenido del correo electrónico:

   ```
   {% let householdTotal = 0 %}
   {{#each journey.datasetlookup.3709000.entities as |product|}}
   {%#if get(product, "category") = "household"%}
   {% let householdTotal = householdTotal + product.price %}{%/if%}
   {{/each}}
   "Hi, thanks for spending " + {%= householdTotal %} + " on household products. Here is your reward!"
   ```

+++

+++Personalization con datos de lealtad externos

**Escenario**: identifique qué cuenta de correo electrónico de un perfil tiene un estado de fidelidad de Platino. En esta situación, la cuenta de fidelización está asociada a un ID de correo electrónico y los datos de fidelidad no están disponibles en el almacén de búsqueda de perfiles estándar.

**Flujo de Recorrido**:

1. **Déclencheur de eventos de perfil**: capture los ID de correo electrónico a partir del perfil o contexto de evento.

1. **Actividad de búsqueda de conjuntos de datos**:
   * Conjunto de datos: `loyalty-member-dataset` (correo electrónico como clave principal).
   * Claves de búsqueda: `@profile.email`.
   * Campos que se van a devolver: `["email", "loyaltyTier"]`.

1. **Actividad de condición**:

   Ramificar el recorrido en función del nivel de fidelidad:

   ```
   @datasetLookup{MyDatasetLookUpActivity1.entity.loyaltyMember.loyaltyTier} == 'Platinum'
   ```

1. **Editor de Personalization**:

   Utilice los datos del nivel de lealtad enriquecido para personalizar la comunicación saliente:

   ```
   {{context.journey.datasetLookup.1482319411.entity.loyaltyMember.loyaltyTier}}
   ```
