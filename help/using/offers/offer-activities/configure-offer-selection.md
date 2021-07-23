---
title: Configurar selección de ofertas en decisiones
description: Aprenda a administrar la selección de ofertas en decisiones.
feature: Ofertas
topic: Integraciones
role: User
level: Intermediate
source-git-commit: 3db5756236b6ac05d9b95b8b051dd99dc7d5cf7e
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 7%

---

# Configurar selección de ofertas en decisiones {#offers-selection-in-activities}

Si varias ofertas son elegibles para una ubicación determinada, puede elegir el método que seleccionará la mejor oferta para cada perfil al configurar una decisión (anteriormente conocida como actividad de oferta). Puede clasificar las ofertas mediante:
* Prioridad de la oferta
* Fórmula de clasificación

## Prioridad de la oferta {#about-offers-priority}

De forma predeterminada, cuando varias ofertas son elegibles para una ubicación determinada en una decisión (anteriormente conocida como actividad de oferta), las ofertas con la **prioridad** más alta se entregarán primero a los clientes.

![](../../assets/offer-priority.png)

Las puntuaciones de prioridad de las ofertas se asignan al crear una oferta. Aprenda a crear una oferta personalizada en [esta sección](../offer-library/creating-personalized-offers.md).

## Fórmula de clasificación {#assign-ranking-formula}

Además de la prioridad de oferta, Journey Optimizer le permite crear **fórmulas de clasificación**. Son fórmulas que determinan qué oferta debe presentarse primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas.

Por ejemplo, puede aumentar la prioridad de todas las ofertas en las que la fecha de finalización sea inferior a 24 horas a partir de ahora, o aumentar las ofertas de la categoría &quot;en ejecución&quot; si el punto de interés del perfil está &quot;en ejecución&quot;.

Aprenda a crear una fórmula de clasificación en [esta sección](../offer-library/create-ranking-formulas.md).

Una vez creada una fórmula de clasificación, puede asignarla a una colocación en una decisión (anteriormente conocida como actividad de oferta). Para realizar esto, siga los pasos a continuación:

1. Cree una decisión o edite una existente. Consulte [Creación de decisiones](../offer-activities/create-offer-activities.md).

1. Añada las ubicaciones que contendrán sus ofertas. Consulte [Crear ubicaciones](../offer-library/creating-placements.md).

1. Para cada ubicación, agregue una colección. Consulte [Crear colecciones](../offer-library/creating-collections.md).

1. Elija clasificar ofertas por **[!UICONTROL Ranking]** en la lista desplegable y haga clic en **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Seleccione la fórmula de clasificación que desee y haga clic en **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

La fórmula de clasificación ahora está asociada a la ubicación.

Si se pueden presentar varias ofertas en esta ubicación, la decisión utilizará la fórmula de la fórmula de clasificación para calcular qué oferta enviar primero.
