---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los recorridos
description: Introducción a los recorridos
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: recorrido, descubrimiento, introducción
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 34%

---


# Introducción a los recorridos{#jo-general-principle}

Los recorridos de Adobe Journey Optimizer le permiten crear recorridos para el cliente personalizados que constan de varios pasos y que se adaptan en tiempo real al comportamiento y las necesidades de su público. Con un lienzo intuitivo de tipo arrastrar y soltar, puede orquestar mensajes y acciones en varios canales, aprovechando los datos contextuales y la segmentación del público para lograr el máximo impacto. Tanto si explora déclencheur en tiempo real como si administra propiedades de recorrido o utiliza herramientas avanzadas como acciones y expresiones personalizadas, esta sección proporciona una hoja de ruta clara que le ayudará a diseñar y refinar recorridos que proporcionen experiencias de cliente significativas y oportunas.

Utilice [!DNL Journey Optimizer] para crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos. Puede diseñar escenarios avanzados de varios pasos con las siguientes funcionalidades:

* Enviar **envío unitario** en tiempo real se activó cuando se recibió un [evento](general-events.md), o **en lote** con las [audiencias](read-audience.md) de Adobe Experience Platform.

* Aproveche **datos contextuales** de [eventos](../event/about-events.md), información de Adobe Experience Platform o datos de servicios API de terceros a través de [fuentes de datos](../datasource/about-data-sources.md).

* Utilice las **[acciones integradas](journeys-message.md)** para enviar los mensajes diseñados en [!DNL Journey Optimizer] o cree **[acciones personalizadas](using-custom-actions.md)** si utiliza un sistema de terceros para enviar sus mensajes.

* Con el **[diseñador de recorridos](using-the-journey-designer.md)**, cree sus casos de uso de varios pasos: arrastre y suelte fácilmente un evento de entrada o una [actividad de lectura de audiencias](read-audience.md), agregue [condiciones](condition-activity.md) y envíe mensajes personalizados.

➡️ [Descubrimiento de Journey Optimizer en vídeo](#video)

## Información general sobre los recorridos

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=es)

Introducción a la creación de Recorridos

Instrucciones paso a paso sobre el diseño, la prueba, la publicación y el seguimiento de recorridos de los clientes para crear campañas omnicanal personalizadas.

[Creación de su primer recorrido](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=es)

Journey Orchestration: Guía completa

Documentación completa que cubre todos los aspectos de la creación, administración y optimización de recorridos en Adobe Journey Optimizer.

