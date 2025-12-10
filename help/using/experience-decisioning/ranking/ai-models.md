---
solution: Journey Optimizer
product: Journey Optimizer
title: Introducción a los modelos de IA
description: Obtenga información acerca de los modelos de IA que permiten clasificar ofertas
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 18%

---

# Introducción a los modelos de IA {#ai-models}

[!DNL Journey Optimizer] le permite utilizar un sistema de modelos entrenado que clasifica las ofertas para mostrarlas en un perfil determinado.

Esta característica le permite crear diferentes **modelos de IA** basados en sus objetivos comerciales. Al usar estas diferentes estrategias basadas en objetivos en una decisión, el sistema de modelos entrenado le ayudará a comprender cómo los diferentes modelos de IA afectan sus objetivos.

<!--For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.-->

## Tipos de modelos de IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="Elección del tipo de modelo"
>abstract="Seleccione el tipo de modelo de IA que desea crear: **Optimización automática** optimiza las ofertas en función del rendimiento de ofertas anteriores, mientras que **Optimización personalizada** optimiza y personaliza ofertas en función de públicos y rendimiento de ofertas."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Creación de un modelo de IA"

Hay dos tipos de modelos de IA disponibles en [!DNL Journey Optimizer]:

* **Los modelos de optimización automática** tienen como objetivo ofrecer ofertas que maximicen el retorno (KPI) establecido por los clientes empresariales. Estos KPI pueden adoptar la forma de tasas de conversión, ingresos, etc. En este punto, la optimización automática se centra en optimizar los clics de oferta con la conversión de ofertas como objetivo. La optimización automática no está personalizada y se optimiza en función del rendimiento &quot;global&quot; de las ofertas. [Más información](auto-optimization-model.md)

* Los **modelos de optimización personalizados** le permiten definir objetivos comerciales y utilizan datos de clientes para entrenar modelos orientados a negocios a fin de ofrecer ofertas personalizadas y maximizar KPI. [Más información](personalized-optimization-model.md)

## Creación de un modelo de IA {#create-ai-model}

Los pasos principales para poder crear y utilizar modelos de IA son los siguientes:

1. Cree un conjunto de datos donde se recopilen los eventos de conversión e impresión. [Más información](../data-collection/create-dataset.md)

1. Cree un modelo de IA que aproveche los eventos del conjunto de datos para clasificar ofertas. [Más información](create-ai-models.md)

1. Configure el esquema de oferta para capturar eventos automáticamente. [Más información](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Los modelos de clasificación requieren que los eventos de comentarios se envíen como eventos de experiencia para que se recopilen. [Más información sobre la toma de decisiones](../data-collection/data-collection.md)

1. Asigne el modelo de IA a una estrategia de selección para clasificar las ofertas aptas. [Más información](../selection-strategies.md#select-ranking-method)
