---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer
description: Descubra las funciones clave y los casos de uso de Adobe Journey Optimizer
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: recorrido optimizer, qué es ajo, adobe recorrido optimizer, introducción, omnicanal, personalización, recorrido del cliente
exl-id: 956178c0-9985-4ff8-a29e-17dd367ce4d4
source-git-commit: 0a87a3c689d9b623a00f0a3a257e4fe34152945d
workflow-type: tm+mt
source-wordcount: '1467'
ht-degree: 23%

---

# Introducción a Journey Optimizer {#cjm-gs}

Esta página presenta Adobe Journey Optimizer: qué es, para quién sirve, sus funciones clave y cómo se adapta a la arquitectura de Adobe Experience Platform. Es el punto de partida recomendado para nuevos usuarios.

## ¿Qué es [!DNL Adobe Journey Optimizer]?{#about-cjm}

[!DNL Adobe Journey Optimizer] es una aplicación empresarial para crear y ofrecer experiencias del cliente conectadas, contextuales y personalizadas en todos los canales y puntos de contacto. Se basa de forma nativa en [!DNL Adobe Experience Platform] y aprovecha un perfil de cliente unificado en tiempo real, un marco de trabajo abierto con prioridad API, Offer Decisioning centralizado y las capacidades de IA/ML. Journey Optimizer permite a las marcas organizar campañas de marketing programadas y comunicaciones activadas por eventos en tiempo real desde una sola aplicación a escala. El resultado son experiencias de marca significativas que aumentan la lealtad del cliente y el valor de duración.

Esta guía se aplica a los profesionales de marketing, los equipos de operaciones y los administradores que utilicen Journey Optimizer por primera vez.

➡️ [Descubrimiento de Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction.html?lang=es){target="_blank"} (vídeo)


<!--
 Use [!DNL Adobe Journey Optimizer] to build multi-step customer journeys that initiate a sequence of interactions, offers, and messages across channels in real time. This approach ensures customers are engaged at the optimal moments based on their actions and relevant business signals. Learn how to build journeys in [this section](../building-journeys/journey-gs.md).

You can also create audience-based campaigns to send messages.
-->


## Casos de uso {#use-cases}

Estos ejemplos ilustran cómo las capacidades de Journey Optimizer funcionan en conjunto en diferentes funciones, industrias y canales.

| Ejemplo de uso | Función | Capacidad principal |
|----------|------|----------------|
| Recuperación retrasada del envío | Experto en marketing | [Perfil unificado + exclusión de audiencia](../audience/get-started-profiles.md) |
| Participación en tiempo real en la tienda | Experto en marketing | [Activación de geoperímetro + push](../push/get-started-push.md) |
| Recuperación de abandono del carro | Experto en marketing | [recorrido de varios pasos activado por eventos](../building-journeys/journey-gs.md) |
| Serie de bienvenida del servicio de streaming | Experto en marketing | [recorrido de bienvenida activado por eventos](../building-journeys/journey-gs.md) |
| Recordatorio de reserva con indicaciones | Experto en marketing | [Mensajería programada + según la ubicación](../campaigns/get-started-with-campaigns.md) |
| Notificación de interrupción proactiva del servicio | Operaciones | [Selección automatizada a escala](../audience/about-audiences.md) |
| Campaña promocional con tecnología de IA | Experto en marketing | [Generación de contenido de IA + experimentación](ai-features.md) |
| Alertas de mantenimiento a través de aplicaciones móviles | Operaciones | [Organización que no es de marketing](../building-journeys/journey-gs.md) |

+++**Recuperación de envío retrasada (experto en marketing)**

Una tienda de ropa suele enviar encuestas posteriores a la compra a todos los clientes que han comprado productos en la última semana. Debido a las inclemencias del tiempo, algunos envíos experimentaron retrasos. Al ver que la clientela no ha recibido sus envíos, la tienda de ropa puede excluirla del envío de satisfacción del cliente programado y, en su lugar, hacerles llegar un correo electrónico personalizado pidiendo disculpas por el retraso y ofreciéndoles un código de descuento con recomendaciones de productos basadas en las compras anteriores del cliente.

[Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

+++

+++**Participación en tiempo real en tiendas (experto en marketing)**

El mismo retailer puede atraer a un cliente fiel que entra en el aparcamiento de la tienda en tiempo real enviándole una notificación push sobre un suéter que vuelve a estar en existencias en la talla del cliente.

[Introducción a las notificaciones push](../push/get-started-push.md)

+++

+++**Recuperación de abandono del carro de compras (Especialista en marketing)**

Cuando un cliente agrega artículos a un carro de compras en línea pero sale sin completar la compra, Journey Optimizer detecta el evento en tiempo real e inicia un recorrido de recuperación automáticamente. El cliente recibe un correo electrónico personalizado que le recuerda los artículos que ha dejado. Si no pulsan en un plazo de 24 horas, se envía una notificación push de seguimiento, personalizada en función de su historial de navegación y su estado de fidelidad.

[Cree su primer recorrido](../building-journeys/journey-gs.md)

+++

+++**Serie de bienvenida de servicio de streaming (Especialista en mercadotecnia)**

Cuando un cliente se suscribe a un servicio de streaming, Journey Optimizer detecta el evento de registro e inicia inmediatamente un recorrido de bienvenida de varios pasos. El cliente recibe un correo electrónico de bienvenida que le anima a abrir la aplicación por primera vez. Si no se detecta ninguna actividad de inicio de sesión en un plazo de 48 horas, se envía una notificación push de seguimiento con recomendaciones de contenido personalizadas en función de sus intereses declarados durante la suscripción, lo que convierte a un suscriptor pasivo en un usuario activo y comprometido desde el primer día.

[Cree su primer recorrido](../building-journeys/journey-gs.md)

+++

+++**Recordatorio de reserva con indicaciones (experto en marketing)**

Una marca de hostelería envía a cada huésped un recordatorio oportuno una hora antes de su reserva. La notificación incluye el nombre del huésped, la hora de reserva y las direcciones según la ubicación al lugar de celebración, ensambladas automáticamente a partir del perfil del cliente y los datos de reserva, sin esfuerzo manual del equipo de marketing.

[Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

+++

+++**Notificación proactiva de interrupción del servicio (equipo de operaciones)**

Cuando se produce una interrupción del servicio, Journey Optimizer identifica automáticamente a los clientes afectados en función de los datos de su cuenta y los patrones de uso. Estos clientes reciben una notificación proactiva que reconoce el problema y describe los pasos siguientes: convertir una experiencia potencialmente negativa en un momento de transparencia y confianza, entregada a escala.

[Cree su primer recorrido](../building-journeys/journey-gs.md)

+++

+++**Campaña promocional con tecnología de IA (experto en marketing)**

Una marca comercial que planea el lanzamiento de un producto utiliza el asistente de IA de Journey Optimizer para generar varias variaciones de línea de asunto y copia del cuerpo en minutos, guiadas por un mensaje en lenguaje natural y sus directrices de marca cargadas. La experimentación de contenido integrada identifica automáticamente la variante con mejor rendimiento entre una muestra de audiencia inicial. El mensaje ganador se implementa a continuación en los destinatarios restantes, lo que maximiza la participación sin esfuerzo adicional de escritura.

[Explorar IA y características inteligentes](ai-features.md) | [Más información acerca de la experimentación de contenido](../content-management/experiment-accelerator-gs.md)

+++

+++**Alertas de mantenimiento a través de la aplicación móvil (equipo de operaciones)**

Quienes no son especialistas en marketing, como los equipos de operaciones y el servicio de atención al cliente, pueden usar [!DNL Adobe Journey Optimizer] para administrar las notificaciones operacionales o supervisar los procesos de incorporación. Por ejemplo, un parque de atracciones donde los visitantes descargan una aplicación móvil como parte de su experiencia: el personal de mantenimiento puede utilizar Journey Optimizer para notificar a los visitantes del parque de las atracciones que están cerradas debido al mantenimiento.

[Cree su primer recorrido](../building-journeys/journey-gs.md)

+++

## Funcionalidades clave {#key-capabilities}

[!DNL Adobe Journey Optimizer] es una aplicación ágil y escalable para crear y ofrecer experiencias del cliente personalizadas, conectadas y puntuales en cualquier aplicación, dispositivo o canal.

![Diagrama que muestra las tres áreas principales de capacidades de Journey Optimizer: Insights y participación del cliente en tiempo real, Organización y ejecución modernas omnicanal, y Decisiones inteligentes y Personalization, todo basado en Adobe Experience Platform.](assets/ajo-capabilities.png)

Las funcionalidades clave incluyen:

### Datos y participación del cliente en tiempo real

Un perfil integrado fusiona los datos activos de todas las fuentes en distintos puntos de contacto del cliente, incluidos los datos de comportamiento, transaccionales, financieros y operativos para optimizar las experiencias personales y contextuales para los clientes en su tiempo. [Más información sobre perfiles y audiencias](../audience/get-started-profiles.md)

### Organización y ejecución omnicanal modernas

Un lienzo único en el que armonizar y optimizar el recorrido del cliente para la participación del cliente y el alcance de marketing de 1:1, a fin de ayudar a las marcas a proporcionar más valor a lo largo del ciclo de vida del cliente. Los recorridos de cliente diseñados en [!DNL Adobe Journey Optimizer] pueden ser dinámicos y estar basados en eventos para ayudar a las marcas a reaccionar a las señales en tiempo real, así como a conectar esas interacciones con campañas programadas, de modo que se puedan tomar las decisiones correctas acerca de qué comunicaciones enviar a un cliente, cuándo y a través de qué canales. Las herramientas de creación de contenido incrustado (incluido un diseñador visual de arrastrar y soltar, plantillas reutilizables, fragmentos de contenido y un editor de personalización) permiten a los equipos crear, personalizar y administrar mensajes para cada canal directamente dentro del mismo flujo de trabajo. [Crea tu primer recorrido](../building-journeys/journey-gs.md) | [Diseña tu contenido](../../rp_landing_pages/content-management-landing-page.md)

### Decisiones inteligentes y Personalization

Las marcas pueden aplicar decisiones centralizadas e incorporar inteligencia artificial y aprendizaje automático para configurar perspectivas predictivas a través de la experiencia del cliente, lo que facilita la automatización de decisiones y la optimización de la experiencia a escala. Decisioning alimenta las ofertas centralizadas entre canales a escala mediante [!DNL Adobe Journey Optimizer]. [Explorar Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) | [Descubra las características de IA](ai-features.md)


## Disponibilidad y licencias {#availability}

Esta documentación cubre la versión actual de Journey Optimizer y se aplica a los usuarios de B2C y B2B edition a menos que se indique lo contrario. Los componentes y las funciones disponibles en su entorno dependen de los [permisos](../administration/permissions.md) y del [paquete de licencias](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Para cualquier pregunta, póngase en contacto con Adobe Customer Success Manager o su representante de Adobe.

Los procedimientos y directrices generales de privacidad de Adobe Experience Cloud se aplican a [!DNL Journey Optimizer]. [Obtenga más información sobre la privacidad de Adobe Experience Cloud](https://www.adobe.com/es/privacy/experience-cloud.html){target="_blank"}.


## Arquitectura {#architecture}

Comprenda la arquitectura básica de [!DNL Adobe Journey Optimizer], los puntos de integración y la relación entre [!DNL Journey Optimizer] y [!DNL Experience Platform] en el diagrama siguiente.

Adobe Experience Platform es una base de datos potente, flexible, abierta y centralizada que recopila, estandariza, controla, aplica conocimientos de la IA  y unifica datos para ofrecer experiencias digitales fundamentadas y relevantes a los clientes.

![Diagrama que muestra Adobe Experience Platform como la capa de datos base, con cuatro aplicaciones creadas de forma nativa en la parte superior: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics y Adobe Mix Modeler. Los servicios compartidos, como el perfil del cliente en tiempo real, el control de datos y la resolución de identidades, son la base de las cuatro aplicaciones.](assets/ajo-aep-architecture-diagram.png){width="70%" zoomable="yes"}

Hay cuatro aplicaciones integradas de forma nativa en Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics y Adobe Mix Modeler.

La funcionalidad y los servicios principales de Journey Optimizer funcionan con los componentes básicos de Adobe Experience Platform, que incluyen el perfil del cliente en tiempo real. Aunque Journey Optimizer funciona sin problemas y es interoperable con Real-Time CDP y Customer Journey Analytics, también puede funcionar de forma independiente como aplicación independiente.

![Diagrama que muestra la arquitectura interna de Journey Optimizer y sus puntos de integración con los servicios de Adobe Experience Platform, incluida la ingesta de datos, el perfil del cliente en tiempo real, el motor de decisiones y la entrega de canales salientes a través de correo electrónico, push, SMS y web.](assets/ajo-architecture-diagram.png){width="70%" zoomable="yes"}


### Modelos de Adobe Journey Optimizer

Los modelos de experiencia digital proporcionan diagramas de la arquitectura del flujo de datos y del sistema para comprender mejor cómo se integran e implementan las aplicaciones de Adobe Experience Platform. Los modelos proporcionan una representación visual de los flujos de contenido y datos entre sistemas y componentes, la secuencia de operaciones y las dependencias para ayudar a informar el diseño de casos de uso y la arquitectura de Adobe Experience Platform y aplicaciones.

Vea los [modelos de Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.


>[!MORELIKETHIS]
>
>* [Pasos clave para el inicio](quick-start.md): guías de inicio rápido basadas en roles para administradores, especialistas en marketing e ingenieros de datos.
>* [Introducción a la administración de datos](../data/gs-data.md): Descubra cómo se incorporan, unifican y activan los datos en Journey Optimizer.
>* [Diseñar recorridos y enviar mensajes](../building-journeys/journey-gs.md): cree su primer recorrido de cliente y configure las acciones del canal.
>* [Informes en vivo](../reports/live-report.md) — Monitorice el rendimiento de la campaña y del recorrido en tiempo real.
>* [Tutorial de introducción a Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"}: un tutorial en vídeo guiado de conceptos básicos de Journey Optimizer.
>* [Información general sobre la seguridad de Journey Optimizer](https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf) (PDF): arquitectura de seguridad, protección de datos y detalles de conformidad.
>* [Descripción del producto Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} — Términos de licencia oficiales y desglose de funciones de edición.
