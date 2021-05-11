---
title: Conjunto de datos de ofertas personalizadas
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para ofertas.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1789'
ht-degree: 3%

---

# Conjunto de datos de ofertas personalizadas {#offers-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para ofertas de contenido personalizado.

![](../assets/dataset-offers.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Las ofertas personalizadas forman el conjunto de opciones para una decisión. El objetivo de la adopción de decisiones es realizar un gran inventario de artículos y aplicar numerosas reglas de restricción a ese inventario para reducirlo y clasificar las opciones que reúnen los requisitos según un criterio. Las propuestas resultantes ensamblan y personalizan la experiencia para individuos específicos.

Esta es la lista de todos los campos que se pueden utilizar en el conjunto de datos **[!UICONTROL Decision Object Repository - Personalized Offers]**.

## Identificador

Identificador único del registro.
Tipo: cadena

## _experiencia

### decisioning

#### calendarConstraints

**Detalles de restricción del calendario**. Las restricciones del calendario deciden si una opción de decisión es válida en un intervalo de fechas. Fuera de ese intervalo de fechas, no se puede proponer la opción .
Tipo: object

* **Fecha y hora de finalización**

   La fecha de finalización de la validez de las opciones de decisión. Las opciones que han pasado su fecha de finalización ya no pueden proponerse en el proceso de toma de decisiones.

   Tipo: cadena

* **Fecha y hora de inicio**

   La fecha de inicio de validez de las opciones de decisión. Las opciones que aún no han alcanzado su fecha de inicio no se pueden proponer en el proceso de toma de decisiones.

   Tipo: cadena

#### características

**Características de la opción de decisión**. Propiedades o atributos adicionales que pertenecen a esta opción de decisión en particular. Las diferentes instancias pueden tener características diferentes (claves en el mapa). Las características son pares de valor de nombre que se utilizan para distinguir una opción de decisión de otras. Las características se utilizan como valores en el contenido que representa esta opción de decisión y como características para analizar y optimizar el rendimiento de una opción. Cuando cada instancia tiene el mismo atributo o propiedad, ese aspecto debe modelarse como un esquema de extensión que se derive del detalle de la opción de decisión.

Tipo: object

#### contenido

**Detalles de contenido**. Elementos de contenido para representar el elemento de decisión en diferentes contextos. Una sola opción de decisión puede tener varias variantes de contenido. El contenido es información dirigida a una audiencia para su consumo en una experiencia (digital). El contenido se entrega a través de canales en una ubicación determinada.

Tipo: matriz

* ****
componentesComponentes del contenido que representan la opción de decisión, incluidas todas sus variantes de idioma. Los componentes específicos se encuentran en &quot;dx:format&quot;, &quot;dc:subject&quot; y &quot;dc:language&quot; o en una combinación de ellos. Estos metadatos se utilizan para localizar o representar el contenido asociado a una oferta e integrarlos según el contrato de colocación.

   * **Content Component**
TypeConjunto enumerado de URIs donde cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.
Tipo: cadena

   * **_dc**

      * ****
FormatoLa manifestación física o digital del recurso. Normalmente, Format debe incluir el tipo de medio del recurso. El formato puede utilizarse para determinar el software, el hardware u otro equipo necesario para visualizar o utilizar el recurso. La práctica recomendada es seleccionar un valor de un vocabulario controlado (por ejemplo, la lista de [Internet Media Types](http://www.iana.org/ asignaciones/tipos de medios/) que define los formatos de medios de equipo).

         Tipo: cadena

         Ejemplo: &quot;application/vnd.adobe.photoshop&quot;

      * ****
IdiomaEl idioma o los idiomas del recurso.\nLos idiomas se especifican en el código de idioma tal como se define en [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), que forma parte de BCP 47, que se utiliza en otras partes en XDM.

         Tipo: cadena

         Ejemplos: &quot;/n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
   * **_repo**

      * **id**

         Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se usan las API de plataforma para recuperar la representación, el cliente puede esperar que una propiedad adicional \&quot;repo:resolveUrl\&quot; recupere el recurso.

         Tipo: cadena

      * **name**

         Algunas sugerencias sobre dónde ubicar el repositorio que almacena el recurso externo por \&quot;repo:id\&quot;.

         Tipo: cadena

      * **repositoryID**

         Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se usan las API de plataforma para recuperar la representación, el cliente puede esperar que una propiedad adicional \&quot;repo:resolveUrl\&quot; recupere el recurso.

         Tipo: cadena

         Ejemplo: &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         Un localizador de recursos único opcional para leer el recurso en un repositorio de contenido. Esto facilitará la obtención del recurso sin que el cliente entienda dónde se administra el recurso y qué API llamar. Esto es similar a un enlace HAL pero la semántica es más simple y útil.

         Tipo: cadena

         Ejemplo: &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&amp;quot&quot;
   * **content**

      Campo opcional para guardar contenido directamente. En lugar de hacer referencia al contenido en un repositorio de recursos, el componente puede incluir contenido simple directamente. Este campo no se utiliza para recursos de contenido compuesto, complejo y binario.

      Tipo: cadena

   * **deliveryURL**

      Un localizador de recursos único opcional para obtener el recurso de una red de entrega de contenido o de un extremo de servicio. Esta URL la utiliza un agente de usuario para acceder al recurso públicamente.

      Tipo: cadena

      Ejemplo: &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      Un localizador de recursos único opcional para interacciones del usuario. Esta URL se utiliza para remitir al usuario final a en un agente de usuario y se puede realizar un seguimiento.

      Tipo: cadena

      Ejemplo: &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg



* **Colocación**

   Colocación para cumplir. El valor es el URI (@id) de la ubicación de la oferta a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.

#### Estado del ciclo vital

El estado del ciclo de vida permite realizar flujos de trabajo con un objeto. El estado puede afectar a los lugares en los que un objeto es visible o se considera relevante. Los cambios de estado los realizan los clientes o servicios que utilizan los objetos.
Tipo: string
Valores posibles: Borrador, aprobado, activo, completado, archivado

#### Nombre de opción de decisión

Nombre de la opción. El nombre se muestra en varias interfaces de usuario.
Tipo: cadena

#### Detalles de restricción de perfil

Las restricciones de perfil deciden si una opción es apta para esta identidad de perfil, en este momento, en este contexto. Si la restricción de perfil no necesita tener en cuenta los valores de cada una de las opciones, es decir, no tiene en cuenta las opciones de la selección de opciones, la restricción de perfil que se evalúa como &quot;false&quot; cancela toda la selección de opciones. Por otro lado, se evalúa una regla de restricción de perfil que toma una opción como parámetro para cada opción de calificación de la selección de opciones.
Tipo: object

* **Descripción**

   Descripción de restricción de perfil. Se utiliza para transmitir intenciones legibles sobre cómo o por qué se construyó esta restricción de perfil y/o qué opción incluirá o excluirá.
Tipo: cadena

* **Regla de elegibilidad**

   Referencia a una regla de decisión que se evalúa como true o false para un perfil determinado u otros objetos XDM contextuales dados. La regla se utiliza para decidir si la opción cumple los requisitos de un perfil determinado. El valor es el URI (@id) de la regla de decisión a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/rule.

   Tipo: cadena

* **Tipo de restricción de perfil**

   Determina si hay restricciones establecidas actualmente y cómo se expresan las restricciones. Podría ser mediante una regla o a través de una o más suscripciones a segmentos.
Tipo: string
Valores posibles:

   * ninguna

   * &quot;eligibilityRule&quot;: &quot;La restricción de perfil se expresa como una regla única que debe evaluarse como verdadera antes de permitir la acción restringida&quot;,

   * &quot;Cualquier segmento&quot;: &quot;La restricción de perfil se expresa como uno o más segmentos y el perfil debe ser miembro de al menos uno de ellos antes de permitir la acción restringida&quot;,

   * &quot;Todos los segmentos&quot;: &quot;La restricción de perfil se expresa como uno o más segmentos y el perfil debe ser miembro de todos ellos antes de permitir la acción restringida&quot;,

   * &quot;reglas&quot;: &quot;La restricción de perfil se expresa como una serie de reglas diferentes, por ejemplo, idoneidad, aplicabilidad, idoneidad, que todos deben evaluar como true antes de permitir la acción restringida&quot;

* **Identificadores de segmento**

   Identificadores de los segmentos

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


#### Detalles de clasificación

Clasificación (prioridad). Define lo que se considera la \&quot;mejor acción\&quot; dado el contexto del criterio de decisión. Entre todas las opciones seleccionadas que cumplan la restricción de elegibilidad, el orden de clasificación decidirá las opciones superiores (o superiores N) que se propongan.

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

      Valores posibles: &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot; <!--(TBC)-->

   * **Estrategia de clasificación**

      Referencia a una estrategia que clasifica una opción de lista de decisiones. Las opciones de decisión se devolverán en una lista ordenada. El valor de esta propiedad es el URI (@id) de la función que se va a invocar con la opción on a la vez. Consulte esquema https://ns.adobe.com/experience/decisioning/rankingStrategy.

      Tipo: cadena

* **Prioridad**

   Prioridad de una única opción de decisión en relación con todas las demás opciones. Las opciones para las que no se ha dado ninguna función de orden se priorizan usando esta propiedad. Las opciones con valores de prioridad más altos se seleccionan antes que las opciones con prioridad más baja. Si dos o más opciones cualificadas comparten el valor de prioridad más alto, se elige uno de forma aleatoria uniforme y se utiliza para la propuesta de decisión.

   Tipo: integer

   Valor mínimo: 0

   Valor predeterminado: 0

#### Etiquetas

Conjunto de etiquetas asociadas a esta entidad. Las etiquetas se utilizan en expresiones de filtro para restringir el inventario general a un subconjunto (categoría).

* **items**

   Identificador de un objeto de etiqueta. El valor es el @id de la etiqueta a la que se hace referencia. Consulte esquema de etiquetas: https://ns.adobe.com/experience/decisioning/tag.

## _repo

### Opción de decisión ETag

Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.

Tipo: cadena



