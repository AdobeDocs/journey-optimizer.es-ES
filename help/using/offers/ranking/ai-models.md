---
product: experience platform
solution: Experience Platform
title: Introducción a los modelos de IA
description: Obtenga información sobre los modelos de IA que permiten clasificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12bc2373ac5c391764df3880c5c87666a19e99b2
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Introducción a los modelos de IA {#ai-models}

[!DNL Journey Optimizer] permite utilizar un sistema de modelos entrenado que clasifica las ofertas para mostrarlas en un perfil determinado.

Esta función le permite crear diferentes **Modelos de IA** en función de sus objetivos comerciales. Utilizando estas diferentes estrategias basadas en objetivos en una decisión, el sistema de modelos entrenado le ayudará a comprender cómo los diferentes modelos de IA están afectando a sus objetivos.

Por ejemplo, puede seleccionar un modelo de IA para el canal de correo electrónico y otro para el canal push. Para cada canal, el sistema de modelos entrenado utilizará múltiples puntos de datos para determinar qué oferta debe presentarse primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas o una [fórmula de clasificación](create-ranking-formulas.md).

## Tipos de modelos de IA {#ai-model-types}

Hay dos tipos de modelos de IA disponibles en [!DNL Journey Optimizer]:

* **Modelos de optimización automática** tiene como objetivo ofrecer ofertas que maximicen los KPI (return) establecidos por los clientes empresariales. Estos KPI podrían presentar tasas de conversión, ingresos, etc. En este punto, la optimización automática se centra en optimizar los clics de ofertas con la conversión de ofertas como nuestro objetivo. La optimización automática no está personalizada y se optimiza según el rendimiento &quot;global&quot; de las ofertas. [Más información](auto-optimization-model.md)

* **Modelos de personalización** le permite definir los objetivos del negocio y utilizar los datos de los clientes para formar modelos orientados al negocio que ofrezcan ofertas personalizadas y maximicen los KPI. [Más información](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >Actualmente, el uso de modelos de Optimización personalizada está disponible en el acceso anticipado solo para usuarios seleccionados.

## Creación de un modelo de IA {#create-ai-model}

Los pasos principales para crear y utilizar modelos de IA son los siguientes:

1. Cree un conjunto de datos donde se recopilen los eventos de conversión e impresión. [Más información](create-dataset.md)
1. Cree un modelo de IA que aproveche los eventos del conjunto de datos para clasificar ofertas. [Más información](create-ranking-strategies.md)
1. Configure el esquema de oferta para que capture automáticamente los eventos. [Más información](schema-requirement.md)
1. Asigne el modelo de IA a una colocación en una decisión para clasificar las ofertas aptas. [Más información](../offer-activities/configure-offer-selection.md)
