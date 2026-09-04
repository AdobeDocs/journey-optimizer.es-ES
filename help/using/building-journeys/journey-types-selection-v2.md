---
solution: Journey Optimizer
product: journey optimizer
title: 'Tipos de recorrido: elija el correcto'
description: Compare tipos de recorridos y elija el adecuado para su caso de uso con guías de decisión y matriz de compatibilidad de funciones
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: tipos de recorrido, unitario, leer audiencia, calificación de audiencia, evento empresarial, comparación, guía de decisión, elegir, selección, tiempo real, programado, por lotes, activado por evento
version: Journey Orchestration
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 3%

---


# Tipos de recorrido: elija el correcto {#journey-types-selection}

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

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-journey-types-selection-v2.md}}
