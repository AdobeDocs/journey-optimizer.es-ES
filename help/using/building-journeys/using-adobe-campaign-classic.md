---
solution: Journey Optimizer
product: journey optimizer
title: Acciones de Adobe Campaign v7/v8
description: Obtenga información sobre las acciones de Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Acciones de Adobe Campaign v7/v8 {#using_campaign_classic}

Una integración está disponible si tiene Adobe Campaign v7 o v8. Le permite enviar correos electrónicos, notificaciones push y SMS utilizando las funciones de mensajería transaccional de Adobe Campaign.

Adobe configura la conexión entre las instancias de Journey Optimizer y Campaign en el momento del aprovisionamiento. Póngase en contacto con Adobe.

Para que esto funcione, debe configurar una acción dedicada. Consulte esta [sección](../action/acc-action.md).

En este ejemplo se presenta un caso de uso completo [sección](../building-journeys/ajo-ac.md).

1. Diseñe su recorrido, empezando por un evento . Consulte esta [sección](../building-journeys/journey.md).
1. En el **Acción** de la paleta, seleccione una acción de campaña y agréguela al recorrido.
1. En el **Parámetros de acción**, se muestran todos los campos esperados en la carga útil del mensaje. Debe asignar cada uno de estos campos al campo que desee utilizar, ya sea desde el evento o desde el origen de datos. Esto es similar a las acciones personalizadas. Consulte esta [sección](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
