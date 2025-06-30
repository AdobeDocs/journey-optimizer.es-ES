---
title: Conjunto de datos de ofertas personalizadas
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para ofertas
badge: label="Heredado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '1963'
ht-degree: 0%

---

# Conjunto de datos de ofertas personalizadas {#offers-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para ofertas de contenido personalizado.

![](../assets/dataset-offers.png)

El lote exitoso más reciente en el conjunto de datos se muestra a la derecha. La vista jerárquica del esquema del conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden usar en el **[!UICONTROL repositorio de objetos de decisión - ofertas personalizadas]** conjunto de datos.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

+++ Identificador

**Campo:** _id
**Título:** Identificador
**Descripción:** Identificador único del registro.
**Tipo:** cadena

+++

+++ _experiencia {#experience}

**Campo:** _experiencia
**Tipo:** objeto

+++

+++ _experience > toma de decisiones

**Campo:** toma de decisiones
**Tipo:** objeto

+++

+++ _experience > decisioning > calendarConstraints

**Campo:** calendarConstraints
**Título:** Detalles de restricción de calendario
**Descripción:** las restricciones de calendario deciden si una opción de decisión es válida dado un intervalo de fechas. Fuera de ese intervalo de fechas, la opción no se puede proponer.
**Tipo:** objeto

* **Fecha y hora de finalización**

  **Campo:** endDate
  **Título:** Fecha y hora de finalización
  **Descripción:** Fecha de finalización de validez de opciones de decisión. Las opciones que han superado su fecha de finalización ya no se pueden proponer en el proceso de toma de decisiones.
  **Tipo:** cadena

* **Fecha y hora de inicio**

  **Campo:** startDate
  **Título:** Fecha y hora de inicio
  **Descripción:** Fecha de inicio de validez de opciones de decisión. Las opciones que no han alcanzado su fecha de inicio aún no se pueden proponer en el proceso de toma de decisiones.
  **Tipo:** cadena

+++

+++ _experience > decisioning > features

**Campo:** características
**Título:** Características de la opción de decisión
**Descripción:** propiedades o atributos adicionales que pertenecen a esta opción de decisión en particular. Las distintas instancias pueden tener diferentes características (claves en el mapa). Las características son pares de nombre-valor que se utilizan para distinguir una opción de decisión de otras. Las características se utilizan como valores en el contenido que representa esta opción de decisión y como características para analizar y optimizar el rendimiento de una opción. Cuando cada instancia tiene el mismo atributo o propiedad, ese aspecto debe modelarse como un esquema de extensión que derive del detalle de la opción de decisión.
**Tipo:** objeto

+++

+++ _experience > decisioning > content

**Campo:** contenido
**Título:** Detalles de contenido
**Descripción:** elementos de contenido para procesar el elemento de decisión en diferentes contextos. Una sola opción de decisión puede tener varias variantes de contenido. El contenido es información dirigida a una audiencia para su consumo en una experiencia (digital). El contenido se entrega a través de canales a una ubicación particular.
**Tipo:** matriz

+++

+++_experiencia > toma de decisiones > contenido > componentes

**Campo:** componentes
**Descripción:** Los componentes del contenido que representan la opción de decisión, incluidas todas las variantes de idioma. Los componentes específicos se encuentran mediante &quot;dx:format&quot;, &quot;dc:subject&quot; y &quot;dc:language&quot; o una combinación de ellos. Estos metadatos se utilizan para localizar o representar el contenido asociado a una oferta e integrarlo según el contrato de colocación.
**Tipo:** matriz
**Requerido:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > toma de decisiones > content > components > Content Component Type**

  **Campo:** _tipo
  **Título:** Tipo de componente de contenido
  **Descripción:** Un conjunto enumerado de URI donde cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.
  **Tipo:** cadena

* **_experiencia > toma de decisiones > contenido > componentes > _dc**

  **Campo:** _dc
  **Tipo:** objeto
  **Requerido:** &quot;formato&quot;

   * **Formato**

     Formato **Campo:**
     Formato **Título:**
     **Descripción:** La manifestación física o digital del recurso. Normalmente, el formato debe incluir el tipo de medio del recurso. El formato se puede utilizar para determinar el software, hardware u otro equipo necesario para mostrar o utilizar el recurso. La práctica recomendada es seleccionar un valor de un vocabulario controlado (por ejemplo, la lista de [tipos de medios de Internet](https://www.iana.org/assignments/media-types/) que definen formatos de medios de equipos).
     **Tipo:** cadena
     **Ejemplo:** &quot;application/vnd.adobe.photoshop&quot;

   * **Idioma**
     **Campo:** idioma
     **Título:** Idioma
     **Descripción:** Idioma o idiomas del recurso. \nLos idiomas se especifican en el código de idioma tal como se definen en [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), que forma parte de BCP 47, que se usa en otras partes de XDM.
     **Tipo:** matriz
     **Ejemplos:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > toma de decisiones > content > components > _repo**

  **Campo:** _repositorio
  **Tipo:** objeto

   * **id**

     **Campo:** id.
     **Descripción:** Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se utilizan las API de Platform para recuperar la representación, el cliente puede esperar una propiedad adicional \&quot;repo:resolveUrl\&quot; para recuperar el recurso.
     **Tipo:** cadena
     **Ejemplo:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

     **Campo:** nombre
     **Descripción:** Algunas sugerencias sobre dónde ubicar el repositorio que almacena el recurso externo mediante el \&quot;repo:id\&quot;.
     **Tipo:** cadena

   * **ID de repositorio**

     **Campo:** repositoryID
     **Descripción:** Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se utilizan las API de Platform para recuperar la representación, el cliente puede esperar una propiedad adicional \&quot;repo:resolveUrl\&quot; para recuperar el recurso.
     **Tipo:** cadena
     **Ejemplo:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

     **Campo:** resolveURL
     **Descripción:** Un localizador de recursos único opcional para leer el recurso en un repositorio de contenido. Esto facilitará la obtención del recurso sin que el cliente entienda dónde se administra el recurso y a qué API llamar. Esto es similar a un vínculo HAL, pero la semántica es más sencilla y útil.
     **Tipo:** cadena
     **Ejemplo:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > toma de decisiones > content > components > content**

  **Campo:** contenido
  **Descripción:** Un campo opcional para guardar contenido directamente. En lugar de hacer referencia al contenido de un repositorio de recursos, el componente puede contener directamente contenido simple. Este campo no se utiliza para recursos de contenido compuesto, complejo y binario.
  **Tipo:** cadena

* **_experience > decisioning > content > components > deliveryURL**

  **Campo:** deliveryURL
  **Descripción:** Un localizador de recursos único opcional para obtener el recurso de una red de entrega de contenido o un extremo de servicio. Esta URL la utiliza un agente de usuario para acceder públicamente al recurso.
  **Tipo:** cadena
  **Ejemplo:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > toma de decisiones > content > components > linkURL**

  **Campo:** linkURL
  **Descripción:** Un localizador de recursos único opcional para las interacciones del usuario. Esta URL se utiliza para remitir al usuario final a en un agente de usuario y se puede rastrear.
  **Tipo:** cadena
  **Ejemplo:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++_experience > decisioning > content > Placement

**Campo:** ubicación
**Título:** ubicación
**Descripción:** ubicación para cumplir. El valor es el URI (@id) de la ubicación de oferta a la que se hace referencia. Consulte schema https://ns.adobe.com/experience/decisioning/placement.
**Tipo:** cadena

+++

+++ _experience > decisioning > Estado del ciclo vital

**Campo:** lifecycleStatus
**Título:** Estado del ciclo vital
**Descripción:** El estado del ciclo de vida permite que los flujos de trabajo se realicen con un objeto. El estado puede afectar a dónde un objeto es visible o se considera relevante. Los cambios de estado son dirigidos por los clientes o servicios que utilizan los objetos.
**Tipo:** cadena
**Valores posibles:** &quot;Borrador&quot; (predeterminado), &quot;Aprobado&quot;, &quot;Activo&quot;, &quot;Completado&quot;, &quot;Archivado&quot;

+++

+++ _experience > decisioning > Nombre de opción de decisión

**Campo:** nombre
**Título:** Nombre de opción de decisión
**Descripción:** Nombre de opción que se muestra en varias interfaces de usuario.
**Tipo:** cadena

+++

+++ _experience > decisioning > profileConstraints

**Campo:** profileConstraints
**Título:** Detalles de restricción de perfil
**Descripción:** las restricciones de perfil deciden si una opción es elegible para esta identidad de perfil, en este momento, en este contexto. Si la restricción de perfil no necesita tener en cuenta los valores de cada una de las opciones, es decir, si es invariante de las opciones de la selección de opciones, la restricción de perfil que se evalúa como &#39;false&#39; cancela toda la selección de opciones. Por otro lado, una regla de restricción de perfil que toma una opción como parámetro se evalúa para cada opción correspondiente de la selección de opciones.
**Tipo:** objeto

+++

+++_experience > decisioning > profileConstraints > Description

**Campo:** descripción
**Título:** Descripción
**Descripción:** descripción de restricción de perfil. Se utiliza para transmitir intenciones legibles por el ser humano sobre cómo o por qué se construyó esta restricción de perfil y/o qué opción se incluirá o excluirá en ella.
**Tipo:** cadena

+++

+++_experience > decisioning > profileConstraints > Eligibility Rule

**Campo:** eligibilityRule
**Título:** Regla De Elegibilidad
**Descripción:** Referencia a una regla de decisión que se evalúa como verdadera o falsa para un perfil determinado u otros objetos XDM contextuales determinados. La regla se utiliza para decidir si la opción cumple los requisitos para un perfil determinado. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte schema https://ns.adobe.com/experience/decisioning/rule.
**Tipo:** cadena

+++

+++_experience > decisioning > profileConstraints > Profile Constraint Type

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

+++_experience > decisioning > profileConstraints > Segment Identifiers

**Campo:** segmentIdentities
**Título:** Identificadores De Segmento
**Descripción:** identificadores de las audiencias
**Tipo:** matriz

* **Identificador**

  **Campo:** _id
  **Título:** Identificador
  **Descripción:** identidad de las audiencias en el área de nombres relacionada.
  **Tipo:** cadena

* **Área de nombres**

  **Campo:** espacio de nombres
  **Título:** Espacio de nombres
  **Descripción:** espacio de nombres asociado con el atributo `xid`.
  **Tipo:** objeto
  **Requerido:** &quot;código&quot;

   * **Código**

     **Campo:** código
     Código **Title:**
     **Descripción:** El código es un identificador en lenguaje natural para el área de nombres y se puede usar para solicitar la identificación técnica del área de nombres que se usa para el procesamiento del gráfico de identidades.
     **Tipo:** cadena

* **Identificador de experiencia**

  **Campo:** xid
  **Título:** Identificador de experiencia
  **Descripción:** Cuando está presente, este valor representa un identificador de área de nombres cruzado que es único en todos los identificadores de ámbito de área de nombres en todas las áreas de nombres.
  **Tipo:** cadena

+++

+++ _experience > decisioning > clasificación

Clasificación **Campo:**
**Título:** Detalles de clasificación
**Descripción:** Clasificación (prioridad). Define lo que se considera la \&quot;mejor acción\&quot; dado el contexto del criterio de decisión. Entre todas las opciones seleccionadas que cumplen con las restricciones de elegibilidad, el orden de clasificación decidirá las opciones principales (o N principales) que se propondrán.
**Tipo:** objeto

+++

+++_experience > decisioning > ranking > Evaluación de pedidos

**Campo:** pedido
**Título:** Evaluación de pedidos
**Descripción:** evaluación de un orden relativo de una o más opciones de decisión. Las opciones con valores ordinales más altos se seleccionan sobre las opciones con valores ordinales más bajos. Los valores determinados por este método pueden ordenarse, pero no pueden medirse las distancias entre ellos ni tampoco pueden calcularse las sumas ni los productos. La mediana y el modo son las únicas medidas de tendencia central que se pueden utilizar para los datos ordinales.
**Tipo:** objeto

* **Función de puntuación**

  **Campo:** función
  **Título:** función de puntuación
  **Descripción:** Referencia a una función que calcula una puntuación numérica para esta opción de decisión. Las opciones de decisión se ordenarán (clasificarán) según esa puntuación. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con una opción a la vez. Consulte schema https://ns.adobe.com/experience/decisioning/function.
  **Tipo:** cadena

* **Tipo de evaluación de pedido**

  **Campo:** orderEvaluationType
  **Título:** Tipo de evaluación de pedido
  **Descripción:** Especifica qué mecanismo de evaluación de pedidos se utiliza, la prioridad estática de las opciones de decisión, una función de puntuación que calcula un valor numérico para cada opción o un modelo de IA que recibe una lista para ordenarla.
  **Tipo:** cadena
  **Valores posibles:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* **Estrategia de clasificación**

  **Campo:** rankingStrategy
  **Título:** Estrategia de clasificación
  **Descripción:** Referencia a una estrategia que clasifica una lista de opciones de decisión. Las opciones de decisión se devolverán en una lista ordenada. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con una opción a la vez. Consulte schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
  **Tipo:** cadena

+++

+++_experiencia > toma de decisiones > clasificación > Prioridad

**Campo:** prioridad
**Título:** Prioridad
**Descripción:** Prioridad de una sola opción de decisión en relación con todas las demás opciones. Las opciones para las que no se proporciona ninguna función de orden se priorizan mediante esta propiedad. Las opciones con valores de prioridad más altos se seleccionan antes que las opciones de prioridad más baja. Si dos o más opciones elegibles comparten el valor de prioridad más alto, se elige una al azar uniforme y se usa para la propuesta de decisión.
**Tipo:** entero
**Valor mínimo:** 0
**Valor predeterminado:** 0

+++

+++ _experience > decisioning > etiquetas

**Campo:** etiquetas
**Título:** Etiquetas
**Descripción:** conjunto de calificadores de colección (anteriormente conocidos como &quot;etiquetas&quot;) asociados a esta entidad. Los calificadores de recopilación se utilizan en expresiones de filtro para restringir el inventario general a un subconjunto (categoría).
**Tipo:** matriz

+++

<!--Field without name under tags: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++_repo

**Campo:** _repositorio
**Tipo:** objeto

+++

+++ _repo > Opción de decisión ETag

**Campo:** etag
**Título:** Opción de decisión ETag
**Descripción:** Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.
**Tipo:** cadena

+++
