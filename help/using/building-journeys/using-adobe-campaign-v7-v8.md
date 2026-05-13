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
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 28%

---

# Acciones de [!DNL Adobe Campaign] versiones 7 y 8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Acciones personalizadas"
>abstract="Una integración está disponible si tiene [!DNL Adobe Campaign] versión 7u 8. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funcionalidades de mensajería transaccional de [!DNL Adobe Campaign]."

Una integración está disponible si tiene [!DNL Adobe Campaign] versión 7u 8. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funcionalidades de mensajería transaccional de [!DNL Adobe Campaign].

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
