---
title: Reglas de decisión
description: Aprenda a trabajar con reglas de decisión
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 9b7280c33ce8238b54f7fd1865545f865ffb72ed
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 5%

---

# Reglas de decisión {#rules}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a Experience Decisioning](gs-experience-decisioning.md)
* Administrar los elementos de decisión
   * [Configurar el catálogo de artículos](catalogs.md)
   * [Crear elementos de decisión](items.md)
   * [Administrar colecciones de elementos](collections.md)
* Configurar la selección de elementos
   * **[Crear reglas de decisión](rules.md)**
   * [Crear métodos de clasificación](ranking.md)
* [Crear estrategias de selección](selection-strategies.md)
* [Crear directivas de decisión](create-decision.md)

>[!ENDSHADEBOX]

Las reglas de decisión permiten definir la audiencia de los elementos de decisión mediante la aplicación de restricciones, ya sea directamente en el nivel del elemento de decisión o dentro de una estrategia de selección específica. Esto le permite controlar con precisión qué elementos se deben presentar a quién.

Por ejemplo, consideremos un escenario en el que tenga elementos de decisión que presenten productos relacionados con el yoga diseñados para mujeres. Con las reglas de decisión, puede especificar que estos elementos solo deben mostrarse a perfiles cuyo sexo sea &quot;Mujer&quot; y que hayan indicado un &quot;Punto de interés&quot; en &quot;Yoga&quot;.

Se puede acceder a la lista de reglas de decisión en la **[!UICONTROL Configuración]** / **[!UICONTROL Reglas de decisiones]** menú.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Por ahora, las reglas de decisión se administran mediante el de Journey Optimizer **Administración de decisiones** menú. Como resultado, la variable **[!UICONTROL Reglas de decisión]** La lista de Experience Decisioning incluye reglas creadas a partir de Journey Optimizer **[!UICONTROL Gestión de decisiones]** o **[!UICONTROL Experience Decisioning]** menús.

Para crear una colección, siga estos pasos:

1. Vaya a **[!UICONTROL Configuración]** / **[!UICONTROL Reglas de decisión]**.
1. La interfaz de usuario de Administración de decisiones de Journey Optimizer se muestra en el área central. Siga los pasos detallados en la [Documentación de gestión de decisiones](../offers/offer-library/creating-decision-rules.md) para crear una regla basada en sus necesidades.

1. Una vez creada la regla, aparece en la lista y está disponible para su uso en elementos de decisión y estrategias de selección para regular la presentación de elementos de decisión a perfiles.
