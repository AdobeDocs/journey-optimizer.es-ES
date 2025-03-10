---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Espera en campañas de varios pasos
description: Aprenda a utilizar la actividad Espera en campañas de varios pasos
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 77%

---

# Espera {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Actividad de espera"
>abstract="La actividad **Espera** se utiliza para retrasar la transición de una actividad a otra."

La actividad **Esperar** es una actividad de **Control de flujo**. Se utiliza para permitir que transcurra un cierto tiempo entre dos actividades que se están ejecutando. Por ejemplo, para esperar varios días después de una actividad de envío de correo electrónico y, después, analizar las aperturas y los clics generados durante este período antes de realizar cualquier operación de seguimiento (correo electrónico recordatorio, creación de un público, etc.).

## Configuración{#wait-configuration}

Siga estos pasos para configurar la actividad **Esperar**:

1. Agregue una actividad **Wait** a su campaña de varios pasos.

1. Especifique la **Duración** de la espera entre las transiciones entrantes y salientes.

1. Seleccione la unidad de tiempo en el campo **Periodos**: segundos, minutos, horas, días.

## Ejemplo{#wait-example}

El siguiente ejemplo ilustra la actividad **Esperar** en un caso de uso típico. Se envía una invitación por correo electrónico a un evento. 24 horas después de su envío, se realiza un envío de SMS a la misma población.

![](../assets/workflow-wait-example.png)
