---
title: Acciones de Adobe Campaign v7/v8
description: Obtenga información sobre las acciones de Adobe Campaign v7/v8
feature: Acciones
topic: Administración
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 12%

---

# Acciones de Adobe Campaign v7/v8 {#using_campaign_classic}

Una integración está disponible si tiene Adobe Campaign v7 o v8. Le permitirá enviar correos electrónicos, notificaciones push y SMS utilizando las funciones de mensajería transaccional de Adobe Campaign.

La conexión entre las instancias de Journey Optimizer y Campaign se configura por Adobe en el momento del aprovisionamiento. Adobe de contacto.

Para que esto funcione, debe configurar una acción dedicada. Consulte esta [sección](../action/acc-action.md).

En esta [sección](../building-journeys/campaign-classic-use-case.md) se presenta un caso de uso completo.

1. Diseñe el recorrido, empezando por un evento . Consulte esta [sección](../building-journeys/journey.md).
1. En la sección **Action** de la paleta, seleccione una acción de Campaign y agréguela al recorrido.
1. En **Action parameters**, se muestran todos los campos esperados en la carga útil del mensaje. Debe asignar cada uno de estos campos al campo que desee utilizar, ya sea desde el evento o desde el origen de datos. Esto es similar a las acciones personalizadas. Consulte esta [sección](../building-journeys/using-custom-actions.md).

![](../assets/accintegration2.png)
