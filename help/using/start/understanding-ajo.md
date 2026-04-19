---
solution: Journey Optimizer
product: journey optimizer
title: Explicación de Journey Optimizer
description: Descubra cómo funciona Adobe Journey Optimizer con Adobe Experience Platform para ofrecer experiencias de cliente personalizadas
feature: Get Started
topic: Content Management
role: Admin, Developer, User
level: Beginner
keywords: recorrido optimizer, funcionamiento, arquitectura, experience platform, áreas funcionales
exl-id: 9df179a0-a5f6-4dbd-a9db-a103731b1854
source-git-commit: 3983f5912cb0579d489af6466025551b60d6938e
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 3%

---

# Explicación de Journey Optimizer {#understanding-ajo}

En esta página se explica cómo Adobe Experience Platform y Journey Optimizer trabajan juntos, abarcando el ciclo continuo de datos a experiencia, las áreas funcionales clave, los detalles de arquitectura y los puntos de integración.

Adobe Journey Optimizer y Adobe Experience Platform trabajan juntos para permitir la personalización basada en datos a escala. Esta página explica cómo funcionan estos sistemas y cómo se combinan sus áreas funcionales clave para ofrecer experiencias de cliente excepcionales. [Más información acerca de las funciones clave](get-started.md) | [Explorar la terminología clave](terminology.md)

## Cómo funciona Journey Optimizer {#how-it-works}

Sin una base de datos unificada, las marcas se ven obligadas a confiar en varias herramientas específicas del canal, lo que dificulta mantener una vista coherente de cada cliente o actuar en su comportamiento en tiempo real. Journey Optimizer resuelve esto basándose en Adobe Experience Platform para conectar los datos de los clientes, la creación de contenido y la orquestación de recorrido en un único sistema continuo. El resultado son experiencias de marca significativas que impulsan la lealtad del cliente y el valor de duración.

Adobe Journey Optimizer funciona como un flujo continuo en el que los datos se recopilan, analizan y aplican para crear recorridos personalizados con los clientes.

