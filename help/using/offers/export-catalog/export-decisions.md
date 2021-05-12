---
title: Introducción a la exportación del catálogo de ofertas
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para tomar decisiones.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 4%

---

# Conjunto de datos de decisiones {#decisions-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las decisiones.

![](../../assets/dataset-activities.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Una decisión (anteriormente conocida como decisión de oferta) se utiliza para controlar el proceso de toma de decisiones. Especifica el filtro aplicado al inventario total para reducir las ofertas por tema o categoría, la ubicación para reducir el inventario a aquellas ofertas que técnicamente caben en el espacio reservado para la oferta y especifica una opción de reserva en caso de que las restricciones combinadas descalifiquen todas las ofertas de personalización disponibles.

Esta es la lista de todos los campos que se pueden utilizar en el conjunto de datos **[!UICONTROL Decision Object Repository - Decisions]** (anteriormente conocido como Repositorio de objetos de decisión - Actividades).

## Identificador

Identificador único del registro.

Tipo: cadena

## _experiencia

### decisioning

#### criterios

Define un conjunto de criterios de decisión en los que cada uno contiene un conjunto de restricciones.

Tipo: matriz

* **Descripción**

   Descripción del criterio. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se construyó este criterio y cómo está afectando a la decisión.

   Tipo: cadena

* **Selección de opciones**

   La selección de opciones define la validez/aplicabilidad de las opciones en este contexto.

   Tipo: object

   * **Descripción**

      Descripción de la selección de opciones. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se creó esta selección de opciones y/o qué opción coincidirá.

      Tipo: cadena

   * **Filtro de opciones**

      La referencia a un filtro basado en etiquetas que coincida con las opciones de un inventario mediante sus etiquetas adjuntas. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/filter.

      Tipo: cadena

   * **Tipo de restricción de perfil**

      Determina si hay restricciones establecidas actualmente y cómo se expresan las restricciones. Podría ser mediante una consulta de filtro o a través de una o más suscripciones a segmentos.

      Tipo: cadena

   * **Lista de opciones**

      Lista que especifica directamente las opciones sin evaluar una consulta de filtro. Se puede especificar una lista de opciones o una regla de filtro de opciones.

      Tipo: matriz

      <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option.-->

* **ubicaciones**

   La restricción de colocación indica que este criterio solo es aplicable a las ubicaciones enumeradas. Solo se tiene en cuenta la selección de opciones cuando la colocación de destino está en la lista `xdm:placements`. De lo contrario, se omiten todos los criterios de decisión. Cuando la lista &quot;xdm:placements&quot; se omite o se vacía, el criterio se considera para cualquier ubicación de destino. Las ubicaciones enumeradas aquí imponen criterios implícitos para la selección de opciones. Una opción a considerar debe tener una representación para la ubicación de destino.

   Tipo: matriz

   * **Identificador de colocación**

   Referencia a una entidad de colocación. El valor es el URI (@id) de la ubicación a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.

   Tipo: cadena

* **Restricción de perfil**

   La restricción de perfil decide si una selección de opciones es apta para esta identidad de perfil en este momento, en este contexto. Si la restricción de perfil no necesita tener en cuenta los valores de cada una de las opciones, es decir, no tiene en cuenta las opciones de la selección de opciones, la restricción de perfil que se evalúa como &quot;false&quot; cancela toda la selección de opciones. Por otro lado, se evalúa una regla de restricción de perfil que toma una opción como parámetro para cada opción de calificación de la selección de opciones.

   Tipo: object

   * **Descripción**

      Descripción de restricción de perfil. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se construyó esta restricción de perfil y/o qué opción incluirá o excluirá.

      Tipo: cadena

   * **Regla de elegibilidad**

      Referencia a una regla de decisión que se evalúa como true o false para un perfil determinado u otros objetos XDM contextuales dados. La regla se utiliza para decidir si la opción cumple los requisitos de un perfil determinado. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/rule.

      Tipo: cadena

   * **Tipo de restricción de perfil**

      Determina si hay restricciones establecidas actualmente y cómo se expresan las restricciones. Podría ser mediante una regla o a través de una o más suscripciones a segmentos.

      Tipo: cadena

      Valores posibles: &quot;none&quot;, &quot;eligibilityRule&quot;, &quot;anySegments&quot;, &quot;allSegments&quot;, &quot;rules&quot;

      Valor predeterminado: &quot;none&quot;

   * **Identificadores de segmento**

      Identificadores de los segmentos

      Cadena: matriz

      * **Identificador**

         Identidad del segmento en el área de nombres relacionada.

         Tipo: cadena

      * **Área de nombres**

         El espacio de nombres asociado al atributo `xid`.

         Tipo: object

         * **Código**

            El código es un identificador legible por humanos para el área de nombres y se puede utilizar para solicitar el id de área de nombres técnica que se utiliza para el procesamiento de gráficos de identidad.

            Tipo: cadena
      * **Identificador de experiencia**

         Cuando está presente, este valor representa un identificador de área de nombres cruzada que es único en todos los identificadores de ámbito de área de nombres en todos los espacios de nombres.

         Tipo: cadena


* **Detalles de clasificación**

   Clasificación (prioridad). Define cómo se determina la \&quot;mejor opción\&quot; teniendo en cuenta el contexto del criterio de decisión. Entre todas las opciones seleccionadas que cumplen las restricciones de perfil, la clasificación decide las opciones superiores (o superiores N) que se proponen.

   Tipo: object

   * **Evaluación de pedidos**

      Evaluación de un orden relativo de una o más opciones de decisión. Las opciones con valores de ordinal más altos se seleccionan sobre cualquier opción con valores de ordinal más bajos. Los valores determinados por este método se pueden ordenar, pero no se pueden medir las distancias entre ellos ni se pueden calcular sumas ni productos. La mediana y el modo son las únicas medidas de tendencia central que pueden utilizarse para los datos ordinales.

      Tipo: object

      * **Función de puntuación**

         Referencia a una función que calcula una puntuación numérica para esta opción de decisión. Las opciones de decisión se ordenarán (clasificarán) según esa puntuación. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con la opción on a la vez. Consulte esquema https://ns.adobe.com/experience/decisioning/function.

         Tipo: cadena

      * **Tipo de evaluación de pedido**

         Especifica qué mecanismo de evaluación de pedidos se utiliza, prioridad estática de las opciones de decisión, función de puntuación que calcula un valor numérico para cada opción o estrategia de clasificación que recibe una lista para solicitarla.

         Tipo: cadena

      * **Estrategia de clasificación**

         Referencia a una estrategia que clasifica una opción de lista de decisiones. Las opciones de decisión se devolverán en una lista ordenada. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con la opción on a la vez. Consulte esquema https://ns.adobe.com/experience/decisioning/rankingStrategy.

         Tipo: cadena
   * **Prioridad**

      Prioridad de una única opción de decisión en relación con todas las demás opciones. Las opciones para las que no se ha dado ninguna función de orden se priorizan usando esta propiedad. Las opciones con valores de prioridad más altos se seleccionan antes que las opciones con prioridad más baja. Si dos o más opciones cualificadas comparten el valor de prioridad más alto, se elige uno de forma aleatoria uniforme y se utiliza para la propuesta de decisión.

      Tipo: integer

      Valor mínimo: 0

      Valor predeterminado: 0


#### Fecha y hora de finalización de la actividad

Fecha de finalización de la decisión y hora de finalización. La propiedad tiene la semántica de la propiedad &#39;endTime&#39; de schema.org definida en http://schema.org/Action.

Tipo: cadena

#### Opción de reserva

La referencia a una opción de reserva que se utiliza al tomar decisiones en el contexto de esta decisión no califica ninguna de las opciones normales (esto suele ocurrir cuando se aplican restricciones duras). El valor es el URI (@id) de la opción de reserva a la que se hace referencia.

Tipo: cadena

#### Nombre de la actividad

Nombre de decisión que se muestra en varias interfaces de usuario.

Tipo: cadena

#### Fecha y hora de inicio de la actividad

Fecha de inicio y hora de finalización de la decisión. La propiedad tiene la semántica de la propiedad &#39;startTime&#39; de schema.org definida en http://schema.org/Action.

Tipo: cadena

## _repo

### ETG de actividad

Revisión en la que se encontraba el objeto de decisión cuando se tomó la instantánea.

Tipo: cadena
