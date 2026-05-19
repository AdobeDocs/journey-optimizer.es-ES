---
solution: Journey Optimizer
product: journey optimizer
title: Terminología clave
description: Términos y conceptos esenciales en Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 26ebbdc6d51ee9ad7c47ce26e7df04064b90268f
workflow-type: tm+mt
source-wordcount: 1576
ht-degree: 7%

---

# Terminología clave {#key-terminology}

Esta guía de referencia define los términos esenciales que se encontrará al utilizar Adobe Journey Optimizer. Comprender estos conceptos le ayuda a navegar por la plataforma con seguridad y a colaborar eficazmente con su equipo.

Para pares de términos que suenan similares y que a menudo se confunden, como **Toma de decisiones vs. Administración de decisiones** o **Tarjetas de contenido vs. Mensajes en la aplicación**, consulte [Cuando los términos tienen un aspecto similar](#disambiguation) en la parte inferior de esta página.

>[!NOTE]
>
>Adobe Journey Optimizer se creó en **Adobe Experience Platform**. Muchos conceptos básicos que encontrará, como perfiles de clientes en tiempo real, zonas protegidas, esquemas y conjuntos de datos, son conceptos de Adobe Experience Platform, no específicos de Journey Optimizer. Para ver las definiciones de esos términos, consulte el [glosario de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html){target="_blank"}.

## Recorrido y términos de la campaña {#journey-campaign-terms}

| Término | Definición |
|------|------------|
| **Recorrido** | Una serie de pasos conectados que guían a los clientes a través de las experiencias con su marca a lo largo del tiempo. Cada paso se produce en función de las acciones del cliente o los déclencheur de tiempo, lo que permite interacciones secuenciales y personalizadas. [Más información](../building-journeys/journey.md) |
| **Campaign** | Una acción de marketing coordinada que ofrece contenido a una audiencia específica en uno o varios canales. A diferencia de los recorridos, las campañas ejecutan acciones simultáneamente. Journey Optimizer admite tres tipos de campañas: **Campañas de acción** (envíos por lotes programados), **Campañas activadas por API** (mensajería en tiempo real impulsada por eventos mediante API) y **Campañas orquestadas** (flujos de trabajo complejos de varios pasos con un lienzo visual). [Más información](../campaigns/get-started-with-campaigns.md) |
| **Evento** | Una acción u ocurrencia que pone en déclencheur o avanza un recorrido. Los eventos pueden ser acciones del cliente (realizar una compra, abandonar un carro de compras) o eventos del sistema (fecha/hora, cambio de datos). [Más información](../event/about-events.md) |
| **Canal** | El método utilizado para comunicarse con los clientes: correo electrónico, SMS, notificaciones push, mensajes en la aplicación, web o correo directo. Cada canal requiere una configuración específica. [Más información](../configuration/get-started-configuration.md) |

## Términos de cliente y audiencia {#customer-audience-terms}

| Término | Definición |
|------|------------|
| **Audiencia** | Un grupo de clientes que comparten características o comportamientos comunes, como &quot;clientes que compraron en los últimos 30 días&quot; o &quot;miembros del programa de fidelidad&quot;. Las audiencias se utilizan para segmentar clientes específicos. [Más información](../audience/about-audiences.md) |
| **Calificación de audiencias** | Proceso automático que se produce cuando un cliente se une a una audiencia o la abandona. Journey Optimizer puede almacenar en déclencheur las acciones que se producen cuando alguien entra o sale de una audiencia, lo que garantiza comunicaciones oportunas y relevantes. [Más información](../building-journeys/audience-qualification-events.md) |
| **Audiencia atractiva** | El número de perfiles de cliente con los que puede ponerse en contacto de forma activa mediante Adobe Journey Optimizer en función del acuerdo de licencia. Esto suele referirse a perfiles contratados en los últimos 12 meses. |
| **Perfil de prueba** | Perfiles ficticios utilizados para probar y previsualizar mensajes antes de enviarlos a clientes reales. Los perfiles de prueba ayudan a comprobar la personalización, el contenido y la lógica de recorrido. [Más información](../audience/creating-test-profiles.md) |

## Contenido y términos de personalización {#content-terms}

| Término | Definición |
|------|------------|
| **Personalización** | Proceso de adaptar el contenido a clientes individuales mediante el uso de sus datos de perfil, preferencias y comportamientos. Por ejemplo, al insertar el nombre de un cliente o mostrar recomendaciones de productos basadas en el historial de navegación. [Más información](../personalization/personalize.md) |
| **Plantilla de contenido** | Un diseño de mensaje reutilizable que se puede utilizar en varias campañas y recorridos para mantener la coherencia de la marca y acelerar la creación de contenido. [Más información](../content-management/content-templates.md) |
| **Fragmento** | Un bloque de contenido reutilizable (como un encabezado, un pie de página o un banner promocional) que se puede utilizar en varios mensajes para garantizar la coherencia y permitir actualizaciones centralizadas. [Más información](../content-management/fragments.md) |
| **Página de aterrizaje** | Una página web independiente en la que los clientes pueden optar por su inclusión o exclusión de comunicaciones, suscribirse a servicios o proporcionar información a través de formularios en línea. [Más información](../landing-pages/get-started-lp.md) |
| **Experimento de contenido** | Un marco de pruebas A/B que divide una audiencia en grupos aleatorios y ofrece diferentes variantes de mensaje (contenido, línea de asunto u oferta) a cada grupo. A continuación, identifica la variante con mejor rendimiento en función de una métrica de éxito definida. [Más información](../content-management/get-started-experiment.md) |
| **Experimentación** | La capacidad más amplia de Journey Optimizer para probar y optimizar decisiones: los experimentos de contenido prueban variantes de mensajes en campañas y recorridos, mientras que las pruebas de experimentación de toma de decisiones ofrecen estrategias de selección. Ambos utilizan el análisis estadístico para identificar los enfoques ganadores. [Más información](../content-management/get-started-experiment.md) |

## Decisión y condiciones de la oferta {#decision-terms}

| Término | Definición |
|------|------------|
| **Toma de decisiones** | El marco de decisión de generación actual en Journey Optimizer, recomendado para nuevas implementaciones. Ofrece administración de catálogos de artículos basada en esquemas, reglas de recopilación flexibles, componentes de decisión reutilizables y capacidades de experimentación. Disponible para experiencia basada en código, push, SMS y correo electrónico (disponibilidad limitada). [Más información](../experience-decisioning/gs-experience-decisioning.md) |
| **Administración de decisiones** | Función heredada de Offer Decisioning en Journey Optimizer. Utiliza una biblioteca central de ofertas de marketing y un motor de decisión basado en reglas que aplica restricciones a perfiles de clientes en tiempo real. Sigue siendo compatible con las implementaciones existentes, pero las nuevas implementaciones deben utilizar Decisioning en su lugar. Admite correo electrónico, aplicación, push, SMS y correo directo. [Más información](../offers/get-started/starting-offer-decisioning.md) |
| **Oferta** | Un mensaje de marketing, un descuento o una promoción que se pueden presentar a los clientes. Las ofertas incluyen reglas de idoneidad que determinan qué clientes pueden recibirlas. [Más información](../offers/offer-library/creating-personalized-offers.md) |
| **Directiva de decisión** | Un conjunto de reglas y estrategias que determinan qué oferta mostrar a qué cliente en qué momento, en función de restricciones como elegibilidad, prioridad y reglas de límite. [Más información](../experience-decisioning/create-decision.md) |

## Términos de configuración y datos {#data-config-terms}

| Término | Definición |
|------|------------|
| **Configuración de canal** | La configuración que define cómo se envían los mensajes para un canal específico, incluidos los detalles del remitente, el subdominio, el grupo de IP y el tipo de mensaje (de marketing o transaccional). Anteriormente, se conocía como &quot;superficie&quot; o &quot;ajuste preestablecido&quot; en la documentación anterior. [Más información](../configuration/channel-surfaces.md) |
| **Lista de supresión** | Una lista de direcciones de correo electrónico y dominios excluidos automáticamente de la entrega de mensajes debido a rechazos graves, quejas de spam o adiciones manuales. La entrega a direcciones suprimidas está bloqueada para proteger la capacidad de entrega y la reputación del remitente. [Más información](../reports/suppression-list.md) |

## Conflicto y términos de priorización {#conflict-terms}

| Término | Definición |
|------|------------|
| **Conjunto de reglas** | Un grupo con nombre de reglas comerciales aplicadas a recorridos y campañas para regular el comportamiento de la mensajería. Un conjunto de reglas puede combinar límites de frecuencia, límites de entrada de recorrido y horas tranquilas en una única directiva reutilizable. [Más información](../conflict-prioritization/rule-sets.md) |
| **Límite de frecuencia** | Una regla de un conjunto de reglas que limita la cantidad de mensajes que puede recibir un perfil en un período de tiempo determinado, por canal o tipo de comunicación (ventas, promocionales, etc.). Los perfiles que exceden el límite se excluyen automáticamente de la entrega. [Más información](../conflict-prioritization/channel-capping.md) |

## Cuando los términos tienen un aspecto similar: guía de desambiguación {#disambiguation}

Adobe Journey Optimizer ha crecido durante varios años, lo que significa que algunas áreas de funcionalidades comparten nombres similares. Utilice las tablas siguientes para identificar rápidamente qué capacidad se adapta a sus necesidades.

### Toma de decisiones vs. administración de decisiones {#decisioning-vs-dm}

Ambas funciones seleccionan y entregan ofertas, pero sirven para diferentes etapas del ciclo de vida del producto.

| | Toma de decisiones | Gestión de decisiones |
|---|---|---|
| **Estado** | Actual: recomendado para todas las implementaciones nuevas | **Heredado**: aún se admite, pero ya no se recomienda para nuevas implementaciones |
| **Presentado** | 2024 | 2021 |
| **Catálogo de artículos** | Metadatos flexibles y basados en esquemas | Biblioteca de ofertas centralizada |
| **Canales compatibles** | Experiencia basada en código, push, SMS, correo electrónico (disponibilidad limitada) | Correo electrónico, aplicación, push, SMS, correo directo |
| **Diferenciador de clave** | Componentes de decisión reutilizables, experimentación, hoja de ruta de canal más amplia | Motor de restricciones probado; migrar a Decisioning para nuevos proyectos |
| **Introducción** | [Toma de decisiones](../experience-decisioning/gs-experience-decisioning.md) | [Administración de decisiones](../offers/get-started/starting-offer-decisioning.md) |

Si está usando Administración de decisiones y desea cambiar, consulte la [guía de migración](../experience-decisioning/migrate-to-decisioning.md).

### Tipos de campañas {#campaign-types-disambiguation}

Journey Optimizer ofrece tres tipos de campañas que se activan de forma diferente y sirven para casos de uso diferentes.

| | Campañas de acción (Campañas programadas) | Campañas activadas por API | Campañas orquestadas |
|---|---|---|---|
| **Activación** | Manual o programado | Llamada de API externa | Lienzo de flujo de trabajo visual |
| **Mejor para** | Envíos por lotes únicos o recurrentes (boletines informativos, promociones) | Mensajería en tiempo real impulsada por eventos (confirmaciones de pedidos, restablecimientos de contraseñas) | Programas multicanal complejos de varios pasos de duración |
| **Origen de Personalization** | Atributos de perfil | Atributos de perfil + contexto de carga útil de API | Atributos de perfil + datos relacionales |
| **Introducción** | [Campañas de acción](../campaigns/create-campaign.md) | [Campañas activadas por API](../campaigns/api-triggered-campaigns.md) | [Campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md) |

Para obtener una descripción general completa de todos los tipos de campañas y cuándo utilizarlos, consulte [Introducción a las campañas](../campaigns/get-started-with-campaigns.md).

### Límite de frecuencia frente a arbitraje de recorrido {#capping-vs-arbitration}

Ambos son mecanismos establecidos por reglas en el conjunto de herramientas Conflicto y priorización, pero abordan problemas diferentes.

| | Restricción de frecuencia | Arbitraje del recorrido |
|---|---|---|
| **Problema resuelto** | Un perfil recibe demasiados mensajes con el tiempo | Un perfil cumple los requisitos para varios recorridos simultáneamente |
| **Ámbito** | Por canal y tipo de comunicación (ventas, promocionales, etc.) | Inscripción en el recorrido: número de recorridos simultáneos o qué recorrido gana |
| **Mecanismo** | Limita el número de mensajes por periodo; excluye automáticamente los perfiles saturados | Utiliza puntuaciones de prioridad y reglas de límite para decidir qué recorrido introduce un perfil |
| **Configurado en** | Conjuntos de reglas → límite de frecuencia | Conjuntos de reglas → límite de Recorrido y arbitraje |
| **Más información** | [Establecer límite de frecuencia por canal](../conflict-prioritization/channel-capping.md) | [Administrar el límite y arbitraje de recorridos](../conflict-prioritization/journey-capping.md) |

### Tarjetas de contenido o mensajes en la aplicación {#content-cards-vs-in-app}

Ambos canales envían mensajes dentro de una aplicación móvil o web, pero tienen diferentes modelos de procesamiento y comportamientos de persistencia.

| | Tarjetas de contenido | Mensajes en la aplicación |
|---|---|---|
| **Modelo de pantalla** | Tarjetas persistentes incrustadas en la IU de la aplicación (fuente, bandeja de entrada o superficie personalizada) | Superposiciones, titulares o modelos transitorios que se muestran en la parte superior de la aplicación |
| **Persistencia** | Permanece visible hasta que se descarta o caduca explícitamente | Desaparece después de que el usuario interactúe o lo cierre |
| **Déclencheur** | SDK se procesa al cargar; las reglas controlan la visualización y el despido | Un evento en tiempo real en la entrega de déclencheur de recorrido o campaña |
| **Mejor para** | Promociones en curso, estado de fidelidad, alertas persistentes | Sugerencias de incorporación, ofertas de tiempo limitado, notificaciones transitorias |
| **Introducción** | [Tarjetas de contenido](../content-card/create-content-card.md) | [Mensajes en la aplicación](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer frente a Journey Optimizer B2B edition:** Son dos productos independientes de la misma familia de marcas. Adobe Journey Optimizer (esta documentación) se dirige a los recorridos de los clientes B2C. Journey Optimizer B2B edition está diseñado específicamente para el marketing basado en cuentas y trabaja con grupos de compra y audiencias de cuenta. Si está buscando documentación de B2B edition, visite la [guía de Journey Optimizer B2B edition](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}.

## Temas relacionados {#related-topics}

* [Descripción del funcionamiento de Journey Optimizer](understanding-ajo.md): vea cómo encajan los recorridos, las campañas, los perfiles y los canales en la arquitectura del producto.
* [Empiece a usar las capacidades de decisión](../experience-decisioning/gs-decision.md): compare la toma de decisiones y la administración de decisiones en paralelo y elija el método adecuado para su implementación.
* [Introducción a recorrido](../building-journeys/journey.md): aprenda a crear experiencias secuenciales de cliente activadas por eventos paso a paso.
* [Empiece a usar las campañas](../campaigns/get-started-with-campaigns.md): comprenda los tres tipos de campañas (de acción, activadas por API y orquestadas) y cuándo utilizarlas.
* [Administración de conflictos y priorización](../conflict-prioritization/gs-conflict-prioritization.md): aprenda a usar conjuntos de reglas, límites de frecuencia, puntuaciones de prioridad y horas de silencio para evitar mensajes excesivos.
* [Introducción a los canales de comunicación](../channels/gs-channels.md): Examine todos los canales disponibles, sus requisitos previos y cómo configurarlos.
