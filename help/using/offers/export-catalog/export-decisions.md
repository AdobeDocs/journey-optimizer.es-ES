---
title: Conjunto de datos de decisiones
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para tomar decisiones
badge: label="Heredado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '1531'
ht-degree: 0%

---

# Conjunto de datos de decisiones {#decisions-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las decisiones.

![](../assets/dataset-activities.png)

El lote exitoso más reciente en el conjunto de datos se muestra a la derecha. La vista jerárquica del esquema del conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden usar en el conjunto de datos **[!UICONTROL Repositorio de objetos de decisión - Decisiones]** (anteriormente conocido como Repositorio de objetos de decisión - Actividades).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ Identificador

**Campo:** _id
**Título:** Identificador
**Descripción:** Identificador único del registro.
**Tipo:** cadena

+++

+++ _experience

**Campo:** _experiencia
**Tipo:** objeto

+++

+++ _experience > toma de decisiones

**Campo:** toma de decisiones
**Tipo:** objeto

+++

+++ _experience > decisioning > criteria

**Campo:** criterios
**Título:** Criterios
**Descripción:** define un conjunto de criterios de decisión donde cada uno contiene un conjunto de restricciones.
**Tipo:** matriz

+++

+++ _experience > decisioning > criteria > description

**Campo:** descripción
**Título:** Descripción
**Descripción:** Descripción del criterio. Se utiliza para transmitir intenciones legibles por el ser humano sobre cómo o por qué se construyó este criterio y cómo está afectando a la decisión.
**Tipo:** cadena

+++

+++_experience > decisioning > criteria > optionSelection

**Campo:** optionSelection
**Título:** Selección de opción
**Descripción:** La selección de opciones define la validez o aplicabilidad de las opciones en este contexto.
**Tipo:** objeto

* Descripción

  **Campo:** descripción
  **Título:** Descripción
  **Descripción:** Descripción de la selección de opciones. Se utiliza para transmitir intenciones legibles en lenguaje natural sobre cómo o por qué se construyó esta selección de opción y/o qué opción coincidirá.
  **Tipo:** cadena

* Filtro de opción

  **Campo:** filtro
  **Título:** Filtro de opción
  **Descripción:** La referencia a un filtro basado en calificador de colección (anteriormente conocido como &quot;etiqueta&quot;) que coincide con las opciones de un inventario que usa sus calificadores de colección adjuntos. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte schema https://ns.adobe.com/experience/decisioning/filter.
  **Tipo:** cadena

* Tipo de restricción de perfil

  **Campo:** optionSelectionType
  **Título:** tipo de restricción de perfil
  **Descripción:** Determina si hay restricciones establecidas actualmente y cómo se expresan las restricciones. Puede ser a través de una consulta de filtro o a través de una o más suscripciones a audiencias.
  **Tipo:** cadena
  **Valores posibles:** &quot;ninguno&quot; (predeterminado), &quot;directList&quot;, &quot;filter&quot;

* Lista de opciones

  **Campo:** opciones
  **Título:** Lista de opciones
  **Descripción:** Una lista que especifica directamente las opciones sin evaluar una consulta de filtro. Se puede especificar una lista de opciones o una regla de filtro de opciones.
  **Tipo:** matriz

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_experiencia > toma de decisiones > criterios > ubicaciones

**Campo:** ubicaciones
**Título:** Restricciones de ubicación
**Descripción:** La restricción de ubicación indica que este criterio solo es aplicable a las ubicaciones enumeradas. La selección de opciones solo se tiene en cuenta cuando la ubicación de destino está en la lista `xdm:placements`. De lo contrario, se omiten todos los criterios de decisión. Cuando la lista &quot;xdm:placements&quot; se omite o está vacía, el criterio se tiene en cuenta para cualquier ubicación de destino. Las ubicaciones enumeradas aquí imponen criterios implícitos para la selección de opciones. Una opción que se vaya a considerar debe tener una representación para la ubicación de destino.
**Tipo:** matriz

* Identificador de ubicación

  **Título:** Identificador de ubicación
  **Descripción:** Una referencia a una entidad de ubicación. El valor es el URI (@id) de la ubicación a la que se hace referencia. Consulte schema https://ns.adobe.com/experience/decisioning/placement.
  **Tipo:** cadena

+++

+++_experience > decisioning > criteria > profileConstraints