[Explorar la guía completa](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

Administración de Recorridos

Administre los recorridos del cliente de forma eficaz con herramientas de filtrado, administración de perfiles, zonas horarias y técnicas de optimización.

[Más información sobre la administración de recorridos](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=es)

Actividades de recorrido

Descubra cómo configurar y utilizar actividades como activadores, pasos de decisión, gestión de público y mensajería personalizada en los recorridos.

[Explorar actividades](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=es)

Creación de expresiones

Domine la creación de expresiones para los flujos de trabajo dinámicos, la manipulación de datos y la orquestación avanzada de recorridos con unas herramientas y sintaxis potentes.

[Más información sobre expresiones](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=es)

Casos de uso de recorrido

Explore las aplicaciones reales de Adobe Journey Optimizer, incluida la mensajería multicanal y la integración con sistemas externos.

[Descubrir casos de uso](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## ¿Qué puedes hacer con los recorridos?

Desde el diseñador de recorrido, los especialistas en marketing pueden enviar mensajes 1:1 activados en tiempo real a través de cualquier canal cuando se produce un evento. Por ejemplo, cuando un cliente se suscribe a un servicio, puede [enviar un correo electrónico de bienvenida](message-to-subscribers-uc.md), alentándolo a iniciar sesión en la aplicación por primera vez y establecer sus preferencias. Acciones como completar la compra, abrir el correo electrónico e iniciar sesión en la aplicación se pueden utilizar para hacer avanzar nuevos clientes a través de sus recorridos.

## tipos de recorrido

Adobe Journey Optimizer admite cuatro tipos de recorrido, cada uno diseñado para diferentes casos de uso y mecanismos de entrada. Elija el tipo adecuado en función de cómo desee que los perfiles especifiquen y avancen en las experiencias de los clientes.

>[!BEGINTABS]

>[!TAB recorridos unitarios]

**Los recorridos unitarios** se activan individualmente mediante un evento cuando se produce una acción específica, como una compra, el inicio de sesión en la aplicación o el envío de formularios. Los perfiles entran en el recorrido de uno en uno en tiempo real cuando se recibe el evento, lo que lo hace ideal para experiencias personalizadas y basadas en el comportamiento.

**Características clave:**

* Entrada en tiempo real impulsada por eventos
* Procesamiento de perfiles individuales
* Ideal para mensajes transaccionales y respuestas inmediatas
* Admite datos contextuales desde el evento de activación

**Casos de uso:**

* Confirmación del pedido después de la compra
* Correo electrónico de bienvenida cuando alguien se suscriba
* Abandono del carro de compras activado por el comportamiento de navegación
* Notificaciones de restablecimiento de contraseña

➡️ [Más información acerca de la configuración del evento](../event/about-events.md) | [Eventos generales](general-events.md) | [Mensaje para el caso de uso de los suscriptores](message-to-subscribers-uc.md)

>[!TAB Leer recorridos de audiencia]

**Leer recorridos de audiencia** comienza con una audiencia de Adobe Experience Platform y envía mensajes en lote a todos los perfiles de esa audiencia. Este tipo de recorrido procesa toda la audiencia a la vez, lo que lo hace ideal para campañas programadas y comunicaciones recurrentes.

**Características clave:**

* Procesamiento por lotes de segmentos de audiencia
* Ejecución programada para una sola vez
* Todos los perfiles entran simultáneamente
* Admite comunicaciones a gran escala

**Casos de uso:**

* Boletines mensuales
* Campañas promocionales para segmentos de destinatario
* Anuncios de productos para todos los clientes
* Campañas de marketing de temporada

➡️ [Más información acerca de la actividad Leer audiencia](read-audience.md) | [Introducción a las audiencias](../audience/about-audiences.md) | [Caso de uso de mensajería multicanal](journeys-uc.md)

>[!TAB recorridos de calificación de audiencia]

**Los recorridos de calificación de audiencia** se activan cuando los perfiles cumplen los requisitos para un segmento de audiencia específico o salen de él. Los perfiles introducen el recorrido de forma individual, ya que cumplen los criterios de audiencia en tiempo real, lo que permite una participación inmediata cuando cambia el comportamiento de los clientes.

**Características clave:**

* Entrada basada en cualificaciones en tiempo real
* Monitorización continua del abono a audiencias
* Procesamiento de perfiles individuales según cumplen los requisitos
* Óptima con audiencias de streaming

**Casos de uso:**

* Notificaciones de actualización de nivel VIP
* Nueva participación cuando los clientes se vuelvan inactivos
* Mensajes de celebración de la primera compra
* Segmentación geográfica cuando los clientes se mueven

➡️ [Más información acerca de la calificación de audiencias](audience-qualification-events.md) | [Actividad de condición](condition-activity.md) | [Creando definiciones de segmento](../audience/creating-a-segment-definition.md)

>[!TAB recorridos de eventos empresariales]

Los **recorridos de eventos empresariales** se desencadenan por eventos empresariales (como actualizaciones de existencias, avisos meteorológicos o cambios de precios) que afectan a varios perfiles simultáneamente. En lugar de reaccionar ante las acciones individuales de los clientes, estos recorridos responden a condiciones comerciales más amplias o a factores externos.

**Características clave:**

* Se activa mediante eventos de nivel empresarial, no acciones individuales
* Afecta a varios perfiles a la vez
* Se dirige a una audiencia específica cuando se produce el evento
* Combina temporización impulsada por evento con segmentación de audiencia

**Casos de uso:**

* Alertas de inventario bajas para clientes interesados
* Anuncios de venta Flash
* Promociones basadas en el tiempo
* Notificaciones de bajada de precios
* Alertas de productos que vuelven a estar en stock

➡️ [Más información acerca de los eventos empresariales](general-events.md) | [Configurar eventos empresariales](../event/about-creating-business.md) | [Administración de entradas](entry-management.md)

>[!ENDTABS]

## Recorrido Designer{#journey-designer}

El [diseñador de recorridos](using-the-journey-designer.md) proporciona todo lo que los especialistas en marketing y los profesionales del recorrido necesitan para organizar recorridos de 1:1 en varios pasos en todos los canales. Esto incluye un lienzo intuitivo de arrastrar y soltar para organizar cada paso del recorrido, definir el público destinatario e incluir los mensajes, ofertas y contenido en todos los canales que verán los miembros del público destinatario en función del comportamiento, los datos contextuales y los eventos empresariales.

El diseñador de recorridos proporciona todo lo necesario para diseñar experiencias de varios pasos:

* **[Acciones de canal integradas](journeys-message.md)**: envía mensajes por correo electrónico, notificaciones push, SMS/MMS, en la aplicación, web, experiencias basadas en código y mucho más, todos diseñados directamente en Journey Optimizer
* **[Acciones personalizadas](using-custom-actions.md)**: integre sistemas de terceros para enviar mensajes o flujos de trabajo de déclencheur en plataformas externas
* **[Actividades de orquestación](about-journey-activities.md)**: agregue lógica, condiciones, tiempos de espera y segmentación de audiencia para crear experiencias de cliente sofisticadas
* **[Condiciones](condition-activity.md)**: ramifique el recorrido en función de atributos de perfil, pertenencia a audiencias o eventos en tiempo real
* **[Expresiones](expression/expressionadvanced.md)**: cree lógica y personalización avanzadas con el editor de expresiones

Aprenda a utilizar el diseñador de recorrido [&#x200B; en estos casos de uso de extremo a extremo](jo-use-cases.md).

>[!NOTE]
>
>En [esta página](../start/guardrails.md) se detallan los mecanismos de protección y limitaciones de los recorridos

## Vídeo práctico {#video}

Descubra los componentes de un recorrido y comprenda los conceptos básicos para construir un recorrido en el lienzo.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

## Recursos adicionales {#additional-resources}

* **[Solución de problemas con los Recorridos del cliente](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnostique y resuelva los problemas de ejecución de recorridos con herramientas, códigos de error y prácticas recomendadas para la depuración y optimización
* **[Preguntas frecuentes sobre el recorrido](journey-faq.md)**: preguntas frecuentes sobre recorridos
* **[Alertas de Recorrido](../reports/alerts.md)**: configure alertas para supervisar el recorrido y suscríbase a notificaciones para recibir actualizaciones en tiempo real
* **[Referencia de códigos de error](error-codes-reference.md)**: pasos para solucionar problemas y códigos de error de recorrido
* **[Solución de problemas](troubleshooting.md)**: problemas y soluciones comunes de recorrido
* **[Tutoriales de Recorrido (vídeos)](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}**: aprenda a crear recorridos con tutoriales de vídeo prácticos que cubren características, funcionalidades y prácticas recomendadas
