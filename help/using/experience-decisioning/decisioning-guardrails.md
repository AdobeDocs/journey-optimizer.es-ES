---
title: Limitaciones y protecciones de decisiones
description: Obtenga más información acerca de las limitaciones y protecciones de Decisioning.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/oTljriepwffzR-LIAc2kWjTQx9Oj0QMgJpbghkSEsmY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: e42070c4cc1dde06786c4075b1e6e45e8c323c12
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 16%

---

# Limitaciones y protecciones de decisiones {#decisioning-guardrails}

Para garantizar un uso óptimo de Decisioning, tenga en cuenta las siguientes limitaciones y protecciones.

La lista completa de [!DNL Journey Optimizer] protecciones y limitaciones está disponible en [esta sección](../start/guardrails.md).

## Solicitudes de decisión {#decision-requests}

| Barrera | Límite |
| ------- | ------- |
| Solicitud de API de experiencia basada en código con política de decisión mediante la segmentación de Edge | 1500 |
| Solicitud de API de experiencia basada en código con política de decisión que no utiliza la segmentación de Edge | 5000 |
| Número máximo de URI de superficie por solicitud de toma de decisiones de Edge | 30 |

## Elementos de decisión {#decision-items}

| Barrera | Límite |
| ------- | ------- |
| Elementos de decisión totales | 10K |
| Tamaño máximo de elementos incluidos atributos (1 KB), máximo de 30 atributos | 1KB |
| Reglas de frecuencia: número máximo de reglas de límite por elemento de decisión | 10 |
| Número máximo de fragmentos de contenido de AEM por elemento de decisión | 5 |

## Colecciones de elementos {#item-collections}

| Barrera | Límite |
| ------- | ------- |
| Colecciones de elementos | 10K |
| Elementos de decisión totales por colección | 500 |

## Política de decisión {#decision-policy}

| Barrera | Límite |
| ------- | ------- |
| Número de estrategias de selección y elementos manuales por política de decisión | 10 |
| Número máximo de elementos de decisión devueltos por política de decisión | 30 |
| Políticas de decisión máximas por correo electrónico | 10 |

## Reglas de elegibilidad {#eligibility-rules}

| Barrera | Límite |
| ------- | ------- |
| Total de reglas de decisión y fórmulas de clasificación | 10K combinado |
| Número máximo de atributos de perfil por regla | 25 |
| Número máximo de atributos de datos de contexto por regla | 30 |
| Tamaño máximo de la regla pql | 15K (UTF-8) |
| Número máximo de niveles de anidación | 30 |

## Fórmulas de clasificación {#ranking-formulas}

| Barrera | Límite |
| ------- | ------- |
| Tamaño máximo de la fórmula de clasificación PQL | 8 K (UTF-8) |
| Número máximo de atributos de perfil | 25 |
| Número máximo de atributos de datos de contexto | 30 |
| Número máximo de niveles de anidación | 30 |

## Otros {#others}

| Barrera | Límite |
| ------- | ------- |
| Número de atributos personalizados por esquema de catálogo de artículos | 100 |
| Ubicaciones totales | 1K |
| Modelo de clasificación de IA | 5 |

## Configuraciones {#configurations}

El número total de configuraciones que admite Decisioning no puede superar los 20 000.

El recuento total de configuración es el número total de [reglas de límite](items.md#capping) que existen en su zona protegida.
