---
title: Acciones de Adobe Campaign v7/v8
description: Obtenga información sobre las acciones de Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---

# Acciones de Adobe Campaign v7/v8 {#using_campaign_classic}

Una integración está disponible si tiene Adobe Campaign v7 o v8. Le permitirá enviar correos electrónicos, notificaciones push y SMS utilizando las funciones de mensajería transaccional de Adobe Campaign.

La conexión entre las instancias de Journey Optimizer y Campaign se configura por Adobe en el momento del aprovisionamiento. Adobe de contacto.

Para que esto funcione, debe configurar una acción dedicada. Consulte esta [sección](../action/acc-action.md).

En este ejemplo se presenta un caso de uso completo [sección](../building-journeys/campaign-classic-use-case.md).

1. Diseñe el recorrido, empezando por un evento . Consulte esta [sección](../building-journeys/journey.md).
1. En el **Acción** de la paleta, seleccione una acción de Campaña y agréguela al recorrido.
1. En el **Parámetros de acción**, se muestran todos los campos esperados en la carga útil del mensaje. Debe asignar cada uno de estos campos al campo que desee utilizar, ya sea desde el evento o desde el origen de datos. Esto es similar a las acciones personalizadas. Consulte esta [sección](../building-journeys/using-custom-actions.md).

![](../assets/accintegration2.png)
