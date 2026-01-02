---
solution: Journey Optimizer
product: journey optimizer
title: 'Recorridos frente a campañas: elija el enfoque adecuado'
description: Compare recorridos, campañas y campañas orquestadas para elegir el enfoque adecuado para sus necesidades de marketing en Adobe Journey Optimizer
feature: Journeys, Campaigns, Get Started, Overview
role: User
level: Beginner
keywords: recorrido, campaña, orquestado, comparación, elegir, decisión, flujo de trabajo, tiempo real, lote, orquestación, varios pasos, programado, activado por API, impulsado por evento
hide: true
hidefromtoc: true
source-git-commit: f749eae4e0a826428880e913219cf6f5a135b17c
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 3%

---


# Recorridos frente a campañas: elija el método adecuado {#journeys-vs-campaigns}

Adobe Journey Optimizer ofrece tres poderosos enfoques para llegar a sus clientes y atraerlos. Es fundamental saber cuándo usar cada una de ellas para crear experiencias de marketing eficaces.

Esta guía le ayuda a elegir entre **Recorridos**, **Campañas** (activadas por acción y API) y **Campañas orquestadas** según sus necesidades de marketing específicas.

## Resumen de comparación rápida {#quick-overview}

| Aproximación | Mejor para | Estilo de ejecución |
|----------|----------|-----------------|
| **Recorridos** | Experiencias de cliente en tiempo real de varios pasos con lógica condicional | 1:1 orquestación: cada perfil a su propio ritmo |
| **Campañas (acción y API)** | Envío de mensaje simple, programado o activado | Activado por lotes o API: todos los perfiles simultáneamente |
| **Campañas orquestadas** | Flujos de trabajo por lotes complejos con segmentación de varias entidades | Lienzo por lotes: todos los perfiles procesados juntos |

## Comparación detallada {#detailed-comparison}

Utilice esta tabla completa para comprender las diferencias clave:

| Función | Recorridos | Campañas (activadas por la acción y la API) | Campañas orquestadas |
|---------|----------|-----------------------------------|----------------------|
| **Propósito principal** | Organización de varios pasos 1:1 con contexto de cliente en tiempo real | Envío de mensajes único o recurrente a las audiencias | Campañas por lotes de varios pasos con flujos de trabajo de segmentación complejos |
| **Tipo de lienzo** | Lienzo 1:1: cada perfil viaja a su propio ritmo | Sin lienzo: ejecución de una sola acción | Lienzo por lotes: todos los perfiles procesados juntos |
| **Flujo de ejecución** | Acciones secuenciales, el perfil mantiene el estado durante todo el recorrido | Ejecución simultánea para toda la audiencia | Flujo de trabajo por lotes de varios pasos con actividades y transiciones |
| **Mecanismo de entrada** | Eventos, audiencias, cualificaciones y eventos empresariales | Activación manual, programación o déclencheur de API | Ejecución programada del flujo de trabajo por lotes |
| **Modelo de datos** | Perfil en tiempo real + datos de evento | Datos de perfil + carga útil de API | Datos relacionales de varias entidades (perfiles, productos, tiendas, reservas) |
| **Segmentación** | Audiencias creadas previamente + condiciones en tiempo real | Audiencias creadas previamente desde Experience Platform | Audiencias a petición creadas dentro del lienzo con recuentos exactos |
| **Procesamiento de perfil** | Individual, en tiempo real (a medida que ocurren los eventos) | Lote, todo a la vez | Lote, todo junto con compatibilidad con varias entidades |
| **Personalización** | Datos contextuales en tiempo real + atributos de perfil | Atributos de perfil + datos de carga útil de API | Datos de varias entidades para una segmentación de precisión |
| **Complejidad** | Varios pasos con ramificación, tiempos de espera y condiciones | Una sola acción o flujo de trabajo simple | Flujos de trabajo por lotes de varios pasos con segmentación, enriquecimiento y divisiones |
| **Mejor para** | Recorridos del ciclo vital del cliente, incorporación, abandono del carro | Campañas promocionales, boletines informativos, anuncios, mensajes transaccionales | Campañas estacionales complejas, promociones de varios pasos y lanzamientos de productos |
| **Tiempo** | Continuo, siempre activo una vez publicado | Fechas de inicio y finalización programadas o activadas por API | Ejecución por lotes según lo programado |
| **Administración de estado** | Mantiene el estado del cliente para acciones en tiempo real | Ejecución sin estado | Procesamiento por lotes con tablas de trabajo |
| **Usar cuando** | Se necesitan varios puntos de contacto con la lógica de decisión en tiempo real | Mensaje simple a la audiencia en un momento específico | Necesita segmentación compleja, datos de varias entidades o recuentos exactos previos al envío |
| **Funciones únicas** | Reacciones en tiempo real, actividades de espera, ritmo basado en perfiles | Programación sencilla, activación de API, control de velocidad | Conjuntos de datos relacionales, segmentación de varias entidades, recuentos exactos, envío de varios niveles |