**Campo:** profileConstraints
**Título:** Restricción de perfil
**Descripción:** La restricción de perfil decide si una selección de opción es elegible para esta identidad de perfil en este momento, en este contexto. Si la restricción de perfil no necesita tener en cuenta los valores de cada una de las opciones, es decir, si es invariante de las opciones de la selección de opciones, la restricción de perfil que se evalúa como &#39;false&#39; cancela toda la selección de opciones. Por otro lado, una regla de restricción de perfil que toma una opción como parámetro se evalúa para cada opción correspondiente de la selección de opciones.
**Tipo:** objeto

+++

+++_experience > decisioning > criteria > profileConstraints > Description

**Campo:** descripción
**Título:** Descripción
**Descripción:** descripción de restricción de perfil. Se utiliza para transmitir intenciones legibles por el ser humano sobre cómo o por qué se construyó esta restricción de perfil y/o qué opción se incluirá o excluirá en ella.
**Tipo:** cadena

+++

+++ _experience > decisioning > criteria > profileConstraints > Eligibility Rule

**Campo:** eligibilityRule
**Título:** Regla De Elegibilidad
**Descripción:** Referencia a una regla de decisión que se evalúa como verdadera o falsa para un perfil determinado u otros objetos XDM contextuales determinados. La regla se utiliza para decidir si la opción cumple los requisitos para un perfil determinado. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte schema https://ns.adobe.com/experience/decisioning/rule.
**Tipo:** cadena

+++

+++ _experience > decisioning > criteria > profileConstraints > Profile Constraint Type

**Campo:** profileConstraintType
**Título:** tipo de restricción de perfil
**Descripción:** Determina si hay restricciones establecidas actualmente y cómo se expresan las restricciones. Puede ser a través de una regla o a través de una o más suscripciones a audiencias.
**Tipo:** cadena
**Valores posibles:**
* &quot;ninguno&quot; (predeterminado)
* &quot;eligibilityRule&quot;: &quot;La restricción de perfil se expresa como una sola regla que debe evaluarse como true antes de permitir la acción restringida.&quot;
* &quot;anySegments&quot;: &quot;La restricción de perfil se expresa como una o más audiencias y el perfil debe ser miembro de al menos una de ellas antes de que se permita la acción restringida.&quot;
* &quot;allSegments&quot;: &quot;La restricción de perfil se expresa como una o más audiencias y el perfil debe ser miembro de todas antes de que se permita la acción restringida.&quot;
* &quot;reglas&quot;: &quot;La restricción de perfil se expresa como una serie de reglas diferentes, por ejemplo, elegibilidad, aplicabilidad e idoneidad, que todas deben evaluar como true antes de permitir la acción restringida&quot;.

+++

+++ _experience > decisioning > criteria > profileConstraints > segmentIdentities

**Campo:** segmentIdentities
**Título:** Identificadores De Segmento
**Descripción:** identificadores de la audiencia.
**Tipo:** matriz

* Identificador

  **Campo:** _id
  **Título:** Identificador
  **Descripción:** identidad de la audiencia en el área de nombres relacionada.
  **Tipo:** cadena

* namespace

  **Campo:** espacio de nombres
  **Título:** Espacio de nombres
  **Descripción:** espacio de nombres asociado con el atributo `xid`.
  **Tipo:** objeto
  **Requerido:** &quot;código&quot;

   * Código

     **Campo:** código
     Código **Title:**
     **Descripción:** El código es un identificador en lenguaje natural para el área de nombres y se puede usar para solicitar la identificación técnica del área de nombres que se usa para el procesamiento del gráfico de identidades.
     **Tipo:** cadena

* Identificador de experiencia

  **Campo:** xid
  **Título:** Identificador de experiencia
  **Descripción:** Cuando está presente, este valor representa un identificador de área de nombres cruzado que es único en todos los identificadores de ámbito de área de nombres en todas las áreas de nombres.
  **Tipo:** cadena

+++

+++_experiencia > toma de decisiones > criterios > clasificación

Clasificación **Campo:**
**Título:** Detalles de clasificación
**Descripción:** Clasificación (prioridad). Define cómo se determina la \&quot;mejor opción\&quot; según el contexto del criterio de decisión. Entre todas las opciones seleccionadas que cumplen con las restricciones de perfil, la clasificación decidirá las opciones principales (o N principales) que se propondrán.
**Tipo:** objeto

