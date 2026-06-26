---
solution: Journey Optimizer
product: journey optimizer
title: 'Recorridos frente a campañas: elija el enfoque adecuado'
description: Compare Recorridos, campañas de acción y campañas activadas por API para elegir el enfoque adecuado para sus necesidades de marketing en Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
hide: true
keywords: recorrido, campaña, comparación, elegir, decisión, flujo de trabajo, tiempo real, lote, orquestación, varios pasos, programado, activado por API, impulsado por evento
source-git-commit: ab31811861ccaab22fc787ce3c687204637fbd46
workflow-type: tm+mt
source-wordcount: '1965'
ht-degree: 2%

---


# Recorridos frente a campañas: elija el enfoque adecuado {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**En esta página:** Compare recorridos con campañas activadas por acciones y API para que pueda elegir el enfoque correcto para cada caso de uso de marketing en Adobe Journey Optimizer. Para campañas orquestadas, consulte [Introducción a campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] ofrece dos maneras principales de llegar a sus clientes y motivarlos: **Recorridos** y **Campañas**. Los recorridos están diseñados para una orquestación en tiempo real de varios pasos dirigida por el comportamiento del cliente, mientras que las campañas son más adecuadas para difusiones únicas o programadas para una audiencia definida, o para activaciones de canal entrantes al límite para una personalización de baja latencia.

>[!NOTE]
>
>**Las campañas orquestadas** tienen características arquitectónicas distintas (ejecución por lotes en el concentrador, datos relacionales de varias entidades) que requieren orientación específica. No se incluyen en la comparación siguiente para evitar una simplificación excesiva. [Más información sobre las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md)

## ¿Qué enfoque debe utilizar? {#decision-guide}

La respuesta normalmente se reduce a una pregunta: *¿qué debe suceder y para quién?*

Si necesita que **cada cliente se mueva a su propio ritmo** — recibiendo mensajes según lo que haga, esperando y luego reaccionando a su siguiente acción — use un **Recorrido**. Los recorridos realizan un seguimiento de dónde está cada perfil y qué han hecho, lo que los hace ideales para experiencias de varios pasos, como secuencias de incorporación, flujos de abandono del carro de compras o programas de lealtad.

Si quieres **enviar un mensaje a un grupo de personas en una programación** (una newsletter, un anuncio de producto, una promoción de temporada), usa una **campaña de acción**. Todos los miembros de la audiencia reciben el mensaje al mismo tiempo, sin necesidad de lógica por perfil. Las campañas de acción también admiten activaciones del canal entrante (en la aplicación, web, tarjetas de contenido, basadas en código) para la personalización de Edge con baja latencia.

Si un **sistema externo necesita almacenar en déclencheur un mensaje inmediatamente** (una confirmación de pedido de su plataforma de comercio electrónico, una alerta de envío de su sistema logístico, un restablecimiento de contraseña de su aplicación), use una **campaña activada por API** para un único mensaje a petición o un **recorrido de evento unitario** si ese déclencheur necesita iniciar un flujo de varios pasos.

Si necesita un **flujo de trabajo por lotes complejo con segmentación avanzada, datos de varias entidades o recuentos exactos de preenvío**, consulte [Introducción a las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md).

>[!TIP]
>
>**¿No está seguro de por dónde empezar?** La mayoría de los equipos utilizan Recorridos para experiencias de comportamiento impulsadas por eventos y campañas de acción para comunicaciones programadas. Estos dos abarcan la mayoría de los casos de uso.

## Cómo se comparan {#quick-overview}

| Enfoque | Mejor para | Estilo de ejecución |
|----------|----------|-----------------|
| **Recorridos** | Experiencias de cliente en tiempo real de varios pasos con lógica condicional | 1:1 orquestación: cada perfil a su propio ritmo |
| **Campañas de acción** | Activaciones programadas o recurrentes para audiencias | Ejecución por lotes: audiencia procesada conjuntamente en el momento del envío |
| **Campañas activadas por API** | Mensajes transaccionales o impulsados por eventos de sistemas externos | Ejecución bajo demanda: activada por una llamada de API con carga útil |

## Funcionamiento de cada enfoque {#key-distinctions}

### Recorridos: 1:1 orquestación en tiempo real

Un Recorrido es un lienzo en el que cada perfil recorre su propio camino a su propio ritmo. AJO realiza un seguimiento de la posición de cada persona en el flujo y reacciona en tiempo real ante su comportamiento, ya sea mediante una acción, un periodo de inactividad o un cambio en el perfil.