![Diagrama que muestra Adobe Experience Platform como la capa de datos fundamental, con Journey Optimizer integrado sobre Real-Time CDP, Customer Journey Analytics y Adobe Mix Modeler, todos compartiendo servicios principales como el perfil del cliente en tiempo real, el control de datos y la resolución de identidades.](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: la base {#aep-foundation}

Adobe Experience Platform sirve como columna vertebral, permitiendo a las marcas centralizar los datos de los clientes y activarlos para experiencias personalizadas:

* **Plataforma de datos**: hub central para recopilar, administrar y estructurar datos de clientes con el fin de garantizar la coherencia en todos los sistemas. [Más información sobre esquemas y conjuntos de datos](../data/get-started-schemas.md)
* **Ingesta de datos (fuentes)**: importe datos de plataformas CRM, sitios web, aplicaciones móviles y almacenamiento en la nube mediante conectores generados previamente. [Explorar orígenes de datos](get-started-sources.md)
* **Perfil del cliente en tiempo real**: crea perfiles unificados combinando datos de varias fuentes (interacciones por correo electrónico, compras en la tienda, comportamiento en la web). [Más información sobre los perfiles](../audience/get-started-profiles.md)
* **Nivel de control**: rige el acceso a los datos, el cumplimiento de la privacidad y la seguridad al tiempo que cumple las regulaciones. [Ver documentación de privacidad](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: el motor de orquestación {#ajo-orchestration}

Adobe Journey Optimizer aplica los datos y las perspectivas de Adobe Experience Platform para ofrecer experiencias de cliente inteligentes y personalizadas:

* **Comprensión del cliente**: los perfiles del cliente en tiempo real habilitan la segmentación en audiencias para la mensajería de destino. [Crear públicos](../audience/about-audiences.md)
* **Contenido y ofertas**: un diseñador visual integrado, plantillas reutilizables y una biblioteca de recursos centralizada permiten que los equipos creen y personalicen mensajes para cualquier canal, sin salir de la plataforma. La personalización dinámica adapta el contenido en función de los atributos, el comportamiento y el contexto del cliente. A continuación, la lógica de toma de decisiones en tiempo real selecciona la mejor oferta para cada individuo. [Contenido de diseño](../../rp_landing_pages/content-management-landing-page.md) | [Administrar recursos](../integrations/assets.md) | [Administrar ofertas](../offers/get-started/starting-offer-decisioning.md)
* **Administración de Recorridos y campañas**: automatiza secuencias de interacciones (recorridos) o programa mensajes de destino únicos (campañas). [Generar recorridos](../building-journeys/journey-gs.md) | [Crear campañas](../campaigns/get-started-with-campaigns.md)
* **Envío (conexiones)**: envía mensajes a través de canales como correo electrónico, SMS, notificaciones push y correo directo; exporta datos a sistemas externos. [Configuración de canales](../configuration/get-started-configuration.md)
* **Medición y análisis**: Rastrea la participación de los clientes y el rendimiento de las campañas con informes para mejorar continuamente. [Ver informes](../reports/campaign-global-report-cja.md)

### El ciclo de optimización continua {#optimization-cycle}

Este ecosistema funciona como un ciclo de optimización continua. Los datos mejoran la comprensión del cliente, que informa el contenido personalizado y las decisiones. Se organizan en recorridos, se entregan en varios canales, se miden para obtener eficacia y se refinan con el tiempo.

![Diagrama que ilustra el ciclo de optimización continua en Journey Optimizer: la ingesta de datos alimenta los perfiles de los clientes, que informan las decisiones de contenido y ofertas, organizados en recorridos, entregados en varios canales, medidos para el rendimiento y refinados a lo largo del tiempo.](../assets/do-not-localize/get-started-flow.png)

## Áreas funcionales clave {#functional-areas}

Journey Optimizer incluye siete áreas funcionales clave que funcionan juntas sin problemas:

| Área funcional | Objetivo | Actividades clave |
|-----------------|---------|----------------|
| **Administración de datos** | Organizar datos de clientes | Defina esquemas, cree conjuntos de datos e importe datos de varios sistemas. [Más información](../data/get-started-schemas.md) |
| **Administración de clientes** | Comprenda quiénes son sus clientes | Cree perfiles unificados, resuelva identidades y cree audiencias. [Más información](../audience/get-started-profiles.md) |
| **Administración de contenido** | Creación de mensajes personalizados | Diseñe correos electrónicos, administre recursos, cree plantillas y fragmentos y personalice contenido. [Más información](../../rp_landing_pages/content-management-landing-page.md) |
| **Gestión de decisiones** | Seleccione la mejor oferta en tiempo real | Administrar la biblioteca de ofertas, definir reglas, aplicar restricciones, establecer lógica de clasificación. [Más información](../offers/get-started/starting-offer-decisioning.md) |
| **Administración de Recorrido** | Diseño de experiencias de cliente automatizadas | Cree recorridos con el diseñador visual, establezca déclencheur, agregue condiciones y espere pasos. [Más información](../building-journeys/journey-gs.md) |
| **Conexiones** | Conexión de fuentes de datos y canales | Configure conectores de origen, configure canales y conéctese a plataformas externas. [Más información](../configuration/get-started-configuration.md) |
| **Administración y privacidad** | Configuración y conformidad de control | Administrar usuarios, configurar zonas protegidas, configurar canales y gestionar solicitudes de privacidad. [Más información](../administration/permissions.md) |

### Cómo funcionan juntas estas áreas {#working-together}

Estas áreas funcionales funcionan en un ciclo continuo:

1. **Ingesta de datos**: los datos fluyen a Adobe Experience Platform, estructurados por la administración de datos
2. **Comprensión del cliente**: los perfiles del cliente en tiempo real unifican los datos; la administración de clientes crea audiencias
3. **Estrategia de contenido y ofertas**: la administración de contenido crea mensajes; la administración de decisiones define la lógica de ofertas
4. **Orquestación**: Administración de Recorrido asigna interacciones entre canales mediante datos de clientes, contenido y decisiones
5. **Envío**: las conexiones facilitan la entrega de mensajes a través de canales o comparten datos con sistemas externos
6. **Medición**: los datos de rendimiento devuelven información para refinar audiencias, contenido, decisiones y recorridos
7. **Gobernanza**: los controles de administración y privacidad garantizan el cumplimiento en todo

## Detalles de arquitectura {#architecture-details}

Journey Optimizer es una de las cuatro aplicaciones creadas de forma nativa en Adobe Experience Platform, junto con Real-Time CDP, Customer Journey Analytics y Adobe Mix Modeler. Comparte los servicios principales de AEP (perfil del cliente en tiempo real, gráfico de identidad, control de datos y servicios de consulta) para acceder a una base de datos de cliente unificada sin requerir integraciones independientes. Journey Optimizer puede funcionar como una aplicación independiente o interoperar con otras aplicaciones nativas de AEP.

Para profundizar en la arquitectura técnica, incluidos los patrones de integración, los requisitos previos y los flujos de datos del sistema, consulte los [modelos de Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}. Para consideraciones de implementación, [revise protecciones y limitaciones](guardrails.md).

## Privacidad y seguridad {#privacy-security}

Las prácticas de privacidad y seguridad de Adobe Experience Cloud se aplican a Adobe Journey Optimizer. Estas medidas garantizan el cumplimiento de las regulaciones de privacidad como el RGPD, lo que le permite ofrecer experiencias personalizadas sin dejar de mantener la confianza de los clientes. [Más información sobre privacidad en Journey Optimizer](../privacy/get-started-privacy.md)
