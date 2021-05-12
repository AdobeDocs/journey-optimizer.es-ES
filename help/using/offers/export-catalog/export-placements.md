---
title: Conjunto de datos de ubicaciones
description: Esta sección enumera todos los campos utilizados en el conjunto de datos exportado para las ubicaciones.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# Conjunto de datos de colocaciones {#placements-dataset}

Cada vez que se modifica una oferta, se actualiza el conjunto de datos generado automáticamente para las ubicaciones.

![](../../assets/dataset-placements.png)

El lote correcto más reciente del conjunto de datos se muestra a la derecha. La vista jerárquica del esquema para el conjunto de datos se muestra en el panel izquierdo.

>[!NOTE]
>
>Obtenga información sobre cómo acceder a los conjuntos de datos exportados para cada objeto de la biblioteca de ofertas en [esta sección](../export-catalog/access-dataset.md).

Una ubicación describe una ubicación o un lugar en un mensaje personalizado. Se utiliza para establecer restricciones técnicas para el contenido que proporciona la decisión de personalización. La ubicación también representa una solicitud para producir ciertos tipos de métricas cuando se produce un evento de experiencia en el que participa esta ubicación. Por ejemplo, la colocación facilita la aparición de una imagen en la que se puede hacer clic personalizada dentro de un correo electrónico que se muestra a un usuario final. La ubicación puede, por ejemplo, solicitar a la experiencia ensamblada que el clic en su imagen se comunique en un evento de experiencia con una métrica https://ns.adobe.com/xdm/data/metrics/web/linkclicks y una referencia a esta ubicación.

Esta es la lista de todos los campos que se pueden utilizar en el conjunto de datos **[!UICONTROL Decision Object Repository - Placements]**.

## Identificador

Identificador único del registro.

Tipo: cadena

## _experiencia

### decisioning

#### Identificador de canal de la colocación

Canal en el que se realizó la propuesta. El valor es un URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.

Tipo: cadena

#### Tipo de componente de contenido

Un conjunto enumerado de URI donde cada valor se asigna a un tipo dado al componente de contenido. Algunos consumidores de las representaciones de contenido esperan que el valor @type sea una referencia al esquema que describe propiedades adicionales del componente de contenido.

Tipo: cadena

#### Tipo de medio MIME

Restricción para el tipo de contenido de los componentes que se espera en esa ubicación. Podría haber más de un tipo de medio posible para un componente, como un formato de imagen diferente.

Tipo: cadena

#### Descripción de colocación

Se utiliza para transmitir intenciones legibles por el usuario sobre cómo se utiliza el contenido dinámico en la entrega general de mensajes. Que un espacio determinado sea un \&quot;banner\&quot; en una página web se transmite a menudo mediante la descripción y no mediante un método formal.

Tipo: cadena

#### Nombre de colocación

Un nombre asignado para que la ubicación haga referencia a él en interacciones humanas.

Tipo: cadena

## _repo

### Etiqueta ET de colocación

Revisión en la que se encontraba el objeto de opción de decisión cuando se tomó la instantánea.

Tipo: cadena
