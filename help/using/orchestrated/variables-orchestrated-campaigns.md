---
solution: Journey Optimizer
product: journey optimizer
title: Uso de variables en campañas organizadas
description: Aprenda a utilizar variables de evento en campañas orquestadas para crear condiciones y reglas de segmentación.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
version: Campaign Orchestration
exl-id: 3f2a1c0d-8e9b-4a7c-b5d1-0f2e3a4b5c6d
feature_v2: 
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 1%

---


# Uso de variables en campañas organizadas {#variables-oc}

## Cómo establecer variables {#set}

En una campaña orquestada, puede trabajar con variables; es decir, valores que impulsen el direccionamiento, las condiciones **[!UICONTROL Test]** y otra lógica de lienzo. Estos valores pueden proceder de dos lugares:

* **Una señal** — Si la programación de la campaña es **[!UICONTROL Activada por una señal]**, puede pasar parámetros cuando active la campaña. Estos parámetros están disponibles como variables en la campaña orquestada activada para esa ejecución. [Aprenda a almacenar en déclencheur una campaña organizada mediante una señal](trigger-orchestrated-campaign.md)

* **Variables globales**: puede definir pares de nombre-valor directamente en la campaña usando el menú **[!UICONTROL Editar variables]**, sin necesidad de API ni señal. [Aprenda a definir variables globales en campañas organizadas](global-variables.md)

>[!NOTE]
>
>Por ahora, las variables solo admiten valores de **text**.
>
>Las variables controlan **lógica de lienzo** (reglas, condiciones) y no se pueden usar para la personalización de mensajes.

## Usar variables en el lienzo {#use}

Las variables están disponibles en los siguientes lugares del lienzo:

* **Generador de reglas**: abra el editor de expresiones de una regla y use el selector de **variables de eventos** para seleccionar una variable e insertar su referencia en la expresión. [Más información sobre cómo editar expresiones](edit-expressions.md)

  En el ejemplo siguiente, se pasó una variable denominada `brand` y la regla la usa como condición de filtro.

  ![Condición del generador de reglas que utiliza una variable de marca de variables de eventos](assets/variables-rule.png){zoomable="yes"}

* **[!UICONTROL Prueba] actividad**: cuando define una condición, la lista desplegable **[!UICONTROL Tipo de condición]** enumera todas las variables en ámbito junto con **[!UICONTROL Recuento de población]**. Seleccione una variable para utilizarla como base para una rama de prueba. [Aprenda a configurar la actividad **[!UICONTROL Prueba]**](activities/test.md)

  En el ejemplo siguiente, la variable `channel` se usa para enrutar el flujo a distintas transiciones según su valor.

  ![Lista desplegable del tipo de condición de actividad de prueba que enumera la variable de canal](assets/variables-test.png){zoomable="yes"}
