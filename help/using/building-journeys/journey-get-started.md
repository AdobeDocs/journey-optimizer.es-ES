---
solution: Journey Optimizer
product: journey optimizer
title: 'Journey Orchestration: guía completa'
description: Guía completa para empezar a utilizar la orquestación de recorrido en Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: recorrido, orquestación, introducción, incorporación, funciones
source-git-commit: 4b14338cd2f152c95e87fa2a36f9c09f60b0806e
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 44%

---


# Journey Orchestration: guía completa{#journey-orchestration-guide}

Los recorridos de Adobe Journey Optimizer le permiten crear recorridos para el cliente personalizados que constan de varios pasos y que se adaptan en tiempo real al comportamiento y las necesidades de su público. Con un lienzo intuitivo de arrastrar y soltar, puede orquestar mensajes y acciones en varios canales, aprovechando los datos contextuales y la segmentación de audiencia para lograr el máximo impacto.

Tanto si explora déclencheur en tiempo real como si administra propiedades de recorrido o utiliza herramientas avanzadas como acciones y expresiones personalizadas, esta guía proporciona una hoja de ruta clara para diseñar y refinar recorridos con seguridad que proporcionen experiencias de cliente significativas y oportunas.

## ¿Qué son los recorridos?

Utilice [!DNL Journey Optimizer] para crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos. Diseñe escenarios avanzados de varios pasos que respondan al comportamiento de los clientes y a los eventos empresariales en tiempo real.

El diseñador de recorridos de Journey Optimizer proporciona todo lo que los especialistas en marketing y en recorrido necesitan para orquestar recorridos 1:1 de varios pasos en todos los canales. Esto incluye un lienzo intuitivo de arrastrar y soltar para organizar cada paso del recorrido, definir el público destinatario e incluir los mensajes, ofertas y contenido en todos los canales que verán los miembros del público destinatario en función del comportamiento, los datos contextuales y los eventos empresariales.

![Interfaz del diseñador de Recorrido con panel de paleta, lienzo y propiedades](assets/journey38.png)

**¿Listo para empezar a crear?** Aprenda a crear y diseñar su primer recorrido en [esta página](journey-gs.md).

## Introducción a recorrido {#section-getting-started}

Explore las áreas clave para dominar la orquestación de recorrido en Adobe Journey Optimizer.

>[!BEGINTABS]

>[!TAB Genere su primer recorrido]

Aprenda a crear y diseñar su primer recorrido desde cero, incluida la configuración de eventos, la adición de actividades y la realización de pruebas antes de publicar.

[![Más información](../assets/do-not-localize/learn-more-button.svg)](journey-gs.md)

>[!TAB Funcionalidades clave]

Descubra lo que puede hacer con recorrido: entrega en tiempo real, datos contextuales, acciones integradas y personalizadas, diseñador visual y capacidades de prueba.

