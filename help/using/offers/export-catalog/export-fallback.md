---
title: Conjunto de datos de ofertas
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para ofertas de reserva
badge: label="Heredado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 2a5591617838e76e9cae99c0f97e8aff59311a69
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%

---

# Conjunto de datos de ofertas {#fallback-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las ofertas de reserva.

El lote exitoso más reciente en el conjunto de datos se muestra a la derecha. La vista jerárquica del esquema del conjunto de datos se muestra en el panel izquierdo.

![](../assets/dataset-fallback.png)

>[!NOTE]
>
>Las ofertas de reserva eliminadas se marcan como archivadas en el conjunto de datos.

Esta es la lista de todos los campos que se pueden usar en el **[!UICONTROL Repositorio de objetos de decisión - Ofertas de reserva]** conjunto de datos.

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

+++ _experience > decisioning > features

**Campo:** características
**Título:** Características de la opción de decisión
**Descripción:** propiedades o atributos adicionales que pertenecen a esta opción de decisión en particular. Las distintas instancias pueden tener diferentes características (claves en el mapa). Las características son pares de nombre-valor que se utilizan para distinguir una opción de decisión de otras. Las características se utilizan como valores en el contenido que representa esta opción de decisión y como características para analizar y optimizar el rendimiento de una opción. Cuando cada instancia tiene el mismo atributo o propiedad, ese aspecto debe modelarse como un esquema de extensión que derive del detalle de la opción de decisión.
**Tipo:** objeto

+++

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

+++ _experience > decisioning > content

**Campo:** contenido
**Título:** Detalles de contenido
**Descripción:** elementos de contenido para procesar el elemento de decisión en diferentes contextos. Una sola opción de decisión puede tener varias variantes de contenido. El contenido es información dirigida a una audiencia para su consumo en una experiencia (digital). El contenido se entrega a través de canales a una ubicación particular.
**Tipo:** matriz

+++

+++_experience > decisioning > content > components

**Campo:** componentes
**Descripción:** Los componentes del contenido que representan la opción de decisión, incluidas todas las variantes de idioma. Los componentes específicos se encuentran en &quot;dx:format&quot;, &quot;dc:subject&quot; y &quot;dc:language&quot; o una combinación de ellos. Estos metadatos se utilizan para localizar o representar el contenido asociado a una oferta e integrarlo según el contrato de colocación.
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
     **Descripción:** La manifestación física o digital del recurso. Normalmente, el formato debe incluir el tipo de medio del recurso. El formato se puede utilizar para determinar el software, hardware u otro equipo necesario para mostrar o utilizar el recurso. La práctica recomendada es seleccionar un valor de un vocabulario controlado (por ejemplo, la lista de [tipos de medios de Internet]&#x200B;(https://www.iana.org/) que definen formatos de medios informáticos).
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
     **Descripción:** Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se utilizan las API de Platform para recuperar la representación, el cliente puede esperar una propiedad \&quot;repo:resolveUrl\&quot; adicional para recuperar el recurso.
     **Tipo:** cadena
     **Ejemplo:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

     **Campo:** nombre
     **Descripción:** Algunas sugerencias sobre dónde ubicar el repositorio que almacena el recurso externo del \&quot;repo:id\&quot;.
     **Tipo:** cadena

   * **ID de repositorio**

     **Campo:** repositoryID
     **Descripción:** Identificador único opcional para hacer referencia al recurso en un repositorio de contenido. Cuando se utilizan las API de Platform para recuperar la representación, el cliente puede esperar una propiedad \&quot;repo:resolveUrl\&quot; adicional para recuperar el recurso.
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

+++

+++ _experience > decisioning > content > Placement

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

+++ _experience > decisioning > etiquetas

**Campo:** etiquetas
**Título:** Etiquetas
**Descripción:** conjunto de calificadores de colección (anteriormente conocidos como &quot;etiquetas&quot;) asociados a esta entidad. Los calificadores de recopilación se utilizan en expresiones de filtro para restringir el inventario general a un subconjunto (categoría).
**Tipo:** matriz

+++

<!--Field without name under collection qualifiers: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++ _repo

**Campo:** _repositorio
**Tipo:** objeto

+++

+++ _repo > Opción de decisión ETag

**Campo:** etag
**Título:** Opción de decisión ETag
**Descripción:** Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.
**Tipo:** cadena

+++