## Guía de decisión {#decision-guide}

Siga este árbol de decisión para elegir el enfoque correcto:

### Paso 1: ¿Cuál es su requisito de ejecución?

**Respuestas individuales en tiempo real al comportamiento de los clientes?**
→ **Usar Recorridos**
- Los perfiles deben moverse a su propio ritmo
- Lógica condicional basada en el comportamiento
- El contexto en tiempo real es fundamental

**Envío de mensaje simple a una audiencia?**
→ **Usar campañas activadas por acción o API**
- Todos los perfiles reciben el mensaje simultáneamente
- Programado o activado mediante API
- No se necesita una lógica compleja de varios pasos

**Flujo de trabajo por lotes complejo con segmentación avanzada?**
→ **Usar campañas orquestadas**
- Necesita datos de varias entidades (productos, tiendas, reservas)
- Requerir recuentos previos al envío exactos
- Procesamiento por lotes de varios pasos con divisiones y enriquecimiento

### Paso 2: Validar la elección

| Su necesidad | Enfoque recomendado | Por qué |
|-----------|---------------------|-----|
| Bienvenido a nuevos clientes con incorporación de varios pasos | Recorridos | Entrada en tiempo real, varios puntos de contacto, rutas condicionales |
| Enviar newsletter mensual a los suscriptores | Campaña de acción | Mensaje programado simple a la audiencia |
| Abandono del carro de compras con secuencia de recordatorio | Recorridos | Déclencheur en tiempo real, tiempos de espera, seguimiento condicional |
| Anuncio promocional para todos los clientes | Campaña de acción | Mensaje único, envío inmediato |
| Volver a atraer a usuarios inactivos según su comportamiento | Recorridos | Activado por calificación de audiencia, ruta personalizada |
| Venta Flash activada por evento empresarial | Recorridos (evento empresarial) | Déclencheur en tiempo real que afectan a varios clientes |
| Promoción de temporada con integración del catálogo de productos | Campaña orquestada | Datos de varias entidades, segmentación compleja, recuento exacto |
| Mensaje transaccional activado por API | Campaña activada por API | Déclencheur del sistema externo, envío inmediato |
| Envío de varios niveles por reserva | Campaña orquestada | Relaciones entre varias entidades, un mensaje por reserva |

## Distinciones clave explicadas {#key-distinctions}

### Recorridos: 1:1 orquestación en tiempo real

**Qué lo hace único:**
- Cada perfil mantiene el estado y el contexto individuales
- Los perfiles entran y progresan a su propio ritmo
- Toma de decisiones en tiempo real basada en el comportamiento y los eventos
- Las actividades de espera crean intervalos personalizados
- La bifurcación condicional crea rutas únicas por perfil

**Flujo de ejemplo:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Cada cliente experimenta su propia cronología de recorridos en función de sus acciones.

[Más información sobre Recorrido](../building-journeys/journey.md)

### Campañas: Envío por lotes simple o activado

**Qué lo hace único:**
- Todos los perfiles procesados de forma idéntica y simultánea
- Ejecución sin estado: sin contexto
- Programación simple o activación de API
- Idóneo para comunicaciones broadcast

