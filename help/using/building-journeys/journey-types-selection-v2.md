---
solution: Journey Optimizer
product: journey optimizer
title: 'tipos de recorrido: elija el correcto'
description: Compare tipos de recorridos y elija el adecuado para su caso de uso con guías de decisión y matriz de compatibilidad de funciones
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: tipos de recorrido, unitario, leer audiencia, calificación de audiencia, evento empresarial, comparación, guía de decisión, elegir, selección, tiempo real, programado, por lotes, activado por evento
version: Journey Orchestration
source-git-commit: d4ed86ea2833c1753d89186a460ba24ae57773fd
workflow-type: tm+mt
source-wordcount: '2109'
ht-degree: 0%

---


# tipos de recorrido: elija el correcto {#journey-types-selection}

>[!BEGINSHADEBOX]

**En esta página:** Obtenga información acerca de los cuatro tipos de recorrido de AJO (evento unitario, lectura de audiencia, calificación de audiencia y evento empresarial) y averigüe cuál se ajusta a su caso de uso.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] admite cuatro tipos de recorrido, cada uno diseñado para un tipo diferente de déclencheur y escenario empresarial. Comprender la diferencia le ayuda a crear la experiencia correcta desde el principio.

## Los cuatro tipos de recorrido {#journey-types}

>[!BEGINTABS]

>[!TAB recorridos de eventos unitarios]

**Cuándo usar:** experiencias activadas por eventos en tiempo real

**Los recorridos de eventos unitarios** se activan individualmente cuando se produce una acción específica (compra, inicio de sesión en la aplicación, envío de formularios). Los perfiles se introducen de uno en uno en tiempo real, lo que los hace ideales para obtener respuestas inmediatas basadas en el comportamiento.

**Perfecto para:** Recuperación de abandono del carro de compras, incorporación de nuevos miembros, correos electrónicos de bienvenida cuando alguien se suscribe y personalización posterior al inicio de sesión.

➡️ [Más información sobre los eventos](../event/about-events.md) | [Mensaje para el caso de uso de los suscriptores](message-to-subscribers-uc.md) | [Cree su primer recorrido](journey-gs.md)

>[!TAB Leer recorridos de audiencia]

**Cuándo usar:** Campañas programadas para segmentos de audiencia

**Leer recorridos de audiencia** comienza con una audiencia de [!DNL Adobe Experience Platform] y envía mensajes en lote a todos los perfiles simultáneamente. Este tipo de recorrido es ideal para comunicaciones programadas a gran escala. Utilice la opción **lectura incremental** en recorridos recurrentes para procesar solo los perfiles que se unieron a la audiencia desde la última ejecución, en lugar de volver a procesar la audiencia completa cada vez.

**Perfecto para:** boletines mensuales, campañas promocionales para segmentos de destinatario, anuncios de productos, series de participación recurrentes y campañas de marketing de temporada.

➡️ [Más información sobre la audiencia de lectura](read-audience.md) | [Introducción a las audiencias](../audience/about-audiences.md) | [Cree su primer recorrido](journey-gs.md)

>[!TAB recorridos de calificación de audiencia]

**Cuándo se debe usar:** Respuestas en tiempo real a los cambios de pertenencia a audiencias

Los **recorridos de calificación de audiencias** dan déclencheur cuando los perfiles cumplen los requisitos para una audiencia específica (o salen de ella). Los perfiles se introducen de forma individual a medida que cumplen los criterios, lo que permite una participación inmediata cuando cambia el comportamiento del cliente. Usar **audiencias evaluadas mediante streaming** — este es el único tipo de audiencia compatible para esta actividad.

>[!CAUTION]
>
>A partir del **agosto de 2026**, los recorridos que usan una audiencia por lotes en un nodo de calificación de audiencias no se pueden publicar. [Aprenda a migrar sus recorridos](aq-batch-audiences-migration.md)

