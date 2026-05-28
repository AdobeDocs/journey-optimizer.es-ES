---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introducción a los modelos de IA
description: Obtenga información acerca de los modelos de IA que permiten clasificar ofertas
badge: label="Heredado" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Ya5F8s8gr9dM-surRM-0K4VaM9GSs8jIZNVZ9b7pdIM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 27%

---

# Introducción a los modelos de IA {#ai-models}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

[!DNL Journey Optimizer] le permite utilizar un sistema de modelos entrenado que clasifica las ofertas para mostrarlas en un perfil determinado.

Esta característica le permite crear diferentes **modelos de IA** basados en sus objetivos comerciales. Al usar estas diferentes estrategias basadas en objetivos en una decisión, el sistema de modelos entrenado le ayudará a comprender cómo los diferentes modelos de IA afectan sus objetivos.

Por ejemplo, puede seleccionar un modelo de IA para el canal de correo electrónico y otro para el canal push. Para cada canal, el sistema de modelos entrenado aprovechará varios puntos de datos para determinar qué oferta se debe presentar primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas o una [fórmula de clasificación](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Actualmente, los modelos de IA no son compatibles con los canales creados por Journey Optimizer.

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Tipos de modelos de IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Elección del tipo de modelo"
>abstract="Seleccione el tipo de modelo de IA que desea crear: **Optimización automática** optimiza las ofertas en función del rendimiento de ofertas anteriores, mientras que **Optimización personalizada** optimiza y personaliza ofertas en función de públicos y rendimiento de ofertas."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Creación de un modelo de IA"

Hay dos tipos de modelos de IA disponibles en [!DNL Journey Optimizer]:

* **Los modelos de optimización automática** tienen como objetivo ofrecer ofertas que maximicen el retorno (KPI) establecido por los clientes empresariales. Estos KPI pueden adoptar la forma de tasas de conversión, ingresos, etc. En este punto, la optimización automática se centra en optimizar los clics de oferta con la conversión de ofertas como objetivo. La optimización automática no está personalizada y se optimiza en función del rendimiento &quot;global&quot; de las ofertas. [Más información](auto-optimization-model.md)

* Los **modelos de optimización personalizados** le permiten definir objetivos comerciales y utilizan datos de clientes para entrenar modelos orientados a negocios a fin de ofrecer ofertas personalizadas y maximizar KPI. [Más información](personalized-optimization-model.md)

## Creación de un modelo de IA {#create-ai-model}

Los pasos principales para crear y utilizar modelos de IA son los siguientes:

1. Cree un conjunto de datos donde se recopilen los eventos de conversión e impresión. [Más información](../data-collection/create-dataset.md)

1. Cree un modelo de IA que aproveche los eventos del conjunto de datos para clasificar ofertas. [Más información](create-ranking-strategies.md)

1. Configure el esquema de oferta para capturar eventos automáticamente. [Más información](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Los modelos de IA requieren que los eventos de comentarios se envíen como eventos de experiencia para que se recopilen. [Más información acerca de la recopilación de datos de Administración de decisiones](../data-collection/data-collection.md)

1. Asigne el modelo de IA a una ubicación en una decisión para clasificar las ofertas elegibles. [Más información](../offer-activities/configure-offer-selection.md)

## Vídeo tutorial {#video}

Aprenda a crear un modelo de IA para Offer Decisioning y cómo aplicarlo a una decisión.

>[!VIDEO](https://video.tv.adobe.com/v/3419959?quality=12)