**Flujo de ejemplo:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Todos reciben el mismo mensaje al mismo tiempo.

**Tipos:**
- **Campañas de acción**: Envío programado (único o recurrente)
- **Campañas activadas por API**: Se activó mediante una llamada API desde sistemas externos

[Más información sobre las Campañas](../campaigns/get-started-with-campaigns.md)

### Campañas organizadas: Flujos de trabajo de lienzo por lotes

**Qué lo hace único:**
- Lienzo por lotes con actividades y transiciones (similar al lienzo de recorrido, pero orientado a lotes)
- Compatibilidad con datos relacionales de varias entidades (perfiles + productos + tiendas + reservas)
- Generación de audiencias bajo demanda dentro del lienzo
- Recuentos exactos antes del envío (visibilidad previa al envío)
- Envío de varios niveles (un mensaje por entidad, por ejemplo, por reserva)
- Todos los perfiles procesados juntos en lote

**Flujo de ejemplo:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Combina la complejidad del flujo de trabajo con la ejecución de campañas por lotes.

[Más información sobre las Campañas organizadas](../orchestrated/gs-orchestrated-campaigns.md)

## Ejemplos de casos de uso {#use-cases}

### Casos de uso de recorrido

&#x200B;* **Recuperación de abandono del carro de compras**: desencadenada por el evento de adición al carro de compras, esperar al cierre de compra o enviar recordatorios en caso de que no se realice la compra
&#x200B;* **Incorporación del cliente**: serie de bienvenida de varios pasos con contenido personalizado basado en datos de perfil
&#x200B;* **Actualización del nivel de fidelización**: Se activa cuando el cliente alcanza un nuevo nivel y envía felicitaciones y beneficios.
&#x200B;* **Campañas de cumpleaños**: la entrada se basa en la fecha de nacimiento y en ofertas personalizadas.
&#x200B;* **Nuevo compromiso**: activado por calificación de audiencia (inactividad), alcance progresivo

### Casos de uso de Campaign (activados por la acción y la API)

**Campañas de acción:**
&#x200B;* **Boletines mensuales**: Envío por lotes programado al segmento del suscriptor
&#x200B;* **Anuncios promocionales**: ofertas con distinción de tiempo para audiencias de destino
&#x200B;* **Lanzamientos de productos**: anuncio coordinado para todos los clientes
&#x200B;* **Saludos de temporada**: Mensajes de vacaciones en fechas específicas

**Campañas activadas por API:**
&#x200B;* **Confirmaciones de pedidos**: Activado por el sistema de comercio electrónico después de la compra
&#x200B;* **Notificaciones de envío**: activado por el sistema logístico
&#x200B;* **Alertas de cuenta**: activadas por el sistema de detección de fraude
&#x200B;* **Restablecimiento de contraseña**: activado por la acción del usuario en la aplicación

### Casos de uso de Campaign organizados

&#x200B;* **Promoción de temporada con integración de catálogo**: consulta el catálogo de productos, identifica a los clientes elegibles, segmenta por preferencias y envía recomendaciones personalizadas de productos
&#x200B;* **Campañas específicas de tiendas**: Dirija a los clientes cerca de ubicaciones de tiendas específicas con datos de inventario de tiendas
&#x200B;* **Comunicaciones con múltiples reservas**: envía un mensaje por reserva (reservas de hotel, reservas de vuelo)
&#x200B;* **Organización compleja de segmentos**: cree audiencias paso a paso con el enriquecimiento de varias fuentes de datos
&#x200B;* **Validación previa al envío**: obtenga los recuentos exactos de destinatarios antes de lanzar las campañas principales

## Disponibilidad de funciones {#feature-availability}

### Canales

| Canal | Recorridos | Campañas de acción | Campañas activadas por API | Campañas orquestadas |
|---------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Correo electrónico | ✅ | ✅ | ✅ | ✅ |
| Push | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ |
| in-app | ✅ | ✅ | ✅ | ❌ |
| Web | ✅ | ✅ | ❌ | ❌ |
| Basado en código | ✅ | ✅ | ❌ | ❌ |
| Tarjetas de contenido | ✅ | ✅ | ❌ | ❌ |
| Correo directo | ✅ | ✅ | ❌ | ❌ |