**Perfecto para:** notificaciones de actualización de nivel de VIP, mensajes de celebración de la primera compra, alertas de riesgo de pérdida y transiciones de fase del ciclo de vida de lealtad.

➡️ [Más información acerca de la calificación de audiencias](audience-qualification-events.md) | [Creando audiencias](../audience/creating-a-segment-definition.md) | [Cree su primer recorrido](journey-gs.md)

>[!TAB recorridos de eventos empresariales]

**Cuándo usar:** Condiciones comerciales que afectan a varios clientes

**Los recorridos de eventos empresariales** se desencadenan por un evento de nivel empresarial (actualizaciones de existencias, cambios de precios) que afecta a varios perfiles simultáneamente. Internamente, el déclencheur de evento empresarial siempre va seguido de un paso Leer audiencia que incorpora los perfiles relevantes, por lo que la entrada de perfil sigue las reglas de rendimiento Leer audiencia, no el rendimiento de evento unitario.

**Perfecto para:** Alertas de inventario bajas para clientes interesados, anuncios de ventas flash, notificaciones de bajadas de precios y alertas de productos que vuelven a estar disponibles.

➡️ [Más información acerca de los eventos empresariales](../event/about-creating-business.md) | [Administración de entradas](entry-management.md) | [Cree su primer recorrido](journey-gs.md)

>[!ENDTABS]

## ¿Qué tipo debe utilizar? {#decision-guide}

La respuesta normalmente se reduce a una pregunta: *¿qué inicia el recorrido?*

Si un **cliente hace algo específico** — abandona un carro de compras, se inscribe y realiza una compra — usa un **recorrido de eventos unitarios**. Se activa inmediatamente cuando se produce la acción, de perfil en perfil.

Si quieres **llegar a una audiencia según una programación**, un boletín mensual, una campaña de temporada o una serie de renovación de participación recurrente, usa un **recorrido de lectura de audiencias**. Usted define la audiencia y el momento; AJO procesa a todos a la vez.

Si desea responder **en el momento en que un cliente alcance un hito** (unirse a un nivel de lealtad, alcanzar un umbral de riesgo de pérdida, completar una primera compra), use un **recorrido de calificación de audiencia**. Se déclencheur en cuanto cambia la pertenencia a la audiencia de streaming, no en un horario fijo.

Si algo cambia **en tu negocio** que afecta a varios clientes a la vez (un nivel de stock cae, un precio cambia, una venta comienza) usa un **recorrido de evento empresarial**.

>[!TIP]
>
>**¿No está seguro de por dónde empezar?** La mayoría de los equipos comienzan con **Evento unitario** para experiencias activadas por comportamiento y **Leer audiencia** para campañas. Estos dos abarcan la mayoría de los casos de uso.

| Su objetivo | Tipo de recorrido recomendado | Por qué |
|-----------|--------------------------|-----|
| Recuperar un carro de compras abandonado | Evento unitario | Respuesta inmediata al comportamiento individual |
| Enviar newsletter mensual a los suscriptores | Leer audiencia | Comunicación por lotes programada |
| Notificar a los clientes cuando lleguen al estado de VIP | Calificación de público | Respuesta en tiempo real a la entrada de audiencia de streaming |
| Alertar a los clientes sobre existencias bajas de artículos en seguimiento | Evento empresarial | La condición empresarial afecta a varios clientes |
| Bienvenido, nuevos usuarios de la aplicación | Evento unitario o calificación de audiencia | Evento de suscripción (evento unitario) o entrada en una audiencia de flujo de nuevo usuario (Calificación de audiencias) |
| Volver a atraer a clientes inactivos (recurrentes, programados) | Leer audiencia | Ejecución por lotes recurrente con audiencia de inactividad |
| Promoción estacional a segmento de destino | Leer audiencia | Campaña programada para la audiencia |
| Anuncio de venta Flash | Evento empresarial | La decisión empresarial afecta a varios clientes |
| Reaccionar tan pronto como un cliente alcanza el nivel de lealtad Oro | Calificación de público | Audiencia de streaming, entrada individual en tiempo real |

