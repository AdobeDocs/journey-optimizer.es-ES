---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Configurar selección de ofertas en decisiones
description: Obtenga información sobre cómo administrar la selección de ofertas en decisiones
badge: label="Heredado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 10%

---

# Configurar selección de ofertas en decisiones {#offers-selection-in-decisions}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

Si se pueden seleccionar varias ofertas para una ubicación determinada, puede elegir el método que seleccione la mejor oferta para cada perfil al configurar una decisión. Puede clasificar ofertas por:

* Prioridad de ofertas
* Fórmula de clasificación
* [Clasificación de IA](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Prioridad de ofertas {#offer-priority}

De manera predeterminada, cuando varias ofertas cumplen los requisitos para una ubicación determinada en una decisión, las ofertas con la **prioridad** más alta se entregarán primero a los clientes.

![](../assets/offer-priority.png)

Las puntuaciones de prioridad de las ofertas se asignan al crear una oferta. Aprenda a crear una oferta personalizada en [esta sección](../offer-library/creating-personalized-offers.md).

## Fórmula de clasificación {#assign-ranking-formula}

Además de la prioridad de ofertas, Journey Optimizer permite crear **fórmulas de clasificación**. Son fórmulas que determinan qué oferta debe presentarse primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas.

Por ejemplo, puede aumentar la prioridad de todas las ofertas en las que la fecha de finalización sea inferior a 24 horas a partir de ahora o aumentar las ofertas de la categoría &quot;en ejecución&quot; si el punto de interés del perfil es &quot;en ejecución&quot;.

Aprenda a crear una fórmula de clasificación en [esta sección](../ranking/create-ranking-formulas.md).

Una vez creada una fórmula, puede asignarla a una ubicación de una decisión. Para realizar esto, siga los pasos a continuación:

1. Cree una decisión o edite una existente. Consulte [Creación de decisiones](../offer-activities/create-offer-activities.md).

1. Añada las ubicaciones que contendrán sus ofertas. Consulte [Crear ubicaciones](../offer-library/creating-placements.md).

1. Para cada ubicación, agregue una colección. Consulte [Crear colecciones](../offer-library/creating-collections.md).

1. Seleccione **[!UICONTROL Fórmula]** como método de clasificación y luego haga clic en **[!UICONTROL Agregar clasificación]**.

   ![](../assets/offer-activity-ranking.png)

1. Seleccione la fórmula que desee y haga clic en **[!UICONTROL Seleccionar]**.

   ![](../assets/ranking-selection.png)

La fórmula de clasificación ahora está asociada a la ubicación.

Si se pueden presentar varias ofertas en esta ubicación, la decisión utilizará la fórmula seleccionada para calcular qué oferta se entregará primero.

## Clasificación de IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=es){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

También puede utilizar un sistema de modelos entrenado que clasifique automáticamente las ofertas para un perfil determinado seleccionando un modelo de IA. Aprenda a crear un modelo de IA en [esta sección](../ranking/create-ranking-strategies.md).

Una vez creado un modelo de IA, puede asignarlo a una ubicación en una decisión. Para ello, siga los pasos a continuación:

1. Cree una decisión o edite una existente. Consulte [Creación de decisiones](../offer-activities/create-offer-activities.md).

1. Añada las ubicaciones que contendrán sus ofertas. Consulte [Crear ubicaciones](../offer-library/creating-placements.md).

1. Para cada ubicación, agregue una colección. Consulte [Crear colecciones](../offer-library/creating-collections.md).

1. Elija clasificar ofertas por **[!UICONTROL clasificación de IA]** en la lista desplegable y haga clic en **[!UICONTROL Agregar clasificación]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Seleccione el modelo de IA que ha creado. Se muestran todos los detalles del modelo.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Haga clic en **[!UICONTROL Seleccionar]**. El modelo de IA ahora está asociado a la ubicación.

Si se admiten varias ofertas, el sistema de modelos entrenado determinará qué oferta debe presentarse primero para una ubicación determinada.

