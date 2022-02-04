---
title: Configurar selección de ofertas en decisiones
description: Aprenda a administrar la selección de ofertas en decisiones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 5%

---

# Configurar selección de ofertas en decisiones {#offers-selection-in-decisions}

Si varias ofertas son elegibles para una ubicación determinada, puede elegir el método que seleccionará la mejor oferta para cada perfil al configurar una decisión (anteriormente conocida como actividad de oferta). Puede clasificar las ofertas mediante:
* Prioridad de la oferta
* Fórmula de clasificación
* [Clasificación de IA](#use-ranking-strategy) (en acceso anticipado solo para usuarios seleccionados)

![](../../assets/offer-rank-by.png)

## Prioridad de la oferta {#offer-priority}

De forma predeterminada, cuando varias ofertas son elegibles para una ubicación determinada en una decisión (anteriormente conocida como actividad de oferta), las ofertas con la mayor **priority** se entregará primero a los clientes.

![](../../assets/offer-priority.png)

Las puntuaciones de prioridad de las ofertas se asignan al crear una oferta. Obtenga información sobre cómo crear una oferta personalizada en [esta sección](../offer-library/creating-personalized-offers.md).

## Fórmula de clasificación {#assign-ranking-formula}

Además de la prioridad de oferta, Journey Optimizer le permite crear **clasificación de fórmulas**. Son fórmulas que determinan qué oferta debe presentarse primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas.

Por ejemplo, puede aumentar la prioridad de todas las ofertas en las que la fecha de finalización sea inferior a 24 horas a partir de ahora, o aumentar las ofertas de la categoría &quot;en ejecución&quot; si el punto de interés del perfil está &quot;en ejecución&quot;.

Obtenga información sobre cómo crear una fórmula de clasificación en [esta sección](../offer-library/create-ranking-formulas.md).

Una vez creada una fórmula de clasificación, puede asignarla a una colocación en una decisión (anteriormente conocida como actividad de oferta). Para realizar esto, siga los pasos a continuación:

1. Cree una decisión o edite una existente. Consulte [Creación de decisiones](../offer-activities/create-offer-activities.md).

1. Añada las ubicaciones que contendrán sus ofertas. Consulte [Creación de ubicaciones](../offer-library/creating-placements.md).

1. Para cada ubicación, agregue una colección. Consulte [Crear colecciones](../offer-library/creating-collections.md).

1. Select **[!UICONTROL Ranking formula]** como método de clasificación, haga clic en **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Seleccione la fórmula de clasificación que desee y haga clic en **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

La fórmula de clasificación ahora está asociada a la ubicación.

Si se pueden presentar varias ofertas en esta ubicación, la decisión utilizará la fórmula de la fórmula de clasificación para calcular qué oferta enviar primero.

## Clasificación de IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can also use an trained model system that automatically ranks offers to display for a given profile by selecting a ranking strategy. Learn how to create a ranking strategy in [this section](../offer-library/create-ranking-strategies.md).

>[!CAUTION]
>
>El uso de la clasificación AI está disponible actualmente en el acceso anticipado solo para usuarios seleccionados.

Una vez creada una estrategia de clasificación, puede asignarla a una colocación en una decisión (anteriormente conocida como actividad de oferta). Para ello, siga los pasos a continuación:

1. Cree una decisión o edite una existente. Consulte [Creación de decisiones](../offer-activities/create-offer-activities.md).

1. Añada las ubicaciones que contendrán sus ofertas. Consulte [Creación de ubicaciones](../offer-library/creating-placements.md).

1. Para cada ubicación, agregue una colección. Consulte [Crear colecciones](../offer-library/creating-collections.md).

1. Elija clasificar ofertas por **[!UICONTROL AI ranking]** en la lista desplegable y haga clic en **[!UICONTROL Add ranking]**.

   ![](../../assets/ranking-selection-ai-ranking.png)

1. Seleccione la estrategia de clasificación que ha creado. Se muestran todos los detalles de la estrategia de clasificación.

   ![](../../assets/ranking-selection-ai-ranking-selected.png)

1. Haga clic en **[!UICONTROL Select]**. La estrategia de clasificación ahora está asociada a la ubicación.

Si se admiten varias ofertas, el sistema de modelos formado determinará qué oferta debe presentarse primero para una ubicación determinada.

