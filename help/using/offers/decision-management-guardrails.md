---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Limitaciones y mecanismos de protección de gestión de decisiones
description: Obtenga más información acerca de las limitaciones y protecciones de administración de decisiones.
badge: label="Heredado" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 18%

---

# Limitaciones y mecanismos de protección de gestión de decisiones {#decision-management-guardrails}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../experience-decisioning/gs-experience-decisioning.md)

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
| Tamaño máximo de ofertas que incluyen atributos (1 KB), máximo de 30 atributos | 1KB |
| Tamaño máximo de representación de la oferta (total para todas las ubicaciones) | 1KB |

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

## Configuraciones  {#configurations}

El número total de configuraciones que admite Administración de decisiones no puede superar los 20 000.

El recuento total de configuración es el número total de [reglas de límite](offer-library/add-constraints.md#capping) que existen en su zona protegida. Para cada regla de límite aplicada en todas las [ubicaciones](offer-library/creating-placements.md), la regla debe multiplicarse en todas las ubicaciones asociadas con la oferta especificada.
