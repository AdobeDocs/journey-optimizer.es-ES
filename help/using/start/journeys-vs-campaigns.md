---
solution: Journey Optimizer
product: journey optimizer
title: 'Recorridos frente a campañas: elija el enfoque adecuado'
description: Compare Recorridos, campañas de acción y campañas activadas por API para elegir el enfoque adecuado para sus necesidades de marketing en Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: recorrido, campaña, comparación, elegir, decisión, flujo de trabajo, tiempo real, lote, orquestación, varios pasos, programado, activado por API, impulsado por evento
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
TQID: https://experienceleague.adobe.com/RWLVSULVO0idnCs5OVQR1yVvNv1G0JwP3y-3sNXQg50
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: addf009e-030a-4310-8534-776a3e62ed48id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: d4be496be65eef2c9cab727804f762350957223a
workflow-type: tm+mt
source-wordcount: 2483
ht-degree: 2%

---

# Recorridos frente a campañas: elija el enfoque adecuado {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**En esta página:** Compare recorridos con campañas activadas por acciones y API para que pueda elegir el enfoque correcto para cada caso de uso de marketing en Adobe Journey Optimizer. Para campañas orquestadas, consulte [Introducción a campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] ofrece dos maneras principales de llegar a sus clientes y motivarlos: **Recorridos** y **Campañas**. Los recorridos están diseñados para una orquestación en tiempo real de varios pasos dirigida por el comportamiento del cliente, mientras que las campañas son más adecuadas para difusiones únicas o programadas para una audiencia definida, o para activaciones de canal entrantes al límite para una personalización de baja latencia. Una vez que haya decidido una campaña, puede elegir el tipo de campaña que mejor se adapte a su caso de uso.

Esta guía le ayuda a elegir entre Recorridos, campañas de acción y campañas activadas por API en función del estilo de ejecución, las necesidades de datos y los casos de uso, con una comparación rápida, un árbol de decisiones y ejemplos concretos.

>[!NOTE]
>
>**Las campañas orquestadas** tienen características arquitectónicas distintas (ejecución por lotes en el concentrador, datos relacionales de varias entidades) que requieren orientación específica. No se incluyen en las tablas de comparación siguientes para evitar una simplificación excesiva. [Más información sobre las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md)

## Resumen de comparación rápida {#quick-overview}

| Enfoque | Mejor para | Estilo de ejecución |
|----------|----------|-----------------|
| **Recorridos** | Experiencias de cliente en tiempo real de varios pasos con lógica condicional | 1:1 orquestación: cada perfil a su propio ritmo |
| **Campañas de acción** | Activaciones programadas o recurrentes para audiencias | Ejecución por lotes: la audiencia se procesa junta en el momento del envío |
| **Campañas activadas por API** | Mensajes transaccionales o impulsados por eventos de sistemas externos | Ejecución bajo demanda: activada por una llamada de API con carga útil |

>[!TIP]
>
>**Regla general rápida:** ¿Necesita que cada cliente se mueva a su propio ritmo con lógica en tiempo real? Usar **Recorridos**. ¿Desea enviar un mensaje a una audiencia según una programación? Usar **campañas de acción**. ¿Se activa un solo mensaje desde un sistema externo a través de una API? Use **campañas activadas por API** o un **recorrido de evento unitario** si necesita orquestación de varios pasos después del evento enviado por API. ¿Necesita personalización entrante y basada en Edge? Usar **campañas de acción**.

## Comparación detallada {#detailed-comparison}

Utilice esta tabla completa para comprender las diferencias clave:

