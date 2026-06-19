---
solution: Journey Optimizer
product: journey optimizer
title: hub de incorporación de Journey Optimizer
description: Un centro de incorporación depurado para Adobe Journey Optimizer que reúne instrucciones paso a paso, casos de uso reales y contenido de vídeo para que los nuevos usuarios puedan aumentar rápidamente y ofrecer su primera experiencia al cliente.
feature: Get Started
topic: Content Management
role: User
level: Beginner
hide: true
keywords: optimizador de recorrido, incorporación, centro de incorporación, casos de uso, vídeos, tutoriales, introducción, ampliación, primer recorrido
source-git-commit: 79337a0d2a65fa1e8aa1e5d47bcf39906d9887a7
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 12%

---

# hub de incorporación de Journey Optimizer {#onboarding-hub}


>[!BEGINSHADEBOX]

**En esta página:** Acércate rápidamente a Adobe Journey Optimizer; observa una breve orientación, sigue instrucciones paso a paso para enviar tu primera experiencia, explora casos de uso reales y sumérgete en contenido de vídeo seleccionado.

>[!ENDSHADEBOX]

<!-- 
rebuild
-->

¿Es nuevo en [!DNL Adobe Journey Optimizer]? Este concentrador recopila los recursos que le ayudan a pasar de cero a la primera experiencia del cliente en directo, con instrucciones paso a paso para objetivos comunes, casos de uso reales que muestran lo que es posible y contenido de vídeo depurado (tutoriales, tutoriales y práctica).

>[!TIP]
>
>¿No está seguro de qué capacidad se ajusta a su objetivo? Empiece por [Encontrar la funcionalidad de Journey Optimizer adecuada para su guía de objetivos](ajo-use-case-guide.md) y vuelva aquí para obtener instrucciones paso a paso.

## Comience aquí: ver y aprender {#start-here}

Si tiene diez minutos, empiece con este vídeo de orientación. Recorre la interfaz y resalta las capacidades clave por función.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

A continuación, genere confianza práctica con estos recursos de aprendizaje:

