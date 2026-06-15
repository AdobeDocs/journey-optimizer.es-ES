---
title: Ventajas de migrar a la toma de decisiones
description: Descubra las ventajas de migrar de Administración de decisiones a Toma de decisiones
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: aedd7845-3d8d-457a-a7f3-03897846b241
TQID: https://experienceleague.adobe.com/DQI-YSVEdN4ffTgnj-LG4U59-dbVxB-wnBOqjOiWoS4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 1320
ht-degree: 4%

---

# Ventajas de migrar a la toma de decisiones {#migrate-to-decisioning}

>[!BEGINSHADEBOX]

**En esta página:** Comprenda las capacidades y los beneficios que ofrece Decisioning sobre Administración de decisiones, junto con las herramientas de migración disponibles, para que pueda decidir si desea migrar.

>[!ENDSHADEBOX]

## ¿Qué es Decisioning? {#what-is-decisioning}

Journey Optimizer Decisioning es una ampliación de la funcionalidad de toma de decisiones que sienta las bases para la toma de decisiones sobre otros objetos (como recorridos) en el futuro. Esta nueva capacidad unifica los conceptos clave del flujo de trabajo para una creación y administración optimizadas, introduce la experimentación en la toma de decisiones y cambia los elementos de decisión a un enfoque basado en esquemas para la representación dinámica de elementos.

El marco de trabajo de decisiones y el conjunto de funciones de próxima generación de Adobe Journey Optimizer permiten a las marcas utilizar los datos, la inteligencia y el contexto disponibles de un cliente para determinar la mejor experiencia y optimizar el valor empresarial para cada uno. [Más información](gs-experience-decisioning.md)

## ¿Por qué migrar a Decisioning? {#why-migrate}

La toma de decisiones ofrece funcionalidades y beneficios significativos con respecto al marco de gestión de decisiones heredado:

### Capacidades de IA y aprendizaje automático

* **Métricas personalizadas**: capacidad de usar métricas de optimización personalizadas para modelos de IA. Esto proporciona interoperabilidad para la generación de informes con [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview){target="_blank"}, estandariza la generación de informes en ambas plataformas y mejora la consistencia y confiabilidad de los datos. La integración optimizada proporciona una vista más clara de las métricas de rendimiento y agrega nuevas funciones, como la creación de métricas sencillas, la publicación de audiencias, la realización de preguntas específicas mediante Insight Builder y la programación de informes.

