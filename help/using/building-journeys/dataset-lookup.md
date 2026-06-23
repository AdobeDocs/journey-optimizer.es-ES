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
TQID: https://experienceleague.adobe.com/4sQ3A15j47fQ6hI1G9oS6T6ne9nbxIaeqc-95zSUIq4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1500
ht-degree: 6%

---

# Usar datos de [!DNL Adobe Experience Platform] en recorridos {#datalookup}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar la actividad de búsqueda de conjuntos de datos para recuperar dinámicamente datos de conjuntos de datos de registros de Adobe Experience Platform en tiempo de ejecución y enriquecer sus recorridos con datos externos para la personalización y la toma de decisiones.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="Actividad de búsqueda de conjuntos de datos"
>abstract="La actividad **[!UICONTROL Búsqueda de conjuntos de datos]** permite recuperar datos de conjuntos de datos de registros de forma dinámica de [!DNL Adobe Experience Platform] durante el tiempo de ejecución. Al aprovechar esta capacidad, puede acceder a datos que pueden no residir en el perfil o en la carga útil del evento, lo que garantiza que las interacciones de los clientes sean relevantes y oportunas."

La actividad **[!UICONTROL Búsqueda de conjuntos de datos]** permite recuperar datos de conjuntos de datos de registros de forma dinámica de [!DNL Adobe Experience Platform] durante el tiempo de ejecución. Al aprovechar esta capacidad, puede acceder a datos que pueden no residir en el perfil o en la carga útil del evento, lo que garantiza que las interacciones de los clientes sean relevantes y oportunas.

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible para todos los clientes como una versión de disponibilidad limitada.

Ventajas principales:

* **Personalización en tiempo real**: adapte las experiencias de los clientes con datos enriquecidos.
* **Toma de decisiones dinámica**: use datos externos para controlar la lógica y las acciones del recorrido.
* **Acceso mejorado a datos**: Recupere metadatos de productos, tablas de precios o datos relacionales vinculados a claves específicas.

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

   >[!IMPORTANT]
   >
   >Debe definir la clave de búsqueda mediante **modo avanzado**. Si utiliza el modo simple para establecer la clave, el resultado de la actividad de búsqueda del conjunto de datos no estará disponible como atributo de contexto en las actividades de flujo descendente y la sintaxis `@datasetLookup{}` fallará con el error &quot;No se encontró la búsqueda del conjunto de datos&quot; en las actividades de condición.

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

+++

## Solución de problemas {#troubleshooting}

### Error &quot;No se encontró la búsqueda del conjunto de datos&quot; en la actividad de condición {#troubleshooting-not-found}

**Síntoma:** La sintaxis `@datasetLookup{}` en el editor de expresiones avanzadas de una actividad de condición devuelve el error &quot;No se encontró la búsqueda de conjuntos de datos&quot;, aunque la actividad de búsqueda de conjuntos de datos esté configurada correctamente en la recorrido.

**Causa:** La clave de búsqueda en la actividad de búsqueda del conjunto de datos se estableció mediante el modo simple. Cuando la clave no se define en el modo avanzado, el resultado de la actividad no se expone como atributo de contexto en las actividades descendentes.

**Corrección:** Abra la actividad de búsqueda del conjunto de datos, busque el campo **[!UICONTROL Teclas de búsqueda]** y cambie a **modo avanzado** para redefinir la expresión de clave. Guarde la actividad y vuelva a publicar el recorrido.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo configurar la actividad de búsqueda de conjuntos de datos para recuperar dinámicamente los datos del conjunto de datos de registros de AEP durante el tiempo de ejecución del recorrido para la personalización en tiempo real y la lógica condicional.

**Intenciones:**

* Agregue una actividad de búsqueda de conjuntos de datos a un recorrido para recuperar datos de registros de AEP externos durante la ejecución
* Seleccione campos específicos de conjuntos de datos (nodos de hoja/valores primitivos) para recuperar durante la búsqueda
* Defina una clave de búsqueda en el modo avanzado para unir el contexto de recorrido con los registros del conjunto de datos
* Utilice datos de conjuntos de datos enriquecidos en el editor de expresiones de recorrido o en el editor de personalización
* Solucionar errores de &quot;No se encontró la búsqueda del conjunto de datos&quot; causados por el uso del modo simple para la clave de búsqueda

