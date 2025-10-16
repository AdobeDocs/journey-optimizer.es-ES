---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con eventos de paso de recorrido
description: Aprenda a trabajar con eventos de paso de recorrido en Adobe Journey Optimizer; comprenda qué son, por qué importan y cómo utilizarlos para el análisis y la optimización
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin, User
level: Intermediate, Experienced
keywords: recorrido, eventos de paso, análisis, creación de informes, monitorización, XDM
hide: true
hidefromtoc: true
exl-id: 9f8e7d6c-5b4a-3928-1756-849302a11c2b
source-git-commit: df3abb7da17eb21e5e4120b55bdeb61fec3e202d
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 1%

---

# Trabajo con eventos de paso de recorrido {#work-with-journey-step-events}

Los eventos de paso de recorrido son eventos generados automáticamente que capturan información detallada sobre cada paso que realiza un perfil a medida que avanza por un recorrido en Adobe Journey Optimizer. Estos eventos proporcionan una visibilidad completa del rendimiento del recorrido y habilitan potentes funciones de análisis.

## ¿Qué son los eventos de paso de recorrido? {#what-are-step-events}

Los eventos de paso de recorrido son eventos XDM (Experience Data Model) generados por el sistema que Adobe Journey Optimizer crea y envía automáticamente a Adobe Experience Platform cada vez que un perfil se mueve de un nodo a otro en un recorrido. Cada evento corresponde a una acción o transición específica en la experiencia de recorrido del cliente.

Existen dos tipos principales de eventos de paso de recorrido:

- **journeyStepEvent**: Eventos relacionados con la progresión de perfiles individuales a través de pasos de recorrido
- **journeyStepProfileEvent**: eventos que incluyen información de contexto de perfil adicional

### ¿Qué eventos de paso de recorrido de déclencheur? {#event-triggers}

Los eventos de paso de recorrido se generan automáticamente para varias actividades de recorrido:

- **Eventos de entrada**: Cuando un perfil entra en un recorrido
- **Ejecución de acciones**: Cuando se envían mensajes o se realizan acciones personalizadas
- **Evaluación de condición**: Cuando los perfiles pasan por los puntos de decisión
- **Actividades de espera**: Cuando los perfiles entran y salen de los nodos de espera
- **Eventos de salida**: Cuando los perfiles se completan o salen de un recorrido
- **Control de errores**: Cuando se producen errores durante la ejecución del recorrido

>[!NOTE]
>
>Los eventos de paso de recorrido se activan de forma predeterminada en todas las instancias. No se pueden modificar ni actualizar los esquemas y conjuntos de datos que se han creado durante el aprovisionamiento para eventos de paso. Estos esquemas y conjuntos de datos están en modo de solo lectura.

## Por qué importan los eventos de paso de recorrido {#why-step-events-matter}

Los eventos de paso de recorrido proporcionan un valor crítico para las organizaciones que utilizan Adobe Journey Optimizer:

### Análisis y monitorización en tiempo real {#real-time-analytics}

- **Seguimiento del rendimiento del Recorrido**: supervise el flujo de perfiles a través de los recorridos en tiempo real
- **Análisis de conversión**: Comprenda los puntos de entrega y las rutas de conversión exitosas
- **Detección de errores**: identifique y solucione problemas a medida que ocurran

### Integración de datos y perspectivas {#data-integration}

- **Análisis entre plataformas**: Combine datos de recorrido con otras fuentes de datos de Adobe Experience Platform
- **Vista del cliente 360**: cree perfiles de cliente completos que incluyan interacciones de recorrido
- **Modelado de atribución**: Conecte los puntos de contacto del recorrido a los resultados comerciales descendentes

### Oportunidades de optimización {#optimization}

- **Perspectivas de pruebas A/B**: Analice el rendimiento de diferentes rutas de recorrido
- **Mejora de Personalization**: Use los datos de comportamiento del recorrido para mejorar las experiencias futuras
- **Eficiencia operativa**: identifique cuellos de botella y optimice el diseño del recorrido

## Cómo utilizar eventos de paso de recorrido {#how-to-use-step-events}

### Acceso a datos de eventos de paso de recorrido {#accessing-data}

Los datos de evento de los pasos de recorrido se almacenan automáticamente en Adobe Experience Platform y se puede acceder a ellos a través de:

1. **Consultas de lago de datos**: use SQL para consultar el conjunto de datos `journey_step_events`
2. **Customer Journey Analytics**: Analice los datos de recorrido con herramientas de análisis avanzadas
3. **Creación de informes en tiempo real**: Acceda a los datos a través de las capacidades de creación de informes integradas de Journey Optimizer
4. **API**: acceso a datos de evento mediante programación para aplicaciones personalizadas

### Puntos de datos clave disponibles {#key-data-points}

Los eventos de paso de recorrido capturan información completa que incluye:

- **Identificación de Recorrido**: Id., versión y nombre de Recorrido
- **Información del perfil**: ID de perfil e identidades asociadas
- **Detalles del paso**: Nombre del nodo, tipo de paso y estado de ejecución
- **Marcas de hora**: Hora exacta de cada paso del recorrido
- **Resultados de la acción**: estado de éxito/error y detalles de ejecución
- **Información del error**: Códigos de error detallados y descripciones cuando ocurren problemas

### Casos de uso comunes {#common-use-cases}

**Monitorización del rendimiento**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**Análisis de errores**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**análisis de funnel de Recorrido**

- Rastrear tasas de conversión en cada paso del recorrido
- Identificar dónde salen los perfiles con mayor frecuencia del recorrido
- Medir el tiempo empleado en diferentes fases del recorrido

## Ejemplos y recursos {#samples-resources}

### Ejemplos y plantillas de consultas {#query-examples}

Explore ejemplos de consultas completos para el análisis de eventos de pasos de recorrido comunes:

- **[ejemplos de consultas de eventos de paso de Recorrido](query-examples.md)**: Consultas SQL listas para usar para escenarios comunes de Analytics
- **[Ejemplos de consultas de conjuntos de datos](../data/datasets-query-examples.md#journey-step-event)**: Ejemplos de consultas de conjuntos de datos de eventos de pasos de recorrido
- **[Consultas basadas en perfiles](query-examples.md#profile-based-queries)**: Rastree recorridos e interacciones de perfiles individuales

### Documentación de campo {#field-documentation}

Comprenda la estructura de datos completa de los eventos de paso de recorrido:

- **[lista de campos de eventos de paso de Recorrido](sharing-field-list.md)**: referencia completa de todos los campos disponibles
- **[Campos comunes](sharing-common-fields.md)**: Campos compartidos entre journeyStepEvent y journeyStepProfileEvent
- **[Campos de ejecución de acción](sharing-execution-fields.md)**: Campos específicos del seguimiento de ejecución de acción
- **[Campos de Recorrido](sharing-journey-fields.md)**: Metadatos e identificadores específicos del Recorrido

### Prácticas recomendadas y solución de problemas {#best-practices}

**Optimización del rendimiento**

- Use `journeyVersionID` en lugar de `journeyVersionName` para obtener un mejor rendimiento de las consultas
- Filtre por intervalos de fechas para mejorar la velocidad de las consultas en conjuntos de datos grandes
- Aproveche las identidades de perfil que coinciden con la configuración de su área de nombres de recorrido

**Calidad de datos**

- Monitorice con regularidad [eventos descartados](sharing-field-list.md#discarded-events) para identificar problemas de datos
- Valide que los esquemas de evento coincidan con los requisitos de análisis
- Implementar el control de errores adecuado en las consultas personalizadas

**Estrategias de Analytics**

- Combinación de eventos de paso de recorrido con datos de comentarios de mensajes para una atribución completa
- Utilice el análisis basado en el tiempo para comprender la velocidad del recorrido y los cuellos de botella
- Crear análisis de cohorte para comparar diferentes variaciones de recorrido.

### Funciones de análisis avanzadas {#advanced-analytics}

**Integración de Customer Journey Analytics**
Los eventos de paso de recorrido se pueden analizar con Customer Journey Analytics para:

- Modelado de atribución avanzado
- Visualización de recorridos en canales múltiples
- Análisis predictivo de los resultados del recorrido

**Toma de decisiones en tiempo real**
Utilice patrones de eventos de paso de recorrido para lo siguiente:

- Déclencheur de la personalización en tiempo real
- Implementación de la optimización dinámica de recorridos
- Habilitar recomendaciones contextuales de acción recomendada siguiente

## Recursos adicionales {#additional-resources}

### Vínculos de documentación {#documentation-links}

- **[Descripción general del uso compartido de pasos de Recorrido](sharing-overview.md)**: Explicación de cómo fluyen los datos de recorrido a Adobe Experience Platform
- **[Diccionario de esquemas integrado](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es)**: referencia de esquema XDM completa
- **[Informes de Journey Optimizer](report-gs-cja.md)**: Información general sobre las capacidades de creación de informes en Journey Optimizer

### Guías de integración {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Analizando datos de Journey Optimizer en CJA
- **[Administración de datos](../data/export-datasets.md)**: exportando y administrando datos de recorrido
- **[Privacidad y control](../privacy/audit-logs.md)**: Consideraciones sobre el control de datos para eventos de recorrido

Los eventos de paso de recorrido forman la base del análisis de recorrido avanzado en Adobe Journey Optimizer. Al comprender y aprovechar estos eventos de forma eficaz, puede obtener información más detallada sobre la conducta de los clientes, optimizar el rendimiento del recorrido y crear experiencias más personalizadas para los clientes.
