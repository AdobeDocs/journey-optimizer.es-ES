---
solution: Journey Optimizer
product: journey optimizer
title: Variables de evento de campaña de varios pasos
description: Aprenda a aprovechar las variables de eventos en sus campañas de varios pasos
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 17%

---

# Variables de evento de campaña de varios pasos {#event-variables}

Algunas actividades de campaña de varios pasos le permiten editar scripts en el editor de expresiones para realizar acciones específicas como recuperar datos procedentes de actividades anteriores, crear condiciones o calcular nombres de archivo basados en variables de evento.

## ¿Qué son las variables de evento? {#scripting}

Los scripts ejecutados en el contexto de una campaña de varios pasos tienen acceso a una serie de **objetos** globales adicionales, como la propia campaña de varios pasos que se está ejecutando (`ìnstance`), sus diversas tareas (`task`) o los eventos que activaron una tarea determinada (`event`).

A cada tipo de **objeto** se asocia una categoría de **variables** que se pueden aprovechar en el editor de expresiones al editar scripts en actividades como **[!UICONTROL JavaScript code]** o **[!UICONTROL Test]**.

* **Las variables de instancia** (`instance.vars.xxx`) son comparables a las variables globales. Las comparten todas las actividades.
* **Las variables de tarea** (`task.vars.xxx`) son comparables a las variables locales. Solo se utilizan en la tarea actual. Las actividades persistentes utilizan estas variables para conservar datos y, a veces, se utilizan para intercambiar datos entre las diferentes secuencias de comandos de una misma actividad.
* **Las variables de eventos** (`vars.xxx`) permiten el intercambio de datos entre las tareas básicas de un proceso de campaña de varios pasos. La tarea que activó la tarea en curso transfiere estas variables. A continuación, se pasan a las siguientes actividades. **Las variables de eventos** son las variables más utilizadas y deben utilizarse con preferencia sobre las variables de instancia.

## Aproveche las variables de evento en el editor de expresiones {#expression-editor}

Las variables de evento predefinidas están disponibles para su uso en el panel lateral izquierdo del editor de expresiones. También puede crear otras nuevas inicializando una nueva variable en el código.

![](assets/event-variables.png)

Además de estas variables de evento, también puede aprovechar el menú **[!UICONTROL Condiciones]** del panel izquierdo para generar condiciones y el menú **[!UICONTROL Agregar fecha actual]** para usar funciones relacionadas con el formato de fecha.