### Funciones avanzadas

| Capacidad | Recorridos | Campañas de acción | Campañas activadas por API | Campañas orquestadas |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Flujos de trabajo de varios pasos | ✅ | ❌ | ❌ | ✅ |
| Déclencheur en tiempo real | ✅ | ❌ | ✅ | ❌ |
| Actividades de espera | ✅ | ❌ | ❌ | ✅ |
| Ramificación condicional | ✅ | ❌ | ❌ | ✅ |
| Ejecución programada | ✅ | ✅ | ✅ | ✅ |
| Activación de API | ❌ | ❌ | ✅ | ❌ |
| Datos de varias entidades | ❌ | ❌ | ❌ | ✅ |
| Recuentos exactos previos al envío | ❌ | ❌ | ❌ | ✅ |
| Segmentación bajo demanda | ❌ | ❌ | ❌ | ✅ |
| Optimización del tiempo de envío | ✅ | ✅ | ✅ | ✅ |
| Prueba A/B | ✅ | ✅ | ❌ | ❌ |
| Flujos de trabajo de aprobación | ✅ | ✅ | ✅ | ❌ |

## Preguntas frecuentes {#common-questions}

**Q: ¿Puedo combinar recorridos y campañas en mi estrategia de marketing?**

R: ¡Por supuesto! La mayoría de las organizaciones utilizan los tres enfoques para diferentes escenarios:
- Recorridos para la participación en tiempo real y basada en el comportamiento
- Campañas de acción para comunicaciones de difusión programadas
- Campañas activadas por API para mensajes transaccionales
- Campañas organizadas para campañas por lotes complejas que requieren gran cantidad de datos

**Q: ¿Puedo convertir una campaña en un recorrido o viceversa?**

R: No, debe reconstruir la experiencia en el formato adecuado. Sin embargo, puede reutilizar el contenido, las audiencias y los conceptos lógicos.

**Q: ¿Qué enfoque es más fácil de compilar?**

R: Las campañas de acción suelen ser las más sencillas (enviar un solo mensaje a la audiencia), seguidas de campañas activadas por API, Recorridos (más complejas con la lógica de varios pasos) y campañas orquestadas (más complejas debido al flujo de trabajo del lienzo y a las capacidades de varias entidades).

**Q: ¿Qué escala es mejor para las audiencias grandes?**

R: Los tres pueden escalar bien, pero:
- **Leer Recorridos de audiencias** y **Campañas de acción** están optimizadas para audiencias de lotes grandes
- **Las campañas orquestadas** sobresalen en la segmentación compleja con conjuntos de datos grandes
- **Recorridos unitarios** procesan los perfiles individualmente, por lo que la escala depende del volumen del evento

**Q: ¿Puedo usar la misma audiencia en recorridos y campañas?**

R: Sí, las audiencias creadas en Adobe Experience Platform se pueden usar en los tres enfoques.

## Próximos pasos {#next-steps}

¿Listo para empezar a construir? Explore la documentación detallada del enfoque elegido:

&#x200B;* **[Introducción a Recorrido](../building-journeys/journey.md)**: obtenga información sobre los tipos de recorrido, el diseñador y el flujo de trabajo
&#x200B;* **[Introducción a las campañas](../campaigns/get-started-with-campaigns.md)**: Explore campañas activadas por acciones y API
&#x200B;* **[Introducción a campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md)**: Descubra flujos de trabajo de lienzo por lotes

**¿Necesita más ayuda para decidir?**
- [Comparación de tipos de recorrido](../building-journeys/journey.md#journey-types-comparison)
- [Comparación de tipos de campaña](../campaigns/get-started-with-campaigns.md#campaign-types)
- [PREGUNTAS FRECUENTES SOBRE RECORRIDO](../building-journeys/journey-faq.md)
- [Preguntas frecuentes sobre campañas organizadas](../orchestrated/orchestrated-campaigns-faq.md)

