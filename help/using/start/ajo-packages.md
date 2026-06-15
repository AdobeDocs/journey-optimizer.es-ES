---
solution: Journey Optimizer
product: journey optimizer
title: Funciones de Journey Optimizer por paquete
description: Comprenda qué funciones de Adobe Journey Optimizer están disponibles en función de la licencia, el paquete y los canales habilitados.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: recorrido optimizer, paquete, licencia, seleccionar, principal, final, funciones, funciones, modular, canales
hide: true
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 5%

---


# ¿Qué hay disponible en mi paquete [!DNL Adobe Journey Optimizer]? {#ajo-packages}

>[!BEGINSHADEBOX]

**En esta página:** Averigüe qué capacidades de Adobe Journey Optimizer desbloquea el paquete, tanto si utiliza el modelo actual de Campañas y Recorridos como las licencias heredadas de Select, Prime y Ultimate, de modo que pueda confirmar lo que está disponible y saltar a cada función.

>[!ENDSHADEBOX]

Las capacidades de [!DNL Adobe Journey Optimizer] varían según el acuerdo de licencia, los canales habilitados y los permisos de usuario. Utilice esta guía para comprender qué funciones suelen estar disponibles en el paquete y vaya directamente a la documentación del producto para cada función.

La disponibilidad también puede depender de la configuración del canal, los requisitos previos de implementación y los complementos adquiridos. Seleccione la ficha que coincida con el modelo de licencia.

>[!BEGINTABS]

>[!TAB Recorridos y campañas]

Esta ficha se aplica a los clientes con licencia del modelo de empaquetado modular actual [!DNL Adobe Journey Optimizer] (Journey Optimizer - Campañas, Journey Optimizer - Recorridos o Journey Optimizer - Campañas y Recorridos).

## Paquetes base {#current-packages}

| Paquete | Qué incluye |
|---------|----------------|
| **Journey Optimizer - Campañas** | Campaign Orchestration: flujos de trabajo de audiencia de uno o varios pasos para la participación por lotes. Mensajería transaccional por correo electrónico, push y SMS incluido. |
| **Journey Optimizer - Recorridos** | Real-time Journey Orchestration: recorridos activados por eventos que admiten el streaming y el procesamiento por lotes. Mensajería transaccional por correo electrónico, push y SMS incluido. |
| **Journey Optimizer - Campañas y Recorridos** | Orquestación de campaña y Real-time Journey Orchestration combinados. Mensajería transaccional por correo electrónico, push y SMS incluido. |

>[!NOTE]
>
>El derecho total del volumen de datos difiere según el paquete: **Campañas** los clientes tienen derecho a 15 KB por perfil direccionable; los clientes de **Recorridos** y **Campañas y Recorridos** tienen derecho a 75 KB por perfil direccionable.

Los siguientes complementos amplían la cobertura de canal sobre cualquier paquete base. El complemento **Todos los canales** agrupa los paquetes de entrega saliente, móvil y web juntos.

| Complemento de | Canales desbloqueados |
|--------|----------------|
| **Envío saliente** | Correo electrónico, notificaciones push, correo directo. Incluye aspectos básicos de entrega. |
| **Mobile** | Mensajería en la aplicación, notificaciones push, tarjetas de contenido y canales basados en código para superficies móviles |
| **Web** | Canal web y canales basados en código para superficies web |
| **Todos los canales** | Paquetes de envío saliente + móvil + web |
| **Toma de decisiones** | Decisiones de oferta en tiempo real y optimización con tecnología de IA |

## Matriz de capacidades {#capability-matrix-current}

