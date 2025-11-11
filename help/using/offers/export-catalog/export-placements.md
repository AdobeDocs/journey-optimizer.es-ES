---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Conjunto de datos de ubicaciones
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para las ubicaciones
badge: label="Heredado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Conjunto de datos de ubicaciones {#placements-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las ubicaciones.

![](../assets/dataset-placements.png)

El lote exitoso más reciente en el conjunto de datos se muestra a la derecha. La vista jerárquica del esquema del conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Esta es la lista de todos los campos que se pueden usar en el **[!UICONTROL Repositorio de objetos de decisión: ubicaciones]** conjunto de datos.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

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

+++ _experience > decisioning > Identificador de canal de la ubicación

**Campo:** channelID
**Título:** Identificador de canal de ubicación
**Descripción:** Canal en el que se hizo la propuesta. El valor es un URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.
**Tipo:** cadena

+++

+++ _experience > decisiones > Tipo de componente de contenido

**Campo:** componentType
**Título:** Tipo de componente de contenido
**Descripción:** conjunto enumerado de URI en el que cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.
**Tipo:** cadena

+++

+++ _experience > decisioning > contentTypes

**Campo:** contentTypes
**Tipo:** matriz

+++

+++_experience > decisioning > contentTypes > Tipo de medio MIME

**Título:** tipo de medio MIME
**Descripción:** Una restricción para el tipo de medios de los componentes que se espera en esa ubicación. Podría haber más de un tipo de medio posible para un componente, como un formato de imagen diferente.
**Tipo:** cadena

+++

+++ _experience > decisioning > Descripción de ubicación

**Campo:** descripción
**Título:** Descripción de ubicación
**Descripción:** se usa para transmitir intenciones legibles por humanos sobre cómo se usa el contenido dinámico en la entrega general de mensajes. Que un espacio determinado sea un \&quot;Banner\&quot; en una página web se transmite a menudo a través de la descripción y no por un método formal.
**Tipo:** cadena

+++

+++ _experience > decisioning > Nombre de ubicación

**Campo:** nombre
**Título:** Nombre de ubicación
**Descripción:** Se ha asignado un nombre a la ubicación para hacer referencia a ella en interacciones humanas.
**Tipo:** cadena

+++

+++ _repo

**Campo:** _repositorio
**Tipo:** objeto

+++

+++ _repo > Ubicación ETag

**Campo:** etag
**Título:** ETag de ubicación
**Descripción:** Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.
**Tipo:** cadena

+++
