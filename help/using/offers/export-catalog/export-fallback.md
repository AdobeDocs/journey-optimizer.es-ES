---
title: 'Ofertas de reserva: conjunto de datos'
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para ofertas de reserva.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 5%

---

# El conjunto de datos de ofertas de reserva {#fallback-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para ofertas de reserva.

![](../assets/dataset-fallback.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden utilizar en el conjunto de datos **[!UICONTROL Decision Object Repository - Fallback Offers]**.

## Identificador

Identificador único del registro.

Tipo: cadena

## _experiencia

### decisioning

#### características

**Características de la opción de decisión**. Propiedades o atributos adicionales que pertenecen a esta opción de decisión en particular. Las diferentes instancias pueden tener características diferentes (claves en el mapa). Las características son pares de valor de nombre que se utilizan para distinguir una opción de decisión de otras. Las características se utilizan como valores en el contenido que representa esta opción de decisión y como características para analizar y optimizar el rendimiento de una opción. Cuando cada instancia tiene el mismo atributo o propiedad, ese aspecto debe modelarse como un esquema de extensión que se derive del detalle de la opción de decisión.

Tipo: object

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### contenido

**Detalles de contenido**. Elementos de contenido para representar el elemento de decisión en diferentes contextos. Una sola opción de decisión puede tener varias variantes de contenido. El contenido es información dirigida a una audiencia para su consumo en una experiencia (digital). El contenido se entrega a través de canales en una ubicación determinada.

Tipo: matriz

* **componentes**

   Los componentes del contenido que representan la opción de decisión, incluidas todas sus variantes de idioma. Los componentes específicos se encuentran en &quot;dx:format&quot;, &quot;dc:subject&quot; y &quot;dc:language&quot; o en una combinación de ellos. Estos metadatos se utilizan para localizar o representar el contenido asociado a una oferta e integrarlos según el contrato de colocación.

   Tipo: matriz

   * **Tipo de componente de contenido**

      Un conjunto enumerado de URI donde cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.

      Tipo: cadena

   * **_dc**

      * **Formato**

         La manifestación física o digital del recurso. Normalmente, Format debe incluir el tipo de medio del recurso. El formato puede utilizarse para determinar el software, el hardware u otro equipo necesario para visualizar o utilizar el recurso. La práctica recomendada es seleccionar un valor de un vocabulario controlado (por ejemplo, la lista de [Internet Media Types](http://www.iana.org/ asignaciones/tipos de medios/) que define los formatos de medios de equipo).

         Tipo: cadena

      * **Idioma**

         El idioma o los idiomas del recurso.\nLos idiomas se especifican en el código de idioma tal como se define en [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), que forma parte de BCP 47, que se utiliza en otras partes en XDM.

         Tipo: cadena
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

      * **resolveURL**

         Un localizador de recursos único opcional para leer el recurso en un repositorio de contenido. Esto facilitará la obtención del recurso sin que el cliente entienda dónde se administra el recurso y qué API llamar. Esto es similar a un enlace HAL pero la semántica es más simple y útil.

         Tipo: cadena
   * **content**

      Campo opcional para guardar contenido directamente. En lugar de hacer referencia al contenido en un repositorio de recursos, el componente puede incluir contenido simple directamente. Este campo no se utiliza para recursos de contenido compuesto, complejo y binario.

      Tipo: cadena

   * **deliveryURL**

      Un localizador de recursos único opcional para obtener el recurso de una red de entrega de contenido o de un extremo de servicio. Esta URL la utiliza un agente de usuario para acceder al recurso públicamente.

      Tipo: cadena

   * **linkURL**

      Un localizador de recursos único opcional para interacciones del usuario. Esta URL se utiliza para remitir al usuario final a en un agente de usuario y se puede realizar un seguimiento.

      Tipo: cadena



* **Colocación**

   Colocación para cumplir. El valor es el URI (@id) de la ubicación de la oferta a la que se hace referencia. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.

   Tipo: cadena



#### Estado del ciclo vital

El estado del ciclo de vida permite realizar flujos de trabajo con un objeto. El estado puede afectar a los lugares en los que un objeto es visible o se considera relevante. Los cambios de estado los realizan los clientes o servicios que utilizan los objetos.

Tipo: cadena

Valores posibles: &quot;borrador&quot;, &quot;aprobado&quot;, &quot;activo&quot;, &quot;completado&quot;, &quot;archivado&quot;

Valor predeterminado: &quot;borrador&quot;

#### Nombre de opción de decisión

Nombre de opción que se muestra en varias interfaces de usuario.

Tipo: cadena

#### Etiquetas

Conjunto de etiquetas asociadas a esta entidad. Las etiquetas se utilizan en expresiones de filtro para restringir el inventario general a un subconjunto (categoría).

Tipo: matriz

## _repo

### Opción de decisión ETag

Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.

Tipo: cadena
