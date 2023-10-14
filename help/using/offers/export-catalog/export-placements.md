---
title: Conjunto de datos de ubicaciones
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para las ubicaciones
feature: Offers, Datasets
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 5%

---

# Conjunto de datos de ubicaciones {#placements-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las ubicaciones.

![](../assets/dataset-placements.png)

El lote exitoso más reciente en el conjunto de datos se muestra a la derecha. La vista jerárquica del esquema del conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden utilizar en la **[!UICONTROL Repositorio de objetos de decisión: ubicaciones]** conjunto de datos.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ Identificador

**Campo:** _id
**Título:** Identificador
**Descripción:** Un identificador único del registro.
**Tipo:** cadena

+++

+++ _experiencia

**Campo:** _experience
**Tipo:** objeto

+++

+++ _experience > toma de decisiones

**Campo:** toma de decisiones
**Tipo:** objeto

+++

+++ _experience > decisioning > Identificador de canal de la ubicación

**Campo:** channelID
**Título:** Identificador de canal de la ubicación
**Descripción:** El canal en el que se hizo la propuesta. El valor es un URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.
**Tipo:** cadena

+++

+++ _experience > decisiones > Tipo de componente de contenido

**Campo:** componentType
**Título:** Tipo de componente de contenido
**Descripción:** Un conjunto enumerado de URI en el que cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.
**Tipo:** cadena

+++

+++ _experience > decisioning > contentTypes

**Campo:** contentTypes
**Tipo:** matriz

+++

+++_experiencia > Toma de decisiones > contentTypes > Tipo de medio MIME

**Título:** Tipo de medio MIME
**Descripción:** Una restricción para el tipo de medio de los componentes que se espera en esa ubicación. Podría haber más de un tipo de medio posible para un componente, como un formato de imagen diferente.
**Tipo:** cadena

+++

+++ _experience > decisioning > Descripción de ubicación

**Campo:** description
**Título:** Descripción de ubicación
**Descripción:** Se utiliza para transmitir intenciones legibles en lenguaje natural sobre cómo se utiliza el contenido dinámico en la entrega general de mensajes. Que un espacio determinado sea un \&quot;Banner\&quot; en una página web se transmite a menudo a través de la descripción y no por un método formal.
**Tipo:** cadena

+++

+++ _experience > decisioning > Nombre de ubicación

**Campo:** name
**Título:** Nombre de ubicación
**Descripción:** Un nombre asignado para la ubicación para hacer referencia a él en interacciones humanas.
**Tipo:** cadena

+++

+++ _repo

**Campo:** _repo
**Tipo:** objeto

+++

+++ _repo > Ubicación ETag

**Campo:** etag
**Título:** ETag de colocación
**Descripción:** Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.
**Tipo:** cadena

+++
