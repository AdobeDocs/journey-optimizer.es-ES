---
title: Caso de uso sobre la toma de decisiones
description: Aprenda a crear decisiones utilizando experimentos con el canal basado en código
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 7%

---

# Caso de uso sobre la toma de decisiones {#experience-decisioning-uc}

Este caso de uso presenta todos los pasos necesarios para utilizar Decisioning con el canal basado en código [!DNL Journey Optimizer].

<!--In this use case, you create a campaign where you define two delivery treatments - each containing a different decision policy in order to measure which one performs best for your target audience.-->

En este caso de uso, no está seguro de si una fórmula de clasificación específica tendrá un mejor rendimiento que las prioridades de oferta preasignadas.

Para medir cuál ofrece el mejor rendimiento para la audiencia de destino, cree una campaña en la que defina dos tratamientos de entrega:

<!--Set up the experiment such that:-->

* El primer tratamiento contiene una estrategia de selección con prioridad como método de clasificación.
* El segundo tratamiento contiene una estrategia de selección diferente para la cual una fórmula es el método de clasificación.

## Creación de estrategias de selección

En primer lugar, debe crear dos estrategias de selección: una con prioridad como método de clasificación y otra con una fórmula como método de clasificación.

### Creación de la primera estrategia de selección

En la primera estrategia de selección, seleccione priority como método de clasificación. Siga los pasos a continuación.

1. Cree un elemento de decisión. [Descubra cómo](items.md)

1. Establezca la **[!UICONTROL Prioridad]** del elemento de decisión en comparación con otros. Si un perfil cumple los requisitos para varios elementos, una prioridad mayor otorga al elemento prioridad sobre otros.

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >La prioridad es un tipo de datos entero. Todos los atributos que son tipos de datos enteros deben contener valores enteros (sin decimales).

1. Defina audiencias o reglas para restringir el elemento solo a perfiles específicos. [Aprenda a establecer la idoneidad del elemento de decisión](items.md#eligibility)

1. Defina las reglas de límite para definir el número máximo de veces que se puede presentar una oferta. [Descubra cómo](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Cree una **colección** en la que se incluirán los elementos de decisión. [Más información](collections.md)

1. Crear una **estrategia de selección**. [Descubra cómo](selection-strategies.md#create-selection-strategy)

1. Seleccione la [colección](collections.md) que contiene las ofertas que se deben considerar.

1. [Elija el método de clasificación](#select-ranking-method) que se usará para seleccionar la mejor oferta para cada perfil. En este caso, seleccione **[!UICONTROL Prioridad de ofertas]**. [Más información](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

   <!--If multiple offers are eligible for this strategy, the [Offer priority](#offer-priority) method uses the value defined in the offers.-->

### Creación de la segunda estrategia de selección

En la segunda estrategia de selección, seleccione una fórmula como método de clasificación. Siga los pasos a continuación.

1. Cree un elemento de decisión. [Descubra cómo](items.md)

<!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Defina audiencias o reglas para restringir el elemento solo a perfiles específicos. [Aprenda a establecer la idoneidad del elemento de decisión](items.md#eligibility)

1. Defina las reglas de límite para definir el número máximo de veces que se puede presentar una oferta. [Descubra cómo](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Cree una **colección** en la que se incluirán los elementos de decisión. [Más información](collections.md)

1. Crear una **estrategia de selección**. [Descubra cómo](selection-strategies.md#create-selection-strategy)

1. Seleccione la [colección](collections.md) que contiene las ofertas que se deben considerar.

1. [Seleccione el método de clasificación](#select-ranking-method) que desee usar para seleccionar la mejor oferta para cada perfil. En este caso, seleccione **[!UICONTROL Fórmula]** para usar una puntuación calculada específica y elegir la oferta elegible para entregar. [Más información](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

<!--
## Create decision items and selection strategies

You first need to create items, group them together in collections, set up rules and ranking methods. These elements will allow you to build selection strategies.

1. Navigate to **[!UICONTROL Decisioning]** > **[!UICONTROL Catalogs]** and create several decision items. Set constraints using audiences or rules to restrict each item to specific profiles only. [Learn more](items.md)

1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)

1. Create **collections** to categorize and group your decision items according to your preferences. [Learn more](collections.md)

1. Create **decision rules** to determine to whom a decision item can be shown. [Learn more](rules.md)

1. Create **ranking methods** and apply them within decision strategies to determine the priority order for selecting decision items. [Learn more](ranking.md)

1. Build **selection strategies** that leverage collections, decision rules, and ranking methods to identify the decision items suitable for displaying to profiles. [Learn more](selection-strategies.md)
-->

## Creación de políticas de decisión

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

1. Cree una campaña y seleccione la acción **[!UICONTROL Experiencia basada en código]**. [Más información](../code-based/create-code-based.md)

1. Desde la ventana **[!UICONTROL Editar contenido]**, empiece a personalizar el tratamiento A.

1. Seleccione el icono **[!UICONTROL Decisiones]**, haga clic en **[!UICONTROL Crear una decisión]** y rellene los detalles de la decisión. [Más información](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Seleccione la primera estrategia que ha creado. Haga clic en **[!UICONTROL Agregar estrategia]**.

1. Haga clic en **[!UICONTROL Crear]**. La nueva decisión se agregó en **[!UICONTROL Decisiones]**.

   ![](assets/decision-code-based-decision-added.png)

1. Haga clic en el icono de más acciones (tres puntos) y seleccione **[!UICONTROL Agregar]**. Ahora puede agregar todos los atributos de decisión que desee dentro de esto.

   ![](assets/decision-code-based-add-decision.png)

1. También puede añadir cualquier otro atributo disponible en el editor de personalización, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. En la página de resumen de la campaña, haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido. [Más información](../content-management/content-experiment.md)

1. En la ventana **[!UICONTROL Editar contenido]**, seleccione el tratamiento B y repita los pasos anteriores para crear otra decisión.

1. Seleccione la segunda estrategia que ha creado. Haga clic en **[!UICONTROL Agregar estrategia]**.

1. Guarde el contenido.