| Función | Recorridos | Campañas de acción | Campañas activadas por API |
|---------|----------|------------------|------------------------|
| **Propósito principal** | Organización de varios pasos 1:1 con contexto de cliente en tiempo real | Envío de mensajes único o recurrente a las audiencias | Mensajes transaccionales o impulsados por eventos iniciados por sistemas externos |
| **Tipo de lienzo** | Lienzo 1:1: cada perfil viaja a su propio ritmo | Sin lienzo: ejecución de una sola acción | Sin lienzo: ejecución de una sola acción |
| **Flujo de ejecución** | Acciones secuenciales, el perfil mantiene el estado durante todo el recorrido | Ejecución simultánea para toda la audiencia | Ejecución inmediata por llamada de API |
| **Mecanismo de entrada** | Eventos, audiencias, cualificaciones y eventos empresariales | Activación y programación manuales | Llamada de API desde un sistema externo |
| **Modelo de datos** | Perfil en tiempo real + datos de evento | Datos de perfil de audiencias de Experience Platform | Datos de carga útil de API con búsqueda de perfil opcional |
| **Segmentación** | Audiencias creadas previamente + condiciones en tiempo real | Audiencias creadas previamente desde Experience Platform | Segmentación impulsada por carga útil (sin audiencia programada) |
| **Procesamiento de perfil** | Individual, en tiempo real (a medida que ocurren los eventos) | Lote, todo a la vez | Por llamada de API, impulsada por carga útil |
| **Personalización** | Datos contextuales en tiempo real + atributos de perfil | Atributos de perfil | Datos de carga útil + atributos de perfil opcionales |
| **Complejidad** | Varios pasos con ramificación, tiempos de espera y condiciones | Una sola acción o flujo de trabajo simple | Acción única con asignación de carga útil |
| **Mejor para** | Recorridos del ciclo vital del cliente, incorporación, abandono del carro | Campañas promocionales, boletines informativos y anuncios | Confirmaciones de pedidos, alertas de envío y restablecimientos de contraseña |
| **Tiempo** | Continuo, siempre activo una vez publicado | Fechas de inicio y finalización programadas | Bajo demanda, impulsado por evento mediante API |
| **Administración de estado** | Mantiene el estado del cliente para acciones en tiempo real | Ejecución sin estado | Ejecución sin estado por llamada |
| **Usar cuando** | Se necesitan varios puntos de contacto con la lógica de decisión en tiempo real | Mensaje sencillo a una audiencia en un momento específico | El sistema externo debe almacenar un mensaje en déclencheur inmediatamente |
| **Funciones únicas** | Reacciones en tiempo real, actividades de espera, ritmo basado en perfiles | Programación, segmentación de audiencia, control de velocidad | Asignación de carga útil de API, activación de sistema a sistema |

## Guía de decisión {#decision-guide}

Siga este árbol de decisión para elegir el enfoque correcto. Muchas marcas utilizan más de un tipo; elija el que mejor se adapte a cada caso de uso.

### Paso 1: ¿Cuál es su requisito de ejecución?

**Respuestas individuales en tiempo real al comportamiento de los clientes?**
→ **Usar Recorridos**
* Los perfiles deben moverse a su propio ritmo
* Lógica condicional basada en el comportamiento
* El contexto en tiempo real es fundamental

**Envío de mensaje simple a una audiencia a una hora programada?**
→ **Usar campañas de acción**
* Todos los perfiles reciben el mensaje simultáneamente
* Envíos programados o recurrentes
* No se necesita una lógica compleja de varios pasos

**Mensaje inmediato activado por un sistema externo?**
→ **Usar campañas activadas por API** (mensaje único) **o un recorrido de evento unitario** (orquestación de varios pasos)
* Se activa bajo demanda mediante una llamada API: las campañas envían un mensaje; los recorridos unitarios consumen el evento mediante [ingesta de Experience Platform](../event/additional-steps-to-send-events-to-journey.md) y ejecutan un flujo de recorrido completo
* Personalización impulsada por carga útil
* Elija campañas cuando no se necesite una lógica de varios pasos

**Flujo de trabajo por lotes complejo con segmentación avanzada, datos de varias entidades o recuentos exactos de preenvío?**
→ **Usar campañas orquestadas**; consulte [Introducción a las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md) para obtener instrucciones detalladas.

