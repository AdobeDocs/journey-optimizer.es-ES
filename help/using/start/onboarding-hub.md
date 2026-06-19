---
solution: Journey Optimizer
product: journey optimizer
title: Guía del proyecto de incorporación | ADOBE JOURNEY OPTIMIZER
description: Planifique y administre un proyecto de incorporación de Adobe Journey Optimizer con funciones de administrador, datos, desarrollador y experto en marketing.
feature: Get Started
topic: Content Management
role: Admin
level: Intermediate
keywords: recorrido optimizer, incorporación, proyecto de incorporación, despliegue, plan de implementación, administrador, csm, socio de implementación, lista de comprobación por fases
source-git-commit: 6a653e1dbb00f68ff689ea3e0dc0b15abda1e21e
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# Guía del proyecto de incorporación {#onboarding-hub}

>[!BEGINSHADEBOX]

**En esta página:** Planifique y coordine un despliegue completo de Adobe Journey Optimizer con una lista de comprobación por fases que incluya las funciones de administrador, ingeniero de datos, desarrollador y experto en marketing.

>[!ENDSHADEBOX]

Esta página es para **administradores de sistemas y socios de implementación** que coordinan un despliegue completo de Journey Optimizer. Proporciona una lista de comprobación por fases que abarca todas las funciones, con vínculos a las guías detalladas específicas de funciones.

>[!NOTE]
>
>Si eres una persona que comienza con una función específica, ve a [Introducción a Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) en su lugar.

## Fase 1: Configuración del entorno (administrador) {#phase-1}

Complete primero estas tareas básicas para que las demás funciones puedan comenzar a trabajar:

* [ ] aprovisionar zonas protegidas (desarrollo, ensayo, producción)
* [ ]: configurar roles y permisos de usuario en Adobe Admin Console
* [ ] Configurar perfiles de producto y control de acceso de nivel de objeto
* [ ] Delegar subdominios y configurar grupos de IP
* [ ] Configurar configuraciones de canal (correo electrónico, SMS, push, web, en la aplicación, correo directo)
* [ ]: configurar listas de supresión y directivas de consentimiento

➡️ Ver detalles completos: [Introducción para administradores](path/administrator.md)

## Fase 2: Fundamento de datos (ingeniero de datos) {#phase-2}

Cree la capa de datos que alimenta los perfiles, las audiencias y los déclencheur de recorrido:

* [ ] Definir áreas de nombres de identidad
* [ ]: crear esquemas XDM (perfil, eventos de experiencia, relacionales)
* [ ]: configurar y habilitar conjuntos de datos para el perfil del cliente en tiempo real
* [ ] Configurar la ingesta de datos (por lotes y streaming)
* [ ] Crear atributos calculados
* [ ] Configuración de eventos de recorrido y fuentes de datos

➡️ Ver detalles completos: [Introducción para ingenieros de datos](path/data-engineer.md)

## Fase 3: Integraciones técnicas (desarrollador) {#phase-3}

Conecte las aplicaciones para que los recorridos puedan ejecutarse en los datos en tiempo real:

* [ ]: integrar Mobile SDK (iOS/Android) con la configuración push
* [ ] Implementar Web SDK para experiencias web y Web Push
* [ ] Implementar el envío de eventos desde aplicaciones
* [ ] Generar extremos de acción personalizados para integraciones de sistema externas
* [ ] Validar mediante Adobe Experience Platform Assurance

➡️ Ver detalles completos: [Introducción para desarrolladores](path/developer.md)

## Fase 4: Primeras experiencias (experto en marketing) {#phase-4}

Ponga la base a trabajar lanzando sus primeros recorridos y campañas:

* [ ]: generar primera audiencia (definición de segmento o carga CSV)
* [ ]: crear un recorrido de prueba con acción de correo electrónico
* [ ] Configurar plantillas y fragmentos de contenido
* [ ]: publicar y supervisar una campaña
* [ ] Revisar informes en vivo

➡️ Ver detalles completos: [Introducción para especialistas en marketing](path/marketer.md)

## Lista de comprobación de incorporación (imprimible) {#checklist}

| Fase | Propietario | Estado |
|-------|-------|--------|
| Configuración del entorno | Administrador | |
| Base de datos | Ingeniero de datos | |
| Integraciones técnicas | Desarrollador | |
| Primeras experiencias | Experto en marketing | |

## Recursos relacionados {#related-resources}

* [Funciones y responsabilidades](quick-start.md): cómo funcionan juntas las cuatro funciones y el orden de implementación recomendado.
* [Tutoriales de Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: vídeos paso a paso y tutoriales guiados para cada función.
* [Introducción a la administración de datos](../data/gs-data.md): Cómo se incorporan, unifican y activan los datos.