* **Medición de alza**: Capacidad para visualizar, explorar y explotar el tráfico en modelos de IA. Esto permite a los especialistas en marketing y a los científicos de datos cuantificar cómo la exploración de IA mejora el rendimiento del modelo a largo plazo y la capacidad de detección de nuevas ofertas ganadoras. La transparencia en la asignación del tráfico genera confianza en las decisiones de IA y permite a los equipos optimizar tanto el aprendizaje como el rendimiento a lo largo del tiempo. [Más información](ranking/auto-optimization-model.md#lift)

* **Generador de fórmulas de IA**: capacidad para aplicar resultados de puntuación del modelo de IA a las capacidades de fórmula existentes. Esto permite a los especialistas en marketing combinar sin problemas los resultados de IA con reglas y pesos deterministas para estrategias de optimización más matizadas, aumentando el control y la flexibilidad mientras siguen aprovechando la inteligencia de aprendizaje automático. [Más información](ranking/ranking-formulas.md)

### Experimentación

Capacidad para experimentar con ofertas, aspectos de una oferta determinada y/o métodos de clasificación. Esto permite a los especialistas en marketing ejecutar experimentos controlados sobre lógica creativa, de elegibilidad y de clasificación para identificar variantes de alto rendimiento, acelerar los ciclos de aprendizaje e impulsar la optimización continua del sistema de toma de decisiones.

### Informes mejorados

Tablero que documenta el rendimiento de los elementos de decisión y las estrategias de selección en relación con los elementos clave del funnel de participación. Un panel de toma de decisiones intuitivo y listo para usar muestra rápidamente el valor del rendimiento de la campaña y del recorrido para los KPI clave en la oferta y la entrega de contenido, la participación de visualización y clics, las tasas de uso de reserva y el alza con respecto a los modelos de clasificación de IA y aprendizaje automático. [Más información](cja-reporting.md)

### Eficiencia operativa

* **Copia de espacio aislado**: capacidad de copiar sobre objetos entre espacios aislados (por ejemplo, de desarrollador a productor). Esto simplifica los flujos de trabajo de implementación y prueba al permitir una migración perfecta de la lógica de decisión, las ofertas y los objetos de configuración entre entornos, lo que reduce el tiempo de instalación y minimiza los errores humanos. [Más información](../configuration/copy-objects-to-sandbox.md)

* **Administración de catálogos de elementos basados en esquemas**: capacidad para definir y administrar elementos de decisión directamente en conjuntos de datos vinculados a esquemas, lo que permite actualizaciones dinámicas y un control simplificado. Esto optimiza la administración del catálogo mediante la sincronización de los elementos de decisión con las fuentes de datos subyacentes, lo que garantiza la precisión del contenido, permite actualizaciones más rápidas y admite el control a escala. [Más información](items.md)

* **Toma de decisiones independiente de la ubicación**: capacidad para reutilizar la lógica de decisión en ubicaciones/ubicaciones, lo que desvincula la selección de decisiones de la entrega. Esto promueve la reutilización y la eficacia al permitir que un solo modelo de decisión active varias ubicaciones o superficies (por ejemplo, web, aplicación, correo electrónico), centralizando la lógica y acelerando los esfuerzos de personalización en canales múltiples. [Más información](placements.md)

* **Fragmentos de contenido reutilizables**: capacidad para definir bloques de contenido JSON o HTML (por ejemplo, títulos, encabezados, pies de página, CTA) una vez y hacer referencia a ellos en varios objetos de oferta. Esto optimiza la creación y el control de contenido, ya que permite que los componentes compartidos se administren de forma centralizada y se actualicen automáticamente en todas las ofertas. [Más información](../content-management/fragments.md)

### Próximas funciones

* **Toma de decisiones en el canal**: capacidad para usar la lógica de decisión a fin de determinar el mejor canal para la participación (p. ej., correo electrónico vs. push vs. web), en lugar de solo la mejor oferta dentro de un solo canal. Esto mejora la experiencia del cliente al optimizar dónde se entrega un mensaje, no solo lo que se entrega.

* **Optimización de mensajes**: capacidad para usar IA o enfoques basados en reglas para optimizar el contenido de los mensajes para cada perfil y mejorar la participación y los resultados de conversión. Esto permite a los especialistas en marketing adaptar el tono, las imágenes y el diseño de forma dinámica en función de los atributos de audiencia y los datos de rendimiento.

* **Optimización de la ruta de Recorrido**: capacidad para determinar la ruta de recorrido que debe seguir un perfil, según los resultados experimentales, el contexto en tiempo real, las reglas o la tendencia a la conversión. Esto permite a los equipos enrutar perfiles de forma inteligente a través de la rama de recorrido óptima, lo que garantiza la cadencia y el contenido adecuados para cada usuario.

* **Toma de decisiones en el Recorrido**: capacidad para arbitrar entre varios recorridos cuando un perfil cumple los requisitos para más de uno, lo que garantiza que se seleccione el recorrido más valioso o relevante. Esto evita conflictos de mensajes y mensajes excesivos al clasificar y seleccionar el recorrido de mayor prioridad para cada perfil.

### Funciones adicionales

* **Aplicación de políticas**: Empoderamiento de usuarios empresariales para utilizar funciones como [Etiquetado y aplicación del uso de datos (DULE)](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"} y [Consentimiento](../action/consent.md) en Decisioning, lo que permite la protección de escudo de privacidad en todo el flujo de trabajo de decisioning. Esto garantiza que las decisiones respeten automáticamente las políticas de uso de datos y las preferencias de consentimiento del cliente.

* **Compatibilidad con canales de mensajería nativos**: mensajería integrada y toma de decisiones en un solo marco de trabajo en varios canales: [experiencia basada en código](../code-based/get-started-code-based.md), [correo electrónico](../email/get-started-email.md), [SMS](../mobile/get-started-mobile.md) y [notificaciones push](../push/get-started-push.md). La compatibilidad intuitiva con la IU permite a los usuarios insertar componentes de toma de decisiones directamente en los flujos de trabajo de creación de mensajes.

* **Búsqueda de conjuntos de datos de Experience Platform**: capacidad para cargar y hacer referencia a [conjuntos de datos de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"} directamente en las reglas de selección de ofertas, clasificación y contenido de ofertas personalizado. Esto aumenta la flexibilidad de personalización y segmentación al permitir que la lógica de decisión utilice fuentes de datos externas dinámicas. [Más información](../data/lookup-aep-data.md)

* **Escalabilidad y rendimiento**: mejora arquitectónica que mueve el cálculo de decisiones del concentrador al perímetro, lo que reduce significativamente la latencia y mejora el rendimiento en los casos de uso de alto tráfico.

## Casos de uso de ejemplo {#use-cases}

| Caso de uso | Gestión de decisiones | Toma de decisiones |
|----------|---------------------|-------------|
| **Estrategia de varias ubicaciones** | Lógica de decisión vinculada a una ubicación específica (por ejemplo, una ubicación web o de correo electrónico) | Una sola estrategia alimenta tanto la página principal como la aplicación móvil |
| **Atributos de oferta coherentes** | Cada oferta gestiona sus propios atributos manualmente; sin coherencia en el nivel de esquema | Un especialista en marketing define &quot;discountType&quot; y &quot;offerValue&quot; una vez; cada oferta hereda estos campos automáticamente |
| **Clasificación de IA dinámica** | Las clasificaciones dependen únicamente de la salida del modelo o de las reglas estáticas | Un experto en marketing puede ajustar la ponderación (por ejemplo, una puntuación de conversión de IA del 60 % + un margen de beneficio del 40 %) para equilibrar los ingresos y los objetivos de participación |
| **Estrategias de prueba A/B** | Sin compatibilidad de experimentación integrada | Un equipo puede probar A/B si &quot;IA + reglas empresariales&quot; supera la &quot;clasificación basada en prioridades&quot; |
| **Métricas de IA personalizadas** | Optimiza solo con la tendencia a hacer clic; no hay visibilidad en la exploración o el alza de modelos | Retailer forma un modelo de &quot;probabilidad de compra&quot; y supervisa el alza de productos nuevos frente a los conocidos |
| **Reutilización de contenido** | Cada oferta almacena el contenido completo de forma independiente | Al actualizar un encabezado o CTA, se propaga automáticamente a cientos de ofertas |
| **Creación integrada** | La toma de decisiones y la mensajería se realizan en marcos independientes con integración limitada | Un especialista en marketing inserta ofertas personalizadas en un correo electrónico sin salir del editor de mensajes |
| **Cumplimiento de la privacidad** | Requiere coordinación manual con equipos de ingeniería y datos para la aplicación | Un experto en marketing crea una regla de oferta sabiendo que las preferencias de consentimiento excluyen automáticamente determinados perfiles |
| **Inventario en tiempo real** | Datos estáticos; flexibilidad limitada para utilizar conjuntos de datos externos o contextuales | Utilice un conjunto de datos de inventario de productos para suprimir ofertas de artículos sin existencias en tiempo real |
| **Rendimiento de escala** | Decisiones tomadas en el concentrador con mayor latencia | Personalización en tiempo real para millones de solicitudes entrantes con un tiempo de respuesta inferior a 100 ms |

## Herramientas de migración {#migration-tooling}

Hay disponible un conjunto completo de **API de herramientas de migración** para migrar las entidades de Administración de decisiones a Toma de decisiones. Estas API permiten una migración sin problemas entre entornos limitados con resolución de dependencia automatizada y funciones de reversión.

Las API de herramientas de migración le permiten lo siguiente:

* **Analizar dependencias** entre zonas protegidas de origen y destino
* **Migrar en diferentes ámbitos**: zona protegida, nivel de oferta o de decisión
* **Migraciones de reversión** si se detectan problemas

Para obtener la documentación completa de la API, incluidos la autenticación, los extremos, los ejemplos de solicitud/respuesta y los flujos de trabajo paso a paso, consulte [esta página](decisioning-migration-api.md).

## Temas relacionados {#related-topics}

* [Introducción a la toma de decisiones](gs-experience-decisioning.md)
* [Limitaciones y protecciones de decisiones](decisioning-guardrails.md)
* [Preguntas frecuentes sobre Decisioning](decisioning-faq.md)
