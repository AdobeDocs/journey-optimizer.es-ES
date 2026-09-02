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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 11%

---

# Acciones de [!DNL Adobe Campaign] versiones 7 y 8 {#using_campaign_v7-v8}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar la integración de Adobe Campaign v7 y v8 para enviar correos electrónicos, notificaciones push y SMS desde sus recorridos a través de la mensajería transaccional de Campaign.

>[!ENDSHADEBOX]

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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo usar Adobe Campaign v7/v8 como acción en Journey Optimizer recorrido para enviar correos electrónicos, notificaciones push y SMS a través de la mensajería transaccional de Campaign.

**Intenciones:**

* Añadir una acción de Campaign v7/v8 a un recorrido para enviar mensajes transaccionales
* Asigne campos de evento de recorrido o fuente de datos a los parámetros de carga útil de mensajes de Campaign
* Combine acciones de las versiones 7 y 8 de Campaign con acciones nativas del canal de Journey Optimizer en el mismo recorrido
* Configure la acción dedicada necesaria para la integración de las versiones 7 y 8 de Campaign

**Glosario:**

* **Mensajería transaccional de Campaign**: La capacidad de Adobe Campaign v7/v8 para enviar mensajes activados (correo electrónico, SMS, push) a través de una acción dedicada integrada con Journey Optimizer *(específico del producto)*
* **Parámetros de acción**: campos en el panel de actividad de recorrido que asignan datos de recorrido a la carga útil de mensaje de Campaign esperada *(específica del producto)*

**Protecciones:**

* Adobe configura la conexión entre Journey Optimizer y la instancia de Campaign en el momento del aprovisionamiento; póngase en contacto con Adobe para habilitarla.
* Se debe configurar una acción específica antes de que las acciones de las versiones 7 y 8 de Campaign estén disponibles en la paleta recorrido.
* Las acciones de las versiones 7 y 8 de Campaign no se pueden usar con las actividades Leer audiencia o Calificación de audiencias.
* El acceso a la mensajería transaccional de Campaign y a los permisos necesarios en Campaign son requisitos previos.

**Terminología:**

* Nombre canónico: Adobe Campaign v7/v8 — Acrónimo: ACC — variantes: Campaign v7, Campaign v8, Campaign Classic
* No confunda: &quot;Acciones de Campaign v7/v8&quot; (se pueden usar junto con acciones nativas) ≠ &quot;Acciones de Campaign Standard&quot; (no se pueden combinar con acciones nativas en el mismo recorrido)

**PREGUNTAS MÁS FRECUENTES:**

* **P: ¿Quién configura la conexión entre Journey Optimizer y las versiones 7 y 8 de Campaign?** — Adobe configura la conexión en el momento del aprovisionamiento; debe ponerse en contacto con Adobe para configurarla.
* **P: ¿Pueden combinarse las acciones de las versiones 7 y 8 de Campaign con las acciones nativas del canal de Journey Optimizer en el mismo recorrido?** — Sí, las acciones de las versiones 7 y 8 de Campaign se pueden usar junto con las acciones del canal nativo; este no es el caso de las acciones de Campaign Standard.
* **Q: ¿Pueden usarse acciones de Campaign v7/v8 con actividades Leer audiencia o Calificación de audiencias?** — No, las acciones de las versiones 7 y 8 de Campaign no se pueden usar con las actividades Leer audiencia o Calificación de audiencias.
* **Q: ¿Cómo asigno los datos de recorrido a la carga útil del mensaje de Campaign?** — en el panel Parámetros de acción, asigne cada campo de carga útil esperado al campo correspondiente desde el evento de recorrido o la fuente de datos, del mismo modo que las acciones personalizadas.

+++
