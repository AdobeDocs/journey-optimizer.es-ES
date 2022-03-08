---
title: 'Ofertas de reserva: conjunto de datos'
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para ofertas de reserva
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 3%

---

# Ofertas de reserva: conjunto de datos {#fallback-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para ofertas de reserva.

![](../assets/dataset-fallback.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden utilizar en la variable **[!UICONTROL Decision Object Repository - Fallback Offers]** conjunto de datos.

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

#### _experiencia > decisiones > características

**Campo:** características
**Título:** Características de la opción de decisión
**Descripción:** Propiedades o atributos adicionales que pertenecen a esta opción de decisión en particular. Las diferentes instancias pueden tener características diferentes (claves en el mapa). Las características son pares de valor de nombre que se utilizan para distinguir una opción de decisión de otras. Las características se utilizan como valores en el contenido que representa esta opción de decisión y como características para analizar y optimizar el rendimiento de una opción. Cuando cada instancia tiene el mismo atributo o propiedad, ese aspecto debe modelarse como un esquema de extensión que se derive del detalle de la opción de decisión.
**Tipo:** object

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

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
      **Descripción:** La manifestación física o digital del recurso. Normalmente, Format debe incluir el tipo de medio del recurso. El formato puede utilizarse para determinar el software, el hardware u otro equipo necesario para visualizar o utilizar el recurso. Una práctica recomendada es seleccionar un valor de un vocabulario controlado (por ejemplo, la lista de [Tipos de medios de Internet](http://www.iana.org/ asignaciones/tipos de medios/) que definen formatos de medios de equipo).
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

   **Campo:** linkURL
   **Descripción:** Un localizador de recursos único opcional para interacciones del usuario. Esta URL se utiliza para remitir al usuario final a en un agente de usuario y se puede realizar un seguimiento.
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

#### _experience > decisiones > etiquetas

**Campo:** etiquetas
**Título:** Etiquetas
**Descripción:** Conjunto de etiquetas asociadas a esta entidad. Las etiquetas se utilizan en expresiones de filtro para restringir el inventario general a un subconjunto (categoría).
**Tipo:** matriz

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo {#repo}

**Campo:** _repo
**Tipo:** object

### _repo > Opción de decisión ETag

**Campo:** etiqueta
**Título:** Opción de decisión ETag
**Descripción:** Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.
**Tipo:** cadena
