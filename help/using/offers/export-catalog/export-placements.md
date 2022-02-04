---
title: Conjunto de datos de ubicaciones
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para las ubicaciones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 0545cda9f91ff18791310a4ee2463b2287ac7557
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 5%

---

# Conjunto de datos de ubicaciones {#placements-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las ubicaciones.

![](../../assets/dataset-placements.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden utilizar en la variable **[!UICONTROL Decision Object Repository - Placements]** conjunto de datos.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

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

#### _experience > decisiones > Identificador de canal de la colocación

**Campo:** channelID
**Título:** Identificador de canal de la colocación
**Descripción:** Canal en el que se realizó la propuesta. El valor es un URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.
**Tipo:** cadena

#### _experience > decisioning > Content Component Type

**Campo:** componentType
**Título:** Tipo de componente de contenido
**Descripción:** Un conjunto enumerado de URI donde cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.
**Tipo:** cadena

#### _experience > decisiones > contentTypes

**Campo:** contentTypes
**Tipo:** matriz

**_experience > decisioning > contentTypes > MIME Media Type**

**Título:** Tipo de medio MIME
**Descripción:** Restricción para el tipo de contenido de los componentes que se espera en esa ubicación. Podría haber más de un tipo de medio posible para un componente, como un formato de imagen diferente.
**Tipo:** cadena

#### _experience > decisioning > Placement Description

**Campo:** descripción
**Título:** Descripción de colocación
**Descripción:** Se utiliza para transmitir intenciones legibles por el usuario sobre cómo se utiliza el contenido dinámico en la entrega general de mensajes. Que un espacio determinado sea un \&quot;banner\&quot; en una página web se transmite a menudo mediante la descripción y no mediante un método formal.
**Tipo:** cadena

#### _experience > decisiones > Nombre de ubicación

**Campo:** name
**Título:** Nombre de colocación
**Descripción:** Un nombre asignado para que la ubicación haga referencia a él en interacciones humanas.
**Tipo:** cadena

## _repo {#repo}

**Campo:** _repo
**Tipo:** object

### _repo > Etiqueta ET de colocación

**Campo:** etiqueta
**Título:** Etiqueta ET de colocación
**Descripción:** Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.
**Tipo:** cadena