Las funciones clave incluyen actividades de espera que crean un tiempo personalizado entre pasos, ramificación condicional que enruta perfiles a diferentes rutas, límite de frecuencia para controlar la frecuencia con la que un cliente recibe mensajes y modo de prueba para validar la lógica antes de lanzarse. Los recorridos también pueden dividir perfiles en grupos basados en porcentajes para experimentos A/B en rutas.

Un recorrido de abandono del carro de compras ilustra claramente la diferencia:

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Cada cliente experimenta una cronología diferente en función de lo que realmente hace. [Más información sobre los Recorridos](../building-journeys/journey.md)

### Campañas: Envío por lotes o activado

Una campaña ejecuta una sola acción, ya sea para todos los miembros de una audiencia a la vez o bajo demanda cuando un sistema externo la llama. No hay lienzo ni estado por perfil: todos los perfiles se procesan de forma idéntica.

**Las campañas de acción** se entregan a una audiencia programada (única o recurrente) y también admiten la entrega de entrada de varias superficies, con un máximo de 10 acciones de canal de entrada por campaña, con reglas de segmentación para crear variantes de mensaje basadas en atributos de perfil o pertenencia a audiencias.

**Las campañas activadas por API** se activan inmediatamente cuando un sistema externo llama a la API y la personalización de mensajes se basa en los datos de carga útil enviados en esa llamada.

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

[Más información sobre las Campañas](../campaigns/get-started-with-campaigns.md)

## Ejemplos de casos de uso {#use-cases}

| Ejemplo de uso | Enfoque recomendado | Por qué |
|----------|---------------------|-----|
| Bienvenido a nuevos clientes con incorporación de varios pasos | Recorridos | Entrada en tiempo real, varios puntos de contacto, rutas condicionales |
| Abandono del carro de compras con secuencia de recordatorio | Recorridos | Déclencheur en tiempo real, tiempos de espera, seguimiento condicional |
| Volver a atraer a usuarios inactivos según su comportamiento | Recorridos | Activado por calificación de audiencia, ruta personalizada |
| Venta Flash activada por un evento empresarial | Recorridos (evento empresarial) | Déclencheur en tiempo real que afectan a varios clientes |
| Newsletter mensual para suscriptores | Campañas de acción | Mensaje programado para la audiencia |
| Anuncio promocional para todos los clientes | Campañas de acción | Mensaje único, envío inmediato |
| Confirmación de pedido o alerta de envío | Campañas activadas por API | Déclencheur del sistema externo, entrega inmediata con una sola toma |
| Flujo de varios pasos activado por API | Recorridos (evento unitario) | El sistema externo envía eventos mediante API; el recorrido organiza pasos de seguimiento |
| Flujo de trabajo por lotes complejo con datos de varias entidades | Campañas orquestadas | Ver [Introducción a campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md) |

## Disponibilidad de funciones {#feature-availability}

### Canales

Los tres enfoques admiten el conjunto completo de canales salientes de AJO: correo electrónico, push, SMS, LINE y WhatsApp. La tabla siguiente muestra las diferencias entre los canales entrantes y digitales.

| Canal | Recorridos | Campañas de acción | Campañas activadas por API |
|---------|:--------:|:----------------:|:-----------------------:|
| in-app | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Basado en código | ✅ | ✅ | ❌ |
| Tarjetas de contenido | ✅ | ✅ | ❌ |
| Correo directo | ✅ | ✅ | ❌ |

