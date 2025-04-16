---
title: Limitaciones y protecciones de decisiones
description: Obtenga más información sobre las barreras y limitaciones de Decisioning.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 17%

---

# Limitaciones y protecciones de decisiones {#decisioning-guardrails}

Para garantizar un uso óptimo de Decisioning, tenga en cuenta las siguientes limitaciones y protecciones.

La lista completa de [!DNL Journey Optimizer] protecciones y limitaciones está disponible en [esta sección](../start/guardrails.md).

## Solicitudes de decisión

| Barandilla | Límite |
| ------- | ------- |
| solicitud de API de experiencia basadas en Code con directiva de decisión que usan Edge segmentación | 1500 |
| solicitud de API de experiencia basadas en Code con decisión directiva no usar Edge segmentación | 5000 |

## Colecciones de elementos

| Barandilla | Límite |
| ------- | ------- |
| Colecciones de elementos | 10K |
| Total oferta elementos por elemento colección | 500 |

## Política de decisión

| Barandilla | Límite |
| ------- | ------- |
| Número de estrategias de selección y elementos manuales por decisión directiva | 10 |
| Máximo de elementos de oferta devueltos por política de decisión | 30 |

## Reglas de idoneidad

| Barandilla | Límite |
| ------- | ------- |
| Reglas de decisión totales y fórmulas de clasificación | 10K combinados |
| Número máximo de atributos de perfil por regla | 25 |
| Número máximo de atributos de datos de contexto por regla | 30 |
| Tamaño máximo de la regla pql | 15K (UTF-8) |
| Número máximo de niveles de anidación | 30 |

## Fórmulas de clasificación

| Barandilla | Límite |
| ------- | ------- |
| Tamaño máximo de clasificación fórmula PQL | 8 K (UTF-8) |
| Número máximo de atributos de perfil | 25 |
| Número máximo de atributos de datos de contexto | 30 |
| Número máximo de niveles de anidación | 30 |

## Otros

| Barandilla | Límite |
| ------- | ------- |
| Número de atributos personalizados por esquema del catálogo de ofertas | 100 |
| Total de elementos de la oferta | 10K |
| Colocaciones totales | 1K |
| Modelo de clasificación de IA | 5 |
| Reglas de frecuencia - Número máximo de reglas de limitación por oferta | 10 |
