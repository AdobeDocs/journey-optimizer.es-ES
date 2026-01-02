---
solution: Journey Optimizer
product: journey optimizer
title: Tipos de recorrido y guía de selección
description: Compare tipos de recorridos y elija el adecuado para su caso de uso con guías de decisión y matriz de compatibilidad de funciones
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: tipos de recorrido, unitario, leer audiencia, calificación de audiencia, evento empresarial, comparación, guía de decisión, elegir, selección, tiempo real, programado, por lotes, activado por evento
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: f749eae4e0a826428880e913219cf6f5a135b17c
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 3%

---


# Tipos de recorrido y guía de selección {#journey-types-selection}

Adobe Journey Optimizer admite cuatro tipos de recorridos, cada uno diseñado para diferentes mecanismos de entrada y escenarios empresariales. Esta guía le ayuda a comprender las diferencias y elegir el tipo adecuado para su caso de uso.

## información general sobre tipos de recorrido {#journey-types}

>[!BEGINTABS]

>[!TAB recorridos unitarios]

**Cuándo usar:** experiencias activadas por eventos en tiempo real

**Los recorridos unitarios** se activan individualmente cuando se produce una acción específica (compra, inicio de sesión en la aplicación, envío de formularios). Los perfiles se introducen de uno en uno en tiempo real, lo que los hace ideales para obtener respuestas inmediatas basadas en el comportamiento.

**Perfecto para:** confirmaciones de pedidos después de la compra, correos electrónicos de bienvenida cuando alguien se suscribe, abandono del carro de compras activado por la navegación y notificaciones de restablecimiento de contraseña.

➡️ [Más información sobre los eventos](../event/about-events.md) | [Mensaje para el caso de uso de los suscriptores](message-to-subscribers-uc.md)

>[!TAB Leer recorridos de audiencia]

**Cuándo usar:** Campañas programadas para segmentos de audiencia

**Leer recorridos de audiencia** comienza con una audiencia de Adobe Experience Platform y envía mensajes en lote a todos los perfiles simultáneamente. Este tipo de recorrido es ideal para comunicaciones programadas a gran escala.

**Perfecto para:** boletines mensuales, campañas promocionales para segmentos de público objetivo, anuncios de productos y campañas de marketing de temporada.

➡️ [Más información sobre la audiencia de lectura](read-audience.md) | [Introducción a las audiencias](../audience/about-audiences.md)

>[!TAB recorridos de calificación de audiencia]

**Cuándo se debe usar:** Respuestas en tiempo real a los cambios de pertenencia a audiencias

Los **recorridos de calificación de audiencias** dan déclencheur cuando los perfiles cumplen los requisitos para una audiencia específica (o salen de ella). Los perfiles se introducen de forma individual según cumplen los criterios en tiempo real, lo que permite una participación inmediata cuando cambia el comportamiento de los clientes.

**Perfecto para:** notificaciones de actualización de nivel de VIP, renovación de la participación cuando los clientes se vuelven inactivos, mensajes de celebración de la primera compra y segmentación geográfica cuando los clientes se mudan.

➡️ [Más información acerca de la calificación de audiencias](audience-qualification-events.md) | [Creación de audiencias](../audience/creating-a-segment-definition.md)

>[!TAB recorridos de eventos empresariales]

**Cuándo usar:** Condiciones comerciales que afectan a varios clientes

Los **recorridos de eventos empresariales** se desencadenan por eventos de nivel empresarial (actualizaciones de existencias, avisos meteorológicos, cambios de precios) que afectan a varios perfiles simultáneamente. Estos responden a condiciones empresariales más amplias que a acciones individuales.

**Perfecto para:** Alertas de inventario bajas para clientes interesados, anuncios de venta flash, promociones basadas en el tiempo, notificaciones de caída de precios y alertas de productos que vuelven a estar en existencias.

➡️ [Más información acerca de los eventos empresariales](../event/about-creating-business.md) | [Administración de entradas](entry-management.md)

>[!ENDTABS]

## Guía de decisión: Elección del tipo de recorrido {#decision-guide}

