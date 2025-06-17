---
title: Limitaciones y mecanismos de protección de gestión de decisiones
description: Obtenga más información acerca de las limitaciones y protecciones de administración de decisiones.
feature: Decisioning
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
source-git-commit: 70543fc2b70b388934c1b3f45e5405f02895a3af
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 16%

---

# Limitaciones y mecanismos de protección de gestión de decisiones {#decision-management-guardrails}

Para garantizar un uso óptimo de la administración de decisiones, tenga en cuenta las siguientes limitaciones y protecciones.

La lista completa de [!DNL Journey Optimizer] protecciones y limitaciones está disponible en [esta sección](../start/guardrails.md).

## Solicitudes de decisión

El rendimiento de entrega corresponde al número de respuestas de decisión que puede entregar el servicio de aplicaciones de gestión de decisiones en un período de tiempo especificado.

| Barrera | Límite |
| ------- | ------- |
| Solicitudes de API de decisiones por segundo | 500 por organización |
| Solicitudes de API de Edge Decisioning por segundo con segmentación de Edge | 1.500 por organización |
| Solicitudes de API de Edge Decisioning por segundo sin segmentación de Edge | 5.000 por organización |
| Ofertas devueltas por respuesta | Hasta 30 por ámbito de decisión o 100 en total |
| Número máximo de reglas de oferta involucradas por solicitud | 100 |

## Decisiones

| Barrera | Límite |
| ------- | ------- |
| Total de decisiones | 10K |
| Decisiones en directo | 1K |
| Ubicaciones por decisión | 30 |

## Colecciones

| Barrera | Límite |
| ------- | ------- |
| Ofertas por colección | 500 |
| Colecciones | 10K |
| Colecciones por decisión | 30 |

## Calificadores de colección

| Barrera | Límite |
| ------- | ------- |
| Calificador de colección por oferta o colección | 20 |
| Cualificadores de recopilación totales | 1.000 |

## Ofertas

| Barrera | Límite |
| ------- | ------- |
| Ofertas totales | 10K |
| Número máximo de **ofertas activas** por zona protegida | 10K |
| Tamaño máximo de ofertas que incluyen atributos (1 KB), máximo de 30 atributos | 1 KB |
| Tamaño máximo de representación de la oferta (total para todas las ubicaciones) | 1 KB |

## Reglas de elegibilidad

| Barrera | Límite |
| ------- | ------- |
| Total de reglas de decisión y fórmulas de clasificación | 10K combinado |
| Número máximo de atributos de perfil por regla | 25 |
| Número máximo de atributos de datos de contexto por regla | 30 |
| Tamaño máximo de la regla de PQL | 15K (UTF-8) |
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
| Ubicaciones | 1000 |
| Modelo de clasificación de IA | 5 |
| Límite de frecuencia: número máximo de reglas de límite por oferta | 10 |
