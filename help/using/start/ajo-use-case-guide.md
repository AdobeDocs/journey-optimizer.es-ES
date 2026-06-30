---
solution: Journey Optimizer
product: journey optimizer
title: Empiece desde su meta | ADOBE JOURNEY OPTIMIZER
description: Descubra los casos de uso principales para los que está diseñado Adobe Journey Optimizer, con instrucciones sobre las funciones de AJO que se adaptan mejor a cada escenario.
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: optimizador de recorrido, caso de uso, guía de decisión, qué capacidad, introducción, objetivos del profesional, tutoriales
source-git-commit: bcf3f322bad0602d0cc2cffc41229eacdcfe93e1
workflow-type: tm+mt
source-wordcount: '3224'
ht-degree: 30%

---

# Empiece desde su meta {#ajo-use-case-guide}

>[!BEGINSHADEBOX]

**En esta página:** Empiece a partir de lo que desea lograr y, a continuación, vaya a la funcionalidad de Adobe Journey Optimizer que lo resuelve, sin necesidad de conocer primero el nombre de la característica.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] ofrece muchas capacidades, y la correcta depende de lo que esté tratando de lograr. Esta guía está organizada en torno a los objetivos comerciales en lugar de las funciones del producto: busque el objetivo que coincida con sus necesidades y, a continuación, siga el vínculo para comenzar con la capacidad recomendada.

Utilice esta página como un enrutador rápido: busque su objetivo y salte directamente a la capacidad correcta. Si acaba de empezar, empiece con [Empiece con Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) para encontrar el punto de entrada correcto para su función.

>[!NOTE]
>
>Para obtener ejemplos de implementación paso a paso, consulte la [biblioteca de casos de uso de Recorrido](../building-journeys/jo-use-cases.md).

Cuando un tutorial completo no está disponible para un escenario específico, el vínculo le lleva al mejor punto de partida actual para aprender la capacidad y comenzar.

