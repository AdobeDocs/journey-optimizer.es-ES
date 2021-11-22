---
title: Configurar selección de ofertas en decisiones
description: Aprenda a administrar la selección de ofertas en decisiones.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: caaf3942853adb4e5eb16a3dd303ca1f088ce23b
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 5%

---

# Configurar selección de ofertas en decisiones {#offers-selection-in-activities}

Si varias ofertas son elegibles para una ubicación determinada, puede elegir el método que seleccionará la mejor oferta para cada perfil al configurar una decisión (anteriormente conocida como actividad de oferta). Puede clasificar las ofertas mediante:
* Prioridad de la oferta
* Fórmula de clasificación
* [AI ranking](#use-ranking-strategy) (in early access for select users only)

![](../../assets/offer-rank-by.png)

## Offer priority {#about-offers-priority}

De forma predeterminada, cuando varias ofertas son elegibles para una ubicación determinada en una decisión (anteriormente conocida como actividad de oferta), las ofertas con la mayor **priority** se entregará primero a los clientes.

![](../../assets/offer-priority.png)

Las puntuaciones de prioridad de las ofertas se asignan al crear una oferta. Learn how to create a personalized offer in [this section](../offer-library/creating-personalized-offers.md).

## Ranking formula {#assign-ranking-formula}

In addition to offer priority, Journey Optimizer allows you to create **ranking formulas**. These are formulas that determine which offer should be presented first for a given placement, rather than taking into account the offers&#39; priority scores.

Por ejemplo, puede aumentar la prioridad de todas las ofertas en las que la fecha de finalización sea inferior a 24 horas a partir de ahora, o aumentar las ofertas de la categoría &quot;en ejecución&quot; si el punto de interés del perfil está &quot;en ejecución&quot;.

Obtenga información sobre cómo crear una fórmula de clasificación en [esta sección](../offer-library/create-ranking-formulas.md).

Once a ranking formula has been created, you can assign it to a placement in a decision (previously known as offer activity). Para realizar esto, siga los pasos a continuación:

1. Cree una decisión o edite una existente. Consulte [Creación de decisiones](../offer-activities/create-offer-activities.md).

1. Añada las ubicaciones que contendrán sus ofertas. See [Create placements](../offer-library/creating-placements.md).

1. Para cada ubicación, agregue una colección. Consulte [Crear colecciones](../offer-library/creating-collections.md).

1. Select **[!UICONTROL Ranking formula]** como método de clasificación, haga clic en **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Select the desired ranking formula, then click **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

La fórmula de clasificación ahora está asociada a la ubicación.

Si se pueden presentar varias ofertas en esta ubicación, la decisión utilizará la fórmula de la fórmula de clasificación para calcular qué oferta enviar primero.

## Clasificación de IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can also use an trained model system that automatically ranks offers to display for a given profile by selecting a ranking strategy. Learn how to create a ranking strategy in [this section](../offer-library/create-ranking-strategies.md).

>[!CAUTION]
>
>The use of AI ranking is currently available in early access to select users only.

Once a ranking strategy has been created, you can assign it to a placement in a decision (previously known as offer activity). To do this this, follow the steps below:

1. Cree una decisión o edite una existente. Consulte [Creación de decisiones](../offer-activities/create-offer-activities.md).

1. Añada las ubicaciones que contendrán sus ofertas. See [Create placements](../offer-library/creating-placements.md).

1. For each placement, add a collection. See [Create collections](../offer-library/creating-collections.md).

1. Elija clasificar ofertas por **[!UICONTROL AI ranking]** en la lista desplegable y haga clic en **[!UICONTROL Add ranking]**.

   ![](../../assets/ranking-selection-ai-ranking.png)

1. Seleccione la estrategia de clasificación que ha creado. Se muestran todos los detalles de la estrategia de clasificación.

   ![](../../assets/ranking-selection-ai-ranking-selected.png)

1. Haga clic en **[!UICONTROL Select]**. The ranking strategy is now associated with the placement.

Si se admiten varias ofertas, el sistema de modelos formado determinará qué oferta debe presentarse primero para una ubicación determinada.

<!--Result? Describe the impact for the user, i.e. what's the effect of selecting this ranking strategy for this collection/placement.-->

<!--Click **[!UICONTROL Next]** to confirm and save your decision.-->
