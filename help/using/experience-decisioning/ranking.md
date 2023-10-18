---
title: Métodos de clasificación
description: Aprenda a trabajar con métodos de clasificación
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 25%

---

# Métodos de clasificación {#rankings}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a Experience Decisioning](gs-experience-decisioning.md)
* Administración de los elementos de decisión
   * [Configuración del catálogo de elementos](catalogs.md)
   * [Creación de elementos de decisión](items.md)
   * [Administración de colecciones de elementos](collections.md)
* Configuración de la selección de elementos
   * [Crear reglas de decisión](rules.md)
   * **[Creación de métodos de clasificación](ranking.md)**
* [Creación de estrategias de selección](selection-strategies.md)
* [Creación de políticas de decisión](create-decision.md)

>[!ENDSHADEBOX]

Los métodos de clasificación permiten clasificar los elementos que se muestran en un perfil determinado. Una vez creado un método de clasificación, puede asignarlo a una estrategia de decisión para definir qué artículos se deben seleccionar primero.

Los métodos de clasificación son accesibles desde el **[!UICONTROL Configuración]** / **[!UICONTROL Métodos de clasificación]** menú. Hay dos tipos de métodos de clasificación disponibles:

* **Fórmulas** permite definir reglas que determinan qué elemento debe presentarse primero, en lugar de tener en cuenta las puntuaciones de prioridad del elemento.

* **modelos de IA** le permite utilizar sistemas de modelos formados que aprovecharán varios puntos de datos para determinar qué elemento se debe presentar primero.

![](assets/ranking-create.png)

Encontrará información detallada sobre cada tipo de método de clasificación y cómo crearlos en la documentación de gestión de decisiones disponible aquí:

* [Fórmulas de clasificación](../offers/ranking/create-ranking-formulas.md)
* [Modelos de IA](../offers/ranking/ai-models.md)