| Capacidad | Lo que puede hacer | Journey Optimizer - Campañas | JOURNEY OPTIMIZER - RECORRIDOS | Journey Optimizer: Campañas y Recorridos | Complemento requerido | Más información |
|-----------|----------------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|-----------|
| **Mensajería transaccional** | Enviar mensajes activados en tiempo real por correo electrónico, push o SMS | ✓ | ✓ | ✓ | — | [Más información sobre la mensajería transaccional](../building-journeys/journey-gs.md) |
| **Correo electrónico** | Diseño y envío de mensajes de correo electrónico personalizados | ✓ | ✓ | ✓ | Entrega saliente | [Más información sobre cómo enviar correo electrónico](../email/get-started-email.md) |
| **Notificaciones push** | Envío de alertas push móviles | ✓ | ✓ | ✓ | Entrega saliente | [Aprenda a enviar notificaciones push](../push/get-started-push.md) |
| **Correo directo** | Creación y envío de fragmentos de correo físico | ✓ | ✓ | ✓ | Entrega saliente | [Aprenda a utilizar el correo postal](../direct-mail/get-started-direct-mail.md) |
| **SMS / MMS** | Envío de mensajes de texto y multimedia | ✓ | ✓ | ✓ | Entrega saliente | [Aprenda a enviar mensajes móviles](../mobile/get-started-mobile.md) |
| **Mensajería en la aplicación** | Mostrar mensajes dentro de la aplicación móvil | ✓ | ✓ | ✓ | Móvil | [Aprenda a utilizar la mensajería en la aplicación](../in-app/get-started-in-app.md) |
| **Tarjetas de contenido** | Entrega de mensajes persistentes y no intrusivos en el producto | ✓ | ✓ | ✓ | Móvil | [Aprenda a utilizar las tarjetas de contenido](../content-card/get-started-content-card.md) |
| **Canal web** | Personalizar páginas web en tiempo real | ✓ | ✓ | ✓ | Web | [Aprenda a utilizar el canal web](../web/get-started-web.md) |
| **Experiencias basadas en código** | Personalice cualquier superficie mediante API o SDK | ✓ | ✓ | ✓ | Móvil o web | [Aprenda a utilizar experiencias basadas en código](../code-based/get-started-code-based.md) |
| **WhatsApp** | Enviar mensajes a través de WhatsApp Business | ✓ | ✓ | ✓ | WhatsApp | [Aprende a usar WhatsApp](../whatsapp/get-started-whatsapp.md) |
| **Campañas orquestadas** | Diseñe flujos de trabajo de audiencia de varios pasos para la participación por lotes. Canales admitidos: correo electrónico, SMS, push y correo directo. | ✓ | — | ✓ | — | [Aprenda a utilizar campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md) |
| **recorridos automatizados** | Diseñar recorridos de clientes en tiempo real activados por eventos | — | ✓ | ✓ | — | [Aprenda a crear recorridos](../building-journeys/journey-gs.md) |
| **déclencheur en tiempo real** | Reacción a los eventos de los clientes a medida que ocurren | — | ✓ | ✓ | — | [Más información sobre los eventos de recorrido](../event/about-events.md) |
| **Toma de decisiones** | Seleccione la mejor oferta para cada cliente en tiempo real | Depende de su licencia | Depende de su licencia | Depende de su licencia | Toma de decisiones | [Aprenda a utilizar la toma de decisiones](../experience-decisioning/gs-experience-decisioning.md) |
| **Clasificación con tecnología de IA** | Optimización de la selección de ofertas mediante aprendizaje automático | Depende de su licencia | Depende de su licencia | Depende de su licencia | Toma de decisiones | [Más información sobre los modelos de IA](../offers/ranking/ai-models.md) |

>[!TAB Seleccionar / Prime / Ultimate]

Esta pestaña se aplica a los clientes con acuerdos de licencia existentes que utilizan la terminología de empaquetado Select, Prime o Ultimate.

## Resúmenes de paquetes {#package-summaries}

+++**Seleccionar**

El más adecuado para las organizaciones que empiezan con la mensajería por lotes y transaccional:

- Campañas por lotes programadas y mensajería transaccional
- Ejecución de la campaña principal y del recorrido
- Fundamentos de canales de correo electrónico, SMS, push y acciones personalizadas
- Protecciones de orquestación estándar