**Glosario:**

* **Actividad de búsqueda de conjuntos de datos**: una actividad de orquestación de recorrido que recupera datos de conjuntos de datos de registros de AEP en tiempo de ejecución mediante una clave de unión *(específica del producto)*
* **Nodo de hoja**: Campo en el nivel inferior de una jerarquía de esquema que contiene un valor primitivo (cadena, número, booleano, fecha) *(específico del producto)*
* **Clave de búsqueda**: La expresión de unión (cadena o lista de cadenas) utilizada para hacer coincidir los datos de contexto del recorrido con los registros del conjunto de datos seleccionado *(específico del producto)*
* **Datos enriquecidos**: datos recuperados por una actividad de búsqueda de conjuntos de datos y almacenados de forma transitoria en el contexto de recorrido para su uso en actividades de flujo descendente *(específicas del producto)*

**Protecciones:**

* Máximo de 10 actividades de búsqueda de conjuntos de datos por recorrido.
* Máximo de 20 campos seleccionados por actividad de búsqueda.
* Máximo de 50 claves en la matriz de claves de búsqueda.
* El tamaño de los datos enriquecidos está limitado a 10 KB.
* El conjunto de datos debe estar habilitado para la búsqueda en Adobe Experience Platform antes de que aparezca en la configuración de la actividad.
* Solo se pueden seleccionar nodos de hoja (valores primitivos); no se pueden seleccionar matrices y mapas.
* Solo se admiten cadenas o listas de cadenas como claves de búsqueda.
* La clave de búsqueda debe definirse en modo avanzado; el uso de modo simple hace que la salida de la actividad no esté disponible como atributo de contexto descendente.
* Los datos enriquecidos son transitorios y están disponibles solo durante el tiempo de ejecución del recorrido y en la personalización de actividades salientes.
* Para obtener rendimiento, se recomiendan hasta 5 actividades de búsqueda por recorrido y hasta 20 atributos por búsqueda.

**Terminología:**

* Nombre canónico: Actividad de búsqueda de conjuntos de datos — Acrónimo: n/a — variantes: búsqueda de datos de AEP, actividad de enriquecimiento de datos
* Sinónimos: &quot;clave de búsqueda&quot; = &quot;clave de unión&quot;
* No confunda: &quot;Actividad de búsqueda de conjuntos de datos&quot; ≠ &quot;Búsqueda de eventos de experiencia&quot;: la búsqueda de conjuntos de datos recupera datos de conjuntos de datos de registro, no eventos de experiencia de series temporales

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Por qué no aparece mi conjunto de datos en la lista desplegable de campos de conjuntos de datos?** — El conjunto de datos debe estar habilitado para la búsqueda en Adobe Experience Platform. Siga las instrucciones de la sección Debe leer para habilitarlo.
* **Q: ¿Por qué `@datasetLookup{}` devuelve el error &quot;No se encontró la búsqueda del conjunto de datos&quot; en una condición?** — La clave de búsqueda se definió mediante el modo simple en lugar del modo avanzado. Vuelva a definirlo en modo avanzado y vuelva a publicar el recorrido.
* **Q: ¿Puedo recuperar matrices o campos de asignación del conjunto de datos?** — No, solo se pueden seleccionar campos de nodo de hoja primitivos (cadena, número, booleano, fecha).
* **Q: ¿Cómo puedo acceder a los datos enriquecidos en un correo electrónico?** — Utilizar el editor de personalización con la sintaxis `{{context.journey.datasetLookup.<activityId>.entities}}`.
* **Q: ¿Persisten los datos enriquecidos después de que finalice el recorrido?** — No, los datos enriquecidos son transitorios y solo están disponibles durante la sesión de tiempo de ejecución de recorrido.

+++
