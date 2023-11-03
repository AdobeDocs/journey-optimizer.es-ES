---
title: Reglas de decisión
description: Aprenda a trabajar con reglas de decisión
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 40%

---

# Reglas de decisión {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Crear reglas de decisión"
>abstract="Las reglas de decisión permiten definir el público de los elementos de decisión mediante la aplicación de restricciones, ya sea directamente en el nivel del elemento de decisión o dentro de una estrategia de selección específica. Esto le permite controlar con precisión qué elementos se deben presentar a quién."

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a Experience Decisioning](gs-experience-decisioning.md)
* Administración de los elementos de decisión
   * [Configuración del catálogo de elementos](catalogs.md)
   * [Creación de elementos de decisión](items.md)
   * [Administración de colecciones de elementos](collections.md)
* Configuración de la selección de elementos
   * **[Crear reglas de decisión](rules.md)**
   * [Creación de métodos de clasificación](ranking.md)
* [Creación de estrategias de selección](selection-strategies.md)
* [Creación de políticas de decisión](create-decision.md)

>[!ENDSHADEBOX]

Las reglas de decisión permiten definir el público de los elementos de decisión mediante la aplicación de restricciones, ya sea directamente en el nivel del elemento de decisión o dentro de una estrategia de selección específica. Esto le permite controlar con precisión qué elementos se deben presentar a quién.

Por ejemplo, consideremos un escenario en el que tenga elementos de decisión que presenten productos relacionados con el yoga diseñados para mujeres. Con las reglas de decisión, puede especificar que estos elementos solo deben mostrarse a perfiles cuyo sexo sea &quot;Mujer&quot; y que hayan indicado un &quot;Punto de interés&quot; en &quot;Yoga&quot;.

>[!NOTE]
>
>Además de las reglas de decisión a nivel de elemento y de estrategia de selección, también puede definir la audiencia a nivel de campaña. [Más información](../campaigns/create-campaign.md#audience)


Se puede acceder a la lista de reglas de decisión en la **[!UICONTROL Configuración]** / **[!UICONTROL Reglas de decisiones]** menú.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Por ahora, las reglas de decisión se administran mediante el de Journey Optimizer **Administración de decisiones** menú. Como resultado, la variable **[!UICONTROL Reglas de decisión]** La lista de Experience Decisioning incluye reglas creadas a partir de Journey Optimizer **[!UICONTROL Gestión de decisiones]** o **[!UICONTROL Experience Decisioning]** menús.

Para crear una regla, siga estos pasos:

1. Vaya a **[!UICONTROL Configuración]** / **[!UICONTROL Reglas de decisión]**.
1. La interfaz de usuario de Administración de decisiones de Journey Optimizer se muestra en el área central. Siga los pasos detallados en la [Documentación de gestión de decisiones](../offers/offer-library/creating-decision-rules.md) para crear una regla basada en sus necesidades.

1. Una vez creada la regla, aparece en la lista y está disponible para su uso en elementos de decisión y estrategias de selección para regular la presentación de elementos de decisión a perfiles.
