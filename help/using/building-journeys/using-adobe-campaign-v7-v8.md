---
solution: Journey Optimizer
product: journey optimizer
title: Acciones en las versiones 7 y 8 de Adobe Campaign
description: Obtenga información acerca de las acciones de las versiones 7 y 8 de Adobe Campaign
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: recorrido, integración, campaign, v7, v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
source-git-commit: 339285cbc82d5b30b221feb235ed8425a66f8802
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 6%

---

# [!DNL Adobe Campaign] acciones de las versiones 7 y 8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Acciones personalizadas"
>abstract="Hay una integración disponible si tiene [!DNL Adobe Campaign] v7 o v8. Le permite enviar correos electrónicos, notificaciones push y SMS mediante las funciones de mensajería transaccional de [!DNL Adobe Campaign]."

Hay una integración disponible si tiene [!DNL Adobe Campaign] v7 o v8. Le permite enviar correos electrónicos, notificaciones push y SMS mediante las funciones de mensajería transaccional de [!DNL Adobe Campaign].

Adobe configura la conexión entre las instancias de Journey Optimizer y Campaign en el momento del aprovisionamiento. Póngase en contacto con Adobe.

**Cuándo se debe usar**: Use las acciones de las versiones 7 y 8 de Campaign cuando la mensajería dependa de plantillas transaccionales de Campaign, modelos de datos específicos de Campaign o flujos de trabajo de envío de Campaign existentes.

**Requisitos previos**

* La instancia de [!DNL Adobe Campaign] v7/v8 está aprovisionada y conectada a Journey Optimizer por Adobe.
* Tiene acceso a la mensajería transaccional de Campaign y los permisos necesarios.

Para que esto funcione, debe configurar una acción dedicada. Consulte esta [sección](../action/acc-action.md).

Se presenta un caso de uso de extremo a extremo en esta [sección](../building-journeys/ajo-ac.md).

1. Diseñe su recorrido, empezando por un evento. Consulte esta [sección](../building-journeys/journey.md).
1. En la sección **Action** de la paleta, seleccione una acción de Campaign y agréguela al recorrido.
1. En los **parámetros de acción**, se muestran todos los campos esperados en la carga útil del mensaje. Debe asignar cada uno de estos campos con el campo que desea utilizar, ya sea desde el evento o desde el origen de datos. Esto es similar a las acciones personalizadas. Consulte esta [sección](../building-journeys/using-custom-actions.md).

>[!NOTE]
>
>* Las acciones de las versiones 7 y 8 de Campaign se pueden usar junto con las acciones del canal nativo en el mismo recorrido. Esto no se aplica a las acciones de Campaign Standard. Consulte [Protecciones de actividad de campaña](../start/guardrails.md#ac-g).
>* Las acciones de las versiones 7 y 8 de Campaign no se pueden usar con las actividades Leer audiencia o Calificación de audiencias. Consulte las protecciones Leer audiencia y Calificación de audiencias en la página Protecciones.

![[!DNL Adobe Campaign] configuración de acciones e integración de las versiones 7 y 8](assets/accintegration2.png)
