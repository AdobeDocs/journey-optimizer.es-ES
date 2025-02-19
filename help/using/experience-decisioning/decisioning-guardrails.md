---
title: Limitaciones y protecciones de decisiones
description: Obtenga más información sobre las limitaciones y protecciones de Decisioning.
feature: Decisioning
role: User
level: Intermediate
source-git-commit: b6c31528784c0c8576e3200e7611a6b6cd43d7a7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 14%

---


# Limitaciones y protecciones de decisiones {#decisioning-guardrails}

Para garantizar un uso óptimo de Decisioning, tenga en cuenta las siguientes limitaciones y protecciones.

La lista completa de [!DNL Journey Optimizer] protecciones y limitaciones está disponible en [esta sección](../start/guardrails.md).

## Solicitudes de decisión

| Barrera | Límite |
| ------- | ------- |
| Solicitud de API de experiencia basada en código con política de decisión que utiliza la segmentación de Edge | 1500 |
| Solicitud de API de experiencia basada en código con política de decisión que no utiliza la segmentación de Edge | 5000 |

## Colecciones de elementos

| Barrera | Límite |
| ------- | ------- |
| Colecciones de elementos | 10K |
| Total de elementos de oferta por colección de elementos | 500 |

## Política de decisión

| Barrera | Límite |
| ------- | ------- |
| Número de estrategias de selección y elementos manuales por política de decisión | 10 |
| Máximo de elementos de oferta devueltos por política de decisión | 30 |

## Reglas de elegibilidad

| Barrera | Límite |
| ------- | ------- |
| Total de reglas de decisión y fórmulas de clasificación | 10K combinado |
| Número máximo de atributos de perfil por regla | 25 |
| Número máximo de atributos de datos de contexto por regla | 30 |
| Tamaño máximo de la regla pql | 15K (UTF-8) |
| Número máximo de niveles de anidación | 30 |

## Fórmulas de clasificación

| Barrera | Límite |
| ------- | ------- |
| Tamaño máximo de la fórmula de clasificación PQL | 8 K (UTF-8) |
| Número máximo de atributos de perfil | 25 |
| Número máximo de atributos de datos de contexto | 30 |
| Número máximo de niveles de anidación | 30 |

## Otros

| Barrera | Límite |
| ------- | ------- |
| Número de atributos personalizados por esquema del catálogo de ofertas | 100 |
| Total de elementos de oferta | 10K |
| Ubicaciones totales | 1K |
| Modelo de clasificación de IA | 5 |
| Reglas de frecuencia: número máximo de reglas de límite por oferta | 10 |
