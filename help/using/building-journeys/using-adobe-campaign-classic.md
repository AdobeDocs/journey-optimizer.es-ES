---
solution: Journey Optimizer
product: journey optimizer
title: Acciones de Adobe Campaign v7/v8
description: Obtenga información acerca de las acciones de las versiones 7 y 8 de Adobe Campaign
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: recorrido, integration, campaign, v7, v8, classic
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 39%

---

# Acciones de Adobe Campaign v7/v8 {#using_campaign_classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Acciones personalizadas"
>abstract="Una integración está disponible si tiene Adobe Campaign v7 o v8. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funciones de mensajería transaccional de Adobe Campaign."

Una integración está disponible si tiene Adobe Campaign v7 o v8. Le permitirá enviar correos electrónicos, notificaciones push y SMS mediante las funciones de mensajería transaccional de Adobe Campaign.

Adobe configura la conexión entre las instancias de Journey Optimizer y Campaign en el momento del aprovisionamiento. Adobe de contacto.

Para que esto funcione, debe configurar una acción dedicada. Consulte esta [sección](../action/acc-action.md).

En este documento se presenta un caso de uso completo [sección](../building-journeys/ajo-ac.md).

1. Diseñe su recorrido, empezando por un evento. Consulte esta [sección](../building-journeys/journey.md).
1. En el **Acción** de la paleta, seleccione una acción de Campaign y agréguela al recorrido.
1. En el **Parámetros de acción**, se muestran todos los campos esperados en la carga útil del mensaje. Debe asignar cada uno de estos campos con el campo que desea utilizar, ya sea desde el evento o desde el origen de datos. Esto es similar a las acciones personalizadas. Consulte esta [sección](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