[![Más información](../assets/do-not-localize/learn-more-button.svg)](#capabilities)

>[!TAB Casos de uso]

Explore ejemplos de recorridos del mundo real, incluidos correos electrónicos de bienvenida, optimización del tiempo de envío, envíos de aumento y segmentación entre semana.

[![Más información](../assets/do-not-localize/learn-more-button.svg)](#use-cases)

>[!TAB Recursos de aprendizaje]

Acceda a tutoriales de vídeo, guías paso a paso y documentación para dominar la creación de recorridos y solucionar problemas.

[![Más información](../assets/do-not-localize/learn-more-button.svg)](#learning-resources)

>[!ENDTABS]

## Funcionalidades clave {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=es)

**Envío en tiempo real y por lotes**

Envíe en tiempo real un **envío unitario** que se activa cuando se recibe un evento, o **en lote** con los públicos de Adobe Experience Platform.

[Más información sobre la entrada de recorrido](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=es)

**Datos contextuales**

Aprovechar **datos contextuales** desde eventos, información de Adobe Experience Platform o datos de servicios API de terceros.

[Trabajo con fuentes de datos](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

**Acciones integradas**

Use **acciones de canal integradas** para enviar mensajes diseñados en [!DNL Journey Optimizer] por correo electrónico, push, SMS/MMS y más.

[Envío de mensajes en recorridos](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

**Acciones personalizadas**

Cree **acciones personalizadas** si usa un sistema de terceros para enviar mensajes o conectarse a API externas.

[Configurar acciones personalizadas](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/layout.svg)

**Diseñador de recorridos visuales**

Con el **diseñador de recorridos**, genere sus casos de uso de varios pasos: arrastre y suelte fácilmente un evento de entrada o una actividad de lectura de público, agregue condiciones y envíe mensajes personalizados.

[Explorar el diseñador de recorridos](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=es)

**Probar y optimizar**

Pruebe los recorridos antes de publicar, supervise su rendimiento y optimice la entrega con funciones avanzadas como la optimización del tiempo de envío.

[Recorridos de prueba y publicación](testing-the-journey.md)
:::

::::

## Casos de uso y ejemplos {#use-cases}

Desde el diseñador de recorrido, los especialistas en marketing pueden enviar mensajes 1:1 activados en tiempo real a través de cualquier canal cuando se produce un evento. Por ejemplo, cuando un cliente se suscribe a un servicio, puede [enviar un correo electrónico de bienvenida](message-to-subscribers-uc.md), alentándolo a iniciar sesión en la aplicación por primera vez y establecer sus preferencias. Acciones como completar la compra, abrir el correo electrónico e iniciar sesión en la aplicación se pueden utilizar para hacer avanzar nuevos clientes a través de sus recorridos.

El [diseñador de recorridos](using-the-journey-designer.md) proporciona [acciones de canal integradas](journeys-message.md) que admiten mensajes salientes, como correos electrónicos, notificaciones push y SMS/MMS, así como canales entrantes, incluidas aplicaciones móviles, sitios web y experiencias basadas en código creadas directamente en Journey Optimizer. También puede utilizar sistemas de terceros para enviar mensajes: Journey Optimizer incluye [acciones personalizadas](using-custom-actions.md) para permitir que estos sistemas se integren en recorridos directamente desde el diseñador de recorrido.

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

**Bienvenido/a a nuevos suscriptores**

Envíe un recorrido de bienvenida personalizado cuando los clientes se suscriban a su servicio, que les guiará por los pasos de incorporación.

[Más información](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=es)

**Optimizar tiempos de envío de correos electrónicos**

Utilice la optimización del tiempo de envío con tecnología de IA para enviar correos electrónicos cuando sea más probable que cada cliente interactúe con ella.

[Más información](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=es)

**Aumento de envíos**

Aumente gradualmente el volumen del mensaje para aumentar la reputación de su envío y evitar problemas de envío.

[Más información](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=es)

**Segmentar por día laborable**

Envíe contenido diferente en función del día de la semana en el que los clientes ingresen a su recorrido.

[Más información](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=es)

**Casos de uso de aprendizaje**

Explore casos de uso de recorrido completos que muestren implementaciones y prácticas recomendadas en el mundo real.

[Descubra todos los casos de uso](jo-use-cases.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/question.svg?lang=es)

**PREGUNTAS FRECUENTES SOBRE EL Recorrido**

Encuentre respuestas a las preguntas frecuentes acerca de la creación de recorridos, la resolución de problemas y las prácticas recomendadas.

[Ver preguntas frecuentes](journey-faq.md)
:::

::::

>[!NOTE]
>
>En [esta página](../start/guardrails.md) se detallan los mecanismos de protección y limitaciones de los recorridos

## Recursos de aprendizaje {#learning-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=es)

**Crear y administrar recorridos**

Instrucciones paso a paso sobre el diseño, la prueba, la publicación y el seguimiento de recorridos de los clientes para crear campañas omnicanal personalizadas.

[Explorar la creación de recorridos](/help/rp_landing_pages/create-journey-landing-page.md) | [Aprender a administrar el recorrido](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=es)

**actividades de Recorrido**

Descubra cómo configurar y utilizar actividades como activadores, pasos de decisión, gestión de público y mensajería personalizada en los recorridos.

[Explorar actividades](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=es)

**Expresiones y condiciones**

Domine la creación de expresiones para los flujos de trabajo dinámicos, la manipulación de datos y la orquestación avanzada de recorridos con unas herramientas y sintaxis potentes.

[Más información sobre expresiones](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=es)

**Solucionar problemas y supervisar**

Diagnostique y resuelva los problemas de ejecución de recorridos con herramientas, códigos de error y prácticas recomendadas para la depuración y optimización.

[Guía de resolución de problemas](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=es)

**descripción general del diseñador de Recorrido**

Comprenda el lienzo de recorrido, la paleta y cómo diseñar los recorridos de cliente mediante la interfaz visual.

[Conozca al diseñador](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=es)

**Probar y publicar**

Pruebe exhaustivamente los recorridos antes de publicarlos para asegurarse de que funcionan según lo esperado y ofrecen la experiencia correcta.

[Guía de pruebas](testing-the-journey.md)
:::

::::

### Tutorial de vídeo {#video}

Descubra los componentes de un recorrido y comprenda los conceptos básicos para construir un recorrido en el lienzo.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

### Recursos adicionales

* **[Referencia de códigos de error](error-codes-reference.md)**: pasos para solucionar problemas y códigos de error de recorrido
* **[Alertas](../reports/alerts.md)**: configure las alertas para la monitorización del recorrido
* **[Solución de problemas](troubleshooting.md)**: problemas y soluciones comunes de recorrido
* **[Tutoriales de Recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}**: aprenda a crear recorridos con tutoriales de vídeo prácticos

