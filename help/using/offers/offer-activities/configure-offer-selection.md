---
title: Configurar la selección de ofertas en decisiones
description: Aprenda a administrar la selección de ofertas en decisiones.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 2%

---

# Configurar la selección de ofertas en decisiones {#offers-selection-in-activities}

## Acerca de la prioridad de ofertas {#about-offers-priority}

De forma predeterminada, cuando varias ofertas son elegibles para una ubicación determinada en una decisión (anteriormente conocida como actividad de oferta), las ofertas con la **prioridad** más alta se entregarán primero a los clientes. Las puntuaciones de prioridad de las ofertas se asignan al crear una oferta (consulte [Crear una oferta personalizada](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

Además, Journey Optimizer le permite crear **fórmulas de clasificación**. Son fórmulas que determinan qué oferta debe presentarse primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas. Por ejemplo, puede aumentar la prioridad de todas las ofertas en las que la fecha de finalización sea inferior a 24 horas a partir de ahora, o aumentar las ofertas de la categoría &quot;en ejecución&quot; si el punto de interés del perfil está &quot;en ejecución&quot;.

Para obtener más información sobre cómo crear una fórmula de clasificación, consulte [esta sección](../offer-library/create-ranking-formulas.md).

## Asignar una fórmula de clasificación a una ubicación {#assign-ranking-formula}

Una vez creada una fórmula de clasificación, puede asignarla a una colocación en una decisión. Para realizar esto, siga los pasos a continuación:

* Cree una decisión o edite una existente y luego cree las ubicaciones que contendrán sus ofertas (consulte [Crear decisiones](../offer-activities/create-offer-activities.md)).

* Para cada ubicación, seleccione **[!UICONTROL Ranking]** en la lista desplegable y haga clic en **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

* Seleccione la fórmula de clasificación que desee y haga clic en **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

La fórmula de clasificación ahora está asociada a la ubicación. Si varias ofertas son elegibles para presentarse en esta ubicación, la decisión utilizará la fórmula de clasificación para calcular qué oferta enviar primero.