>[!NOTE]
>
>* **Composición de audiencia ad hoc**: las campañas orquestadas le permiten definir su audiencia de destino directamente en el lienzo de la campaña utilizando el generador de reglas integrado, sin necesidad de crear previamente y evaluar una audiencia de Adobe Experience Platform primero. [Aprenda a crear su primera regla](../orchestrated/build-query.md)
>* **Datos federados**: use la Composición de audiencia federada para consultar el almacén de datos empresarial y crear o enriquecer audiencias sin importar datos confidenciales a Adobe Experience Platform. [Más información acerca de la composición de audiencias federadas](../audience/federated-audience-composition.md)

### Paso 2: Validar la elección

| Su necesidad | Enfoque recomendado | Por qué |
|-----------|---------------------|-----|
| Bienvenido a nuevos clientes con incorporación de varios pasos | Recorridos | Entrada en tiempo real, varios puntos de contacto, rutas condicionales |
| Enviar newsletter mensual a los suscriptores | Campañas de acción | Mensaje programado simple a la audiencia |
| Abandono del carro de compras con secuencia de recordatorio | Recorridos | Déclencheur en tiempo real, tiempos de espera, seguimiento condicional |
| Anuncio promocional para todos los clientes | Campañas de acción | Mensaje único, envío inmediato |
| Volver a atraer a usuarios inactivos según su comportamiento | Recorridos | Activado por calificación de audiencia, ruta personalizada |
| Venta Flash activada por evento empresarial | Recorridos (evento empresarial) | Déclencheur en tiempo real que afectan a varios clientes |
| Mensaje transaccional activado por API (envío único) | Campañas activadas por API | Déclencheur del sistema externo, entrega inmediata con una sola toma |
| Flujo de varios pasos activado por API | Recorridos (evento unitario) | El sistema externo envía un evento unitario a través de la API; el recorrido organiza los pasos de seguimiento |
| Flujo de trabajo por lotes complejo con datos de varias entidades | Campañas orquestadas | Ver [Introducción a campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md) |

## Distinciones clave explicadas {#key-distinctions}

### Recorridos: 1:1 orquestación en tiempo real

**Qué lo hace único:**
* Cada perfil mantiene el estado y el contexto individuales
* Los perfiles entran y progresan a su propio ritmo
* Toma de decisiones en tiempo real basada en el comportamiento y los eventos
* Las actividades de espera crean intervalos personalizados
* La bifurcación condicional crea rutas únicas por perfil
* Escucha activa integrada: la inacción durante un periodo definido también puede almacenar en déclencheur el siguiente paso, no solo los eventos explícitos. [Más información sobre las actividades de espera](../building-journeys/wait-activity.md)
* Límite de frecuencia: controla la frecuencia con la que un cliente puede introducir o recibir mensajes de un recorrido. [Más información sobre el límite de recorrido](../conflict-prioritization/journey-capping.md)
* Audiencia dividida por porcentaje: divida los perfiles en grupos aleatorios basados en porcentajes para ejecutar experimentos A/B en rutas de recorrido. [Más información sobre la división porcentual](../building-journeys/condition-activity.md)
* Modo de prueba: valide la lógica del recorrido y la entrega de mensajes con perfiles de prueba antes de publicar en directo. [Más información sobre el modo de prueba](../building-journeys/testing-the-journey.md)

**Flujo de ejemplo:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Cada cliente experimenta su propia cronología de recorridos en función de sus acciones.

[Más información sobre Recorrido](../building-journeys/journey.md)

### Campañas: Envío por lotes simple o activado