* [Tutoriales de Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: vídeos paso a paso y tutoriales guiados para cada función.
* [Lista de reproducción de vídeo recopilada por expertos](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"}: Un conjunto secuenciado de vídeos cortos para ver en orden.
* [Entorno aislado de formación](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"}: un entorno seguro con datos de ejemplo para practicar.
* [Desafíos prácticos](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"} — Aplique lo que aprende con ejercicios guiados.

## Cree su primera experiencia {#build-first}

Cada uno de los pasos a continuación es un breve conjunto de pasos orientados a resultados: para qué se construirá, para quién es y cómo llegar allí. Elija el objetivo que coincida con su primer proyecto y siga los vínculos a la documentación detallada.

### Bienvenido nuevos clientes {#build-welcome}

**Creará:** Una serie de bienvenida automatizada que saluda a cada suscriptor nuevo y empuja a los inactivos.
**Ideal para:** especialistas en mercadotecnia · **Capacidad:** recorrido activado por eventos

1. Confirme que sus [perfiles y audiencias unificados](../audience/get-started-profiles.md) están recibiendo el evento de registro.
2. [Cree su primer recorrido](../building-journeys/journey-gs.md) y use el evento de registro como entrada.
3. Agregue un [correo electrónico](../email/get-started-email.md) de bienvenida, luego un paso de espera y una [notificación push](../push/get-started-push.md) de seguimiento para los perfiles que no se hayan comprometido.
4. [Personalice el contenido](../personalization/personalize.md) con atributos de perfil como el nombre y los intereses declarados.

➡️ [Empiece con recorridos](../building-journeys/journey-gs.md)

### Recuperar carros abandonados {#build-cart}

**Creará:** Un flujo de recuperación en tiempo real que recuerda a los clientes los elementos que quedan.
**Ideal para:** especialistas en mercadotecnia · **Capacidad:** recorrido activado por eventos

1. Asegúrese de que el evento de abandono del carro de compras llegue a Journey Optimizer (trabaje con su [equipo de datos](../data/gs-data.md) si es necesario).
2. [Crear un recorrido](../building-journeys/journey-gs.md) desencadenado por el evento de abandono.
3. Envíe un correo electrónico de recordatorio personalizado; si no hay ningún clic en un plazo de 24 horas, bifurque a un seguimiento de [push](../push/get-started-push.md).
4. [Personalizar](../personalization/personalize.md) con los elementos abandonados y el estado de fidelidad.

➡️ [Empiece con recorridos](../building-journeys/journey-gs.md)

### Envío de mensajes transaccionales {#build-transactional}

**Creará:** confirmaciones de pedidos, envíos o citas a petición activadas por un sistema externo.
**Ideal para:** especialistas en marketing y desarrolladores · **Capacidad:** Campaña activada por API

1. Revise cómo funcionan [campañas activadas por API](../campaigns/api-triggered-campaigns.md) y qué carga útil esperan.
2. Diseñe la plantilla de mensaje y [personalícela](../personalization/personalize.md) con los detalles de la transacción.
3. Pida al desarrollador que llame al punto final de la campaña desde el sistema de pedidos o envíos.

➡️ [Trabajar con campañas activadas por API](../campaigns/api-triggered-campaigns.md)

### Lanzamiento de una campaña con pruebas A/B {#build-campaign}

**Crearás:** Una promoción programada que selecciona automáticamente el contenido con mejor rendimiento.
**Ideal para:** especialistas en mercadotecnia · **Capacidad:** Campaña programada + experimentación de contenido

1. [Empiece a usar las campañas](../campaigns/get-started-with-campaigns.md) y defina su audiencia.
2. Use [generación de contenido de IA](../content-management/gs-generative.md) para redactar variaciones de línea de asunto y de copia.
3. Configure un [experimento de contenido](../content-management/experiment-accelerator-gs.md) para probar variantes en una muestra y, a continuación, envíe al ganador al resto.

➡️ [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

### Personalizar ofertas por cliente {#build-offers}

**Creará:** Una decisión que muestra la mejor oferta para cada cliente.
**Ideal para:** especialistas en marketing · **Capacidad:** Toma de decisiones

1. [Empiece con Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) y cree sus ofertas y reglas de elegibilidad.
2. Agregue la decisión a un [recorrido](../building-journeys/journey-gs.md) o mensaje de campaña.
3. Capa en [características de IA](ai-features.md) para clasificar y optimizar ofertas automáticamente.

➡️ [Introducción a Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Casos de uso por objetivo {#use-cases}

Los ejemplos anteriores cubren los puntos de partida más comunes, pero Journey Optimizer admite muchos más escenarios, desde notificaciones proactivas de interrupciones y renovación de la participación de los clientes hasta mensajería en tiempo real según la ubicación. Cada escenario combina una o más funcionalidades que trabajan juntas.

Para encontrar la capacidad exacta para *su objetivo de*, use el índice completo y organizado por objetivos en [Encuentre la capacidad de Journey Optimizer adecuada para su objetivo](ajo-use-case-guide.md). Para ver ejemplos prácticos e integrales, consulte la [biblioteca de casos de uso de Recorrido](../building-journeys/jo-use-cases.md).

## Biblioteca de vídeos {#videos}

Examine contenido de vídeo depurado por tema. Cada pestaña vincula a los tutoriales y listas de reproducción relevantes en Experience League.

>[!BEGINTABS]

>[!TAB Introducción]

* [Introducción a Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"}: conceptos básicos y recorrido del producto.
* [Descripción general de tutoriales de Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: El catálogo completo de vídeos guiados.

>[!TAB Recorridos y campañas]

* [Introducción a la creación de un recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}: Cree su primer recorrido activado por eventos.
* [Generar recorridos con Journey Agent](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"}: cree recorridos a partir de un mensaje en lenguaje natural.

>[!TAB Personalization y IA]

* [Asistente de IA para la generación de contenido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"}: genere copias, imágenes y variaciones.
* [Use la toma de decisiones para personalizar ofertas web](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"}: adapte las ofertas por cliente.

>[!TAB Informes y optimización]

* [Monitorice y analice su recorrido con informes en vivo](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} — Rastree el rendimiento en tiempo real.
* [Crear experimentos de contenido para campañas de correo electrónico](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"}: Pruebe y optimice el contenido.

>[!ENDTABS]

## Lista de comprobación de incorporación por función {#checklist}

La incorporación abarca varias funciones. Elija su función para ver una ruta de inicio centrada:

* **Administrador**: configure zonas protegidas, permisos y canales. [Introducción como administrador](path/administrator.md)
* **Ingeniero de datos**: Modele esquemas e ingrese datos. [Introducción como ingeniero de datos](path/data-engineer.md)
* **Desarrollador** — Integrar SDK y eventos de déclencheur. [Introducción como desarrollador](path/developer.md)
* **Especialista en mercadotecnia**: cree recorridos, contenido y audiencias. [Introducción como experto en marketing](path/marketer.md)

Para obtener una descripción general completa de cómo funcionan juntas estas funciones, consulte [Funciones y responsabilidades](quick-start.md).

## Recursos relacionados {#related-resources}

* [Encuentre la capacidad de Journey Optimizer adecuada para su objetivo](ajo-use-case-guide.md): guía de decisión para cada capacidad basada en objetivos.
* [Biblioteca de casos de uso de Recorrido](../building-journeys/jo-use-cases.md): ejemplos prácticos y patrones de implementación.
* [Terminología clave](terminology.md): aclare los conceptos subyacentes a cada capacidad.
* [IA y funciones inteligentes](ai-features.md): Explore el asistente de IA, la optimización del tiempo de envío y la generación de contenido.
* [Introducción a la administración de datos](../data/gs-data.md): Cómo se incorporan, unifican y activan los datos.
