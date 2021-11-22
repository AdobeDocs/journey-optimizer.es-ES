---
title: Conjunto de datos de ofertas personalizadas
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para ofertas.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '2003'
ht-degree: 3%

---

# Conjunto de datos de ofertas personalizadas {#offers-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para ofertas de contenido personalizado.

![](../../assets/dataset-offers.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden utilizar en la variable **[!UICONTROL Decision Object Repository - Personalized Offers]** conjunto de datos.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## Identificador

**Campo:** _id
**Título:** Identificador
**Descripción:** Identificador único del registro.
**Tipo:** cadena

## _experiencia

**Campo:** _experience
**Tipo:** object

### _experiencia > decisiones

**Campo:** decisioning
**Tipo:** object

#### _experience > decisiones > calendarConstraints

**Field:** calendarConstraints
**Title:** Calendar Constraint Details
**Description:** Calendar constraints decide if a decision option is valid given a date range. Fuera de ese intervalo de fechas, no se puede proponer la opción .
**Tipo:** object

* **Fecha y hora de finalización**

   **Campo:** endDate
   **Título:** Fecha y hora de finalización
   **Descripción:** La fecha de finalización de la validez de las opciones de decisión. Las opciones que han pasado su fecha de finalización ya no se pueden proponer en el proceso de toma de decisiones.
   **Tipo:** cadena

* **Fecha y hora de inicio**

   **Campo:** startDate
   **Título:** Fecha y hora de inicio
   **Descripción:** La fecha de inicio de validez de las opciones de decisión. Las opciones que aún no han alcanzado su fecha de inicio no se pueden proponer en el proceso de toma de decisiones.
   **Tipo:** cadena

#### _experiencia > decisiones > características

**Campo:** características
**Título:** Características de la opción de decisión
**Descripción:** Propiedades o atributos adicionales que pertenecen a esta opción de decisión en particular. Las diferentes instancias pueden tener características diferentes (claves en el mapa). Las características son pares de valor de nombre que se utilizan para distinguir una opción de decisión de otras. Las características se utilizan como valores en el contenido que representa esta opción de decisión y como características para analizar y optimizar el rendimiento de una opción. Cuando cada instancia tiene el mismo atributo o propiedad, ese aspecto debe modelarse como un esquema de extensión que se derive del detalle de la opción de decisión.
**Tipo:** object

#### _experience > decisioning > content

**Campo:** contenido
**Título:** Detalles de contenido
**Descripción:** Elementos de contenido para representar el elemento de decisión en diferentes contextos. Una sola opción de decisión puede tener varias variantes de contenido. El contenido es información dirigida a una audiencia para su consumo en una experiencia (digital). El contenido se entrega a través de canales en una ubicación determinada.
**Tipo:** matriz

**_experience > decisioning > content > components**

**Campo:** componentes
**Descripción:** Los componentes del contenido que representan la opción de decisión, incluidas todas sus variantes de idioma. Los componentes específicos se encuentran en &quot;dx:format&quot;, &quot;dc:subject&quot; y &quot;dc:language&quot; o en una combinación de ellos. Estos metadatos se utilizan para localizar o representar el contenido asociado a una oferta e integrarlos según el contrato de colocación.
**Tipo:** matriz
**Requerido:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisioning > content > components > Content Component Type**

   **Campo:** _type
   **Título:** Tipo de componente de contenido
   **Descripción:** Un conjunto enumerado de URI donde cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.
   **Tipo:** cadena

* **_experience > decisioning > content > components > _dc**

   **Campo:** _dc
   **Tipo:** object
   **Requerido:** &quot;format&quot;

   * **Formato**

      **Campo:** format
      **Título:** Formato
      **Descripción:** La manifestación física o digital del recurso. Normalmente, Format debe incluir el tipo de medio del recurso. Format may be used to determine the software, hardware or other equipment needed to display or operate the resource. Una práctica recomendada es seleccionar un valor de un vocabulario controlado (por ejemplo, la lista de [Tipos de medios de Internet](http://www.iana.org/assignments/media-types/) definición de formatos multimedia del equipo).
      **Tipo:** cadena
      **Ejemplo:** &quot;application/vnd.adobe.photoshop&quot;

   * **Idioma**
      **Campo:** language
      **Título:** Idioma
      **Descripción:** El idioma o los idiomas del recurso. \nLos idiomas se especifican en el código de idioma tal como se define en [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), que forma parte de BCP 47, que se utiliza en otras partes de XDM.
      **Tipo:** matriz
      **Ejemplos:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > decisioning > content > components > _repo**

   **Campo:** _repo
   **Tipo:** object

   * **id**

      **Campo:** id
      **Descripción:** Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se usan las API de plataforma para recuperar la representación, el cliente puede esperar que una propiedad adicional \&quot;repo:resolveUrl\&quot; recupere el recurso.
      **Tipo:** cadena
      **Ejemplo:** urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

      **Campo:** name
      **Descripción:** Algunas sugerencias sobre dónde ubicar el repositorio que almacena el recurso externo por \&quot;repo:id\&quot;.
      **Tipo:** cadena

   * **repositoryID**

      **Campo:** repositoryID
      **Descripción:** Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se usan las API de plataforma para recuperar la representación, el cliente puede esperar que una propiedad adicional \&quot;repo:resolveUrl\&quot; recupere el recurso.
      **Tipo:** cadena
      **Ejemplo:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **Campo:** resolveURL
      **Descripción:** Un localizador de recursos único opcional para leer el recurso en un repositorio de contenido. Esto facilitará la obtención del recurso sin que el cliente entienda dónde se administra el recurso y qué API llamar. Esto es similar a un vínculo HAL, pero la semántica es más simple y tiene más propósito.
      **Tipo:** cadena
      **Ejemplo:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience > decisioning > content > components > content**

   **Campo:** contenido
   **Descripción:** Campo opcional para guardar contenido directamente. En lugar de hacer referencia al contenido en un repositorio de recursos, el componente puede incluir contenido simple directamente. Este campo no se utiliza para recursos de contenido compuesto, complejo y binario.
   **Tipo:** cadena

* **_experience > decisioning > content > components > deliveryURL**

   **Campo:** deliveryURL
   **Descripción:** Un localizador de recursos único opcional para obtener el recurso de una red de entrega de contenido o de un extremo de servicio. Esta URL la utiliza un agente de usuario para acceder al recurso públicamente.
   **Tipo:** cadena
   **Ejemplo:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > content > components > linkURL**

   **Field:** linkURL
   **Description:** An optional unique resource locator for user interactions. This URL is used to refer the end user to in a user agent and can be tracked.
   **Tipo:** cadena
   **Ejemplo:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning > content > Placement**

**Campo:** placement
**Título:** Colocación
**Descripción:** Colocación para cumplir. El valor es el URI (@id) de la ubicación de la oferta a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.
**Tipo:** cadena

#### _experience > decisiones > Estado del ciclo vital

**Campo:** lifecycleStatus
**Título:** Estado del ciclo vital
**Descripción:** El estado del ciclo de vida permite realizar flujos de trabajo con un objeto. El estado puede afectar a los lugares en los que un objeto es visible o se considera relevante. Los cambios de estado los realizan los clientes o servicios que utilizan los objetos.
**Tipo:** string
**Valores posibles:** &quot;Borrador&quot; (predeterminado), &quot;Aprobado&quot;, &quot;Activo&quot;, &quot;Completado&quot;, &quot;Archivado&quot;

#### _experience > decisioning > Nombre de la opción de decisión

**Campo:** name
**Título:** Nombre de opción de decisión
**Descripción:** Nombre de opción que se muestra en varias interfaces de usuario.
**Tipo:** cadena

#### _experience > decisioning > profileConstraints

**Field:** profileConstraints
**Title:** Profile Constraint Details
**Description:** The profile constraints decide if an option is eligible for this profile identity, at this moment, in this context. Si la restricción de perfil no necesita tener en cuenta los valores de cada una de las opciones, es decir, no tiene en cuenta las opciones de la selección de opciones, la restricción de perfil que se evalúa como &quot;false&quot; cancela toda la selección de opciones. Por otro lado, se evalúa una regla de restricción de perfil que toma una opción como parámetro para cada opción correspondiente de la selección de opciones.
**Tipo:** object

**_experience > decisiones > profileConstraints > Descripción**

**Campo:** descripción
**Título:** Descripción
**Descripción:** Descripción de restricción de perfil. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se construyó esta restricción de perfil y/o qué opción incluirá o excluirá.
**Tipo:** cadena

**_experience > decisiones > profileConstraints > Regla de elegibilidad**

**Field:** eligibilityRule
**Title:** Eligibility Rule
**Description:** A reference to a decision rule that evaluates to true or false for a given profile and/or other given contextual XDM objects. The rule is used to decide if the option qualifies for a given profile. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. See schema https://ns.adobe.com/experience/decisioning/rule.
**Tipo:** cadena

**_experience > decisioning > profileConstraints > Tipo de restricción de perfil**

**Campo:** profileConstraintType
**Título:** Tipo de restricción de perfil
**Descripción:** Determina si hay restricciones establecidas actualmente y cómo se expresan. Podría ser a través de una regla o a través de una o más suscripciones a segmentos.
**Tipo:** string
**Valores posibles:**
* &quot;none&quot; (predeterminado)
* &quot;eligibilityRule&quot;: &quot;La restricción de perfil se expresa como una regla única que debe evaluarse como verdadera antes de permitir la acción restringida.&quot;
* &quot;anySegments&quot;: &quot;La restricción de perfil se expresa como uno o más segmentos y el perfil debe ser miembro de al menos uno de ellos antes de permitir la acción restringida.&quot;
* &quot;allSegments&quot;: &quot;La restricción de perfil se expresa como uno o más segmentos y el perfil debe ser miembro de todos ellos antes de permitir la acción restringida.&quot;
* &quot;reglas&quot;: &quot;La restricción de perfil se expresa como una serie de reglas diferentes, por ejemplo, idoneidad, aplicabilidad, idoneidad, que todos deben evaluar como true antes de permitir la acción restringida.&quot;

**_experience > decisiones > profileConstraints > Identificadores de segmentos**

**Campo:** segmentIdentities
**Título:** Identificadores de segmento
**Descripción:** Identificadores de los segmentos
**Tipo:** matriz

* **Identificador**

   **Field:** _id
   **Title:** Identifier
   **Descripción:** Identidad del segmento en el área de nombres relacionada.
   **Tipo:** cadena

* **Área de nombres**

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

#### _experiencia > decisiones > clasificación

**Campo:** clasificación
**Título:** Detalles de clasificación
**Descripción:** Clasificación (prioridad). Define lo que se considera la \&quot;mejor acción\&quot; dado el contexto del criterio de decisión. Entre todas las opciones seleccionadas que cumplan la restricción de elegibilidad, el orden de clasificación decidirá las opciones superiores (o superiores N) que se propongan.
**Type:** object

**_experience > decisioning > ranking > Evaluación de pedidos**

**Campo:** pedido
**Título:** Evaluación de pedidos
**Descripción:** Evaluación de un orden relativo de una o más opciones de decisión. Options with higher ordinal values are selected over any options with lower ordinal values. Los valores determinados por este método se pueden ordenar, pero no se pueden medir las distancias entre ellos ni se pueden calcular sumas ni productos. The median and the mode are the only measures of central tendency that can be used for ordinal data.
**Type:** object

* **Scoring Function**

   **Field:** function
   **Título:** Función de puntuación
   **Descripción:** Referencia a una función que calcula una puntuación numérica para esta opción de decisión. Decision options will then be ordered (ranked) by that score. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con la opción on a la vez. See schema https://ns.adobe.com/experience/decisioning/function.
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

**_experience > decisiones > clasificación > Prioridad**

**Campo:** priority
**Título:** Prioridad
**Descripción:** Prioridad de una única opción de decisión en relación con todas las demás opciones. Las opciones para las que no se proporciona ninguna función de pedido se priorizan usando esta propiedad. Las opciones con valores de prioridad más altos se seleccionan antes que las opciones con prioridad más baja. If two or more qualifying options share the highest priority value, one is chosen at uniform random and used for the decision proposition.
**Tipo:** integer
**Valor mínimo:** 0
**Valor predeterminado:** 0

#### _experience > decisiones > etiquetas

**Campo:** etiquetas
**Título:** Etiquetas
**Descripción:** Conjunto de etiquetas asociadas a esta entidad. Las etiquetas se utilizan en expresiones de filtro para restringir el inventario general a un subconjunto (categoría).
**Tipo:** matriz

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**Campo:** _repo
**Tipo:** object

### _repo > Opción de decisión ETag

**Field:** etag
**Title:** Decision Option ETag
**Description:** The revision that the decision option object was at when the snapshot was taken.
**Tipo:** cadena
