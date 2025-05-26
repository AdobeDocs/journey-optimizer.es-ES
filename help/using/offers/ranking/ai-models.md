---
product: experience platform
solution: Experience Platform
title: Introducción a los modelos de IA
description: Obtenga información acerca de los modelos de IA que permiten clasificar ofertas
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: e63a21b5dcc8f227d56c696c8fd0825c75684189
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 13%

---

# Introducción a los modelos de IA {#ai-models}

[!DNL Journey Optimizer] le permite utilizar un sistema de modelos entrenado que clasifica las ofertas para mostrarlas en un perfil determinado.

Esta característica le permite crear diferentes **modelos de IA** basados en sus objetivos comerciales. Al usar estas diferentes estrategias basadas en objetivos en una decisión, el sistema de modelos entrenado le ayudará a comprender cómo los diferentes modelos de IA afectan sus objetivos.

Por ejemplo, puede seleccionar un modelo de IA para el canal de correo electrónico y otro para el canal push. Para cada canal, el sistema de modelos entrenado aprovechará varios puntos de datos para determinar qué oferta se debe presentar primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas o una [fórmula de clasificación](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Por ahora, los modelos de clasificación no son compatibles con los canales creados por Journey Optimizer.

## Tipos de modelos de IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Elección del tipo de modelo"
>abstract="Seleccione el tipo de modelo de IA que desea crear: **Optimización automática** optimiza las ofertas en función del rendimiento de ofertas anteriores, mientras que **Optimización personalizada** optimiza y personaliza ofertas en función de públicos y rendimiento de ofertas."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Crear un modelo de IA&quot;—>"

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
   >Los modelos de clasificación requieren que los eventos de comentarios se envíen como eventos de experiencia para que se recopilen. [Más información acerca de la recopilación de datos de Administración de decisiones](../data-collection/data-collection.md)

1. Asigne el modelo de IA a una ubicación en una decisión para clasificar las ofertas elegibles. [Más información](../offer-activities/configure-offer-selection.md)