La IA está integrada en muchas de estas capacidades. Busque la etiqueta **(AI)** en las tablas siguientes. El asistente conversacional [AI Assistant](ai-features.md#ai-assistant) también puede responder preguntas sobre productos y obtener información operacional sobre tus recorridos en cualquier momento. Para ver el conjunto completo de características inteligentes, consulte [IA y características inteligentes](ai-features.md).

>[!TIP]
>
>¿Es nuevo en Journey Optimizer? Empiece por [Empiece con Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) para elegir la ruta correcta para su rol y, a continuación, lea [Qué es Journey Optimizer](get-started.md) para lo esencial. Para generar confianza práctica, examine los [tutoriales de Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}, siga una [lista de reproducción de vídeo](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"} seleccionada por expertos y practique en una [zona protegida de formación](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} o con los [desafíos prácticos](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}.

## Configuración de Journey Optimizer para su equipo {#setup-admin}

Para administradores y usuarios técnicos que necesitan configurar el entorno antes de crear recorridos o campañas.

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Configure el correo electrónico, los SMS o los canales push antes de enviar | Configuración de canal | [Introducción a la configuración del canal](../configuration/get-started-configuration.md) |
| Calentar una nueva dirección IP para el envío de correo electrónico | plan de calentamiento de IP | [Introducción al calentamiento de IP](../configuration/ip-warmup-gs.md) |
| Configuración de funciones, permisos y control de acceso | Control de acceso | [Introducción al control de acceso](../administration/permissions-overview.md) |
| Trabaje en varios entornos o regiones | Zonas protegidas | [Trabajo con zonas protegidas](../administration/sandboxes.md) |

## Captar clientes a medida que ocurren eventos {#engage-real-time}

Para escenarios en los que reacciona ante una acción o un evento del cliente mientras sucede.

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Dar la bienvenida a un nuevo cliente o suscriptor automáticamente | Recorrido activado por evento | [Introducción a recorrido](../building-journeys/journey-gs.md) · [Introducción a la creación de un recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de compilar:**, asegúrese de que tiene (1) un [evento de entrada de recorrido configurado](../event/about-events.md) para capturar el déclencheur de registro, (2) una [superficie de canal push o de correo electrónico](../configuration/channel-surfaces.md) configurada para su zona protegida y (3) al menos un [perfil de prueba](../audience/creating-test-profiles.md) disponible para validar la recorrido antes de publicar.

>[!ENDSHADEBOX]

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Recuperar un carro de compras o una sesión de navegación abandonados | Recorrido activado por evento | [Introducción a recorrido](../building-journeys/journey-gs.md) · [Tutorial de exploración abandonado](https://experienceleague.adobe.com/es/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de compilar:** necesita (1) un [evento de comportamiento](../event/about-events.md) que capture la acción de examinar o del carro de compras desde su SDK web o móvil, (2) una [actividad de espera](../building-journeys/wait-activity.md) que se decida por estrategia (normalmente de 1 a 4 horas antes del primer empujón) y (3) una superficie de canal lista para el mensaje de seguimiento. Nota: El recorrido debe incluir una condición para salir de los perfiles que completan la compra antes de que finalice el período de espera.

>[!ENDSHADEBOX]

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Déclencheur de un recorrido desde un envío de formulario de sitio web | Recorrido activado por evento | [Introducción a recorrido](../building-journeys/journey-gs.md) · [Tutorial](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/trigger-journey-on-form-submission/introduction){target="_blank"} |
| Reacción al comportamiento en la aplicación (aplicación abierta, vista de pantalla) | Recorrido + En la aplicación | [Introducción a la aplicación](../in-app/get-started-in-app.md) |
| Enviar confirmaciones de pedidos, envíos o citas | Campaña activada por API | [Trabajar con campañas activadas por API](../campaigns/api-triggered-campaigns.md) |
| Volver a atraer clientes inactivos o caducados | Recorridos + audiencias | [Introducción a perfiles y audiencias](../audience/get-started-profiles.md) · [Crear audiencias con el generador de reglas](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/profiles-audiences-subscriptions/create-audiences-using-the-rule-builder){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de compilar:** necesita (1) una audiencia [definida en Adobe Experience Platform](../audience/about-audiences.md) que identifique perfiles inactivos (por ejemplo, sin compras ni inicios de sesión en 60 días), (2) una decisión sobre el canal de reparticipación (correo electrónico, push o SMS) y (3) una regla de supresión o [límite de frecuencia](../conflict-prioritization/channel-capping.md) para evitar contactar con perfiles enviados recientemente. Use una entrada de recorrido **Leer audiencia**, no un evento, para este escenario.

>[!ENDSHADEBOX]

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Prueba de un recorrido con datos reales antes de activarlo | Recorrido seco | [Probar el recorrido con simulación](../building-journeys/journey-dry-run.md) |
| Pausar un recorrido en directo para hacer ediciones sin detener los perfiles en vuelo | Recorrido pausar y reanudar | [Pausar y reanudar un recorrido](../building-journeys/journey-pause.md) |
| Crear u optimizar un recorrido desde un indicador en lenguaje natural | Journey Agent **(IA)** | [agentes de IA](ai-features.md#ai-agents) · [tutorial de Journey Agent](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} |

## Alcanzar audiencias a escala {#reach-at-scale}

Para una difusión programada, de uno a varios, a una audiencia definida.

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Enviar una newsletter o promoción a un segmento | Campaña programada | [Comience con las campañas](../campaigns/get-started-with-campaigns.md) |

>[!BEGINSHADEBOX]

**Antes de compilar:** necesita (1) un [segmento de audiencia publicado](../audience/about-audiences.md) en Adobe Experience Platform, (2) una [superficie de canal de correo electrónico](../configuration/channel-surfaces.md) con un dominio de envío verificado y (3) cualquier [fragmento o plantilla de contenido](../content-management/fragments.md) que planee reutilizar ya publicado. Las campañas programadas son la opción correcta aquí, no los recorridos, si se trata de un envío único o recurrente sin lógica de ramificación.

>[!ENDSHADEBOX]

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Lanzamiento de un producto con una prueba A/B | Experimentación de contenido **(IA)** | [Empiece a experimentar con el contenido](../content-management/experiment-accelerator-gs.md) · [Cree experimentos de contenido para campañas de correo electrónico](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} |
| Notificar a los clientes de una interrupción o actualización del servicio | Campaña programada + audiencias | [Acerca de las audiencias](../audience/about-audiences.md) |
| Diseño de una campaña de varios pasos con lógica de ramificación | Campañas orquestadas | [Introducción a las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md) |
| Segmentar solo los perfiles que hayan cambiado desde la última ejecución de mi campaña | Campañas organizadas: consulta incremental | [Generar consultas en campañas orquestadas](../orchestrated/build-query.md) <!-- TODO: verify target — no dedicated "incremental query" page found; build-query.md ("Build your first rule") is the closest existing page --> |
| Compruebe cuántos perfiles coinciden con mi audiencia antes de iniciar | Previsualización de audiencia | [Acerca de las audiencias](../audience/about-audiences.md) <!-- TODO: verify target — no "create-compositions.md#preview" page/anchor exists; about-audiences.md used as placeholder --> |
| Coordinar la mensajería en muchos canales a escala | Orquestación | [Introducción a las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md) · [Escalar la orquestación a la participación omnicanal](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/scaling-orchestration-to-omnichannel-engagement/introduction){target="_blank"} |
| Envíe cada mensaje en el mejor momento para cada cliente | Optimización del tiempo de envío **(IA)** | [Optimización del tiempo de envío](../building-journeys/send-time-optimization.md) |

## Personalice lo que ve cada cliente {#personalize}

Para adaptar las ofertas y el contenido a cada individuo.

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Mostrar la mejor oferta para cada cliente | Toma de decisiones | [Introducción a Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) · Tutorial de [ofertas web](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de generar:** la toma de decisiones requiere una secuencia de configuración específica. Necesita (1) [elementos de decisión (ofertas) creados](../experience-decisioning/items.md) con reglas y atributos de elegibilidad, (2) una [estrategia de selección](../experience-decisioning/selection-strategies.md) o fórmula de clasificación configurada y (3) una [política de decisión](../experience-decisioning/create-decision.md) adjunta a la superficie donde aparecerán las ofertas. Omitir esta secuencia es la razón más común por la que las configuraciones de toma de decisiones por primera vez no devuelven resultados.

>[!ENDSHADEBOX]

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Clasificar ofertas mediante una fórmula (código postal, ingresos, tiempo) | Decisioning — fórmula de clasificación | [Fórmulas de clasificación](../experience-decisioning/ranking/ranking-formulas.md) · [Tutorial de fórmula de clasificación](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/personalizing-offers-with-ranking-formulas-based-on-user-zip-code-and-income/introduction){target="_blank"} · [Tutorial de datos meteorológicos](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction){target="_blank"} |
| Usar datos de productos externos o CRM para personalizar ofertas | Decisioning: búsqueda de conjuntos de datos de AEP | [Usar la búsqueda de conjuntos de datos en la toma de decisiones](../experience-decisioning/context-data.md) |
| Personalización del contenido del mensaje con datos de perfil | Personalización | [Personaliza tu contenido](../personalization/personalize.md) |
| Generar variaciones de copias, imágenes y mensajes | Generación de contenido de IA **(IA)** | [Generación de contenido de IA](../content-management/gs-generative.md) · [Tutorial](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} |
| Conversión de una imagen de diseño en una plantilla de correo electrónico editable | Convertidor de imagen a HTML **(AI)** | [Convertir una imagen en una plantilla de correo electrónico](../content-management/image-to-html.md) |
| Clasificar y personalizar ofertas automáticamente | Modelos de clasificación de IA **(AI)** | [modelos de IA para la toma de decisiones](../experience-decisioning/ranking/ai-models.md) |
| Entrega de contenido contextual siempre activo (sin campaña) | Tarjetas de contenido | [Introducción a las tarjetas de contenido](../content-card/get-started-content-card.md) · [Crear tarjetas de contenido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/channels/content-cards/create-content-cards){target="_blank"} |
| Entrega de contenido personalizado mediante API a cualquier aplicación o superficie | Experiencia basada en código | [Introducción a la experiencia basada en código](../code-based/get-started-code-based.md) |
| Controlar qué partes de una plantilla de correo electrónico puede editar mi equipo | Bloqueo de contenido | [Bloquear contenido en plantillas de correo electrónico](../content-management/content-locking.md) |

## Coordinación y administración de la entrega {#coordinate-govern}

Para controlar cómo, cuándo y con qué frecuencia se contacta a los clientes entre canales.

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Evitar la fatiga de mensajes entre canales | Restricción de frecuencia | [Establecer límite de frecuencia por canal](../conflict-prioritization/channel-capping.md) |
| Resolución de mensajes conflictivos o en competencia | Priorización de conflictos | [Identificar posibles conflictos](../conflict-prioritization/conflicts.md) · [Tutorial](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"} |
| Decidir qué recorrido tiene prioridad | Arbitraje del recorrido | [Usar fórmulas para clasificar recorridos](../conflict-prioritization/journey-ranking-formulas.md) |
| Respetar las horas de silencio y el consentimiento | Horas de silencio / Privacidad | [Establecer horas tranquilas](../conflict-prioritization/quiet-hours.md) |
| Aplicar políticas de consentimiento y etiquetas de uso de datos en todos los canales | Consentimiento y control de datos | [Introducción a la privacidad](../privacy/get-started-privacy.md) |
| Reciba alertas cuando un recorrido tenga altas tasas de error o descarte | alertas de recorrido | [Configurar alertas de recorrido](../reports/alerts.md) |

## Elija un canal en el que realizar el envío {#choose-channel}

| Quiero enviar a... | Canal | Empiece aquí |
| --- | --- | --- |
| Enviar boletines de correo electrónico, promociones o mensajes transaccionales | Correo electrónico | [Introducción al correo electrónico](../email/get-started-email.md) |
| Notificaciones push móviles (iOS y Android) | Push | [Introducción a las notificaciones push](../push/get-started-push.md) |
| Mensajes de texto SMS, MMS o RCS | SMS/MMS/RCS | [Introducción a SMS/MMS/RCS](../mobile/get-started-mobile.md) · [Centro de aprendizaje móvil](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/mobile-learning-hub/overview){target="_blank"} |
| Mensajes de WhatsApp a través de la API de Meta Cloud | WhatsApp | [Introducción a WhatsApp](../whatsapp/get-started-whatsapp.md) |
| Superposiciones y titulares en el explorador o en la aplicación | in-app | [Introducción a la aplicación](../in-app/get-started-in-app.md) |
| Contenido de página web personalizado | Web | [Introducción al canal web](../web/get-started-web.md) |
| Cualquier superficie a través de API (quiosco, dispositivo conectado, aplicación sin encabezado) | Experiencia basada en código | [Introducción a la experiencia basada en código](../code-based/get-started-code-based.md) |
| Fragmentos de correo físicos activados a partir de un recorrido | Correo directo | [Introducción al correo postal](../direct-mail/get-started-direct-mail.md) |

## Medir y optimizar {#measure-optimize}

Para realizar el seguimiento del rendimiento, diagnosticar problemas y mejorar los resultados a lo largo del tiempo.

| Quiero... | Capacidad recomendada | Empiece aquí |
| --- | --- | --- |
| Consulte las métricas de rendimiento de un recorrido o una campaña en directo | Informes en vivo | [Informes en vivo](../reports/live-report.md) · [Supervise y analice su recorrido con informes en vivo](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} |
| Informar sobre el rendimiento total de la campaña o del recorrido una vez finalizado | Informes globales | [Introducción a creación de informes](../reports/gs-reports.md) |
| Analizar un experimento y obtener recomendaciones de paso siguiente | Experimentation Agent **(IA)** | [Experimentation Agent](ai-features.md#experimentation-agent) · [Tutorial](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/experimentation/experimentation-agent-overview){target="_blank"} |
| Monitorizar el estado y la latencia de las acciones personalizadas en mis recorridos | Monitorización de acciones personalizadas | [Usar acciones personalizadas](../building-journeys/using-custom-actions.md) <!-- TODO: verify target — no dedicated "custom-action-monitoring.md" page found; using-custom-actions.md is the closest existing page --> |
| Reciba alertas cuando las tasas de error de recorrido o descarte superen los umbrales | alertas de recorrido | [Configurar alertas de recorrido](../reports/alerts.md) |

## Flujos de inicio {#starter-flows}

Cada flujo de inicio que aparece a continuación es un conjunto de pasos corto y orientado a resultados: qué va a generar, para quién sirve y cómo llegar allí. Elija el objetivo que coincida con su primer proyecto y siga los vínculos a la documentación detallada.

### Bienvenido nuevos clientes {#flow-welcome}

**Creará:** Una serie de bienvenida automatizada que saluda a cada suscriptor nuevo y empuja a los inactivos.**Ideal para:** especialistas en mercadotecnia · **Capacidad:** recorrido activado por eventos

1. Confirme que sus [perfiles y audiencias unificados](../audience/get-started-profiles.md) están recibiendo el evento de registro.
1. [Cree su primer recorrido](../building-journeys/journey-gs.md) y use el evento de registro como entrada.
1. Agregue un [correo electrónico](../email/get-started-email.md) de bienvenida, luego un paso de espera y una [notificación push](../push/get-started-push.md) de seguimiento para los perfiles que no se hayan comprometido.
1. [Personalice el contenido](../personalization/personalize.md) con atributos de perfil como el nombre y los intereses declarados.

➡️ [Empiece con recorridos](../building-journeys/journey-gs.md)

### Recuperar carros abandonados {#flow-cart}

**Creará:** Un flujo de recuperación automatizado que recuerda a los clientes los elementos que se han dejado atrás.**Ideal para:** especialistas en mercadotecnia · **Capacidad:** recorrido activado por eventos

1. Asegúrese de que el evento de abandono del carro de compras llegue a Journey Optimizer (trabaje con su [equipo de datos](../data/gs-data.md) si es necesario).
1. [Crear un recorrido](../building-journeys/journey-gs.md) desencadenado por el evento de abandono.
1. Envíe un correo electrónico de recordatorio personalizado; si no hay ningún clic en un plazo de 24 horas, bifurque a un seguimiento de [push](../push/get-started-push.md).
1. [Personalizar](../personalization/personalize.md) con los elementos abandonados y el estado de fidelidad.

➡️ [Empiece con recorridos](../building-journeys/journey-gs.md)

### Envío de mensajes transaccionales {#flow-transactional}

**Creará:** confirmaciones de pedidos, envíos o citas a petición activadas por un sistema externo.**Ideal para:** especialistas en marketing y desarrolladores · **Funcionalidad:** Campaña desencadenada por un sistema externo

1. Revise cómo funcionan las [campañas activadas por un sistema externo](../campaigns/api-triggered-campaigns.md) y qué carga útil esperan.
1. Diseñe la plantilla de mensaje y [personalícela](../personalization/personalize.md) con los detalles de la transacción.
1. Pida al desarrollador que llame al punto final de la campaña desde el sistema de pedidos o envíos.

➡️ [Trabaje con campañas activadas por un sistema externo](../campaigns/api-triggered-campaigns.md)

### Lanzamiento de una campaña con pruebas de contenido {#flow-campaign}

**Crearás:** Una promoción programada que selecciona automáticamente el contenido con mejor rendimiento.**Ideal para:** especialistas en mercadotecnia · **Capacidad:** Campaña programada + experimentación de contenido

1. [Empiece a usar las campañas](../campaigns/get-started-with-campaigns.md) y defina su audiencia.
1. Use [generación de contenido](../content-management/gs-generative.md) para redactar variaciones de línea de asunto y de copia.
1. Configure un [experimento de contenido](../content-management/experiment-accelerator-gs.md) para probar variantes en una muestra y, a continuación, envíe al ganador al resto.

➡️ [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

### Personalizar ofertas por cliente {#flow-offers}

**Creará:** Una decisión que muestra la mejor oferta para cada cliente.**Óptimo para:** Especialistas en marketing · **Capacidad:** Toma de decisiones

1. [Empiece con Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) y cree sus ofertas y reglas de elegibilidad.
1. Agregue la decisión a un [recorrido](../building-journeys/journey-gs.md) o mensaje de campaña.
1. Capa en [funciones inteligentes](ai-features.md) para clasificar y optimizar ofertas automáticamente.

➡️ [Introducción a Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Casos de ejemplo {#example-scenarios}

Estos ejemplos ilustran cómo las capacidades de Journey Optimizer funcionan en conjunto en diferentes funciones, sectores y canales.

### Recuperación retrasada del envío {#scenario-delayed-shipment}

**Función:** Profesional de marketing | **Capacidad principal:** [Perfil unificado + exclusión de público](../audience/get-started-profiles.md)

Una tienda de ropa suele enviar encuestas posteriores a la compra a todos los clientes que han comprado productos en la última semana. Debido a las inclemencias del tiempo, algunos envíos experimentaron retrasos. Al ver que la clientela no ha recibido sus envíos, la tienda de ropa puede excluirla del envío de satisfacción del cliente programado y, en su lugar, hacerles llegar un correo electrónico personalizado pidiendo disculpas por el retraso y ofreciéndoles un código de descuento con recomendaciones de productos basadas en las compras anteriores del cliente.

[Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

### Participación en tiempo real en la tienda {#scenario-instore}

**Función:** Profesional de marketing | **Capacidad principal:** [Activación de geoperímetro + push](../push/get-started-push.md)

El mismo retailer puede atraer a un cliente fiel que entra en el aparcamiento de la tienda enviándole una notificación push sobre un suéter que vuelve a estar en existencias en la talla del cliente.

[Introducción a las notificaciones push](../push/get-started-push.md)

### Recuperación de abandono del carro {#scenario-cart}

**Función:** Profesional de marketing | **Capacidad principal:** [recorrido de varios pasos activado por eventos](../building-journeys/journey-gs.md)

Cuando un cliente agrega artículos a un carro de compras en línea pero sale sin completar la compra, Journey Optimizer detecta el evento e inicia un recorrido de recuperación automáticamente. El cliente recibe un correo electrónico personalizado que le recuerda los artículos que ha dejado en el carro. Si no hace clic en un plazo de 24 horas, se envía una notificación push de seguimiento, personalizada en función de su historial de navegación y su nivel de fidelidad.

[Creación de su primer recorrido](../building-journeys/journey-gs.md)

### Serie de bienvenida del servicio de streaming {#scenario-welcome}

**Función:** Profesional de marketing | **Capacidad principal:** [recorrido de bienvenida activado por eventos](../building-journeys/journey-gs.md)

Cuando un cliente se suscribe a un servicio de streaming, Journey Optimizer detecta el evento de registro e inicia inmediatamente un recorrido de bienvenida de varios pasos. El cliente recibe un correo electrónico de bienvenida que le anima a abrir la aplicación por primera vez. Si no se detecta ninguna actividad de inicio de sesión en un plazo de 48 horas, se envía una notificación push de seguimiento con recomendaciones de contenido personalizadas en función de sus intereses declarados durante la suscripción, lo que convierte a un suscriptor pasivo en un usuario activo e implicado desde el primer día.

[Creación de su primer recorrido](../building-journeys/journey-gs.md)

### Recordatorio de reserva con indicaciones {#scenario-reservation}

**Función:** Profesional de marketing | **Capacidad principal:** [Mensajería programada + con reconocimiento de ubicación](../campaigns/get-started-with-campaigns.md)

Una marca de hostelería envía a cada huésped un recordatorio puntual una hora antes de su reserva. La notificación incluye el nombre del huésped, la hora de reserva y las direcciones según la ubicación al lugar de celebración, ensambladas automáticamente a partir del perfil del cliente y los datos de reserva, sin esfuerzo manual del equipo de marketing.

[Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

### Notificación de interrupción proactiva del servicio {#scenario-outage}

**Función:** Operaciones | **Capacidad principal:** [Selección automatizada de públicos a escala](../audience/about-audiences.md)

Cuando se produce una interrupción del servicio, Journey Optimizer identifica automáticamente a los clientes afectados en función de los datos de su cuenta y los patrones de uso. Estos clientes reciben una notificación proactiva que reconoce el problema y describe los pasos siguientes: convertir una experiencia potencialmente negativa en un momento de transparencia y confianza, entregada a escala.

[Creación de su primer recorrido](../building-journeys/journey-gs.md)

### Campaña promocional inteligente {#scenario-ai-campaign}

**Rol:** Especialista en marketing | **Capacidad principal:** [Generación de contenido + experimentación](ai-features.md)

Una marca comercial que planea el lanzamiento de un producto utiliza el asistente de IA de Journey Optimizer para generar varias variaciones de línea de asunto y texto del cuerpo en minutos, guiadas por una indicación en lenguaje natural y sus directrices de marca cargadas. La experimentación de contenido integrada identifica automáticamente la variante con mejor rendimiento entre una muestra de público inicial. El mensaje ganador se implementa a continuación en los destinatarios restantes, lo que maximiza la participación sin esfuerzo adicional de escritura.

[Explorar características inteligentes](ai-features.md) | [Más información sobre la experimentación de contenido](../content-management/experiment-accelerator-gs.md)

### Alertas de mantenimiento a través de aplicaciones móviles {#scenario-maintenance}

**Función:** Operaciones | **Capacidad principal:** [Organización de recorrido que no es de marketing](../building-journeys/journey-gs.md)

Quienes no son especialistas en marketing, como los equipos de operaciones y el servicio de atención al cliente, pueden usar [!DNL Adobe Journey Optimizer] para administrar las notificaciones operacionales o supervisar los procesos de incorporación. Por ejemplo, un parque de atracciones donde los visitantes descargan una aplicación móvil como parte de su experiencia: el personal de mantenimiento puede utilizar Journey Optimizer para notificar a los visitantes del parque de las atracciones que están cerradas debido al mantenimiento.

[Creación de su primer recorrido](../building-journeys/journey-gs.md)

## Biblioteca de vídeos {#videos}

Examine contenido de vídeo depurado por tema. Cada pestaña vincula a los tutoriales y listas de reproducción relevantes en Experience League.

>[!BEGINTABS]

>[!TAB Introducción]

* [Introducción a Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"}: conceptos básicos y recorrido del producto.
* [Descripción general de tutoriales de Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: El catálogo completo de vídeos guiados.

>[!TAB Recorridos y campañas]

* [Introducción a la creación de un recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}: Cree su primer recorrido activado por eventos.
* [Generar recorridos con Journey Agent](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"}: cree recorridos a partir de un mensaje en lenguaje natural.

>[!TAB Personalization e inteligencia]

* [Asistente de IA para la generación de contenido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"}: genere copias, imágenes y variaciones.
* [Use la toma de decisiones para personalizar ofertas web](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"}: adapte las ofertas por cliente.

>[!TAB Informes y optimización]

* [Supervise y analice su recorrido con informes en vivo](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"}: efectúe el seguimiento del rendimiento a medida que se ejecutan sus recorridos.
* [Crear experimentos de contenido para campañas de correo electrónico](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"}: Pruebe y optimice el contenido.

>[!ENDTABS]

## Elección entre recorridos, campañas y campañas organizadas {#choosing}

| Situación | Utilice |
| -------- | --- |
| Impulsado por el comportamiento, con varios pasos, cada cliente se mueve a su propio ritmo | Recorrido |
| Mensaje simple programado o activado por API a una audiencia | Campaign |
| Flujo de trabajo por lotes complejo con segmentación de varias entidades | Campaña organizada |

Para ver una comparación detallada con un árbol de decisiones y tablas de características, consulte [Recorridos frente a campañas: elija el método adecuado](journeys-vs-campaigns.md). Una vez que haya decidido los Recorridos, consulte [Tipos de Recorridos: elija el adecuado](../building-journeys/journey-types-selection.md) para elegir entre recorridos de evento unitario, audiencia de lectura, calificación de audiencia y evento empresarial.

## ¿No está seguro? {#not-sure}

Si su objetivo se asigna a un término con el que no está familiarizado o no está seguro de a qué capacidad apunta la tabla, comience con la página [terminología clave de Journey Optimizer](terminology.md) para aclarar los conceptos subyacentes a cada capacidad.

También puede generar confianza práctica con los ejercicios de extremo a extremo en [tutoriales de Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