**Qué lo hace único:**
* Todos los perfiles procesados de forma idéntica y simultánea
* Ejecución sin estado: sin contexto
* Programación simple o activación de API
* Idóneo para comunicaciones broadcast
* Envío entrante de varias superficies: añada hasta 10 acciones de canal entrante (experiencia basada en código, aplicación, tarjeta de contenido, web) en una sola campaña, utilizando reglas de segmentación para crear variantes de mensaje basadas en la pertenencia a audiencias o atributos de perfil. [Más información](../campaigns/campaign-action.md#multi-action)

**Flujo de ejemplo:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Todos reciben el mismo mensaje al mismo tiempo.

**Tipos:**
* **Campañas de acción**: Envío programado a audiencias (único o recurrente)
* **Campañas activadas por API**: envío a petición activado por una llamada de API con datos de carga útil

[Más información sobre las Campañas](../campaigns/get-started-with-campaigns.md)

## Ejemplos de casos de uso {#use-cases}

### Casos de uso de recorrido

* **Recuperación de abandono del carro de compras**: desencadenada por el evento de adición al carro de compras, esperar al cierre de compra o enviar recordatorios en caso de que no se realice la compra
* **Incorporación del cliente**: serie de bienvenida de varios pasos con contenido personalizado basado en datos de perfil
* **Actualización del nivel de fidelización**: Se activa cuando el cliente alcanza un nuevo nivel y envía felicitaciones y beneficios.
* **Campañas de cumpleaños**: la entrada se basa en la fecha de nacimiento y en ofertas personalizadas.
* **Nuevo compromiso**: activado por calificación de audiencia (inactividad), alcance progresivo

### Casos de uso de Campaign (activados por la acción y la API)

**Campañas de acción:**
* **Boletines mensuales**: Envío por lotes programado al segmento del suscriptor
* **Anuncios promocionales**: ofertas con distinción de tiempo para audiencias de destino
* **Lanzamientos de productos**: anuncio coordinado para todos los clientes
* **Saludos de temporada**: Mensajes de vacaciones en fechas específicas

**Campañas activadas por API:**
* **Confirmaciones de pedidos**: Activado por el sistema de comercio electrónico después de la compra
* **Notificaciones de envío**: activado por el sistema logístico
* **Alertas de cuenta**: activadas por el sistema de detección de fraude
* **Restablecimiento de contraseña**: activado por la acción del usuario en la aplicación

## Disponibilidad de funciones {#feature-availability}

### Canales

| Canal | Recorridos | Campañas de acción | Campañas activadas por API |
|---------|:--------:|:----------------:|:-----------------------:|
| Correo electrónico | ✅ | ✅ | ✅ |
| Push | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ |
| in-app | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Basado en código | ✅ | ✅ | ❌ |
| Tarjetas de contenido | ✅ | ✅ | ❌ |
| Correo directo | ✅ | ✅ | ❌ |
| LINE | ✅ | ✅ | ✅ |
| WhatsApp | ✅ | ✅ | ✅ |

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
| Activación de API | ✅ (solo evento unitario: evento enviado mediante API) | ❌ | ✅ |
| Datos de varias entidades | ❌ | ❌ | ❌ |
| Recuentos exactos previos al envío | ❌ | ❌ | ❌ |
| Segmentación bajo demanda | ❌ | ❌ | ❌ |
| Optimización del tiempo de envío | ✅ | ❌ | ❌ |
| Prueba A/B | ✅ | ✅ | ❌ |
| Flujos de trabajo de aprobación | ✅ | ✅ | ✅ |

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

Las campañas de acción suelen ser las más sencillas (un solo punto de contacto o participación entregada a una audiencia), seguidas de campañas activadas por API y, a continuación, Recorridos (más complejas con la lógica de varios pasos).

+++

+++ ¿Qué escala es mejor para grandes audiencias?

Los tres se pueden escalar bien; la elección correcta depende de su patrón:

* **Leer Recorridos de audiencias** y **Campañas de acción** están optimizadas para audiencias de lote grande (un mensaje o flujo a muchos perfiles a la vez).
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