+++

+++_experiencia > toma de decisiones > criterios > clasificación > pedido

**Campo:** pedido
**Título:** Evaluación de pedidos
**Descripción:** evaluación de un orden relativo de una o más opciones de decisión. Las opciones con valores ordinales más altos se seleccionan sobre las opciones con valores ordinales más bajos. Los valores determinados por este método pueden ordenarse, pero no pueden medirse las distancias entre ellos ni tampoco pueden calcularse las sumas ni los productos. La mediana y el modo son las únicas medidas de tendencia central que se pueden utilizar para los datos ordinales.
**Tipo:** objeto

* Función de puntuación

  **Campo:** función
  **Título:** función de puntuación
  **Descripción:** Referencia a una función que calcula una puntuación numérica para esta opción de decisión. Las opciones de decisión se ordenarán (clasificarán) según esa puntuación. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con una opción a la vez. Consulte schema https://ns.adobe.com/experience/decisioning/function.
  **Tipo:** cadena

* Tipo de evaluación de pedido**

  **Campo:** orderEvaluationType
  **Título:** Tipo de evaluación de pedido
  **Descripción:** Especifica qué mecanismo de evaluación de pedidos se utiliza, la prioridad estática de las opciones de decisión, una función de puntuación que calcula un valor numérico para cada opción o un modelo de IA que recibe una lista para ordenarla.
  **Tipo:** cadena
  **Valores posibles:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* Estrategia de clasificación

  **Campo:** rankingStrategy
  **Título:** Estrategia de clasificación
  **Descripción:** Referencia a una estrategia que clasifica una lista de opciones de decisión. Las opciones de decisión se devolverán en una lista ordenada. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con una opción a la vez. Consulte schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
  **Tipo:** cadena

+++

+++ _experience > decisioning > criteria > ranking > Priority

**Campo:** prioridad
**Título:** Prioridad
**Descripción:** Prioridad de una sola opción de decisión en relación con todas las demás opciones. Las opciones para las que no se proporciona ninguna función de orden se priorizan mediante esta propiedad. Las opciones con valores de prioridad más altos se seleccionan antes que las opciones de prioridad más baja. Si dos o más opciones elegibles comparten el valor de prioridad más alto, se elige una al azar uniforme y se usa para la propuesta de decisión.
**Tipo:** entero
**Valor mínimo:** 0
**Valor predeterminado:** 0

+++

+++ _experience > decisioning > Fecha y hora de finalización de la actividad

**Campo:** endTime
**Título:** Fecha y hora de finalización de la actividad
**Descripción:** fecha de finalización y hora de finalización de la decisión (anteriormente conocida como actividad). La propiedad tiene la semántica de la propiedad &#39;endTime&#39; de schema.org definida en https://schema.org/Action.
**Tipo:** cadena

+++

+++ _experience > decisioning > Opción de reserva

**Campo:** reserva
**Título:** Opción De Reserva
**Descripción:** La referencia a una opción de reserva que se usa al tomar decisiones en el contexto de esta decisión no califica ninguna de las opciones normales (esto suele ocurrir cuando se aplican restricciones graves). El valor es el URI (@id) de la opción de reserva a la que se hace referencia.
**Tipo:** cadena

+++

+++ _experience > decisioning > Nombre de la actividad

**Campo:** nombre
**Título:** Nombre de actividad
**Descripción:** nombre de decisión (anteriormente conocida como actividad) que se muestra en varias interfaces de usuario.
**Tipo:** cadena

+++

+++_experience > decisioning > Fecha y hora de inicio de la actividad

**Campo:** startTime
**Título:** Fecha y hora de inicio de la actividad
**Descripción:** fecha de inicio y hora de finalización de la decisión (anteriormente conocida como actividad). La propiedad tiene la semántica de la propiedad &#39;startTime&#39; de schema.org definida en https://schema.org/Action.
**Tipo:** cadena

+++

+++ _repo

**Campo:** _repositorio
**Tipo:** objeto

+++

+++ _repo > ETag de actividad

**Campo:** etag
**Título:** ETag de actividad
**Descripción:** Revisión en la que se encontraba el objeto de decisión (anteriormente conocido como actividad) cuando se tomó la instantánea.
**Tipo:** cadena

+++