Siga este árbol de decisión para seleccionar el tipo de recorrido adecuado para su caso de uso:

### Paso 1: ¿Cuáles son los déclencheur del recorrido?

* **El cliente realiza una acción específica** (compra, clic, inicio de sesión) → Vaya al paso 2
* **Tiempo/programación** (enviar a una hora específica o de forma recurrente) → **Usar el recorrido de lectura de audiencias**
* **El estado del cliente cambia** (se une y abandona un segmento) → Vaya al paso 3
* **Condición de la empresa** (nivel de existencias, cambio de precio, tiempo) → **Usar recorrido de evento empresarial**

### Paso 2: déclencheur de acción de cliente individuales

* **¿Se necesita una respuesta inmediata y en tiempo real?**
   * Sí → **Usar recorrido Unitario**
   * Sin → Considere el recorrido Leer audiencia con la ejecución programada

### Paso 3: Cambios en el estado del cliente

* **¿Necesita responder cuando los clientes entran o salen de un segmento?**
   * Sí → **Usar recorrido de calificación de audiencia**
   * No, solo al introducir → filtro Considerar recorrido unitario con evento o Leer audiencia con audiencia

### Selección rápida por caso de uso

| Su objetivo | Tipo de recorrido recomendado | Por qué |
|-----------|------------------------|-----|
| Enviar confirmación de pedido después de la compra | Unitario | Respuesta inmediata a la acción individual |
| Enviar newsletter mensual a los suscriptores | Leer audiencia | Comunicación por lotes programada |
| Notificar a los clientes cuando lleguen al estado de VIP | Calificación de público | Respuesta en tiempo real al cambio de estado |
| Alertar a los clientes sobre existencias bajas de artículos en seguimiento | Evento empresarial | La condición empresarial afecta a varios clientes |
| Bienvenido, nuevos usuarios de la aplicación | Unitario | Activado por evento de suscripción |
| Volver a atraer clientes inactivos | Calificación de público | Responde a la entrada de segmento de inactividad |
| Promoción estacional a segmento de destino | Leer audiencia | Campaña programada para la audiencia |
| Anuncio de venta Flash | Evento empresarial | La decisión empresarial afecta a varios clientes |

>[!NOTE]
>
>¿No está seguro de qué tipo elegir? Comience con **recorridos unitarios** para experiencias basadas en eventos o **recorridos de audiencia de lectura** para campañas programadas, que cubren los casos de uso más comunes.

## Comparación detallada de los tipos de recorrido {#journey-types-comparison}

Utilice esta tabla para comparar rápidamente los tipos de recorrido y elegir el adecuado para su caso de uso:

| Aspecto | Recorridos unitarios | Leer recorridos de audiencia | Recorridos de calificación de audiencia | Recorridos de evento empresarial |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **Mecanismo de entrada** | Déclencheur de evento individual | Lote programado | Cambio de pertenencia a audiencia en tiempo real | Evento de nivel empresarial |
| **Horario de entrada** | Tiempo real, a medida que ocurren los eventos | Programado (una vez o recurrente) | Tiempo real, a medida que se produce la calificación | Tiempo real, cuando se activa un evento empresarial |
| **Entrada de perfil** | Uno a la vez | Todo a la vez (lote) | Uno a la vez | Varios perfiles simultáneamente |
| **origen de Déclencheur** | Acción del cliente (compra, clic, inicio de sesión) | Programación basada en el tiempo | Abono a audiencias (entrada/salida) | Condición de la empresa (stock, tiempo, precio) |
| **Mejor para** | Mensajes transaccionales, respuestas de comportamiento | Campañas de marketing, boletines informativos | Programas de fidelización, fases del ciclo vital | Alertas de inventario, promociones, condiciones comerciales |
| **Usar cuando** | Respuesta inmediata a las acciones individuales necesarias | Alcanzar segmentos de audiencia grandes según lo programado | Respuesta a los cambios de estado del cliente | Los eventos empresariales afectan a varios clientes |
| **Ejemplos** | Confirmación del pedido, restablecimiento de contraseña | Newsletter mensual, campaña de temporada | Actualización de VIP, alerta de inactividad | Alerta baja de acciones, venta flash, caída de precios |
| **Reentrada** | Configurable (permitir varias entradas por perfil) | Cada perfil introduce una vez por ejecución | Configurable por evento de calificación | El mismo evento puede afectar a varios perfiles |
| **Requisitos de datos** | Esquema de evento con datos de déclencheur | Audiencia de Adobe Experience Platform | Streaming o audiencia por lotes | Esquema de evento empresarial |

