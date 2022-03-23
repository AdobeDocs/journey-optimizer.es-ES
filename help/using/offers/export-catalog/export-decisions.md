---
title: Conjunto de datos de decisiones
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para tomar decisiones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '1546'
ht-degree: 3%

---

# Conjunto de datos de decisiones {#decisions-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para decisiones (anteriormente conocido como actividades).

![](../assets/dataset-activities.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden utilizar en la variable **[!UICONTROL Decision Object Repository - Decisions]** conjunto de datos (anteriormente conocido como Repositorio de objetos de decisión - Actividades).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

## Identificador {#identifier}

**Campo:** _id
**Título:** Identificador
**Descripción:** Identificador único del registro.
**Tipo:** cadena

## _experiencia {#experience}

**Campo:** _experience
**Tipo:** object

### _experiencia > decisiones

**Campo:** decisioning
**Tipo:** object

#### _experiencia > decisiones > criterios

**Campo:** criterios
**Título:** Criterios
**Descripción:** Define un conjunto de criterios de decisión en los que cada uno contiene un conjunto de restricciones.
**Tipo:** matriz

**_experiencia > decisiones > criterios > descripción**

**Campo:** descripción
**Título:** Descripción
**Descripción:** Descripción del criterio. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se construyó este criterio y cómo está afectando a la decisión.
**Tipo:** cadena

**_experience > decisioning > criteria > optionSelection**

**Campo:** optionSelection
**Título:** Selección de opciones
**Descripción:** La selección de opciones define la validez/aplicabilidad de las opciones en este contexto.
**Tipo:** object

* **Descripción**

   **Campo:** descripción
   **Título:** Descripción
   **Descripción:** Descripción de la selección de opciones. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se creó esta selección de opciones y/o qué opción coincidirá.
   **Tipo:** cadena

* **Filtro de opciones**

   **Campo:** filter
   **Título:** Filtro de opciones
   **Descripción:** La referencia a un filtro basado en etiquetas que coincida con las opciones de un inventario mediante sus etiquetas adjuntas. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/filter.
   **Tipo:** cadena

* **Tipo de restricción de perfil**

   **Campo:** optionSelectionType
   **Título:** Tipo de restricción de perfil
   **Descripción:** Determina si hay restricciones establecidas actualmente y cómo se expresan. Puede ser a través de una consulta de filtro o a través de una o más suscripciones a segmentos.
   **Tipo:** cadena
   **Valores posibles:** &quot;none&quot; (predeterminado), &quot;directList&quot;, &quot;filter&quot;

* **Lista de opciones**

   **Campo:** opciones
   **Título:** Lista de opciones
   **Descripción:** Lista que especifica directamente las opciones sin evaluar una consulta de filtro. Se puede especificar una lista de opciones o una regla de filtro de opciones.
   **Tipo:** matriz

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_experiencia > decisiones > criterios > ubicaciones**

**Campo:** ubicaciones
**Título:** Restricciones de colocación
**Descripción:** La restricción de colocación indica que este criterio solo es aplicable a las ubicaciones enumeradas. Solo cuando la ubicación de destino se encuentra en la `xdm:placements` list es la selección de opciones que se considera. De lo contrario, se omiten todos los criterios de decisión. Cuando la lista &quot;xdm:placements&quot; se omite o se vacía, el criterio se considera para cualquier ubicación de destino. Las ubicaciones enumeradas aquí imponen criterios implícitos para la selección de opciones. Una opción a considerar debe tener una representación para la ubicación de destino.
**Tipo:** matriz

* **Identificador de colocación**

   **Título:** Identificador de colocación
   **Descripción:** Referencia a una entidad de colocación. El valor es el URI (@id) de la ubicación a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.
   **Tipo:** cadena

**_experience > decisiones > criterios > profileConstraints**

**Campo:** profileConstraints
**Título:** Restricción de perfil
**Descripción:** La restricción de perfil decide si una selección de opciones es apta para esta identidad de perfil en este momento, en este contexto. Si la restricción de perfil no necesita tener en cuenta los valores de cada una de las opciones, es decir, no tiene en cuenta las opciones de la selección de opciones, la restricción de perfil que se evalúa como &quot;false&quot; cancela toda la selección de opciones. Por otro lado, se evalúa una regla de restricción de perfil que toma una opción como parámetro para cada opción correspondiente de la selección de opciones.
**Tipo:** object

* **_experience > decisiones > criterios > profileConstraints > Descripción**

   **Campo:** descripción
   **Título:** Descripción
   **Descripción:** Descripción de restricción de perfil. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se construyó esta restricción de perfil y/o qué opción incluirá o excluirá.
   **Tipo:** cadena

* **_experience > decisiones > criterios > profileConstraints > Regla de elegibilidad**

   **Campo:** eligibilityRule
   **Título:** Regla de elegibilidad
   **Descripción:** Referencia a una regla de decisión que se evalúa como true o false para un perfil determinado u otros objetos XDM contextuales dados. La regla se utiliza para decidir si la opción cumple los requisitos de un perfil determinado. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/rule.
   **Tipo:** cadena

* **_experience > decisioning > criteria > profileConstraints > Tipo de restricción de perfil**

   **Campo:** profileConstraintType
   **Título:** Tipo de restricción de perfil
   **Descripción:** Determina si hay restricciones establecidas actualmente y cómo se expresan. Podría ser a través de una regla o a través de una o más suscripciones a segmentos.
   **Tipo:** cadena
   **Valores posibles:**
   * &quot;none&quot; (predeterminado)
   * &quot;eligibilityRule&quot;: &quot;La restricción de perfil se expresa como una regla única que debe evaluarse como verdadera antes de permitir la acción restringida.&quot;
   * &quot;anySegments&quot;: &quot;La restricción de perfil se expresa como uno o más segmentos y el perfil debe ser miembro de al menos uno de ellos antes de permitir la acción restringida.&quot;
   * &quot;allSegments&quot;: &quot;La restricción de perfil se expresa como uno o más segmentos y el perfil debe ser miembro de todos ellos antes de permitir la acción restringida.&quot;
   * &quot;reglas&quot;: &quot;La restricción de perfil se expresa como una serie de reglas diferentes, por ejemplo, idoneidad, aplicabilidad, idoneidad, que todos deben evaluar como true antes de permitir la acción restringida.&quot;

* **_experience > decisiones > criterios > profileConstraints > segmentIdentities**

   **Campo:** segmentIdentities
   **Título:** Identificadores de segmento
   **Descripción:** Identificadores de los segmentos.
   **Tipo:** matriz

   * **Identificador**

      **Campo:** _id
      **Título:** Identificador
      **Descripción:** Identidad del segmento en el área de nombres relacionada.
      **Tipo:** cadena

   * **namespace**

      **Campo:** namespace
      **Título:** Área de nombres
      **Descripción:** El espacio de nombres asociado con la variable `xid` atributo.
      **Tipo:** object
      **Requerido:** &quot;code&quot;

      * **Código**

         **Campo:** code
         **Título:** Código
         **Descripción:** El código es un identificador legible por humanos para el área de nombres y se puede utilizar para solicitar el id de área de nombres técnica que se utiliza para el procesamiento de gráficos de identidad.
         **Tipo:** cadena
   * **Identificador de experiencia**

      **Campo:** xid
      **Título:** Identificador de experiencia
      **Descripción:** Cuando está presente, este valor representa un identificador de área de nombres cruzada que es único en todos los identificadores de ámbito de área de nombres en todos los espacios de nombres.
      **Tipo:** cadena


**_experiencia > decisiones > criterios > clasificación**

**Campo:** clasificación
**Título:** Detalles de clasificación
**Descripción:** Clasificación (prioridad). Define cómo se determina la \&quot;mejor opción\&quot; teniendo en cuenta el contexto del criterio de decisión. Entre todas las opciones seleccionadas que cumplen las restricciones de perfil, la clasificación decide las opciones superiores (o superiores N) que se proponen.
**Tipo:** object

* **_experiencia > decisiones > criterios > clasificación > orden**

   **Campo:** pedido
   **Título:** Evaluación de pedidos
   **Descripción:** Evaluación de un orden relativo de una o más opciones de decisión. Las opciones con valores de ordinal más altos se seleccionan sobre cualquier opción con valores de ordinal más bajos. Los valores determinados por este método se pueden ordenar, pero no se pueden medir las distancias entre ellos ni se pueden calcular sumas ni productos. La mediana y el modo son las únicas medidas de tendencia central que pueden utilizarse para los datos ordinales.
   **Tipo:** object

   * **Función de puntuación**

      **Campo:** function
      **Título:** Función de puntuación
      **Descripción:** Referencia a una función que calcula una puntuación numérica para esta opción de decisión. Las opciones de decisión se ordenarán (clasificarán) según esa puntuación. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con la opción on a la vez. Consulte esquema https://ns.adobe.com/experience/decisioning/function.
      **Tipo:** cadena

   * **Tipo de evaluación de pedido**

      **Campo:** orderEvaluationType
      **Título:** Tipo de evaluación de pedido
      **Descripción:** Especifica qué mecanismo de evaluación de pedidos se utiliza, prioridad estática de las opciones de decisión, función de puntuación que calcula un valor numérico para cada opción o estrategia de clasificación que recibe una lista para solicitarla.
      **Tipo:** cadena
      **Valores posibles:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

   * **Estrategia de clasificación**

      **Campo:** rankingStrategy
      **Título:** Estrategia de clasificación
      **Descripción:** Referencia a una estrategia que clasifica una opción de lista de decisiones. Las opciones de decisión se devolverán en una lista ordenada. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con la opción on a la vez. Consulte esquema https://ns.adobe.com/experience/decisioning/rankingStrategy.
      **Tipo:** cadena

* **_experience > decisiones > criterios > clasificación > Prioridad**

   **Campo:** priority
   **Título:** Prioridad
   **Descripción:** Prioridad de una única opción de decisión en relación con todas las demás opciones. Las opciones para las que no se proporciona ninguna función de pedido se priorizan usando esta propiedad. Las opciones con valores de prioridad más altos se seleccionan antes que las opciones con prioridad más baja. Si dos o más opciones cualificadas comparten el valor de prioridad más alto, se elige uno de forma aleatoria uniforme y se utiliza para la propuesta de decisión.
   **Tipo:** integer
   **Valor mínimo:** 0
   **Valor predeterminado:** 0

#### _experience > decisiones > Fecha y hora de finalización de la actividad

**Campo:** endTime
**Título:** Fecha y hora de finalización de la actividad
**Descripción:** Fecha de finalización y hora de finalización de la decisión (anteriormente conocida como actividad). La propiedad tiene la semántica de la propiedad &#39;endTime&#39; de schema.org definida en http://schema.org/Action.
**Tipo:** cadena

#### _experience > decisioning > Opción de reserva

**Campo:** reserva
**Título:** Opción de reserva
**Descripción:** La referencia a una opción de reserva que se utiliza al tomar decisiones en el contexto de esta decisión no califica ninguna de las opciones normales (esto suele ocurrir cuando se aplican restricciones duras). El valor es el URI (@id) de la opción de reserva a la que se hace referencia.
**Tipo:** cadena

#### _experience > decisiones > Nombre de la actividad

**Campo:** name
**Título:** Nombre de la actividad
**Descripción:** Nombre de decisión (anteriormente conocido como actividad) que se muestra en varias interfaces de usuario.
**Tipo:** cadena

#### _experience > decisiones > Fecha y hora de inicio de la actividad

**Campo:** startTime
**Título:** Fecha y hora de inicio de la actividad
**Descripción:** La decisión (anteriormente conocida como actividad) es la fecha de inicio y la hora de finalización. La propiedad tiene la semántica de la propiedad &#39;startTime&#39; de schema.org definida en http://schema.org/Action.
**Tipo:** cadena

## _repo {#repo}

**Campo:** _repo
**Tipo:** object

### _repo > Activity ETag

**Campo:** etiqueta
**Título:** ETG de actividad
**Descripción:** Revisión en la que se encontraba el objeto de decisión (anteriormente conocido como actividad) cuando se tomó la instantánea.
**Tipo:** cadena
