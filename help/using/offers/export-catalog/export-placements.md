---
title: Conjunto de datos de ubicaciones
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para las ubicaciones.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 4%

---

# Conjunto de datos de colocaciones {#placements-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las ubicaciones.

![](../../assets/dataset-placements.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden utilizar en el conjunto de datos **[!UICONTROL Decision Object Repository - Placements]**.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Identificador

**Campo:**  _id 
**Título:** Identificador 
**Descripción:**  Identificador único del registro.
**Tipo:** cadena

## _experiencia

**Campo:** _experience 
**Type:** object

### decisioning

**Campo:** 
**tipo de decisión:** objeto

#### Identificador de canal de la colocación

**Campo:** 
**Título de ID de canal:** Descripción del identificador de canal de la 
**ubicación:** El canal en el que se realizó la propuesta. El valor es un URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.
**Tipo:** cadena

#### Tipo de componente de contenido

**Campo:** componenteTipo 
**Título:** Tipo de componente de contenido 
**Descripción:**  Un conjunto enumerado de URI donde cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.
**Tipo:** cadena

#### contentTypes

**Campo:** contentTypes 
**Type:** array

* **Tipo de medio MIME**

   **Título:** Tipo de medio MIME
   **Descripción:** Una restricción para el tipo de contenido de los componentes que se espera en esa ubicación. Podría haber más de un tipo de medio posible para un componente, como un formato de imagen diferente.
   **Tipo:** cadena

#### Descripción de colocación

**Campo:** descripción 
**Título:** Descripción de la ubicación 
**Descripción:**  Se utiliza para transmitir intenciones legibles sobre cómo se utiliza el contenido dinámico en la entrega general de mensajes. Que un espacio determinado sea un \&quot;banner\&quot; en una página web se transmite a menudo mediante la descripción y no mediante un método formal.
**Tipo:** cadena

#### Nombre de colocación

**Campo:** Nombre 
**Título:** Nombre de ubicación 
**Descripción:**  Un nombre asignado para la ubicación que hace referencia a él en interacciones humanas.
**Tipo:** cadena

## _repo

**Campo:** _repo 
**Tipo:** objeto

### Etiqueta ET de colocación

**Campo:** Etiqueta 
**Título:** Ubicación ETag 
**Descripción:**  La revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.
**Tipo:** cadena