## Referencia de disponibilidad de funciones {#feature-compatibility}

Todos los tipos de recorrido admiten el conjunto completo de canales de AJO (correo electrónico, push, SMS, en la aplicación, web, tarjetas de contenido), las actividades de orquestación principales (espera, condición, acciones personalizadas), el modo de prueba, la ejecución en seco y la optimización del tiempo de envío. La tabla siguiente muestra solo las capacidades que difieren entre tipos.

>[!NOTE]
>
>Limitaciones de actividades de salto: un recorrido que comienza con una actividad Leer audiencia o Calificación de audiencias no puede contener una actividad de salto y no puede ser el objetivo de una actividad de salto de otro recorrido.
>
>La actividad Leer audiencia como entrada de recorrido solo está disponible en los recorridos **Leer audiencia** y **Evento empresarial**; no se puede agregar a los recorridos de entrada de Calificación de audiencia o Evento unitario.

| Capacidad | Evento unitario | Leer audiencia | Calificación de público | Evento empresarial |
|-----------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Entrada** | | | | |
| Entrada activada por un evento | ✅ | ❌ | ❌ | ✅ (evento empresarial déclencheur el recorrido; los perfiles entran a través de un paso interno de Leer audiencia) |
| Entrada programada | ❌ | ✅ | ❌ | ❌ |
| Entrada basada en audiencias | ❌ | ✅ (lote) | ✅ (solo streaming) | ❌ |
| **Orquestación** | | | | |
| Leer actividad de audiencia (entrada de recorrido) | ❌ | ✅ | ❌ | ✅ (paso automático después de un evento empresarial) |
| Actividad de salto | ✅ | ❌ | ❌ | ✅ |
| **Administración de perfiles** | | | | |
| Reentrada de perfil | ✅ configurable | ❌ Una vez por ejecución de forma predeterminada ([Forzar reentrada en repetición](read-audience.md#schedule) disponible) | ✅ configurable (el perfil que ya está en el recorrido no puede volver a introducir la misma versión) | ✅ por evento |
| **Optimización** | | | | |
| Experimentos de ruta (pruebas A/B) | ✅ | ✅ | ✅ | ❌ |
| **Avanzado** | | | | |
| Lectura incremental | ❌ | ✅ | ❌ | ❌ |
| Rendimiento máximo | 5000 TPS (compartido a nivel de organización con calificación de audiencia) | 20.000 TPS por zona protegida | 5.000 TPS (compartido a nivel de organización con evento unitario) | Evento empresarial: 5.000 TPS; Leer el paso de la audiencia: 20.000 TPS |

**Leyenda:** ✅ = Compatible | ❌ = No compatible

## Próximos pasos {#next-steps}

Ahora que ha elegido un tipo de recorrido:

* **[Cree su primer recorrido](journey-gs.md)** — Guía paso a paso desde la entrada hasta la publicación
* **[Más información sobre el diseñador de recorridos](using-the-journey-designer.md)**: Diseña tu lienzo de recorrido
* **[Entrada de perfil en recorrido](entry-management.md)**: reglas de entrada, reentrada y rendimiento por tipo
* **[Introducción a recorrido](journey.md)**: Información general sobre aspectos básicos y funcionalidades
* **[Preguntas frecuentes sobre Journey Orchestration](journey-faq.md)** — Preguntas frecuentes respondidas

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página proporciona una comparación completa de los cuatro tipos de recorrido de AJO (evento unitario, audiencia de lectura, calificación de audiencia y evento empresarial), junto con una guía de decisión y una matriz de compatibilidad de características para ayudar a los usuarios a elegir el tipo adecuado para su caso de uso.

**Intenciones:**

* Elija el tipo de recorrido correcto para un caso de uso empresarial determinado mediante la tabla de decisión
* Compare los tipos de recorridos en paralelo utilizando la matriz de compatibilidad de funciones detallada
* Saber cuándo usar Leer recorridos de audiencia para comunicaciones por lotes programadas
* Comprenda cuándo utilizar recorridos de evento unitarios para experiencias activadas por eventos en tiempo real
* Comprender cuándo usar recorridos de calificación de audiencia para respuestas de cambio de estado en tiempo real
* Comprender cuándo usar recorridos de evento empresarial para comunicaciones basadas en condiciones empresariales
* Comprenda los límites de rendimiento por tipo de recorrido al planificar implementaciones de gran volumen

**Glosario:**

* **recorrido de eventos unitarios**: Un recorrido desencadenado por una acción individual del cliente específica (por ejemplo, compra o inicio de sesión) en la que los perfiles escriben uno a la vez en tiempo real. *(específico del producto)*
* **Leer recorrido de audiencias**: Un recorrido que comienza con una audiencia de Adobe Experience Platform y envía mensajes en lote a todos los perfiles simultáneamente según una programación. *(específico del producto)*
* **recorrido de calificación de audiencias**: un recorrido que déclencheur cuándo los perfiles cumplen los requisitos para un segmento de audiencia específico o lo abandonan. Requiere una audiencia evaluada por streaming para el comportamiento de entrada en tiempo real. *(específico del producto)*
* **recorrido de evento empresarial**: recorrido desencadenado por un evento de nivel empresarial (por ejemplo, actualización de existencias, cambio de precio) que afecta a varios perfiles simultáneamente; siempre asociado con un paso Leer audiencia interno para la ingesta de perfiles. *(específico del producto)*
* **Lectura incremental**: una capacidad de Audiencia de lectura que procesa solo perfiles que se unieron a la audiencia desde la última ejecución, no la audiencia completa cada vez. Solo está disponible para recorridos de audiencia de lectura. *(específico del producto)*
* **Audiencia de streaming**: una audiencia de Adobe Experience Platform se evalúa continuamente en tiempo real, a diferencia de una audiencia por lotes que se evalúa según una programación (por ejemplo, diariamente). Necesario para que los recorridos de cualificación de audiencia logren un comportamiento de entrada en tiempo real. *(específico del producto)*

**Protecciones:**

* La lectura incremental solo está disponible para recorridos de audiencia de lectura, no para recorridos de evento unitario, calificación de audiencia o evento empresarial
* Los experimentos de ruta (pruebas A/B) no son compatibles con los recorridos de eventos empresariales
* La reentrada de perfiles en Read Audience recorrido está limitada a una vez por ejecución de forma predeterminada; utilice Forzar reentrada en repetición en ejecuciones programadas para permitir que los perfiles vuelvan a entrar en la siguiente ejecución
* La actividad Leer audiencia solo está disponible como entrada de recorrido en recorridos Leer audiencia y Evento empresarial, no en recorridos de entrada de evento unitario o de calificación de audiencia
* Los recorridos de cualificación de audiencia y lectura de audiencia no pueden contener una actividad de salto y no pueden ser el destino de una actividad de salto de otro recorrido
* Los recorridos de calificación de audiencias requieren una audiencia evaluada por streaming. A partir de agosto de 2026, las audiencias evaluadas por lotes no se podrán usar en un nodo de calificación de audiencias; consulte la [guía de migración](aq-batch-audiences-migration.md)
* Los recorridos de calificación de eventos unitarios y audiencias comparten un límite de rendimiento de 5000 TPS a nivel de organización; los recorridos de audiencia de lectura admiten hasta 20 000 TPS por zona protegida
* Un perfil que ya está presente en un recorrido no puede volver a introducir la misma versión de ese recorrido, independientemente de la configuración de reentrada

**Terminología:**

* Nombre canónico: recorrido de evento unitario — variantes: recorrido activado por evento, recorrido unitario
* Nombre canónico: Leer recorrido de audiencia — variantes: recorrido por lotes
* Nombre canónico: recorrido de calificación de audiencias — variantes: recorrido de evento de calificación de audiencias
* Nombre canónico: recorrido de evento de negocio — variantes: recorrido activado por evento de negocio
* No confunda: &quot;Leer recorrido de audiencias&quot; ≠ &quot;recorrido de calificación de audiencias&quot;: la lectura de audiencia procesa a todos los miembros de la audiencia en lote según lo programado; la calificación de audiencias responde a cambios de pertenencia individuales en tiempo real (transmite audiencias solo para su entrada inmediata)
* No confundir: &quot;recorrido de evento unitario&quot; ≠ &quot;recorrido de evento empresarial&quot;: el evento unitario se activa por una acción del cliente que afecta a un perfil; el evento empresarial se activa por una condición empresarial y consume varios perfiles a través de un paso interno de Leer audiencia

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Qué tipo de recorrido debo usar para una newsletter mensual?** — Utilice un recorrido Leer audiencia; está diseñado para la comunicación programada por lotes a todos los perfiles de un segmento de audiencia simultáneamente.
* **Q: ¿Qué tipo de recorrido debo usar para recuperar un carro de compras abandonado?** — Utilizar un recorrido de eventos unitario; se aplica inmediatamente como déclencheur cuando se produce el evento de abandono y responde al comportamiento del individuo en tiempo real.
* **Q: ¿Puedo ejecutar experimentos de ruta A/B en un recorrido de eventos empresariales?** — No; los experimentos de ruta no son compatibles con los recorridos de evento empresarial.
* **Q: ¿Cuál es la diferencia entre un recorrido de evento unitario y un recorrido de calificación de audiencia?** — Un recorrido de evento unitario se activa por una acción específica del cliente (por ejemplo, compra); un recorrido de calificación de audiencia se activa cuando un perfil entra o sale de un segmento de audiencia en función de la evaluación de criterios de flujo continuo.
* **Q: ¿Qué tipos de recorrido admiten la lectura incremental?** — Solo los recorridos de audiencia de lectura admiten la lectura incremental; los otros tres tipos de recorrido no.
* **Q: ¿Puedo agregar una actividad Leer audiencia a un recorrido de eventos unitario?** — No; la actividad Leer audiencia solo está disponible como entrada de recorrido en recorridos Leer audiencia y Evento empresarial.
* **Q: ¿Puedo usar una actividad de salto en un recorrido de lectura de audiencias?** — No; los recorridos que comienzan con una actividad Leer audiencia o Calificación de audiencia no pueden contener una actividad Saltar y no pueden ser el destino de un salto de otro recorrido.
* **Q: ¿Puedo dar la bienvenida a los nuevos usuarios de la aplicación con un recorrido de calificación de audiencia?** — Sí, si la entrada está dirigida por una audiencia de flujo continuo (por ejemplo, cuando un perfil se une a un segmento de nuevo usuario); un recorrido de evento unitario de registro también es un patrón común.
* **Q: mi recorrido de calificación de audiencia no se activa en tiempo real. ¿Por qué?** — Los recorridos de cualificación de audiencias requieren una audiencia evaluada por streaming. El uso de una audiencia evaluada por lotes está obsoleto y se bloqueará a partir de agosto de 2026. [Consulte la guía de migración](aq-batch-audiences-migration.md)
* **Q: ¿Cuál es la diferencia de rendimiento entre el evento unitario y los recorridos de lectura de audiencia?** — Los recorridos de eventos unitarios comparten un límite de 5000 TPS con los recorridos de calificación de audiencias a nivel de organización. Los recorridos de audiencia de lectura admiten hasta 20 000 TPS por zona protegida, lo que los hace más adecuados para campañas por lotes a gran escala.

+++