## Compatibilidad de funciones por tipo de recorrido {#feature-compatibility}

No todas las funciones están disponibles para todos los tipos de recorrido. Utilice esta matriz para comprender qué capacidades funcionan con qué tipos de recorrido:

| Funcionalidad/Funcionalidad | Unitario | Leer audiencia | Calificación de público | Evento empresarial |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Mecanismos de entrada** |
| Entrada activada por un evento | ✅ | ❌ | ❌ | ✅ |
| Entrada programada | ❌ | ✅ | ❌ | ❌ |
| Entrada basada en audiencias | ❌ | ✅ | ✅ | ❌ |
| **Características de orquestación** |
| Actividades de espera | ✅ | ✅ | ✅ | ✅ |
| Actividades de condición | ✅ | ✅ | ✅ | ✅ |
| Acciones personalizadas | ✅ | ✅ | ✅ | ✅ |
| Leer actividad de audiencia (dentro del recorrido) | ✅ | ✅ | ✅ | ✅ |
| Actividad de calificación de audiencia | ✅ | ✅ | ✅ | ✅ |
| Actividad de salto | ✅ | ✅ | ✅ | ✅ |
| **Administración de perfiles** |
| Reentrada de perfil | ✅ configurable | ❌ Una vez por ejecución | ✅ configurable | ✅ por evento |
| Configuración del área de nombres | Se requiere ✅ | ✅ Opcional | Se requiere ✅ | Se requiere ✅ |
| Límite de perfil | ✅ | ✅ | ✅ | ✅ |
| **Pruebas y optimización** |
| Modo de prueba | ✅ | ✅ | ✅ | ✅ |
| Ejecución en seco | ✅ | ✅ | ✅ | ✅ |
| Experimentos de ruta (pruebas A/B) | ✅ | ✅ | ✅ | ❌ |
| Optimización del tiempo de envío | ✅ | ✅ | ✅ | ✅ |
| **Canales** |
| Correo electrónico | ✅ | ✅ | ✅ | ✅ |
| Notificaciones push | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| Mensajes en la aplicación | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Tarjetas de contenido | ✅ | ✅ | ✅ | ✅ |
| **Funciones avanzadas** |
| Lectura incremental | ❌ | ✅ | ❌ | ❌ |
| Exportar audiencia | ✅ | ✅ | ✅ | ✅ |
| Administración de husos horarios | ✅ | ✅ | ✅ | ✅ |
| Eventos de reacción | ✅ | ✅ | ✅ | ✅ |
| Fuentes de datos externas | ✅ | ✅ | ✅ | ✅ |
| Restricción/Límite | ✅ | ✅ | ✅ | ✅ |

**Leyenda:** ✅ = Compatible | ❌ = No compatible

## Próximos pasos {#next-steps}

Ahora que comprende los tipos de recorrido, está listo para lo siguiente:

* **[Cree su primer recorrido](journey-gs.md)** - Guía paso a paso
* **[Más información sobre el diseñador de recorridos](using-the-journey-designer.md)**: Diseña tu lienzo de recorrido
* **[Explorar las funcionalidades del recorrido](journey.md#capabilities)**: descubra características avanzadas
* **[Ver preguntas frecuentes sobre el recorrido](journey-faq.md)** - Preguntas frecuentes respondidas

**¿Necesita comparar con campañas?**

* [Guía de comparación de Recorridos vs. Campañas](../start/journeys-vs-campaigns.md): elija entre recorridos, campañas de acción/API y campañas organizadas

