---
solution: Journey Optimizer
product: journey optimizer
title: Paquetes y funciones de Journey Optimizer
description: Comprenda cómo se empaqueta Adobe Journey Optimizer y qué capacidades están disponibles en función de su oferta base, complementos de canal y complementos de capacidades avanzadas.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: recorrido optimizer, paquete, licencia, campañas, recorridos, canales, toma de decisiones, saliente, móvil, web, modular
hide: true
source-git-commit: d0e43b37ab759fde2794e2bf981e233875ba620a
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 2%

---


# Paquetes y funciones de Adobe Journey Optimizer {#ajo-packages-v2}

[!DNL Adobe Journey Optimizer] usa un modelo de empaquetado modular. Comience con la oferta base que coincida con su caso de uso principal y, a continuación, añada los canales y las funciones avanzadas que necesita.

>[!NOTE]
>
>La disponibilidad del paquete y las capacidades incluidas pueden variar según el acuerdo, los complementos seleccionados y la disponibilidad regional. Póngase en contacto con su representante de Adobe para obtener detalles específicos de su organización.

## Paso 1: Selección de la oferta base {#base-offers}

Hay tres ofertas de base disponibles. Elija el que coincida con la forma en que atrae principalmente a los clientes.

| Oferta básica | Mejor para | Comportamiento principal |
|-----------|---------|--------------|
| **Journey Optimizer - Campañas** | Divulgación por lotes planificada por expertos en marketing | Orquestación programada basada en audiencias. Flujos de trabajo de campaña de uno o varios pasos que utilizan el almacén de datos relacional. |
| **Journey Optimizer - Recorridos** | Participación del cliente en tiempo real | Impulsado por eventos, orquestación 1:1. Admite el procesamiento de recorridos por lotes y streaming. |
| **Journey Optimizer - Campañas y Recorridos** | Clientes que necesitan ambos | Combina orquestación de campaña basada en audiencias y orquestación de recorrido en tiempo real. |

### Campañas vs. Recorridos. ¿Cuál es la diferencia? {#campaigns-vs-journeys}

| | Journey Optimizer - Campañas | JOURNEY OPTIMIZER - RECORRIDOS | Journey Optimizer: Campañas y Recorridos |
|--|:-----------------------------:|:----------------------------:|:----------------------------------------:|
| Orquestación por lotes basada en audiencias | ✓ | Limitado a casos de uso de recorrido | ✓ |
| Organización impulsada por eventos en tiempo real | — | ✓ | ✓ |
| Mensajería transaccional (correo electrónico, push, SMS) | ✓ | ✓ | ✓ |
| Complementos de canal disponibles | ✓ | ✓ | ✓ |
| Complemento de decisiones disponible | ✓ | ✓ | ✓ |

>[!NOTE]
>
>El derecho total del volumen de datos difiere: **Campañas** clientes reciben 15 KB por perfil direccionable; **Recorridos** y **Campañas y Recorridos** clientes reciben 75 KB por perfil direccionable.

## Paso 2: Añadir los canales que necesita {#channel-addons}

Los canales no están agrupados en la oferta base. Seleccione el complemento de canal o el paquete de complementos que se ajuste a su estrategia de participación.

>[!BEGINTABS]

>[!TAB Envío saliente]

Llegue a las audiencias a través de canales de mensajería salientes.

**Incluye:** correo electrónico, notificaciones push, correo directo

**Casos de uso habituales:** correos electrónicos promocionales, alertas push transaccionales y campañas de correo físico

**Superficies compatibles:** bandeja de entrada, pantalla de bloqueo del dispositivo móvil/bandeja de notificaciones, dirección postal

Incluye aspectos básicos de la capacidad de entrega para admitir el calentamiento de IP en nuevas instancias. [Más información sobre la entrega](../reports/deliverability.md)

>[!TAB Mobile]

Capte a los usuarios de la aplicación con experiencias móviles persistentes y en la sesión.

**Incluye:** mensajería en la aplicación, notificaciones push, tarjetas de contenido y canales basados en código para superficies móviles

**Casos de uso habituales:** flujos de incorporación, anuncios de funciones, avances de fidelidad y ofertas en la aplicación en tiempo real

**Superficies compatibles:** pantallas de aplicaciones móviles, bandeja de notificaciones, ranuras de contenido persistente, superficies de aplicaciones personalizadas mediante SDK

>[!TAB Web]

Personalice experiencias web sin implementar código.

**Incluye:** canal web (editor visual y no visual), canales basados en código para superficies web

**Casos de uso habituales:** titulares de páginas de inicio, personalización de páginas de aterrizaje, pruebas A/B y personalización web sin encabezado mediante API

**Superficies compatibles:** páginas de explorador, aplicaciones de una sola página (SPA) y extremos web sin encabezado

>[!TAB Todos los canales]

El complemento **Todos los canales** agrupa los paquetes de envío saliente + Móvil + Web en una sola compra.

Ideal para organizaciones que necesitan una cobertura omnicanal completa en las superficies web, de aplicaciones móviles y de salida.

>[!ENDTABS]

