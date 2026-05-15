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
TQID: https://experienceleague.adobe.com/E2ksPVFZBggv1RgEri7jx30G2oSanpmNs77vH9Yuq78
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: af7571a6-3ddb-4c1c-abdf-4d4dde592140
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 957
ht-degree: 3%

---

# Explicación de Journey Optimizer {#understanding-ajo}

En esta página se explica cómo Adobe Experience Platform y Journey Optimizer trabajan juntos, abarcando el ciclo continuo de datos a experiencia, las áreas funcionales clave, los detalles de arquitectura y los puntos de integración.

Adobe Journey Optimizer y Adobe Experience Platform trabajan juntos para permitir la personalización basada en datos a escala. Esta página explica cómo funcionan estos sistemas y cómo se combinan sus áreas funcionales clave para ofrecer experiencias de cliente excepcionales. [Más información acerca de las funcionalidades clave](get-started.md) | [Explorar la terminología clave](terminology.md)

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
* **Contenido y ofertas**: un diseñador visual integrado, plantillas reutilizables y una biblioteca de recursos centralizada permiten que los equipos creen y personalicen mensajes para cualquier canal, sin salir de la plataforma. La personalización dinámica adapta el contenido en función de los atributos, el comportamiento y el contexto del cliente. A continuación, la lógica de toma de decisiones en tiempo real selecciona la mejor oferta para cada individuo. [Diseñar contenido](../../rp_landing_pages/content-management-landing-page.md) | [Administrar recursos](../integrations/assets.md) | [Administrar ofertas](../offers/get-started/starting-offer-decisioning.md)
* **Administración de Recorridos y campañas**: automatiza secuencias de interacciones (recorridos) o programa mensajes de destino únicos (campañas). [recorridos de compilación](../building-journeys/journey-gs.md) | [Crear campañas](../campaigns/get-started-with-campaigns.md)
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
| **Administración de decisiones** | Seleccione la mejor oferta en tiempo real | Administrar la biblioteca de ofertas, definir reglas, aplicar restricciones, establecer lógica de clasificación. [Más información](../offers/get-started/starting-offer-decisioning.md) |
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