>[!NOTE]
>
>Para la disponibilidad del canal de campañas orquestadas, consulte [Canales en recorridos y campañas](../channels/gs-channels.md#channels).

### Funciones avanzadas

| Capacidad | Recorridos | Campañas de acción | Campañas activadas por API |
|-----------|:--------:|:----------------:|:-----------------------:|
| Flujos de trabajo de varios pasos | ✅ | ❌ | ❌ |
| Déclencheur en tiempo real | ✅ | ❌ | ✅ |
| Actividades de espera | ✅ | ❌ | ❌ |
| Ramificación condicional | ✅ | ❌ | ❌ |
| Ejecución programada | ✅ | ✅ | ✅ |
| Activación de API | ✅ (solo evento unitario) | ❌ | ✅ |
| Optimización del tiempo de envío | ✅ | ❌ | ❌ |
| Prueba A/B | ✅ | ✅ | ❌ |
| Flujos de trabajo de aprobación | ✅ | ✅ | ✅ |
| Datos de varias entidades | ❌ | ❌ | ❌ |
| Recuentos exactos previos al envío | ❌ | ❌ | ❌ |

>[!NOTE]
>
>Para obtener detalles de la capacidad de las campañas orquestadas, incluidos los experimentos de contenido, la activación de API por lotes y la segmentación de varias entidades, consulte [Introducción a las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md).

## Preguntas frecuentes {#common-questions}

+++ ¿Puedo combinar recorridos y campañas en mi estrategia de marketing?

Sí. Muchas organizaciones utilizan todos los enfoques para diferentes escenarios:

* **Recorridos** para participación en tiempo real y de comportamiento
* **Campañas de acción** para comunicaciones programadas o activaciones entrantes
* **Campañas activadas por API** para mensajes transaccionales
* **Campañas orquestadas** para campañas por lotes complejas que requieren gran cantidad de datos; consulte [Introducción a las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md)

Utilice la herramienta adecuada para cada caso de uso en lugar de forzar un enfoque para todo.

+++

+++ ¿Puedo convertir una campaña en un recorrido o viceversa?

No, debe reconstruir la experiencia en el formato adecuado. Sin embargo, puede reutilizar el contenido, las audiencias y los conceptos lógicos.

+++

+++ ¿Qué enfoque es más fácil de crear?

Las campañas de acción suelen ser las más sencillas (un solo punto de contacto entregado a una audiencia), seguidas de campañas activadas por API y, a continuación, de Recorridos, que requieren más trabajo de diseño debido a la lógica de varios pasos.

+++

+++ ¿Qué escala es mejor para grandes audiencias?

Los tres se pueden escalar bien; la elección correcta depende de su patrón:

* **Leer Recorridos de audiencias** y **Campañas de acción** están optimizadas para audiencias de lotes grandes.
* **Recorridos unitarios (basados en eventos)** procesan los perfiles individualmente a medida que se producen eventos, por lo que la escala depende del volumen y el rendimiento del evento.

Para la segmentación compleja con conjuntos de datos grandes y datos de varias entidades, consulte [Campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md).

+++

+++ ¿Puedo usar la misma audiencia en recorridos y campañas?

Sí. Las audiencias creadas en [!DNL Adobe Experience Platform] se pueden usar en Recorridos, campañas de acción y campañas organizadas. Las campañas activadas por API son impulsadas por carga útil y no utilizan audiencias generadas previamente del mismo modo.

+++

## Próximos pasos {#next-steps}

¿Listo para comenzar a crear? Explore la documentación detallada del enfoque elegido:

* **[Introducción a Recorrido](../building-journeys/journey.md)**: tipos de Recorrido, diseñador y flujo de trabajo
* **[Introducción a campañas](../campaigns/get-started-with-campaigns.md)**: campañas activadas por acciones y API
* **[Introducción a las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md)**: flujos de trabajo en lienzo por lotes con datos de varias entidades (instrucciones independientes)

>[!MORELIKETHIS]
>
>* [Comparación de tipos de Recorrido](../building-journeys/journey.md#journey-types-comparison)
>* [Comparación de tipos de campaña](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [PREGUNTAS FRECUENTES SOBRE EL Recorrido](../building-journeys/journey-faq.md)
>* [Preguntas frecuentes sobre campañas orquestadas](../orchestrated/orchestrated-campaigns-faq.md)

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Elija entre Recorridos, campañas de acción y campañas activadas por API en función de si necesita orquestación 1:1 en tiempo real, entrega por lotes programada o entrante o ejecución activada por API a petición.

**Intenciones:**
* Comprenda las diferencias clave entre Recorridos, campañas de acción y campañas activadas por API
* Seleccione el método adecuado para un caso de uso de marketing determinado mediante la guía de decisión y las tablas de comparación
* Comprender cuándo las campañas de acción admiten activaciones de canal entrante frente a difusiones salientes
* Saber cuándo escalar a campañas orquestadas (composición ad hoc, datos federados, varias entidades)
* Combinar varios enfoques de forma eficaz en una estrategia de marketing

**Glosario:**
* **Recorrido**: Flujo de orquestación en tiempo real de varios pasos en el que cada perfil progresa a su propio ritmo en función del comportamiento y los eventos. *(específico del producto)*
* **Campaña de acción**: Una campaña que entrega activaciones programadas o recurrentes a audiencias: activaciones de canal entrante o difusión saliente al perímetro de para una personalización de baja latencia. *(específico del producto)*
* **Campaña activada por API**: Una campaña iniciada por un sistema externo a través de una llamada de API, que entrega un único mensaje bajo demanda con personalización controlada por carga útil. *(específico del producto)*
* **Campaña orquestada**: una campaña por lotes del lado del concentrador que admite datos relacionales de varias entidades, composición de audiencias ad hoc y fuentes de datos federadas; no incluida en las tablas de comparación de esta página. *(específico del producto)*
* **recorrido de eventos unitarios**: un recorrido activado por una única acción de perfil en tiempo real; úselo cuando se necesite orquestación de varios pasos después de un evento enviado por API. *(específico del producto)*
* **Activación del canal entrante**: entrega de experiencias personalizadas al perímetro (experiencia basada en código, aplicación, tarjeta de contenido, web) para una representación de baja latencia, compatible con campañas de acción. *(específico del producto)*

**Protecciones:**
* Hasta 10 acciones de canal entrante por campaña de acción (límite estricto): se aplica solo a los canales entrantes: experiencia basada en código, aplicación, tarjeta de contenido, web
* Las campañas orquestadas se excluyen de las tablas de comparación de esta página para evitar una simplificación excesiva; consulte la documentación de campañas orquestadas dedicadas para obtener información de arquitectura

**Terminología:**
* Nombre canónico: Campañas de acción. Variantes: &quot;campañas programadas&quot;, &quot;campañas de difusión&quot;
* Nombre canónico: campañas activadas por API. Variantes: &quot;campañas transaccionales&quot;, &quot;campañas impulsadas por eventos&quot;.
* No confunda: &quot;Campañas de acción&quot; (envío programado/entrante a audiencias) ≠ &quot;campañas activadas por API&quot; (bajo demanda, impulsadas por carga útil, sin audiencia generada previamente) ≠ &quot;Campañas orquestadas&quot; (lote del lado del concentrador con datos relacionales)
* No confunda: &quot;recorrido de evento unitario&quot; (activado por la acción en tiempo real de un perfil) ≠ &quot;recorrido de evento empresarial&quot; (activado por un evento que no es de perfil que afecta a varias personas a través de un paso interno de Leer audiencia)
* Sinónimos: &quot;activación de canal entrante&quot; = &quot;acción de canal entrante&quot; (se utiliza de forma intercambiable en esta página para experiencias entregadas por Edge en campañas de acción)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Cuándo debo usar un Recorrido en lugar de una campaña de acción?** : utilice Recorridos cuando los clientes necesiten moverse a su propio ritmo con lógica condicional en tiempo real en varios puntos de contacto; utilice campañas de acción para envíos programados o entrantes a una audiencia predefinida.
* **Q: ¿Pueden las campañas de acción entregar a los canales entrantes?** — Sí. Las campañas de acción admiten la activación del canal entrante (experiencia basada en código, aplicación, tarjeta de contenido, web) hasta el perímetro de para la personalización con baja latencia, con hasta 10 acciones entrantes por campaña y reglas de segmentación para variantes de mensaje.
* **Q: ¿Qué distingue a las campañas orquestadas de las campañas de acción?** — Las campañas organizadas ejecutan la ejecución por lotes en el concentrador con datos relacionales de varias entidades, recuentos exactos de preenvío, composición de audiencias ad hoc y compatibilidad con datos federados. Las campañas de acción son envíos sin estado de ejecución única a audiencias de Experience Platform.
* **Q: ¿Cuándo debo usar una campaña desencadenada por API en lugar de un recorrido de evento unitario?** — Utilice una campaña activada por API cuando un sistema externo necesite almacenar en déclencheur un solo mensaje inmediatamente con datos de carga útil; utilice un recorrido de evento unitario cuando sea necesaria la orquestación de varios pasos después del evento enviado por API.
* **Q: ¿Puedo combinar Recorridos y campañas en la misma estrategia de marketing?** — Sí. Utilice Recorridos para la participación en tiempo real basada en el comportamiento, campañas de acción para difusiones programadas o activaciones entrantes, campañas activadas por API para mensajes transaccionales y campañas orquestadas para flujos de trabajo por lotes complejos.

+++
<!-- ai-accordion-version: 1 | source-hash: 873097f5 -->
