---
solution: Journey Optimizer
product: journey optimizer
title: 'Journey Orchestration: guía completa'
description: Guía completa para empezar a utilizar la orquestación de recorrido en  [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
keywords: recorrido, orquestación, introducción, incorporación, funciones
exl-id: 96b1d619-986d-493d-a73b-d7c63b92cca8
TQID: https://experienceleague.adobe.com/Ht6fS6uanOs-rXoT4bAnK6eGvm9kOmH-N5B-y8KU6Rc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: b9d00d1b-a371-4a75-a52a-3f8ea2029020
  - id: ba62ad25-65cb-4ea9-b7aa-0fa87c4a9fa0
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: da923278-9c80-47b0-bebd-b68c341e76fb
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
source-git-commit: 0201927f8d9260e8ba1d0db7014d6a7b30d09062
workflow-type: tm+mt
source-wordcount: 943
ht-degree: 49%

---

# orquestación de recorrido: guía completa{#journey-orchestration-guide}

Los recorridos de [!DNL Adobe Journey Optimizer] le permiten crear recorridos personalizados de clientes de varios pasos que se adaptan en tiempo real al comportamiento y las necesidades de su audiencia. Con un lienzo intuitivo de tipo arrastrar y soltar, puede orquestar mensajes y acciones en varios canales, aprovechando los datos contextuales y la segmentación del público para lograr el máximo impacto.

Tanto si explora déclencheur en tiempo real como si administra propiedades de recorrido o utiliza herramientas avanzadas como acciones y expresiones personalizadas, esta guía proporciona una hoja de ruta clara para diseñar y refinar recorridos con seguridad que proporcionen experiencias de cliente significativas y oportunas.

## ¿Qué son los recorridos?

Utilice [!DNL Journey Optimizer] para crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos. Diseñe escenarios avanzados de varios pasos que respondan al comportamiento de los clientes y a los eventos empresariales en tiempo real.

El diseñador de recorridos de Journey Optimizer proporciona todo lo que los especialistas en marketing y en recorrido necesitan para orquestar recorridos 1:1 de varios pasos en todos los canales. Esto incluye un lienzo intuitivo de arrastrar y soltar para organizar cada paso del recorrido, definir el público destinatario e incluir los mensajes, ofertas y contenido en todos los canales que verán los miembros del público destinatario en función del comportamiento, los datos contextuales y los eventos empresariales.

![Interfaz del diseñador de recorrido con panel de paleta, lienzo y propiedades](assets/journey38.png)

**¿Listo para empezar a crear?** Aprenda a crear y diseñar su primer recorrido en [esta página](journey-gs.md).


## Funcionalidades clave {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=es)

**Envío en tiempo real y por lotes**

Enviar en tiempo real **envío unitario** se activó cuando se recibió un evento, o **en lote** con [!DNL Adobe Experience Platform] audiencias.

[Más información sobre la entrada de recorrido](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=es)

**Datos contextuales**

Aprovechar **datos contextuales** de eventos, información de [!DNL Adobe Experience Platform] o datos de servicios API de terceros.

[Trabajo con paquetes de datos](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

**Acciones integradas**

Use **acciones de canal integradas** para enviar mensajes diseñados en [!DNL Journey Optimizer] por correo electrónico, push, SMS/RCS/MMS y más.

[Envío de mensajes en recorridos](journey-action.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

**Acciones personalizadas**

Cree **acciones personalizadas** si usa un sistema de terceros para enviar mensajes o conectarse a API externas.

[Configurar acciones personalizadas](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=es)

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

El [diseñador de recorridos](using-the-journey-designer.md) proporciona [acciones de canal integradas](journey-action.md) que admiten mensajes salientes, como correos electrónicos, notificaciones push y SMS/RCS/MMS, así como canales entrantes, incluidas aplicaciones móviles, sitios web y experiencias basadas en código creadas directamente en Journey Optimizer. También puede utilizar sistemas de terceros para enviar mensajes: Journey Optimizer incluye [acciones personalizadas](using-custom-actions.md) para permitir que estos sistemas se integren en recorridos directamente desde el diseñador de recorrido.


:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=es)

**Casos de uso de aprendizaje**

Explore casos de uso de recorrido completos que muestren implementaciones y prácticas recomendadas en el mundo real.

[Descubra todos los casos de uso](jo-use-cases.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

**Dé la bienvenida a nuevos suscriptores**

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

Aumente gradualmente el volumen del mensaje para aumentar la reputación de su envío y evitar problemas de entregabilidad.

[Más información](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=es)

**Segmente por día laborable**

Envíe contenido diferente en función del día de la semana en el que los clientes ingresen a su recorrido.

[Más información](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/question.svg?lang=es)

**PREGUNTAS FRECUENTES SOBRE EL Recorrido**

Encuentre respuestas a las preguntas frecuentes acerca de la creación de recorridos, la resolución de problemas y las prácticas recomendadas.

[Ver preguntas frecuentes](journey-faq.md)
:::

::::



## Recursos de aprendizaje {#learning-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=es)

**Crear y administrar recorridos**

Instrucciones paso a paso sobre el diseño, la prueba, la publicación y el seguimiento de recorridos de los clientes para crear campañas omnicanal personalizadas.

[Explorar la creación de recorridos](../../rp_landing_pages/create-journey-landing-page.md) | [Administración de recorrido de aprendizaje](../../rp_landing_pages/manage-journey-landing-page.md) | [Pasos del flujo de trabajo de Recorrido](journey.md#workflow)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=es)

**actividades de Recorrido**

Descubra cómo configurar y utilizar actividades como activadores, pasos de decisión, gestión de público y mensajería personalizada en los recorridos.

[Explorar actividades](../../rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=es)

**Expresiones y condiciones**

Domine la creación de expresiones para los flujos de trabajo dinámicos, la manipulación de datos y la orquestación avanzada de recorridos con unas herramientas y sintaxis potentes.

[Más información sobre expresiones](../../rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=es)

**Solucionar problemas y supervisar**

Diagnostique y resuelva los problemas de ejecución de recorridos con herramientas, códigos de error y prácticas recomendadas para la depuración y optimización.

[Guía de resolución de problemas](../../rp_landing_pages/troubleshoot-journey-landing-page.md)
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

>[!VIDEO](https://video.tv.adobe.com/v/3430353?captions=spa&quality=12)

### Recursos adicionales

* **[Referencia de códigos de error](error-codes-reference.md)**: pasos para solucionar problemas y códigos de error de recorrido
* **[Alertas](../reports/alerts.md)**: configure las alertas para la monitorización del recorrido
* **[Solución de problemas](troubleshooting.md)**: problemas y soluciones comunes de recorrido
* **[Tutoriales de Recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}**: aprenda a crear recorridos con tutoriales de vídeo prácticos
* **[limitaciones y protecciones de Recorrido](../start/guardrails.md)**: compruebe las limitaciones y protecciones al usar [!DNL Adobe Journey Optimizer]
