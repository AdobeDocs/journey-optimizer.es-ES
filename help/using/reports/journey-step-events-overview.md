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
source-git-commit: a7da542320a38dbc739ec42ee4926fce1dea1df0
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 1%

---

# Trabajo con eventos de paso de recorrido {#work-with-journey-step-events}

Los eventos de paso de recorrido son eventos generados automáticamente que capturan información detallada acerca de cada paso que realiza un [perfil](../audience/get-started-profiles.md) a medida que progresan a través de un [recorrido](../building-journeys/journey.md) en Adobe Journey Optimizer. Estos eventos proporcionan una amplia visibilidad del [rendimiento del recorrido](../building-journeys/report-journey.md) y habilitan potentes funcionalidades de análisis.

## ¿Qué son los eventos de paso de recorrido? {#what-are-step-events}

Los eventos de paso de recorrido son eventos [XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"} generados por el sistema que Adobe Journey Optimizer crea y envía automáticamente a [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=es){target="_blank"} cada vez que un perfil se mueve de un nodo a otro en un recorrido. Cada evento corresponde a una [actividad de recorrido](../building-journeys/about-journey-activities.md) o transición específica en la experiencia de recorrido del cliente.

Existen dos tipos principales de eventos de paso de recorrido:

- **journeyStepEvent**: Eventos relacionados con la progresión de perfiles individuales a través de pasos de recorrido
- **journeyStepProfileEvent**: eventos que incluyen información de contexto de perfil adicional

### ¿Qué eventos de paso de recorrido de déclencheur? {#event-triggers}

Los eventos de paso de recorrido se generan automáticamente para varias actividades de recorrido:

- **Eventos de entrada**: cuando un perfil [entra en un recorrido](../building-journeys/entry-management.md)
- **Ejecución de acciones**: Cuando se envían [mensajes](../building-journeys/journeys-message.md) o se realizan [acciones personalizadas](../building-journeys/using-custom-actions.md)
- **Evaluación de condición**: Cuando los perfiles pasan por [condiciones](../building-journeys/condition-activity.md) y puntos de decisión
- **Actividades de espera**: Cuando los perfiles entran y salen de [nodos de espera](../building-journeys/wait-activity.md)
- **Eventos de salida**: cuando los perfiles se completen o [salga de un recorrido](../building-journeys/end-journey.md)
- **Control de errores**: Cuando se producen errores durante la ejecución del recorrido

>[!NOTE]
>
>Los eventos de paso de recorrido se activan de forma predeterminada en todas las instancias. No puede modificar ni actualizar los [esquemas y conjuntos de datos](sharing-overview.md) que se han creado durante el aprovisionamiento para los eventos del paso. Estos esquemas y conjuntos de datos están en modo de solo lectura.

Más información sobre [esquemas de eventos de paso de recorrido](sharing-field-list.md).

## Por qué importan los eventos de paso de recorrido {#why-step-events-matter}

Los eventos de paso de recorrido proporcionan un valor crítico para las organizaciones que utilizan Adobe Journey Optimizer:

### Análisis y monitorización en tiempo real {#real-time-analytics}

- **Seguimiento del rendimiento del Recorrido**: supervise cómo fluyen los perfiles entre sus recorridos en tiempo real mediante [informes en vivo](live-report.md)
- **Análisis de conversión**: Comprenda los puntos de entrega y las rutas de conversión exitosas con [análisis de recorrido](journey-global-report-cja.md)
- **Detección de errores**: identifique y solucione problemas a medida que ocurran mediante [supervisión y alertas](alerts.md)

### Integración de datos y perspectivas {#data-integration}

- **Análisis entre plataformas**: Combine datos de recorrido con otras [fuentes de datos de Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md)
- **Vista del cliente 360**: cree [perfiles de cliente](../audience/get-started-profiles.md) completos que incluyan interacciones de recorrido
- **Modelado de atribución**: Conecte los puntos de contacto del recorrido con los resultados comerciales descendentes mediante [Customer Journey Analytics](cja-ajo.md)

### Oportunidades de optimización {#optimization}

- **Perspectivas de pruebas A/B**: Analice el rendimiento de diferentes rutas de recorrido mediante [experimentación](campaign-global-report-cja-experimentation.md)
- **Mejora de Personalization**: Use los datos de comportamiento del recorrido para mejorar las experiencias futuras con [contenido dinámico](../personalization/dynamic-content.md)
- **Eficiencia operativa**: identifique cuellos de botella y optimice [el diseño del recorrido](../building-journeys/using-the-journey-designer.md)

## Cómo utilizar eventos de paso de recorrido {#how-to-use-step-events}

### Acceso a datos de eventos de paso de recorrido {#accessing-data}

Los datos de evento de los pasos de recorrido se almacenan automáticamente en Adobe Experience Platform y se puede acceder a ellos a través de:

1. **Consultas de lago de datos**: use SQL para consultar el conjunto de datos `journey_step_events` con [servicio de consulta](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=es){target="_blank"}
2. **Customer Journey Analytics**: Analizar datos de recorrido con [herramientas de análisis avanzadas](cja-ajo.md)
3. **Creación de informes en tiempo real**: Acceda a los datos a través de las [funciones de creación de informes integradas de Journey Optimizer](gs-reports.md)
4. **API**: acceso a datos de evento mediante programación para aplicaciones personalizadas

Más información sobre [acceso a conjuntos de datos](../data/datasets-query-examples.md).

### Puntos de datos clave disponibles {#key-data-points}

Los eventos de paso de recorrido capturan información completa que incluye:

- **Recorrido**: [ID., versión y nombre del Recorrido](sharing-journey-fields.md)
- **Información del perfil**: [Id. del perfil e identidades asociadas](sharing-identity-fields.md)
- **Detalles del paso**: [Nombre, tipo y estado de ejecución del nodo](sharing-common-fields.md)
- **Marcas de hora**: Hora exacta de cada paso del recorrido
- **Resultados de la acción**: [Estado de éxito/error y detalles de ejecución](sharing-execution-fields.md)
- **Información del error**: [códigos de error y descripciones detalladas](sharing-field-list.md#discarded-events) cuando ocurren problemas

Explorar todas las [definiciones de campo disponibles](sharing-field-list.md).

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

Más información sobre [técnicas de consulta para el análisis de funnel](query-examples.md#common-queries).

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

- Use `journeyVersionID` en lugar de `journeyVersionName` para obtener un mejor rendimiento de las consultas ([obtener más información acerca de las propiedades del recorrido](../building-journeys/expression/journey-properties.md))
- Filtre por intervalos de fechas para mejorar la velocidad de las consultas en conjuntos de datos grandes
- Aproveche las identidades de perfil que coincidan con su [configuración del área de nombres de recorrido](../building-journeys/entry-management.md)

**Calidad de datos**

- Monitorice con regularidad [eventos descartados](sharing-field-list.md#discarded-events) para identificar problemas de datos
- Valide que los esquemas de evento coincidan con los requisitos de análisis
- Implementar el control de errores adecuado en las consultas personalizadas

**Estrategias de Analytics**

- Combine eventos de paso de recorrido con [datos de comentarios de mensajes](../data/datasets-query-examples.md#message-feedback-event-dataset) para la atribución completa
- Utilice el análisis basado en el tiempo para comprender la velocidad del recorrido y los cuellos de botella

### Funciones de análisis avanzadas {#advanced-analytics}

**Integración de Customer Journey Analytics**
Los eventos de paso de recorrido se pueden analizar con [Customer Journey Analytics](cja-ajo.md) para:

- Modelado de atribución avanzado
- Visualización de recorridos en canales múltiples
- Análisis predictivo de los resultados del recorrido

Aprenda a [configurar Customer Journey Analytics](report-gs-cja.md) para los datos de Journey Optimizer.

## Recursos adicionales {#additional-resources}

### Vínculos de documentación {#documentation-links}

- **[Descripción general del uso compartido de pasos de Recorrido](sharing-overview.md)**: Explicación de cómo fluyen los datos de recorrido a Adobe Experience Platform
- **[Diccionario de esquemas integrado](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es){target="_blank"}**: referencia de esquema XDM completa
- **[Informes de Journey Optimizer](report-gs-cja.md)**: Información general sobre las capacidades de creación de informes en Journey Optimizer

### Guías de integración {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Analizando datos de Journey Optimizer en CJA
- **[Administración de datos](../data/export-datasets.md)**: exportando y administrando datos de recorrido
- **[Privacidad y control](../privacy/audit-logs.md)**: Consideraciones sobre el control de datos para eventos de recorrido


**Pasos siguientes:**

- Empiece por [crear sus primeros informes de recorrido](sharing-overview.md)
- Explorar [ejemplos de consultas](query-examples.md) para casos de uso específicos
- Obtenga información acerca de [prácticas recomendadas de administración de recorridos](../building-journeys/journey.md)