**WhatsApp** está disponible como un complemento independiente para los clientes que necesitan enviar mensajes a través de WhatsApp Business. [Aprende a usar WhatsApp](../whatsapp/get-started-whatsapp.md)

## Paso 3: Adición de funciones avanzadas {#advanced-addons}

### Toma de decisiones {#decisioning-addon}

El complemento **Decisioning** le permite definir, administrar y entregar la mejor oferta, acción o experiencia para cada perfil en tiempo real, en cualquier canal.

**Lo que desbloquea:**
- Selección de ofertas en tiempo real mediante reglas de idoneidad, lógica de clasificación y restricciones
- Modelos de clasificación con tecnología de IA para optimizar el rendimiento de la oferta automáticamente
- Políticas de decisión utilizables en recorridos, campañas y experiencias basadas en código

**Disponible en:** las tres ofertas base, según el contrato de licencia. [Aprenda a utilizar la toma de decisiones](../experience-decisioning/gs-experience-decisioning.md) | [Más información sobre los modelos de IA](../offers/ranking/ai-models.md)

## Comparar de un vistazo {#comparison-matrix}

| Capacidad | Journey Optimizer - Campañas | JOURNEY OPTIMIZER - RECORRIDOS | Journey Optimizer: Campañas y Recorridos | Complemento requerido |
|-----------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|
| Mensajería transaccional (correo electrónico, push, SMS) | ✓ | ✓ | ✓ | — |
| Campañas por lotes | ✓ | — | ✓ | — |
| Campañas organizadas _(correo electrónico, SMS, push, solo correo directo)_ | ✓ | — | ✓ | — |
| Recorridos automatizados | — | ✓ | ✓ | — |
| Déclencheur de eventos en tiempo real | — | ✓ | ✓ | — |
| Correo electrónico | ✓ | ✓ | ✓ | Entrega saliente |
| Notificaciones push | ✓ | ✓ | ✓ | Entrega saliente |
| Correo directo | ✓ | ✓ | ✓ | Entrega saliente |
| SMS/MMS | ✓ | ✓ | ✓ | Entrega saliente |
| Mensajería en la aplicación | ✓ | ✓ | ✓ | Móvil |
| Tarjetas de contenido | ✓ | ✓ | ✓ | Móvil |
| Canal web | ✓ | ✓ | ✓ | Web |
| Experiencias basadas en código | ✓ | ✓ | ✓ | Móvil o web |
| WhatsApp | ✓ | ✓ | ✓ | WhatsApp |
| Toma de decisiones | Depende de la licencia | Depende de la licencia | Depende de la licencia | Toma de decisiones |
| Clasificación con tecnología de IA | Depende de la licencia | Depende de la licencia | Depende de la licencia | Toma de decisiones |

## Preguntas frecuentes {#faq}

+++**¿Cada oferta base incluye cada canal?**

No. [!DNL Adobe Journey Optimizer] utiliza un modelo modular: la oferta base determina la capacidad de orquestación (campañas, Recorridos o ambos) y los complementos de canal determinan qué superficies de mensajería se pueden utilizar. Elija la combinación que se adapte a su caso de uso y presupuesto.

+++

+++**¿Cuál es la diferencia entre campañas y Recorridos?**

**Las campañas** están basadas en audiencias y planificadas por expertos en marketing; usted define una audiencia, crea un mensaje y lo programa o lo déclencheur como un envío por lotes. Son perfectas para flujos de trabajo de alcance promocional, boletines informativos y audiencias de varios pasos.

Los **Recorridos** están impulsados por eventos y en tiempo real; reaccionan al comportamiento individual de los clientes a medida que ocurre y orquestan experiencias de 1:1 en puntos de contacto. Son ideales para flujos de incorporación, secuencias posteriores a la compra y mensajes activados en tiempo real.

**Campañas y Recorridos** le ofrece ambas funciones en una sola licencia.

+++

+++**¿Qué canales son compatibles con las campañas orquestadas?**

Las campañas organizadas (flujos de trabajo de audiencia de varios pasos que usan la función Campaign Orchestration) solo admiten **correo electrónico, SMS, notificaciones push y correo directo**. Los canales web, en la aplicación, basados en código y de tarjeta de contenido no son compatibles con los flujos de trabajo de campañas organizadas.

+++

+++**¿Se incluye Decisioning en cada configuración?**

No. Decisioning es un complemento de capacidad avanzada diferenciado y no se incluye en ninguna oferta base de forma predeterminada. Póngase en contacto con su representante de Adobe para agregar Decisioning a la configuración.

+++

+++**He oído hablar de Select, Prime o Ultimate. ¿Sigue siendo el modelo de empaquetado actual?**

[!DNL Adobe Journey Optimizer] ahora se ofrece a través de un modelo de empaque modular construido alrededor de ofertas base (Campañas, Recorridos, Campañas y Recorridos) y complementos. Si es un cliente existente que utiliza la terminología Select, Prime o Ultimate y tiene preguntas sobre sus derechos actuales, póngase en contacto con su representante de Adobe.

+++
