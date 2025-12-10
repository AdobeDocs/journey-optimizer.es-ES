---
solution: Journey Optimizer
product: journey optimizer
title: Explicación de Journey Optimizer
description: Descubra cómo funciona Adobe Journey Optimizer con Adobe Experience Platform para ofrecer experiencias de cliente personalizadas
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 3%

---

# Explicación de Journey Optimizer {#understanding-ajo}

Adobe Journey Optimizer y Adobe Experience Platform trabajan juntos para permitir la personalización basada en datos a escala. Esta página explica cómo funcionan estos sistemas y cómo se combinan sus áreas funcionales clave para ofrecer experiencias de cliente excepcionales. [Más información acerca de las funcionalidades clave](get-started.md) | [Explorar la terminología clave](terminology.md)

## Cómo funciona Journey Optimizer {#how-it-works}

Adobe Journey Optimizer funciona como un flujo continuo en el que los datos se recopilan, analizan y aplican para crear recorridos personalizados con los clientes.

![](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: The Foundation {#aep-foundation}

Adobe Experience Platform sirve como columna vertebral, permitiendo a las marcas centralizar los datos de los clientes y activarlos para experiencias personalizadas:

* **Plataforma de datos**: hub central para recopilar, administrar y estructurar datos de clientes con el fin de garantizar la coherencia en todos los sistemas. [Más información sobre esquemas y conjuntos de datos](../data/get-started-schemas.md)
* **Ingesta de datos (fuentes)**: importe datos de plataformas CRM, sitios web, aplicaciones móviles y almacenamiento en la nube mediante conectores generados previamente. [Explorar orígenes de datos](../data/get-started-sources.md)
* **Perfil del cliente en tiempo real**: crea perfiles unificados combinando datos de varias fuentes (interacciones por correo electrónico, compras en la tienda, comportamiento en la web). [Más información sobre los perfiles](../audience/get-started-profiles.md)
* **Nivel de control**: rige el acceso a los datos, el cumplimiento de la privacidad y la seguridad al tiempo que cumple las regulaciones. [Ver documentación de privacidad](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: Motor de orquestación {#ajo-orchestration}

Adobe Journey Optimizer aplica los datos y las perspectivas de Adobe Experience Platform para ofrecer experiencias de cliente inteligentes y personalizadas:

* **Comprensión del cliente**: los perfiles del cliente en tiempo real habilitan la segmentación en audiencias para la mensajería de destino. [Crear públicos](../audience/about-audiences.md)
* **Contenido y ofertas**: herramientas para crear, administrar y personalizar contenido; lógica en tiempo real para seleccionar la mejor oferta para cada individuo. [Diseñar contenido](../content-management/get-started-content.md) | [Administrar ofertas](../offers/get-started/starting-offer-decisioning.md)
* **Administración de Recorridos y campañas**: automatiza secuencias de interacciones (recorridos) o programa mensajes de destino únicos (campañas). [recorridos de compilación](../building-journeys/journey-gs.md) | [Crear campañas](../campaigns/get-started-with-campaigns.md)
* **Envío (conexiones)**: envía mensajes a través de canales como correo electrónico, SMS, notificaciones push y correo directo; exporta datos a sistemas externos. [Configuración de canales](../configuration/get-started-configuration.md)
* **Medición y análisis**: Rastrea la participación de los clientes y el rendimiento de las campañas con informes para mejorar continuamente. [Ver informes](../reports/campaign-global-report.md)

### El ciclo de optimización continua {#optimization-cycle}

Este ecosistema funciona como un ciclo de optimización continua. Los datos mejoran la comprensión del cliente, que informa el contenido personalizado y las decisiones. Se organizan en recorridos, se entregan en varios canales, se miden para obtener eficacia y se refinan con el tiempo.

![](../assets/do-not-localize/get-started-flow.png)

## Áreas funcionales clave {#functional-areas}

Journey Optimizer incluye siete áreas funcionales clave que funcionan juntas sin problemas:

| Área funcional | Objetivo | Actividades clave |
|-----------------|---------|----------------|
| **Administración de datos** | Organizar datos de clientes | Defina esquemas, cree conjuntos de datos e importe datos de varios sistemas. [Más información](../data/get-started-schemas.md) |
| **Administración de clientes** | Comprenda quiénes son sus clientes | Cree perfiles unificados, resuelva identidades y cree audiencias. [Más información](../audience/get-started-profiles.md) |
| **Administración de contenido** | Creación de mensajes personalizados | Diseñe correos electrónicos, administre recursos, cree plantillas y fragmentos y personalice contenido. [Más información](../content-management/get-started-content.md) |
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

Para los equipos técnicos, este es el diagrama de arquitectura detallado que muestra cómo Journey Optimizer se integra con Adobe Experience Platform. [Navegue por la interfaz](user-interface.md) para explorar estos componentes en la práctica.

![Arquitectura de Adobe Journey Optimizer](assets/ajo-architecture.png)

Hay cuatro aplicaciones creadas de forma nativa en Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics y Adobe Mix Modeler. Journey Optimizer funciona a la perfección con estas aplicaciones, pero también de forma independiente. [Revise las limitaciones y protecciones](guardrails.md) por motivos de implementación.

### Puntos de integración {#integration-points}

Journey Optimizer se integra con Adobe Experience Platform en varios niveles:

* **Capa de datos** - Comparte el mismo perfil de cliente en tiempo real, gráfico de identidad y conjuntos de datos
* **Nivel de servicio**: aprovecha el control, la privacidad y los servicios de consultas de Adobe Experience Platform
* **Nivel de aplicación**: proporciona orquestación de recorrido, administración de decisiones y administración de contenido además de Adobe Experience Platform

Más información sobre [modelos de Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.

## Privacidad y seguridad {#privacy-security}

Las prácticas de privacidad y seguridad de Adobe Experience Cloud se aplican a Adobe Journey Optimizer. Estas medidas garantizan el cumplimiento de las regulaciones de privacidad como el RGPD, lo que le permite ofrecer experiencias personalizadas sin dejar de mantener la confianza de los clientes. [Más información sobre privacidad en Journey Optimizer](../privacy/get-started-privacy.md)
