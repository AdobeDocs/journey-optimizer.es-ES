---
title: Limitaciones y protecciones de decisiones
description: Obtenga más información acerca de las limitaciones y protecciones de Decisioning.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: bb672c8eb917a29aaebc7134cc833c423c0ecc5c
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 5%

---

# Limitaciones y protecciones de decisiones {#decisioning-guardrails}

Para garantizar un uso óptimo de Decisioning, tenga en cuenta las siguientes limitaciones y protecciones.

La lista completa de [!DNL Journey Optimizer] protecciones y limitaciones está disponible en [esta sección](../start/guardrails.md).

## Solicitudes de decisión {#decision-requests}

|| Barrera | Límite |
|| ------- | ------- |
|| Solicitud de API de experiencia basada en código con política de decisión mediante la segmentación de Edge | 1500 |
|| Solicitud de API de experiencia basada en código con política de decisión que no utiliza la segmentación de Edge | 5000 |
|| Número máximo de URI de superficie por solicitud de toma de decisiones de Edge | 30 |

## Colecciones de elementos {#item-collections}

|| Barrera | Límite |
|| ------- | ------- |
|| Colecciones de elementos | 10K |
|| Total de elementos de oferta por colección de elementos | 500 |

## Política de decisión {#decision-policy}

|| Barrera | Límite |
|| ------- | ------- |
|| Número de estrategias de selección y elementos manuales por política de decisión | 10 |
|| Máximo de elementos de oferta devueltos por política de decisión | 30 |

## Reglas de elegibilidad {#eligibility-rules}

|| Barrera | Límite |
|| ------- | ------- |
|| Total de reglas de decisión y fórmulas de clasificación | 10K combinado |
|| Número máximo de atributos de perfil por regla | 25 |
|| Número máximo de atributos de datos de contexto por regla | 30 |
|| Tamaño máximo de la regla pql | 15K (UTF-8) |
|| Número máximo de niveles de anidación | 30 |

## Fórmulas de clasificación {#ranking-formulas}

|| Barrera | Límite |
|| ------- | ------- |
|| Tamaño máximo de la fórmula de clasificación PQL | 8 K (UTF-8) |
|| Número máximo de atributos de perfil |25 |
|| Número máximo de atributos de datos de contexto | 30 |
|| Número máximo de niveles de anidación | 30 |

## Otros {#others}

|| Barrera | Límite |
|| ------- | ------- |
|| Número de atributos personalizados por esquema del catálogo de ofertas | 100 |
|| Total de elementos de oferta | 10K |
|| Ubicaciones totales | 1K |
|| Modelo de clasificación de IA | 5 |
|| Reglas de frecuencia: número máximo de reglas de límite por oferta | 10 |

## Configuraciones  {#configurations}

El número total de configuraciones que admite Decisioning no puede superar los 20 000.

El recuento total de configuración es el número total de [reglas de límite](items.md#capping) que existen en su zona protegida.