+++

+++**Prime**

Incluye todo en Select, además de orquestación en tiempo real y canales entrantes:

- Orquestación de recorrido activada por eventos en tiempo real
- Canales entrantes: web, mensajería en la aplicación, experiencias basadas en código, tarjetas de contenido y correo directo
- Segmentación y direccionamiento avanzados de audiencias

+++

+++**Ultimate**

Incluye todo lo que hay en Prime, además de la toma de decisiones y la optimización avanzada:

- Decisiones y personalización de ofertas en tiempo real
- Modelos de optimización y clasificación con tecnología de IA
- Capacidades avanzadas de creación de informes y experimentación

+++

## Matriz de capacidades {#capability-matrix-legacy}

| Capacidad | Lo que puede hacer | Seleccionar | Prime | Ultimate | Más información |
|-----------|----------------|:------:|:-----:|:--------:|-----------|
| **Correo electrónico** | Diseño y envío de mensajes de correo electrónico personalizados | Incluido | Incluido | Incluido | [Más información sobre cómo enviar correo electrónico](../email/get-started-email.md) |
| **SMS / MMS** | Envío de mensajes de texto y multimedia | Incluido | Incluido | Incluido | [Aprenda a enviar mensajes móviles](../mobile/get-started-mobile.md) |
| **Notificaciones push** | Envío de alertas push móviles | Incluido | Incluido | Incluido | [Aprenda a enviar notificaciones push](../push/get-started-push.md) |
| **Campañas por lotes** | Programación de mensajes para una audiencia | Incluido | Incluido | Incluido | [Aprenda a crear campañas](../campaigns/get-started-with-campaigns.md) |
| **recorridos automatizados** | Diseño de recorridos de cliente activados por eventos | Incluido | Incluido | Incluido | [Aprenda a crear recorridos](../building-journeys/journey-gs.md) |
| **déclencheur de recorrido en tiempo real** | Reaccionar ante el comportamiento del cliente a medida que sucede | — | Incluido | Incluido | [Más información sobre los eventos de recorrido](../event/about-events.md) |
| **Mensajería en la aplicación** | Mostrar mensajes dentro de la aplicación móvil | — | Incluido | Incluido | [Aprenda a utilizar la mensajería en la aplicación](../in-app/get-started-in-app.md) |
| **Canal web** | Personalizar páginas web en tiempo real | — | Incluido | Incluido | [Aprenda a utilizar el canal web](../web/get-started-web.md) |
| **Experiencias basadas en código** | Personalice cualquier superficie mediante API o SDK | — | Incluido | Incluido | [Aprenda a utilizar experiencias basadas en código](../code-based/get-started-code-based.md) |
| **Tarjetas de contenido** | Entrega de mensajes persistentes y no intrusivos en el producto | — | Incluido | Incluido | [Aprenda a utilizar las tarjetas de contenido](../content-card/get-started-content-card.md) |
| **Correo directo** | Creación y envío de fragmentos de correo físico | — | Disponible con Prime y versiones posteriores | Incluido | [Aprenda a utilizar el correo postal](../direct-mail/get-started-direct-mail.md) |
| **Toma de decisiones** | Seleccione la mejor oferta para cada cliente en tiempo real | — | — | Incluido | [Aprenda a utilizar la toma de decisiones](../experience-decisioning/gs-experience-decisioning.md) |
| **Clasificación con tecnología de IA** | Optimización de la selección de ofertas y contenido mediante el aprendizaje automático | — | — | Incluido | [Más información sobre los modelos de IA](../offers/ranking/ai-models.md) |
| **WhatsApp** | Enviar mensajes a través de WhatsApp Business | Depende de la licencia y de la configuración del canal | Depende de la licencia y de la configuración del canal | Depende de la licencia y de la configuración del canal | [Aprende a usar WhatsApp](../whatsapp/get-started-whatsapp.md) |

>[!ENDTABS]
