---
title: Introducción a Experience Decisioning
description: Más información sobre Experience Decisioning
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 6%

---

# Introducción a Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* **[Introducción a Experience Decisioning](gs-experience-decisioning.md)**
* Administrar los elementos de decisión
   * [Configurar el catálogo de artículos](catalogs.md)
   * [Crear elementos de decisión](items.md)
   * [Administrar colecciones de elementos](collections.md)
* Configurar la selección de elementos
   * [Crear reglas de decisión](rules.md)
   * [Crear métodos de clasificación](ranking.md)
* [Crear estrategias de selección](selection-strategies.md)
* [Crear directivas de decisión](create-decision.md)

>[!ENDSHADEBOX]

## Qué es Experience Decisioning {#about}

>[!AVAILABILITY]
>
>Actualmente, la función Experience Decisioning está disponible como una versión beta solo para usuarios seleccionados. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.

Experience Decisioning simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como &quot;elementos de decisión&quot; y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar los elementos de decisión más relevantes a cada individuo.

Estos elementos de decisión se integran perfectamente en una amplia gama de superficies entrantes a través del nuevo canal de experiencia basado en código, ahora accesible dentro de las campañas de Journey Optimizer.

**Limitaciones:**

* Las políticas de decisión solo están disponibles para su uso en campañas de experiencia basadas en código.
* Por ahora, el límite de frecuencia no está disponible en Experience Decisioning.

## Pasos clave de Experience Decisioning {#steps}

Los pasos principales para trabajar con Experience Decisioning son los siguientes:

1. **Configuración de atributos personalizados**: adapte el catálogo de elementos de decisión a sus necesidades específicas configurando atributos personalizados en el esquema del catálogo.

1. **Crear elementos de decisión** para mostrarlo a su audiencia de destino.

1. **Organizar con colecciones**: utilice las colecciones para categorizar los elementos de decisión según las reglas basadas en atributos. Incorpore colecciones en las estrategias de selección para determinar qué colección de elementos de decisión se debe tener en cuenta.

1. **Creación de reglas de decisión**: Las reglas de decisión se utilizan en elementos de decisión o estrategias de selección para determinar a quién se puede mostrar un elemento de decisión.

1. **Implementación de métodos de clasificación**: Cree métodos de clasificación y aplíquelos dentro de las estrategias de decisión para determinar el orden de prioridad para seleccionar los elementos de decisión.

1. **Crear estrategias de selección**: genere estrategias de selección que aprovechen las colecciones, las reglas de decisión y los métodos de clasificación para identificar los elementos de decisión adecuados para mostrarlos a los perfiles.

1. **Incrustar una política de decisión en la campaña basada en código**: las políticas de decisión combinan varias estrategias de selección para determinar los elementos de decisión aptos que se mostrarán a la audiencia objetivo.

## Glosario

Brandon para proporcionar términos.
